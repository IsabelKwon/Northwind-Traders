# 노스윈드 트레이더스 SQL 분석

## 프로젝트 소개

Dataquest의 가이드 프로젝트를 기반으로, 제공된 데이터베이스 스키마와 시작 질문을 출발점으로 삼았습니다. 다만 주어진 질문에 답하는 데서 멈추지 않고, 결과가 새로운 질문을 낳을 때마다 한 단계씩 더 파고들었습니다. 예를 들어 들쭉날쭉한 전월 대비 성장률은 3개월 이동평균으로 노이즈를 걷어냈고, 고객 주문 분포는 Python(pandas, matplotlib)으로 시각화해 SQL 출력만으로는 보이지 않던 패턴을 확인했습니다.

## 사용 도구

- **PostgreSQL** — 데이터베이스 (Northwind 샘플 데이터셋)
- **SQL** ([JupySQL](https://jupysql.ploomber.io/) 사용) — 쿼리, CTE, 윈도우 함수
- **Python** (pandas, matplotlib) — 시각화 및 추가 탐색

## 다룬 내용

- customers, orders, order_details, employees를 재사용 가능한 뷰로 결합
- 직원별 매출 순위 — 전체 기준과 직무별 기준 각각
- 월별 매출 추이: 누적 합계, 전월 대비 성장률, 노이즈를 줄이기 위한 3개월 이동평균
- matplotlib으로 성장률 추이 시각화
- 평활 후에도 남은 급락을 주문 건수와 객단가로 분해해 어느 쪽이 움직였는지 확인
- 주문액의 평균과 중앙값을 비교해, 급락이 큰 주문의 이탈 때문인지 전반적인 축소 때문인지 검증
- 고객별 주문 빈도와 평균 비교, 그리고 분포 형태가 드러내는 고객 구성
- 주문 금액과 할인율의 관계를 산점도로 확인 — 할인이 실제로 주문 규모를 키우는지 검증
- 카테고리별 매출 비중과 카테고리 내 상위 상품 — 단일 상품에 의존하는 카테고리 탐지

## 파일

- `northwind_query.ipynb` — 분석 노트북 (SQL 쿼리, 설명, Python 시각화)
- `northwind.sql` — 데이터베이스 스키마 및 시드 데이터


---

# Northwind Traders SQL Analysis (영문)

## About

This project is based on a Dataquest guided project, using their provided database schema and starter questions as a foundation. Beyond the original prompts, I extended the analysis further whenever a result raised a new question — for example, smoothing noisy month-over-month growth rates with a 3-month moving average, visualizing customer order distributions with Python (pandas and matplotlib), and so on to better understand patterns that weren't obvious from the SQL output alone.

## Tools

- **PostgreSQL** — database (Northwind sample dataset)
- **SQL** (via [JupySQL](https://jupysql.ploomber.io/)) — querying, CTEs, window functions
- **Python** (pandas, matplotlib) — data visualization and further exploration

## What's covered

- Combining customers, orders, order details, and employees into reusable views
- Ranking employees by total sales, overall and within job title
- Monthly sales trends: running totals, month-over-month growth rate, and a 3-month moving average to reduce noise
- Visualizing growth rate trends with matplotlib
- Breaking the remaining sales dips into order count vs. average order value to find which side actually moved
- Comparing mean and median order value to test whether the dips came from missing large orders or an across-the-board shift
- Customer order frequency vs. average, and what the distribution shape reveals about customer segments
- Order value vs. average, with discount rate — plotted as a scatter to check whether discounts actually predict larger orders
- Sales percentage by category, and top products within each category to flag categories that lean on a single product

## Files

- `northwind_query.ipynb` — main analysis notebook (SQL queries, explanations, and Python visualizations)
- `northwind.sql` — database schema/seed data

