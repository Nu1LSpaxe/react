# BrowserRouter and RouterProvider

Intro to components in 'react-router-dom':
- BroserRoute: 使用其中的路由器組件
- Routes: 路由組件
- Route: 單一路由組件
    > Routes 和 Route 用來實際設置路由
- Link: 連結不同頁面

Source code be like this:
```javascript
    <BrowserRouter>
        <header>
            <nav>
                <h1>Innovation Town</h1>
                <NavLink to="/">Home</NavLink>
                <NavLink to="about">About</NavLink>
            </nav>
        </header>
        <main>
            <Routes>
                // 在未設定路徑的情況下，react 會導向根目錄 path='/'，所以改成 index 效果一樣
                <Route index element={<Home />} />
                <Route path='/about' element={<About />} />
            </Routes>
        </main>
    </BrowserRouter>
```


Unfortunately, it's old version.

Now We can use `<RouterProvider>`,

First `createrowserRouter()` as constant router,
    
then pass it to `<RouterProvider router={ router } />`

Note: In `createRoutesFromElements()`, couldn't have `<Routes>`, but only `<Route>`