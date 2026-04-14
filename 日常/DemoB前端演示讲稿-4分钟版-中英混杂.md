# Demo B Frontend Presentation Script (4-minute version)

**Target Audience:** Shaowen Si  
**Scope:** Sprint 2 Frontend, focusing on `Query / Result / History`  
**Style Goal:** Short, steady, spoken presentation style with inline action cues

---

## 0. Opening (15s)

Hello everyone, my part will focus on the frontend progress in Sprint 2.  
My focus has been the `Query`, `Result`, and `History` pages, along with creating a unified UI and interactive experience across all three. Powered by shadcn ui and tailwindcss

---

## 2. Query Page (40s)

Let's start with the Query page. *(切换到 Query 页面)*  
We designed it as a centered AI query panel, so users instantly know the core action here is asking questions. *(指向上方的 query panel)*  

The navbar at the top has been extracted into a common component, and the Result and History pages will reuse this exact same navigation. *(指向上方 navbar)*  

Below is the recommended questions section. *(指向下方推荐问题区)*  

It refreshes automatically, and you can also refresh it manually. *(点击刷新按钮演示)*  

I'll type in a question now. *(在输入框输入问题)*  
After typing, the configuration area below automatically expands. *(等待配置区展开)*  
Here we see the year, program, and the analysis mode—either `Brief` or `Deep Dive`. *(依次指向这几个配置项)*  

---

## 3. Brief Success Page (50s)

I'll run it in `Brief` mode first. *(点击 Brief 模式并提交)*  
This mode is best for a quick overview.  

Now we're on the Result page. *(等待页面跳转到 Result 页)*  
This is a major focus of our refactoring.  

At the top, the context is clearly laid out: *(指向顶部 Context 区域)*  
1. What the user asked,  
2. The mode being used,  
3. The status of the result,  
4. And metadata like generation time, sample size, filters, and run ID.  

In the middle is our six-part result structure: *(向下滑动展示中间结果区域)*  
`Executive Summary`, `Ranked Themes`, `Theme Evidence`, `Interpretation`, `Recommended Actions`, and `Confidence & Caveats`.  

This floating navigation on the left makes it easy to jump around long result pages without endless scrolling. *(点击左侧导航栏的几个项演示跳转)*  

I'll open one piece of evidence. *(点击展开一条 evidence)*  
Here we can view the detailed comments.  

---

## 4. Deep Dive Comparison (25s)

Next, I'll switch to `Deep Dive` using the same question. *(返回并使用相同问题，选择 Deep Dive 模式提交)*  
This makes it easy to see the difference.  

`Brief` is for a quick overview, good for high-level takeaways.  
`Deep Dive` retains more analytical depth, for when you need the complete picture. *(上下滚动展示 Deep Dive 的结果)*  
we can choose when different use cases.  

---

## 5. Three Special Status Pages (55s)

Beyond successful results, we've separated three other states into distinct pages.  

The first is `Privacy Protected`. *(切换到 Privacy Protected 演示页或截图)*  
When the matched sample is too small, the system hides fine-grained evidence.  
This isn't an error; it's intentional privacy protection.  

The second is `No Data`. *(切换到 No Data 演示页或截图)*  
This means the question is valid, but there's not enough relevant data under the current filters.  

The third is `Refused`. *(切换到 Refused 演示页或截图)*  
This indicates the question is outside the scope of academic feedback, so the system declines to answer.  

So our result page now handles four distinct states:  
`success`, `privacy protected`, `no data`, and `refused`.  

---

## 6. History Page (45s)

Finally, let's look at the History page. *(点击导航栏切换到 History 页面)*  
This page has also been refactored.  

Every history record displays: *(指向其中一条记录)*  
1. The query text  
2. Time  
3. Mode  
4. Result flag  
5. Run ID  

This allows users to quickly understand a past query right from the list view, without having to open each one.  

I'll demonstrate two actions here:  
`Open` takes you directly back to the result page, and `Delete` removes the record. *(依次点击 Open 和 Delete 演示)*  

The side panel on the left currently supports `search` and `sort`. *(指向左侧边栏并演示搜索/排序)*  
We've reserved space for `Filter`, which we'll build out in Sprint 3.  

---

## 7. Wrap-up (20s)

To wrap up, my work in Sprint 2 focused on unifying the main `Query -> Result -> History` flow and making the various result states clearer for users.  
This ensures that from asking a question, to viewing results, to checking history, the entire experience feels complete and cohesive. *(返回到初始界面或停留在有代表性的界面，结束演示)*