[Browser Router]: https://reactrouter.com/en/main/routers/create-browser-router

---

# React Router V6.4

## Adding a Router

Điều đầu tiên cần làm là tạo [`Browser Router`][Browser Router] và định cấu hình tuyến đường đầu tiên của chúng tôi. Điều này sẽ cho phép định tuyến phía máy khách cho ứng dụng web của chúng tôi.

Tệp `main.jsx` là điểm vào. Mở nó lên và chúng ta sẽ đưa React Router lên trang.

```jsx
// src/main.jsx

import * as React from 'react';
import * as ReactDOM from 'react-dom/client';
import { createBrowserRouter, RouterProvider } from 'react-router-dom';
import './index.css';

const router = createBrowserRouter([
  {
    path: '/',
    element: <div>Hello world!</div>,
  },
]);

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <RouterProvider router={router} />
  </React.StrictMode>,
);
```

Tuyến đường đầu tiên này là cái mà chúng tôi thường gọi là "tuyến đường gốc" vì phần còn lại của các tuyến đường của chúng tôi sẽ hiển thị bên trong tuyến đường đó. Nó sẽ đóng vai trò là bố cục gốc của giao diện người dùng, chúng ta sẽ có các bố cục lồng nhau khi chúng ta tiến xa hơn.
