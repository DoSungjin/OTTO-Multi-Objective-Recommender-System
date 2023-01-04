# Python Template
![image](https://user-images.githubusercontent.com/100894816/207234514-8f4774dd-7fae-4226-a0de-0de77bae0025.png)
![image](https://user-images.githubusercontent.com/100894816/207234536-ba208aa7-0004-4fd1-bb1a-60447f1c72ea.png)

Template repository for Python project
## 🎯**Goal of the Competition**

The goal of this competition is to predict **e-commerce clicks**, **cart additions**, and **orders**. You'll build a multi-objective recommender system based on **previous events in a user session**.\

## 🚀 Features
- E-commerce clicks
- Cart additions
- Orders

## 📖**Context**

- OTTO는 독일 최대의 온라인 상점 (https://otto.de/)
- 너무 많은 선택지는 구매자들에게 부담
: 관련성 높은 항목을 추천해서 구매자들의 탐색 비용을 줄이고, 소비를 촉진 시키기 위함.
- **November 1, 2022** - Start Date.
- **January 31, 2023** - **Final Submission Deadline.**

All deadlines are at 11:59 PM UTC on the corresponding day unless otherwise noted. The competition organizers reserve the right to update the contest timeline if they deem it necessary.

## 💾Data

### Train data

Train data size : `12,899,779`

columns : session ; events

- 각 세션은 2회부터 495회 까지 구성되어 있다.
- events 항목 안에는 dic 형태로 aid, ts, type이 존재함

### Data structure

- session : The unique session id. Each session contains a list of time ordered events.
- events : The time ordered sequence of events in the session. Each event contains 3 pieces of information.
    - aid : the article id (product code) of the associated event
    - ts : The Unix timestamp of the event
    - type : The event type (clicks, carts, orders)

### Actions

- Action frequency
    
    ![Clicks 수가 월등히 많고 carts에 넣고 주문한 수는 적다.](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4d3fcb32-b587-4f9f-bbde-c6884706b53d/Untitled.png)
    
    Clicks 수가 월등히 많고 carts에 넣고 주문한 수는 적다.
    
- Distribution of the number of actions taken in each session
    
    ![10회 미만의 actions가 분포의 대부분을 차지한다. ](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/48165eb0-c5eb-42b2-a4c2-216beca1a037/Untitled.png)
    
    10회 미만의 actions가 분포의 대부분을 차지한다. 
    
- Length of each session

### Github Actions

- [release-drafter](https://github.com/release-drafter/release-drafter)
- Check code quality when PR (`black`, `isort`, `flake8`)

### Other

- Commit template
- Issue, PR Template
- Add dummy test code
- Auto-close stale issue

## 📄 Guideline

### 1. Setup

- precommit, style, pytest, gitmessage, requirements

```bash
make setup
```

### 2. Writes your own code! ✏️

Don't forget to update the `README`!

## ⬆️ Contributing

### 1. Test

```bash
make test
```

### 2. Execute code formatting & Check lint

```bash
make style
```

In github DATA folder is handle by ignore file.

Day 1.4 - EDA first
