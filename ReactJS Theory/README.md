# ReactJS Theory
## Mục lục

<details>
  <summary>Ôn tập lại JS</summary>

- [I. SPA/MPA là gì?](#i-spampa-là-gì)
- [II. Ôn lại ES6+](#ii-ôn-lại-es6)
  - [1. Arrow function](#1-arrow-function)
  - [2. Enhanced object literals](#2-enhanced-object-literals)
  - [3. Destructuring, Rest](#3-destructuring-rest)
  - [4. Spread operator](#4-spread-operator)
  - [5. Modules](#5-modules)
- [III. Set up](#iii-set-up)
</details>

<details>
  <summary>ReactJS</summary>

- [I. React, ReactDOM](#i-react-reactdom)
- [II. JSX](#ii-jsx)
  - [1. JSX](#1-jsx)
  - [2. Component](#2-component)
  - [3. Props](#3-props)
  - [4. Cách viết hàm chuẩn](#4-cách-viết-hàm-chuẩn)
  - [5. Sử dụng thư viện clsx để viết câu lệnh if](#5-sử-dụng-thư-viện-clsx-để-viết-câu-lệnh-if)
  - [6. Truyền props sử dụng toán tử Spread](#6-truyền-props-sử-dụng-toán-tử-spread)
  - [7. Trích xuất giá trị từ mảng với Destructuring](#7-trích-xuất-giá-trị-từ-mảng-với-destructuring)
  - [8. Ký hiệu dấu chấm](#8-ký-hiệu-dấu-chấm)
  - [9. dangerouslySetInnerHTML](#9-dangerouslysetinnerhtml)
- [III. Hook - useState](#iii-hook---usestate)
  - [1. useState](#1-usestate)
  - [2. Closures](#2-closures)
  - [3. Các nguyên tắc khi làm việc với Hooks](#3-các-nguyên-tắc-khi-làm-việc-với-hooks)
  - [4. Tính bất biến trong ReactJS](#4-tính-bất-biến-trong-reactjs)
  - [5. Trạng thái với mảng](#5-trạng-thái-với-mảng)
  - [6. Trạng thái với đối tượng](#6-trạng-thái-với-đối-tượng)
  - [7. Xử lý form](#7-xử-lý-form)
  - [8. Truyền vào hàm](#8-truyền-vào-hàm)
  - [9. Chuyển trạng thái lên](#9-chuyển-trạng-thái-lên)
- [IV. Hook - useEffect](#iv-hook---useeffect)
  - [1. useEffect](#1-useeffect)
  - [2. Các hiệu ứng yêu cầu phải dọn dẹp](#2-các-hiệu-ứng-yêu-cầu-phải-dọn-dẹp)
  - [3. Effect dependencies](#3-effect-dependencies)
  - [4. Local Storage](#4-local-storage)
  - [5. Life cycle](#5-life-cycle)
- [V. Fetch](#v-fetch)
  - [1. Fetch API](#1-fetch-api)
  - [2. Fetch POST](#2-fetch-post)
  - [3. Axios](#3-axios)
- [VI. Custom Hooks](#vi-custom-hooks)
  - [1. Custom hooks với useEffect](#1-custom-hooks-với-useeffect)
  - [2. Custom hooks với useState](#2-custom-hooks-với-usestate)
  - [3. Custom hooks với useFetch](#3-custom-hooks-với-usefetch)
- [VII. Hook - useRef](#vii-hook---useref)
- [VIII. Context](#viii-context)
  - [1. Tạo Context](#1-tạo-context)
  - [2. Sử dụng Context](#2-sử-dụng-context)
  - [3. Giá trị Context](#3-giá-trị-context)
  - [4. Cập nhật giá trị Context](#4-cập-nhật-giá-trị-context)
- [IX. React Router](#ix-react-router)
  - [1. Điều hướng cơ bản](#1-điều-hướng-cơ-bản)
  - [2. Tham số URL](#2-tham-số-url)
  - [3. Hook - useParams](#3-hook---useparams)
  - [4. Nested routes](#4-nested-routes)
  - [5. Hook - useOutletContext](#5-hook---useoutletcontext)
  - [6. Xử lý lỗi 404](#6-xử-lý-lỗi-404)
  - [7. Trang hoạt động NavLink](#7-trang-hoạt-động-navlink)
  - [8. Hook - useNavigate](#8-hook---usenavigate)
  - [9. Hook - useLocation](#9-hook---uselocation)
- [X. Redux](#x-redux)
  - [1. Redux là gì](#1-redux-là-gì)
  - [2. State, Store và Reducer](#2-state-store-và-reducer)
  - [3. Thực hiện dispatch một action](#3-thực-hiện-dispatch-một-action)
- [XI. Redux Toolkit](#xi-redux-toolkit)
  - [1. Slices](#1-slices)
  - [2. Actions & payloads](#2-actions--payloads)
  - [3. Provider](#3-provider)
  - [4. Hook - useSelector](#4-hook---useselector)
  - [5. Hook - useDispatch](#5-hook---usedispatch)

</details>

<details>
  <summary>Một số lỗi có thể gặp</summary>

- [1. error:0308010C:digital envelope routines::unsupported](#1-error0308010cdigital-envelope-routinesunsupported)
</details>

## I. SPA/MPA là gì?
[:arrow_up: Mục lục](#mục-lục)

**1. SPA - Single-Page Application**
- ReactJS là 1 trong những thư viện tạo SPA
- Các "ông lớn" sử dụng SPA: Google, Facebook, Twitter
- Các SPA khác: F8, Shoppe, 30shine, chotot, zingmp3

**2. Các triển khai**
- SPA - Single-Page Application
- MPA - Multi-Page Application

**3. Sự khác biệt**

- SPA
  - Được cho là cách tiếp cận hiện tại hơn
  - Không yêu cầu tải lại trang trong quá trình sử dụng

- MPA
  - Là cách tiếp cận cổ điện hơn
  - Tải lại trang trong quá trình sử dụng (click vào đường link, chuyển sang, ...)

**4. So sánh**

- Tốc độ
  - SPA nhanh hơn khi sử dụng
    - Phần lớn tài nguyên được tải trong lần đầu
    - Trang chỉ tải thêm dữ liệu mới khi cần
  - MPA chậm hơn khi sử dụng
    - Luôn tải lại toàn bộ trang khi truy cập và chuyển hướng

**5. Bóc tách**
- SPA có phần Front-end riêng biệt
- MPA Front-end & Back-end phụ thuộc nhau nhiều hơn, được đặt trong cùng 1 dự án

**6. SEO**
- SPA không thiện thiện với SEO như MPA
- Trải nghiệm trên thiết bị di động tốt hơn

**7. UX**
- SPA cho trải nghiệm tốt hơn, nhất là các thao tác chuyển trang
- Trải nghiệm trên thiết bị di động tốt hơn

**8. Quá trình phát triển**
- SPA dễ dàng tái sử dụng code (component)
- SPA bóc tách FE & BE
    - Chia team phát tiển song song
    - Phát triển thêm mobile app dễ dàng

## II. Ôn lại ES6+ 
[:arrow_up: Mục lục](#mục-lục)
### 1. Arrow function
[:arrow_up: Mục lục](#mục-lục)

```jsx
// Arrows function không viết được cho trường hợp có context, function contructor...
// Viết bình thường
const logger = function(log) {
    console.log(log);
}

logger('Message...');

// Viết kiểu arrow function: bỏ từ function đi, thêm => vào sau đối số
const logger1 = log => {
    console.log(log);
}

logger1('Message...');

// Phân biệt => {}, =>, => ({})
const sum = (a, b) => a + b; // => không phải return 

const sum1 = (a, b) => { // => {} phải return 
    return a + b;
}

const sum2 = (a, b) => ({a: a, b:b}); // => ({}) không phải return 

// Nâng cao
// Viết bình thường
const course = {
    name: 'JavaScript basic!',
    getName: function() {
        return this; // context
    }
};

console.log(course.getName()); // JavaScript basic!

// Viết kiểu arrow function
const course1 = {
    name: 'JavaScript basic!',
    getName: () => {
        return this; // context
    }
};

console.log(course1.getName()); // Lỗi
```

### 2. Enhanced object literals
[:arrow_up: Mục lục](#mục-lục)

```jsx
// 1. Định nghĩa key: value cho object
// 2. Định nghĩa method cho object
// 3. Định nghĩa key cho object dưới dạng biến

// VD1:
// Viết bình thường
var name = 'Javascript';
var price = '1000';

var course = {
    name: name,
    price: price,
    getName: function() {
        return name;
    }
};

// Nên viết thành
var name = 'Javascript';
var price = '1000';

var course = {
    name,
    price,
    getName(){
        return name;
    }
};

// VD2:
// Viết bình thường
const course = {
    name: 'Javascript',
    price: 1000
};


// Viết thành
var fieldName = 'name';
var fieldPrice = 'price';

const course = {
    [fieldName]: 'Javascript',
    [fieldPrice]: 1000
};
```

### 3. Destructuring, Rest
[:arrow_up: Mục lục](#mục-lục)

```jsx
// Bình thường viết
var array = ['Javascript', 'PHP', 'Ruby'];

var a = array[0];
var b = array[1];
var c = array[2];

console.log(a, b, c);
// Javascript, PHP, Ruby

// 1. Destructuring (phân rã) sẽ viết
// VD1:
var array = ['Javascript', 'PHP', 'Ruby'];

var [a, b, c] = array;

console.log(a, b, c);
// Javascript, PHP, Ruby
// VD2:
var array = ['Javascript', 'PHP', 'Ruby'];

var [a, , c] = array;

console.log(a, c);
// Javascript, Ruby


// 2. Toán tử Rest ... lấy ra những phần còn lại
// VD1:
var array = ['Javascript', 'PHP', 'Ruby'];

var [a, ...rest] = array;

console.log(a); // Javascript
console.log(rest); // ["PHP", "Ruby"]

// VD2:
var course = {
    name: 'Javascript',
    price: 1000,
    image: 'image-address',
    children: {
        name: 'ReactJS',
    }
};

// Đổi tên name: parentName, name: childName do 2 name trùng tên nhau
var { name: parentName, children: { name: childrenName } } = course;

console.log(parentName);
console.log(childrenName);

// 3. Toán tử Rest ... trở thành mảng gần giống Arguments
// VD1:
function logger(...params) {
    console.log(params);
}

console.log(logger(1,2,3,4,5,6,7,8));
// [1,2,3,4,5,6,7,8]

// VD2:
function logger([a, b, ...rest]) {
    console.log(a);
    console.log(b);
    console.log(rest);
}

logger([2, 6, 12, 3, 4, 4])
// 2
// 6
// [12, 3, 4, 4]
```

### 4. Spread operator
[:arrow_up: Mục lục](#mục-lục)

```jsx
// Toán tử Spread ... có tác dụng bỏ đi dấu [], {}
// VD1:
var array1 = ['Javascript', 'Ruby', 'PHP'];

var array2 = ['ReactJS', 'Dart'];

var array3 = [...array2, ...array1];

console.log(array3);
// ['ReactJS', 'Dart', 'Javascript', 'Ruby', 'PHP']

// VD2:
var object1 = {
    name: 'Javascript',
};

var object2 = {
    price: 1000,
};

var object3 = {
    ...object1,
    ...object2
};

console.log(object3);
// {name: 'Javascript', price: 1000}

// VD3:
var array = ['Javascript', 'PHP', 'Ruby'];

function logger(...rest){
    for(var i = 0; i < rest.length; i++) {
        console.log(rest[i]);
    }
}

logger(...array);
// Javascript
// PHP
// Ruby
```

### 5. Modules
[:arrow_up: Mục lục](#mục-lục)

```jsx
// File logger.js
import { TYPE_LOG } from './constants.js'

function logger(log, type = TYPE_LOG) {
    console[type](log);
}

export default logger; // Đẩy logger ra ngoài
// 1 module chỉ export default được 1 cái

// File constants.js
export const TYPE_LOG = 'log';
export const TYPE_WARN = 'warn';
export const TYPE_ERROR = 'error';


// File main.js
// Modules: Import / Export
// VD1: Trực tiếp
import logger from './logger.js'; // export default

import {
    TYPE_LOG,
    TYPE_WARN,
    TYPE_ERROR
} from './constants.js'

// Nếu không:
// import {
//     TYPE_LOG,
//     TYPE_WARN,
//     TYPE_ERROR
// } from './constants.js'
// mà:
// import constants from './constants.js sẽ sinh ra lỗi bởi vì không export default
// Cách khắc phục:

import * as constants from './constants.js'
console.log(constants); // object

logger('Test message...', TYPE_ERROR)

// VD2: Trung gian
import { logger2 } from './logger/index.js';
import * as constants from './constants.js'

console.log(constants); // object
logger2('Test message...', constants.TYPE_WARN)
```

## III. Set up
[:arrow_up: Mục lục](#mục-lục)

Extension sử dụng:

```
- Auto Rename Tag
- Babel Javascript
- Bookmarks
- DotENV
- ESLint
- Javascript (ES6) code snippets
- Prettier
- Reactjs code snippets
- Tailwind CSS Intellisense
- Turbo Console Log
- Visual Studio IntelliCode
- styled-components-snippets
- vscode-styled-components
```

File `setting.json`

```
"editor.defaultFormatter": "esbenp.prettier-vscode", "editor.inlineSuggest.enabled": true, "editor.formatOnSave": true, "typescript.updateImportsOnFileMove.enabled": "always", "emmet.includeLanguages": { "javascript": "javascriptreact", "vue-html": "html" }, "emmet.triggerExpansionOnTab": true, "[javascript]": { "editor.defaultFormatter": "esbenp.prettier-vscode" }, "javascript.updateImportsOnFileMove.enabled": "always", "eslint.alwaysShowStatus": true, "[jsonc]": { "editor.defaultFormatter": "esbenp.prettier-vscode" }, "editor.suggestSelection": "first", "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue", "editor.wordWrapColumn": 100,
```

Extension tools sử dụng:

![image](https://github.com/CUNGVANTHANG/Front-end/assets/96326479/710561dc-4eb0-4df6-befe-386baa820e4a)

![image](https://github.com/CUNGVANTHANG/Front-end/assets/96326479/f1285c66-7479-4e0d-a112-fd1f7dacc2e0)

![image](https://github.com/CUNGVANTHANG/Front-end/assets/96326479/1ec88a8c-f4f5-4637-a2de-b1da53ec085a)

## I. React, ReactDOM
[:arrow_up: Mục lục](#mục-lục)

### 1. Làm quen với React
[:arrow_up: Mục lục](#mục-lục)

Để cài đặt gói **react** vào dự án, bạn cần cài đặt bằng trình quản lý gói (**npm** hoặc **yarn**).

Chúng ta sẽ sử dụng Trình quản lý Gói Node (npm).

```
npm install react
```

Dưới đây là cách thêm React (sau khi đã cài đặt React):

```jsx
import React from "react";
```

**React Element** là khối xây dựng nhỏ nhất đại diện cho một đơn vị nhỏ trong giao diện người dùng.

`React.createElement` trả về một đối tượng đại diện cho phần tử DOM.

Đối tượng có dạng như sau:

```jsx
const element = React.createElement("h1");
//returns an object similar to this one:
{
  type: 'h1',
  props: {}
}
```

Lý do tại sao `React.createElement` trả về một đối tượng thay vì phần tử DOM là vì React hoạt động dựa trên Virtual DOM (DOM ảo). Chúng ta sẽ tìm hiểu chi tiết sau này, trước hết hãy xem phần giải thích đơn giản về Virtual DOM:

Virtual DOM là một phiên bản của giao diện người dùng được lưu giữ trong bộ nhớ và được đồng bộ với DOM thật.

Vì vậy, `React.createElement()` trả về một đối tượng thay vì phần tử DOM vì điều này cho phép React tối ưu hóa hiệu suất (như Virtual DOM).

**Thay đổi lớp/kiểu dáng**

Cú pháp của hai phương thức tương tự nhau khi thiết lập các thuộc tính này:

```jsx
React.createElement("h1", {className: "center", style: "color: red"})
```

**Viết văn bản**

Để viết văn bản bên trong phần tử, bạn phải **cung cấp tham số thứ ba** cho `React.createElement`, được gọi là children (có thể truyền các phần tử React khác làm children).

```jsx
React.createElement("h1", {}, "Hello World")
```

### 2. Làm quen với React DOM
[:arrow_up: Mục lục](#mục-lục)

Hãy bắt đầu bằng việc cài đặt ReactDOM:

```
npm install react-dom
```

React và ReactDOM là hai phần của cùng một thư viện tên là React. Sau đó, chúng đã được tách ra thành hai thư viện độc lập là React và ReactDOM để tạo điều kiện cho việc phát triển React Native.

React Native là sự kết hợp giữa React và ứng dụng native. React là thư viện cho phép bạn viết UI có thể tái sử dụng và:

- ReactDOM làm cho UI đó hiển thị trên trình duyệt.
- React Native làm cho UI đó hiển thị trên ứng dụng native.

React tạo ra phiên bản ảo của UI trong bộ nhớ, sau đó ReactDOM nhận và đồng bộ hóa UI (và các thay đổi trong đó) vào DOM. Quá trình này được gọi là reconciliation.

Thêm phương thức `createRoot` của ReactDOM: 

```jsx
import {createRoot} from "react-dom/client"
```

Với phần tử root trên, chúng ta có thể hiển thị phần tử React đầu tiên:

```jsx
import {createRoot} from "react-dom/client";

const root = document.querySelector("#root");
createRoot(root).render(React.createElement("p", {}, "Hello World"));
```

## II. JSX
[:arrow_up: Mục lục](#mục-lục)

### 1. JSX
[:arrow_up: Mục lục](#mục-lục)

- **JSX là cú pháp rút gọn cho React.createElement**

Khi làm việc với React, bạn cần sử dụng `React.createElement` để biểu diễn giao diện người dùng. Tuy nhiên, **cú pháp của nó khá dài**. Cú pháp sẽ **trở nên càng dài và nhàm chán hơn** khi bạn bắt đầu phát triển giao diện người dùng phức tạp hơn.

React sử dụng một cú pháp đặc biệt được gọi là **JSX** **để giải quyết vấn đề đó**. Cú pháp **JSX** trông có vẻ giống **HTML**, nhưng nó KHÔNG PHẢI LÀ HTML.

```jsx
import React from "react";

const title = <h1>Hello World</h1>
```

nó sẽ biên dịch thành 

```jsx
import React from "react";

const title = React.createElement("h1", {}, "Hello World");
```

- **JSX KHÔNG PHẢI là một phần của trình duyệt**

Trình duyệt không hiểu được JSX vì đó là một cú pháp được tạo bởi React. Bạn sẽ cần một công cụ (như **babel**) để **chuyển đổi code JSX thành JavaScript thông thường** (sẽ chứa các cuộc gọi `React.createElement`). **Ngoài ra babel còn giúp cho các trình duyệt cũ có thể chạy được khi ta sử dụng ES6 (phiên bản mới so với ES5)**

- **Làm việc với JSX**

Vì JSX được chuyển đổi thành `React.createElement()` trả về một đối tượng, bạn có thể coi phần tử JSX như một đối tượng.

Vì vậy, bạn có thể coi `<h1 className="title">Supermarket</h1>` như một đối tượng với các thuộc tính sau (được đơn giản hóa):

```jsx
{
  type: 'h1',
  props: {
    className: "title",
    children: "Supermarket"
  }
}
```

- **Biểu thức trong JSX**
  
Bạn có thể sử dụng các biểu thức trên trong JSX bằng cách đóng gói trong dấu ngoặc nhọn `{expression}`.

_Ví dụ cơ bản:_

```jsx
const title = <h1>You have {2 + 3} notifications</h1>;
```

Câu lệnh này sẽ tạo một phần tử h1 chứa văn bản: **You have 5 notifications**.

**Gọi hàm:**

Bạn cũng có thể gọi hàm trong biểu thức, ví dụ:

```jsx
function capitalise(word) {
    return word[0].toUpperCase() + word.substring(1).toLowerCase();
}
const name = "brendan";

const element = <p className="user-info">Welcome {capitalise(name)}</p>
```

Đoạn code trên sẽ tạo một đoạn văn bản chứa nội dung: **Welcome Brendan** (lưu ý chữ B viết hoa).

- **Biểu thức thuộc tính**

JSX cũng hỗ trợ biểu thức thuộc tính, tức là giá trị của thuộc tính được xác định dựa trên biểu thức (hoặc thường là biến), ví dụ:

```jsx
const limit = 5;

const element = <input type="number" max={limit} />;
```

Khi chuyển đổi thành `React.createElement()`, code sẽ có dạng:

```jsx
const limit = 5;
const element = React.createElement("input", {
  type: "number",
  max: limit
});
```

Ví dụ này cho thấy các thuộc tính có thể có giá trị chuỗi cũng như giá trị động; ví dụ: thuộc tính max lấy giá trị của biến limit.

**Số và boolean**

Giá trị của các thuộc tính số và boolean nên được truyền dưới dạng biểu thức:

```jsx
<input max={2} disabled={true} className="textbox" />
```

- **Luôn đóng gói các phần tử JSX bằng `()` khi viết JSX sau một lệnh re**turn.

```jsx
const getList = () => {
    return (
        <ul>
            <li>First Item</li>
            <li>Second Item</li>
        </ul>
    );
}
```

- **Trả về nhiều element bằng JSX Fragments**

React giúp giải quyết vấn đề này bằng cách yêu cầu trả về một **Fragment** đóng gói các phần tử cần trả về.

Vì vậy, nếu bạn muốn trả về HTML dưới đây từ một hàm:

```jsx
<h1>Grocery delivered to your door</h1>
<h2>Free delivery</h2>
<p>Get started now!</p>
```

Bạn sẽ phải sử dụng một Fragment đóng gói 3 phần tử này:

```jsx
function getHeroBanner() {
    return (
        <>
            <h1>Grocery delivered to your door</h1>
            <h2>Free delivery</h2>
            <p>Get started now!</p>
        </>
    );
}
```

Cú pháp ngắn gọn cho `React.Fragment` (`<>` và `</>`) vừa được đề cập ở trên.

Bạn có thể thấy ở đâu đó sử dụng cú pháp gốc dài hơn với `React.Fragment`:

```jsx
function getHeroBanner() {
    return (
        <React.Fragment>
            <h1>Grocery delivered to your door</h1>
            <h2>Free delivery</h2>
            <p>Get started now!</p>
        </React.Fragment>
    );
}
```

Sử dụng `React.Fragment` (`<></>`) để bọc các phần tử con và bạn cần cung cấp một thuộc tính `key` để mỗi phần tử trong danh sách có một định danh duy nhất. Thuộc tính `key` giúp React theo dõi và cập nhật hiệu quả các phần tử trong danh sách khi chúng thay đổi.

_Ví dụ:_

```jsx
import React from 'react';

function MyComponent({ items }) {
  return (
    <div>
      {items.map(item => (
        <React.Fragment key={item.id}>
          <h1>{item.title}</h1>
          <p>{item.description}</p>
        </React.Fragment>
      ))}
    </div>
  );
}

export default MyComponent;
```

### 2. Component
[:arrow_up: Mục lục](#mục-lục)

Component React là một mẫu hoặc bản thiết kế cho phép bạn mô tả một phần của giao diện người dùng; ví dụ: `<Footer></Footer>` là component mô tả phần chân trang.

_Ví dụ:_

Dưới đây là một ví dụ về component React:

```jsx
function Footer() {
    return (
        <div>
            <h3>Company name</h3>
            <p>All rights reserved</p>
        </div>
    );
}
```

Sau khi định nghĩa, component Footer có thể được sử dụng trong cùng một file JavaScript với JSX:

```jsx
import {createRoot} from "react-dom/client";

function Footer() {
    return (
        <div>
            <h3>Company name</h3>
            <p>All rights reserved</p>
        </div>
    );
}

const root = document.querySelector("#root");

createRoot(root).render(<Footer></Footer>);
```

Chúng ta gọi đây là **function component** vì Component được định nghĩa dưới dạng **hàm**.

- **Tên component viết hoa chữ cái đầu (UpperCamelCase)**

Bạn có thể nhận thấy đoạn code trên gọi hàm là **Footer** thay vì **footer**. Điều này là cần thiết. **Ký tự đầu tiên phải viết hoa** để React nhận biết rằng đó là một **Component**; lý do sẽ được giải thích trong bài học tiếp theo.

Hãy luôn viết tên hàm theo kiểu UpperCamelCase; dưới đây là một số ví dụ:

- Footer
- ChatMessage
- Button
- ListItem

- **Quy tắc code: Một file chỉ chứa 1 Component**

Một ứng dụng được xây dựng bằng React sẽ có **nhiều component**.

Quy ước là định nghĩa **một component trong mỗi file riêng biệt** để sau này dễ dàng tìm thấy nó (có một số ngoại lệ, nhưng hiện tại bạn chưa cần để ý đến những ngoại lệ này).

Tên file phải khớp với tên Component, ví dụ:

- file: `Footer.js` cho Component Footer
- file: `AppNavbar.js` cho Component AppNavbar

**index.js**

Ứng dụng sẽ có một file `index.js` là điểm mà quá trình chạy ứng dụng bắt đầu (đôi khi được gọi là `app.js`).

Vì vậy, bạn sẽ định nghĩa các component trong những file khác và sau đó sử dụng chúng trong `index.js`.

_Ví dụ:_

Hãy xem một ví dụ bằng cách sử dụng hai file: **Footer.js** và **index.js**:

File `Footer.js` định nghĩa component Footer:

```jsx
//Footer.js
export default function Footer() {
    return (
        <>
             <h3>Footer</h3>
             <p>All rights reserved</p>
        </>
    );
}
```

Để ý file này sử dụng `default export` để khai báo component Footer.

Điều này là bắt buộc để có thể sử dụng component Footer trong các file khác.

```
//index.js
import {createRoot} from "react-dom/client";
import Footer from "./Footer.js";

function App() {
    return (<>
         <Footer />
         <Footer />
    </>);
}

const root = document.querySelector("#root");

createRoot(root).render(<App />);
```

Để ý component Footer đã được thêm vào file `index.js` từ `./Footer.js` để file có thể sử dụng component.

Điều đó là vì `<Footer />` được chuyển đổi thành: `React.createElement(Footer, {})` vì vậy để component hoạt động, hàm Footer phải có phạm vi hoạt động trong file `index.js`, tức là nó phải được thêm vào file.

Ngoài ra, đoạn code hiển thị Footer hai lần bằng cách sử dụng component hai lần trong component App.

**Class Component:**

Functional component sau đây:

```jsx
import {createRoot} from "react-dom/client";

function App() {
    return (<h1>Hello World</h1>);
}

createRoot(document.querySelector("#react-root")).render(<App />);
```

Có thể được viết dưới dạng lớp:

```jsx
import React from "react";
import {createRoot} from "react-dom/client";

class App extends React.Component {
    render() {
        return (<h1>Hello World</h1>);
    }
}

createRoot(document.querySelector("#react-root")).render(<App />);
```

Để ý là phần `react-dom` không thay đổi chút nào. Điểm khác biệt duy nhất là chúng ta **định nghĩa một lớp thay vì hàm**.

**Class... kế thừa từ React.Component**

Thêm một chi tiết nữa: lớp phải mở rộng (kế thừa) từ `React.Component`.

Điều này sẽ cho phép component kế thừa tất cả các chức năng cần thiết từ thư viện React.

Bạn có thể thấy cú pháp `React.Component` hơi khó hiểu vì những lý do sau:

- React là một đối tượng.
- Component là một trường thuộc tính trên đối tượng React mà bạn truy cập bằng `React.Component`.
- `React.Component` là một lớp nên chúng ta có thể kế thừa từ nó.

Nếu muốn, bạn cũng có thể thêm trực tiếp Component từ một file khác trong React, sau đó code trở thành:

```jsx
import {Component} from "react"; // this changed
import {createRoot} from "react-dom/client";

class App extends Component { // this changed
    render() {
        return (<h1>Hello World</h1>);
    }
}

createRoot(document.querySelector("#react-root")).render(<App />);
```

### 3. Props
[:arrow_up: Mục lục](#mục-lục)

- **Props**

Giả sử chúng ta có một component tên là **<GreetUser />** hiển thị: **Welcome Sam** hoặc **Welcome Alex**.

Chúng ta cần làm cho component hiển thị **Welcome** và sau đó là tên người dùng.

Hãy bắt đầu bằng phiên bản hiển thị thủ công của component này:

```jsx
//GreetUser.js
export default function GreetUser() {
    return <div>Welcome USER</div>;
}
```

Component **<GreetUser />** sẽ hiển thị **Welcome USER**.

Thay vì hiển thị **<GreetUser />**, chúng ta có thể hiển thị **<GreetUser user="Sam" />**.

`user="Sam"` là thuộc tính user với giá trị Sam được thêm vào component **GreetUser**.

Bây giờ chúng ta có thể đọc `user="Sam"` này như một đối tượng: {user: "Sam"}.

Chúng ta gọi đối tượng đó là **props** (viết tắt của properties - trường thuộc tính).

```jsx
//GreetUser.js
export default function GreetUser(props) {
    console.log(props); // {user: "Sam"}
    return <div>Welcome USER</div>;
}
```

Trường thuộc tính được truyền bây giờ nằm bên trong đối tượng mà hàm **GreetUser** nhận làm đối số đầu tiên.

Vì vậy, chúng ta có thể sử dụng biểu thức để hiển thị tên người dùng (có thể đọc là `props.user`):

```jsx
//GreetUser.js
export default function GreetUser(props) {
    return <div>Welcome {props.user}</div>;
}
```

`<GreetUser user="Sam"/>` sẽ hiển thị `<div>Welcome Sam</div>`

`<GreetUser user="Alex"/>` sẽ hiển thị `<div>Welcome Alex</div>`

Điều này làm cho component linh hoạt hơn và có thể tái sử dụng!

- **Props con**

Có một loại props đặc biệt dành cho trường thuộc tính con. Hãy xem một ví dụ:

```jsx
const element = <HeroTile>Welcome!</HeroTitle>
```

Nội dung nằm giữa các thẻ `<HeroTitle>` và `</HeroTitle>` được gọi là trường thuộc tính con.

Bạn có thể truy cập vào bằng cách sử dụng props.children, ví dụ:

```jsx
const element = <HeroTitle>Welcome!</HeroTitle>
```

Một ví dụ về `props.children` là chuỗi "Welcome!", nhưng trên thực tế, nó có thể là bất cứ kiểu dữ liệu nào.

`props.children` có thể tham chiếu đến các phần tử hoặc component React khác (hoặc thậm chí là nhiều component); ví dụ:

```jsx
function Navbar(props){
    return <div className="navbar">{props.children}</div>;
}

const element = <Navbar>
    <HeroTitle>Welcome!</HeroTitle>
    <div>Some content</div>
    <p>Another content</p>
</Navbar>;
```

Trong ví dụ này, `props.children` là một mảng chứa 3 mục:

```jsx
<HeroTitle>Welcome!</HeroTitle>
<div>Some content</div>
<p>Another content</p>
```

**Props trong class Component:**

Trong class component, các `props` được nhận bởi `constructor` của lớp `React.Component` và được lưu trữ như các biến thực thể `this.props`.

Vì vậy, nếu bạn muốn truy cập vào `props` từ bất kỳ đâu bên trong component, bạn cần sử dụng `this.props`. Ví dụ:

```jsx
import React from "react";

class App extends React.Component {
    render() {
        console.log(this.props); // {size: "large"}
        return (<h1>Hello World</h1>);
    }
}

const element = <App size="large" />;
```

Bạn có thể **truy cập** vào `props` **ở bất kỳ đâu** trong lớp bằng cách sử dụng `this.props`.

**Ghi đè constructor (cách cũ)**

Chúng ta có thể sẽ cần ghi đè `constructor` để xử lý sự kiện. Trong trường hợp đó, bạn cần cẩn thận và đảm bảo truyền `props` cho `constructor` cha bằng `super(props)`.

Vì lớp kế thừa từ `React.Component` và bạn đang ghi đè `constructor()`, điều này có nghĩa là `constructor()` của `React.Component` sẽ không được thực thi nữa.

Vì vậy, bạn sẽ phải gọi `super(props)`, điều này sẽ truyền `props` cho `constructor` của `React.Component`. Sau đây là cú pháp:

```jsx
import React from "react";

class App extends React.Component {
    constructor(props) {
        super(props); // has to be the first line inside the constructor
        // the rest of your constructor code can go here
        this.state = {};
    }

    render() {
        console.log(this.props); // {...}
        return (<h1>Hello World</h1>);
    }
}
```

Ở trên, `constructor()` nhận `props` và sau đó truyền chúng cho `constructor` của lớp cha (`React.Component`) bằng cách sử dụng `super(props)`.

Nhắc lại kiến thức cũ, `super` là một từ khóa JavaScript cho phép bạn truy cập vào các phương thức trên lớp cha.

`super(props)` phải là dòng đầu tiên trong `constructor`. Và sau đó, trong `constructor` đó, bạn có thể truy cập `props` bằng `this.props` hoặc `props`. Hãy nhớ rằng không bao giờ thay đổi giá trị của `props`.

**Sử dụng public class fields (cách mới)**

Bạn nên sử dụng cú pháp mới này vì nó đơn giản hơn. Bạn không cần ghi đè `constructor` hoặc gọi `super`.

Sử dụng cú pháp `public class fields` của JavaScript, bạn có thể định nghĩa biến trạng thái như sau:

```jsx
import React from "react";

class App extends React.Component {
    // public class fields
    state = {};

    render() {
        console.log(this.props); // {...}
        return (<h1>Hello World</h1>);
    }
}
```

### 4. Cách viết hàm chuẩn
[:arrow_up: Mục lục](#mục-lục)

- **Hàm thuần túy (Pure function)**

Tất cả các component React không bao giờ thay đổi các props của chúng.

Điều này có nghĩa là **bạn không nên thay đổi giá trị của prop bên trong component**; hãy xem một ví dụ:

```jsx
function Notifications(props) {
    // ❌ 
    props.data.count = props.data.count - 1;
    return <h3>You have {props.data.count} unread notifications.</h3>;
}

const notifications = {
    count: 3
};

const element = <Notifications data={notifications} />;
console.log(notifications); // {count: 2}
```

Để ý việc sử dụng phần tử `<Notifications  data={notifications}/>` có tác dụng phụ là thay đổi giá trị của props `(notifications.count)`.

Thay vào đó, code nên được viết như sau:

```jsx
function Notifications(props) {
    // ☑️ 
    const value = props.data.count - 1;
    return <h3>You have {value} unread notifications.</h3>;
}

const notifications = {
    count: 3
};

const element = <Notifications data={notifications} />;
console.log(notifications); // {count: 3}
```

Vì vậy, bạn nên **coi props là thuộc tính chỉ đọc.**

### 5. Sử dụng thư viện clsx để viết câu lệnh if
[:arrow_up: Mục lục](#mục-lục)

- **Để cài đặt clsx, chạy lệnh:**

```
npm install clsx
```

- **Thêm clsx vào file**

Bạn có thể sử dụng clsx trong bất kỳ bài tập React nào bằng cách nhập lệnh import vì gói đã được cài đặt sẵn.

Để thêm **clsx**, bạn phải thêm clsx từ tên gói:

```
import clsx from "clsx";
```

- **Các lớp có điều kiện**:

Sau khi đã thêm **clsx**, hãy xem cách thư viện giúp đơn giản hóa việc sử dụng lớp có điều kiện:

```jsx
import clsx from "clsx";

const result = clsx({
    "link": true,
    "link-primary": true
});

console.log(result); //"link link-primary"
```

Chúng ta đã truyền cho **clsx** một đối tượng chứa:

- khóa link với giá trị true
- và khóa `link-primary` với giá trị true, kết quả trả về một chuỗi chứa cả hai lớp được phân tách bằng dấu cách.

Hãy xem một ví dụ khác:

```jsx
import clsx from "clsx";

const result = clsx({
    "link": true,
    "link-primary": false
});

console.log(result); //"link"
```

Đây về cơ bản cùng một cách làm như ví dụ trước. Tuy nhiên, lần này chúng ta chỉ định rằng `link-primary` là `false`, vì vậy chuỗi kết quả sẽ **không bao gồm link-primary**.

Thay vì thiết lập giá trị cố định là true hoặc false, điều gì sẽ xảy ra nếu chúng ta thay thế chúng bằng một biến hoặc kết quả của một biểu thức? Ví dụ:

```jsx
import clsx from "clsx";

function MyComponent(props) {
    const className = clsx({
        "title": props.loggedIn
    });

    return <h1 className={className}></h1>
}

const example1 = <MyComponent loggedIn={true} />; // className="title"
const example2 = <MyComponent loggedIn={false} />; // className=""
```

Trong đoạn code trên, `props.loggedIn` là một giá trị boolean. Chúng ta sử dụng giá trị boolean đó để thêm/xóa lớp title theo điều kiện:

- khi `props.loggedIn` là **true**, clsx nhận `{"title": true}` và trả về chuỗi title.
- Ngược lại, khi `props.loggedIn` là **false**, clsx nhận`{"title": false}` và trả về chuỗi rỗng "".

### 6. Truyền props sử dụng toán tử Spread
[:arrow_up: Mục lục](#mục-lục)

Việc sử dụng cú pháp này trong JSX đôi khi có khá nhiều công dụng hữu ích. Ví dụ, bạn có **một Component nhận nhiều props** và bạn muốn lấy ra **children**, sau đó **destructure tất cả các props còn lại vào một biến mới** và truyền chúng vào một phần tử:

```jsx
function Navbar(props) {
    const {children, ...rest} = props;
    return <h1 {...rest}>{children}</h1>;
}
```

Chúng ta bắt đầu bằng cách `destructure children` từ props, sau đó chúng ta tạo một đối tượng mới gọi là rest chứa tất cả các props khác.

Và cuối cùng, chúng ta sử dụng cú pháp `spread` để truyền đối tượng này vào `<h1>`, theo đó truyền toàn bộ props vào phần tử `<h1>`.

Ví dụ, nếu bạn sử dụng Navbar như sau: `<Navbar tabIndex="2" className="navbar">Hello World</Navbar>`, bạn sẽ nhận được biến `children = "Hello World"` và biến rest với đối tượng sau:

```jsx
{
    tabIndex: "2",
    className: "navbar"
}
```

và sau đó Component sẽ trả về phần tử React sau:

```jsx
<h1 tabIndex="2" className="navbar">Hello World</h1>
```

Giả sử chúng ta thêm một thuộc tính mới, ví dụ: `disabled={true}`, khi đó code vẫn hoạt động và vẫn áp dụng thuộc tính **disabled** cho h1 **mà không cần cập nhật Component**.

### 7. Trích xuất giá trị từ mảng với Destructuring
[:arrow_up: Mục lục](#mục-lục)

Hãy giả sử chúng ta có đối tượng person sau:

```jsx
const person = {
    firstName: "Sam",
    lastName: "Doe",
    age: 24
}
```

và bạn muốn tạo 2 biến firstName và lastName:

```jsx
const firstName = person.firstName;
const lastName = person.lastName;
```

Bạn có thể làm điều đó trong một dòng bằng cú pháp destructuring sau:

```jsx
const {firstName, lastName} = person;
```

Bạn cũng có thể cung cấp giá trị mặc định cho biến trong trường hợp không có giá trị tương ứng trong đối tượng. Ví dụ:

```jsx
const {firstName, lastName, status = 'single'} = person;
```

Trong trường hợp này, `status` sẽ có giá trị mặc định là `"single"` vì đối tượng `person` không có thuộc tính này.

Bạn cũng có thể destructuring biến props trong đối số, thoạt nhìn thì code có vẻ khó đọc nhưng bạn sẽ thấy nó được sử dụng khá nhiều trong thực tế:

```jsx
function WelcomeUser({username, notifications}) {
    return <div>Welcome {username}! You've got {notifications} unread notifications.</div>;
}
```

Thay vì viết WelcomeUser(props), bạn ngay lập tức thay thế props bằng `{username, notifications}`, lệnh này trích xuất `props.username` và `props.notifications` và tạo ra 2 biến: `username` và `notifications`.

### 8. Ký hiệu dấu chấm
[:arrow_up: Mục lục](#mục-lục)

Vì JSX luôn chuyển đổi `<Component />` thành cuộc gọi `React.createElement(Component, {})`, do đó một đối tượng có thể chứa nhiều component, ví dụ:

```jsx
const Buttons = {
    Default: function(props) {
        return <button className="btn-default">{props.children}</button>;
    },
    Outline: function(props) {
        return <button className="btn-outline">{props.children}</button>;
    }
}
```

Sau đó, bạn có thể sử dụng các component trên như sau:

```jsx
<Buttons.Default>Login</Buttons.Default>
<Buttons.Outline>Register</Buttons.Outline>
```

Lý do tại sao điều này hoạt động là vì chúng sẽ được chuyển đổi thành các cuộc gọi `React.createElement` như sau:

```jsx
React.createElement(Buttons.Default, {}, "Login");
React.createElement(Buttons.Outline, {}, "Register");
```

Chúng ta đã sử dụng `ThemeContext.Provider` trong các chương về `Context`:

```jsx
return (
    <ThemeContext.Provider value={value}>
      {props.children}
    </ThemeContext.Provider>
  );
```

Cú pháp cũng được sử dụng trong các Thư viện Giao diện người dùng, trong đó thư viện sẽ xuất tất cả các nút trong một đối tượng duy nhất tên là `Buttons`, và sau đó bạn có thể chọn loại nút bằng cách sử dụng `Buttons.Default` hoặc `Buttons.Outline`.

Cú pháp tương tự cũng được áp dụng cho `<React.StrictMode />`.

### 9. dangerouslySetInnerHTML
[:arrow_up: Mục lục](#mục-lục)

Hãy xem xét component sau:

```jsx
function Footer() {
    const text = "<strong>All rights reserved ©</strong>";

    return <div>{text}</div>;
}
```

Dự đoán sẽ hiển thị: All rights reserved © (in đậm)

Kết quả thực tế là: <strong>All rights reserved &copy;</strong> không in đậm và ký hiệu bản quyền được hiển thị dưới dạng một thực thể HTML.

React sẽ tự động thoát các thực thể HTML (chuyển đổi thực thể HTML thành ký tự an toàn). Đây là một tính năng bảo mật nhằm ngăn chặn `XSS injectio`

**XSS Injection là gì?**

Cross-Site Scripting (XSS) là một lỗ hổng bảo mật trong đó người dùng có thể chèn code của họ (HTML, CSS hoặc JavaScript) vào trang web của bạn. Giả sử bạn muốn gửi lời chúc mừng sinh nhật cho bạn bè trên mạng xã hội. Thay vì viết: **Happy Birthday**, bạn viết:

```html
<script>alert("You got hacked!")</script>
```

Nếu trang mạng xã hội cho phép bạn viết tập lệnh của riêng bạn và hiển thị trên trang, đây sẽ là một lỗ hổng bảo mật nghiêm trọng vì bạn có thể đọc cookie của người dùng, mạo danh người dùng, chuyển hướng đến các trang web khác và thực hiện nhiều hành vi khác.

Để ngăn chặn XSS Injection, bạn cần thoát các phần tử HTML (nói một cách đơn giản).

Vì vậy, đoạn code ở trên trở thành: `&lt;script&gt;alert("You got hacked!")&lt;/script&gt;`. Bằng cách thoát các ký tự `<` và `>`, trình duyệt sẽ hiểu đoạn code trên là văn bản thông thường thay vì một đoạn lệnh.

**Biểu thức JSX được thoát:**

Tuy nhiên, **có các tình huống mà bạn muốn ghi đè lên hành vi này và bỏ qua biện pháp phòng ngừa**. 

```jsx
function Footer() {
    const text = "<strong>All rights reserved ©</strong>";

    return <div dangerouslySetInnerHTML={{__html: text}}></div>;
}
```

Để ý là chúng ta đã loại bỏ biểu thức `{text}` và thêm một prop tên là `dangerouslySetInnerHTML`, nó nhận đối tượng `{__html: text}` được đóng gói bởi biểu thức `{}` (vì vậy chúng ta có `{{}}`, một cho đối tượng và một cho biểu thức).

Bên trong đối tượng này, bạn phải đặt khóa `__html` (hai dấu gạch dưới). Việc thiết kế `dangerouslySetInnerHTML` với cấu trúc phức tạp như vậy nhằm mục đích nhắc nhở bạn rằng việc sử dụng nó tiềm ẩn các rủi ro bảo mật.

## III. Hook - useState
[:arrow_up: Mục lục](#mục-lục)

### 1. useState
[:arrow_up: Mục lục](#mục-lục)

- **Cài đặt useState**

Hãy bắt đầu bằng cách tạo biến trạng thái đầu tiên.

Để làm điều đó, chúng ta cần thêm hàm **useState** từ gói `"react"`.

**useState** là một named export có cú pháp thêm là:

```jsx
import {useState} from "react";
```

Nếu bạn đã thêm React vào trong cùng một file, bạn có thể kết hợp các lệnh import thành một lệnh import duy nhất. Ví dụ:

```jsx
import React from "react";
import {useState} from "react";
```

2 câu lệnh có thể được kết hợp thành một lệnh import duy nhất:

```jsx
import React, {useState} from "react";
```

Thoạt nhìn cú pháp có thể trông hơi lạ mắt, nhưng bạn hãy nhớ rằng:

1. React là **default export** (không có dấu ngoặc nhọn)
2. useState là **named export** (được đóng gói trong dấu ngoặc nhọn)

- **useState trả về cái gì?**

useState trả về một mảng gồm 2 phần tử:

1. phần tử đầu tiên là **giá trị hiện tại của trạng thái**
2. phần tử thứ hai là một hàm cập nhật trạng thái

Vì vậy, thay vì viết:

```jsx
const result = useState(0)
const seconds = result[0];
const setSeconds = result[1];
```

Chúng ta sẽ sử dụng cú pháp array destructuring:

```jsx
const [seconds, setSeconds] = useState(0);
```

`seconds` hiện tại là một số có giá trị `0` và `setSeconds` là một hàm.

Điều quan trọng là đặt tên các thuộc tính được destructure như sau:

1. Phần tử đầu tiên nên lấy tên của trạng thái (trong ví dụ này là `seconds`)
2. Phần tử thứ hai có phần đầu là `set` và theo sau là tên trạng thái viết hoa chữ cái đầu (trong ví dụ này là `setSeconds`)

Điều này quan trọng vì khi các component trở nên phức tạp hơn, chúng ta cần biết rằng **seconds là trạng thái** và **setSeconds là hàm cập nhật trạng thái của seconds**.

**Các điểm quan trọng cần lưu ý:**

1. Bạn chỉ nên gọi **useState bên trong component**, không phải bên ngoài.
2. **useState nên là thành phần đầu tiên được gọi bên trong hàm**

- **Thay đổi trạng thái?**

Trạng thái là **một biến mà chúng ta có thể cập nhật** vào thời điểm nào đó trong tương lai.

Để cập nhật trạng thái, **bạn luôn phải sử dụng hàm 'set' nhận được từ useState**.

Vì vậy nếu ta tạo một trạng thái gọi là `seconds` thì ta sẽ sử dụng hàm `setSeconds(newValue)` đã được destructure. Hãy sử dụng Component Stopwatch giống như trước đây:

```jsx
import {useState} from "react";

function Stopwatch() {
    // hooks have to be at the top
    const [seconds, setSeconds] = useState(0);

    return (<>
        <h2>{seconds}</h2>
        {/* increment seconds state by 1, when you click on the button*/}
        <button onClick={() => setSeconds(seconds + 1)}>Click to add 1</button>
    </>);
}
```

Đoạn code cập nhật trạng thái bằng cách gọi `setSeconds()` và truyền vào đó giá trị mới của trạng thái.

Giá trị mới của trạng thái là `seconds + 1`, tương đương với: **giá trị hiện tại + 1**.

Điều đó xảy ra là vì `seconds` lưu giữ giá trị hiện tại của trạng thái, vì vậy `seconds + 1` sẽ **tăng giá trị đó lên 1.**

- **Thay đổi trạng thái có điều kiện: Props**

Giả sử chúng ta có một **component có thể tăng giá trị của bộ đếm**. Tuy nhiên, component này **có thể được kích hoạt hoặc vô hiệu hóa**. Khi component bị vô hiệu hóa, bộ đếm sẽ không tăng giá trị.

```jsx
import {useState} from "react";

function Counter(props) {
    const [counter, setCounter] = useState(0);

    function handleIncrementClick() {
        if (props.enabled){
            setCounter(counter + 1);
        }
    }

    return (<>
        <h2>{counter} times clicked</h2>
        <button onClick={handleIncrementClick}>Add 1</button>
    </>);
}

// Sample usages:
const element1 = <Counter enabled={true} />;
const element2 = <Counter enabled={false} />;
```

Chúng ta có thể kiểm tra giá trị của Prop và dựa trên đó thay đổi trạng thái như sau:

```jsx
if (props.enabled) {
    setCounter(counter + 1);
}
```

- **Stale state**

```jsx
const Counter = () => {
    const [count, setCount] = useState(0);
    const handleIncrement = () => {
        setTimeout(function delay() {
            setCount(count + 1);
        }, 1000);
    };

    return <div onClick={handleIncrement}>Increment {count}</div>;
};
```

Kết quả của đoạn code trên là khi ta bấm 5 lần thì nó vẫn chỉ hiện thị 1. Đây còn gọi là hiện tượng Stale state, khi mà ta cố gắng thay đổi giá trị của biến bên ngoài trong function. Để khắc phục điều này chúng ta sử dụng callback

```jsx
const Counter = () => {
    const [count, setCount] = useState(0);
    const handleIncrement = () => {
        setTimeout(function delay() {
            setCount((count) => count + 1);
        }, 1000);
    };

    return <div onClick={handleIncrement}>Increment {count}</div>;
};
```

**State trong class Component:**

Với class component, trạng thái được khai báo như một biến thực thể tên là `state`. Do đó, bạn có thể truy cập vào nó bằng `this.state`.

Vì vậy, functional component sau đây:

```jsx
import {useState} from "react";

function Button() {
    const [isDisabled, setIsDisabled] = useState(false);

    return <button disabled={isDisabled}>Button text</button>;
}
```

có thể được viết lại thành một class component:

```jsx
class Button extends React.Component {
    state = {
        isDisabled: false
    };

    render() {
        return <button disabled={this.state.isDisabled}>Button text</button>;
    }
}
```

**Cập nhật trạng thái**

Tương tự như với hook, việc cập nhật trạng thái trực tiếp không được phép. Thay vào đó, bạn phải sử dụng một phương thức đặc biệt. Trong class component, bạn có sẵn phương thức thực thể `this.setState()` được thừa kế từ `React.Component`.

**Nhiều trạng thái**

Chúng ta cũng có thể định nghĩa nhiều trạng thái trong cùng một class component. Biến thực thể `state` là một đối tượng, vì vậy bạn có thể thêm nhiều prop `key/value`. Ví dụ:

```jsx
// inside the constructor
this.state = {
    isDisabled: false,
    grades: [10, 20],
    counter: 0
}
```

### 2. Closures
[:arrow_up: Mục lục](#mục-lục)

Hiểu đơn giản là truy xuất 1 biến ở bên ngoài function được gọi là **Closure**

**Closure** là khi hàm bên trong có quyền truy cập vào các biến của hàm bên ngoài. Hãy xem ví dụ dưới đây:

```jsx
function getUser() {
    const name = "Sam";

    function getWelcomeMessage() {
        return `Hello ${name}`;
    }

    return {
        name: name,
        message: getWelcomeMessage()
    }
}
```

Chúng ta có một closure ở đây vì chúng ta có hàm `getWelcomeMessage` bên trong hàm `getUser`.

Giải thích đoạn code:

- Hàm getUser định nghĩa biến name có giá trị là "Sam".
- Bên trong hàm đó, chúng ta định nghĩa hàm getWelcomeMessage trả về Hello ${name}.
- Sau đó, chúng ta return một đối tượng chứa name và message, trong đó message là kết quả trả về bởi `getWelcomeMessage()`.

Như bạn thấy, biến `name` có thể được truy cập bởi hàm `getWelcomeMessage` vì `getWelcomeMessage` được định nghĩa bên trong `getUser`.
Vì vậy, vì `name` được định nghĩa trong `getUser`, nó có thể được truy cập bởi bất kỳ hàm nào được định nghĩa bên trong `getUser`, trong ví dụ này là `getWelcomeMessage`.

### 3. Các nguyên tắc khi làm việc với Hooks
[:arrow_up: Mục lục](#mục-lục)

Để hook hoạt động chính xác, bạn phải tuân theo hai quy tắc.

- Quy tắc số 1: Chỉ gọi Hook từ các hàm React
- Quy tắc số 2: Chỉ gọi Hook ở Cấp độ trên cùng và **không bao giờ gọi hook trong vòng lặp, điều kiện if hoặc các hàm lồng nhau**.

React phụ thuộc vào thứ tự các hook được gọi để hoạt động một cách chính xác.

### 4. Tính bất biến trong ReactJS
[:arrow_up: Mục lục](#mục-lục)

Hãy bắt đầu bằng việc so sánh số, chuỗi và boolean:

```
1 === 1; //true
27 === 27; //true
"hello world" === "hello world"; //true
"welcome" === "welcome"; //true
true === true; //true
false === false; //true (because they're the same)
```

Không có gì đặc biệt ở đây. Chúng ta đang so sánh hai giá trị hoàn toàn giống nhau, vì vậy kết quả là true.

Bây giờ hãy thử với mảng và đối tượng:

```
[] === []; //false
{} === {}; //false
[10] === [10]; //false
{key: "something"} === {key: "something"}; //false
```

Chú ý: bạn vẫn nhận được `false` ngay cả khi bạn sử dụng `==` thay vì `===`.

Mảng và Đối tượng đều được coi là đối tượng trong JavaScript.

Khi bạn viết `[]`, bạn đang tạo một thực thể mới của **Array**.

Khi bạn viết `{}`, bạn đang tạo một thực thể mới của **Object**.

```
new Array(); // creates []
new Object(); //creates {}
```

Hãy quay lại ví dụ trước và thay đổi các mảng và đối tượng thành cú pháp mới:

```
new Array() === new Array(); //false
new Object() === new Object(); //false

const arr1 = new Array();
arr1.push(10);
const arr2 = new Array();
arr2.push(10);
arr1 === arr2; //false

const obj1 = new Object();
obj1.key = "something";
const obj2 = new Object();
obj2.key = "something";
obj1 === obj2; //false
```

Điều này sẽ giải thích lý do tại sao chúng không bằng nhau.

`new Array()` tạo ra một **thực thể mới của mảng**.

Mỗi lần bạn gọi `new Array()`, bạn nhận được một thực thể mới, tức là `new Array()` **chắc chắn không giống** `new Array()` vì chúng là **các thực thể khác nhau**.

Vì vậy, với Mảng và Đối tượng, chúng ta cần một phương pháp khác để so sánh ngang bằng từ quan điểm giá trị.

Chúng ta mong đợi `[] === []` là `true` vì chúng đều là mảng rỗng, nhưng JavaScript lại hoạt động theo cách khác, nó kiểm tra xem chúng có phải là cùng một thực thể hay không.

- **Tính bất biến (Immutability) là gì?**

**Đối tượng bất biến là một đối tượng không thể thay đổi. Mỗi lần cập nhật tạo ra một giá trị mới, không làm thay đổi giá trị cũ.**

Hãy cùng tìm hiểu lý do tại sao React yêu cầu tính bất biến khi làm việc với Mảng và Đối tượng. Giả sử bạn đã viết Component sau:

```jsx
import {useState} from "react";

function App() {
  const [data, setData] = useState([]);
  
  function handleAddClick() {
      data.push(10)
      setData(data);
  }

  return <button onClick={handleAddClick}>Add 10</button>;
}
```

Đây không phải là cách chính xác để thêm **10** vào trạng thái data (mảng). Nhưng hãy xem lý do tại sao và điều gì xảy ra sau cùng.

Khi bạn gọi `useState` với một mảng rỗng, `const [data, setData] = useState([])`, nó sẽ tạo một biến trạng thái với giá trị `[]`.

Sau đó, hàm `setData` sẽ lấy `newState` (giá trị mới của trạng thái) và kiểm tra xem nó đã thay đổi chưa. Nếu nó đã thay đổi, nó sẽ yêu cầu ReactDOM hiển thị lại Component này.

Nếu chúng ta viết một hàm setData đơn giản, nó sẽ có dạng như sau:

```jsx
let state = []; //created by `useState([])`

// newState is the result of `data.push(10)` on <button /> click 
function setData(newState) {
  if (state === newState) {
    // no need to re-render because the state has not changed
    return false;
  }
  // store the newState for the next time the user calls setData()
  state = newState;
  // Ask ReactDOM to re-render
}
```

Để ý React đã so sánh `state === newState`. Điều này cho React biết trạng thái đã thay đổi hay chưa.

Nếu `state === newState` là `true`, **điều đó có nghĩa là trạng thái KHÔNG thay đổi, tức là không cần hiển thị lại Component.**

Nhưng khi `state === newState` là `false`, **điều đó có nghĩa là trạng thái đã thay đổi và React phải hiển thị lại Component bằng ReactDOM.**

- **Điều gì xảy ra khi không sử dụng tính bất biến?**

Trong ví dụ trước, chúng ta sử dụng `data.push(10)` để thay đổi mảng. Nếu chúng ta viết tất cả các thao tác theo từng dòng, chương trình sẽ trông như sau:

```jsx
let state = []; //from useState([])
let newState = state;
state.push(10);

state === newState; //true, whereas it should have been false
```

Vì **chúng ta đã thay đổi mảng bằng `.push`**, React sẽ nghĩ rằng chúng ta **CHƯA thay đổi trạng thái** và do đó sẽ **KHÔNG hiển thị lại Component.**

Và đây là lý do tại sao React yêu cầu sử dụng tính bất biến.

Vì vậy, cách duy nhất để `state === newState` trả về false khi ta sửa đổi mảng là trả về một mảng mới. 

Lưu ý rằng React sử dụng toán tử `===` thay vì so sánh sâu vì so sánh sâu thường khá chậm (khi số lượng Component trong ứng dụng tăng lên).

Đây là lý do tại sao mỗi khi bạn có một trạng thái của mảng hoặc đối tượng, chúng phải là bất biến.

### 5. Trạng thái với mảng
[:arrow_up: Mục lục](#mục-lục)

- **Thêm phần tử vào mảng (bất biến)**

Vậy làm thế nào để thêm một phần tử vào mảng mà vẫn duy trì tính bất biến?

Chúng ta không thể sử dụng `.push()` vì `push` sẽ thay đổi mảng.

Thay vào đó, chúng ta phải tạo một bản sao nông và chèn phần tử mới vào mảng mới:

```jsx
const numbers = [1, 2, 3];
const result = [...numbers, 4];
console.log(result); //[1, 2 ,3 ,4]
```

Chúng ta sao chép các giá trị của mảng numbers và sau đó thêm 4. Mảng mới sẽ chứa `1, 2, 3, 4`.

Đây là thao tác bất biến vì chúng ta **KHÔNG thay đổi mảng numbers** mà **tạo ra một bản sao mới và thêm giá trị vào**.

- **Cập nhật phần tử (bất biến)**

Để cập nhật một hoặc nhiều phần tử trong mảng, bạn có thể sử dụng phương thức [`.map`](https://github.com/CUNGVANTHANG/Front-end/tree/master/Javascript%20Theory#6-l%C3%A0m-vi%E1%BB%87c-v%E1%BB%9Bi-m%E1%BA%A3ng) để trả về một bản sao của mảng và đồng thời sửa đổi một hoặc nhiều phần tử. Ví dụ:

```jsx
const grades = [10, 20, 18, 14];
// change 18 to 17
const updatedGrades = grades.map(grade => {
    if (grade === 18){
        return 17;
    }
    // in all other cases, keep it as it was
    return grade;
});
console.log(updatedGrades); //[10, 20, 17, 14]
```

Bạn cũng có thể cập nhật nhiều phần tử, ví dụ: cộng 1 cho tất cả các điểm thi thấp hơn 10:

```jsx
const grades = [10, 8, 9, 4, 16];
// add 1 to all grades below 10
const updatedGrades = grades.map(grade => {
    if (grade < 10){
        return grade + 1;
    }
    // in all other cases, keep it as it was
    return grade;
});
console.log(updatedGrades); //[10, 9, 10, 5, 16]
```

- **Xóa phần tử (bất biến)**

Bạn có thể xóa phần tử một cách bất biến bằng cách sử dụng phương thức [`.slice`](https://github.com/CUNGVANTHANG/Front-end/tree/master/Javascript%20Theory#6-l%C3%A0m-vi%E1%BB%87c-v%E1%BB%9Bi-m%E1%BA%A3ng) (slice chứ không phải splice). **slice là phương thức bất biến trong khi splice là phương thức thay đổi mảng**.

```jsx
const grades = [10, 8, 9, 4, 16];

// remove the first grade
// think of it as: get all grades except the first one
const subset1 = grades.slice(1); //start from position 1
console.log(subset1); // [8, 9, 4, 16]

// remove the last 2 grades
// think of it as: get all grades except the last 2
// so start from 0 and stop after 5 - 2 = 3 items
const subset2 = grades.slice(0, grades.length - 2); 
console.log(subset2); // [10, 8, 9]
```

Đôi khi việc sử dụng [`.filter`](https://github.com/CUNGVANTHANG/Front-end/tree/master/Javascript%20Theory#6-l%C3%A0m-vi%E1%BB%87c-v%E1%BB%9Bi-m%E1%BA%A3ng) sẽ dễ dàng hơn bởi nó **trả về một tập con của mảng gốc dựa trên điều kiện**, ví dụ:

```jsx
const grades = [10, 8, 9, 4, 16];

// return all grades >= 10
const subset1 = grades.filter(grade => grade >= 10);
console.log(subset1); // [10, 16]

// remove the 2nd grade
const subset2 = grades.filter(grade => grade !== 8);
console.log(subset2); // [10, 9, 4, 16]
```

Lưu ý rằng ví dụ thứ hai sẽ bỏ qua tất cả các điểm thi là 8. Nếu bạn chỉ muốn bỏ qua phần tử thứ hai, bạn có thể sử dụng đối số thứ hai mà bạn nhận được với `filter`, đó là chỉ số.

```jsx
const grades = [10, 8, 9, 4, 16];

const subset = grades.filter((grade, index) => index !== 1);
console.log(subset); // [10, 9, 4, 16];
```

- **Trạng thái của mảng**

Giả sử chúng ta có mảng grades và chúng ta muốn tạo một thẻ ul và một thẻ li cho mỗi điểm số:

```jsx
function Grades(){
    const grades = [8, 18, 10, 7, 14];

    // this will generate a warning (keep reading)
    return <ul>
        { grades.map(grade => <li>{grade}</li>) }
    </ul>;
}
```

Component trên sẽ hiển thị:

```jsx
<ul>
    <li>8</li>
    <li>18</li>
    <li>10</li>
    <li>7</li>
    <li>14</li>
</ul>
```

Mỗi khi sử dụng phương thức map trong JSX, bạn cần cung cấp một **thuộc tính key** để tránh gặp cảnh báo (vì lý do hiệu suất):

```jsx
function Grades() {
    const grades = [8, 18, 10, 10];

    return <ul>{
        grades.map((grade, index) => <li key={index}>{grade}</li>)
    }</ul>;
}
```

`key` nên là giá trị đại diện duy nhất cho từng phần tử trong danh sách. Tuy nhiên, trong trường hợp các phần tử không phải là duy nhất, chúng ta có thể sử dụng index được cung cấp bởi phương thức `.map` làm `key`.

Chỉ số bắt đầu từ 0 và tăng lên 1 sau mỗi lần lặp.

Nếu mảng chứa các mục duy nhất thì các giá trị của mục sẽ là key:

```jsx
function Users() {
    // collection of user ids
    const users = [1, 10, 3, 4, 13];

    return <ul>{
        users.map(user => <li key={user}>{user}</li>)
    }</ul>;
}
```

Vì vậy, việc sử dụng `index` làm key chỉ nên là phương án cuối cùng. Trong các ví dụ trước đây, vì chúng ta chỉ làm việc với mảng chứa chuỗi và mảng số nên việc sử dụng chỉ số làm `key` là tạm thời chấp nhận.

Tuy nhiên, khi tìm hiểu về mảng chứa đối tượng, bạn sẽ được hướng dẫn cách chọn giá trị `key` phù hợp cho từng trường hợp.

- **Tại sao chúng ta cần key?**

Khi **một phần tử mảng thay đổi**, **React cần biết li nào cần được cập nhật**; do đó, nó yêu cầu **cung cấp một key duy nhất** để chỉ **cập nhật phần tử đó** mà không **xóa tất cả các li khác** và hiển thị lại.

### 6. Trạng thái với đối tượng
[:arrow_up: Mục lục](#mục-lục)

- **Thêm khóa/giá trị một cách bất biến**

Hãy bắt đầu với phương thức làm thay đổi đối tượng:

```jsx
const data = {
    id: 1,
    name: "Sam"
}

//BAD: mutates
data.age = 18;
console.log(data); // {id: 1, name: "Sam", age: 18}
```

Thay vì cách trên, chúng ta có thể tạo một bản sao của đối tượng bằng cách sử dụng toán tử `spread: {...data}`.

Toán tử này tạo ra một đối tượng mới với các khóa và giá trị tương tự, sau đó chúng ta có thể thêm cặp khóa/giá trị mới vào đối tượng:

```jsx
const data = {
    id: 1,
    name: "Sam"
}

//GOOD: immutable
const newObj = {...data, age: 18}
console.log(newObj); // {id: 1, name: "Sam", age: 18}
```

- **Thay thế giá trị của khóa hiện có**

Cách sử dụng phương thức thay đổi đối tượng sẽ như sau:

```jsx
const data = {
    id: 1,
    name: "Sam"
}

//GOOD: immutable
const newObj = {...data, age: 18}
console.log(newObj); // {id: 1, name: "Sam", age: 18}
```

Thay vì cách trên, chúng ta có thể tạo một bản sao mới của đối tượng với `{...data}` và sau đó kết hợp nó với khóa mới nhưng có giá trị khác:

```jsx
const data = {
    id: 1,
    age: 19
}

// GOOD: immutable
const newObj = {...data, age: 20};
console.log(newObj); // {id: 1, age: 20}
console.log(data); // original object did not change {id: 1, age: 19}
```

Đoạn code này hoạt động vì `age: 20` trong `{...data, age: 20}` sẽ ghi đè lên `age` hiện tại.

- **Để ý thứ tự**

Lưu ý rằng khi bạn muốn thay thế giá trị, các giá trị mới nên đứng sau bản sao của đối tượng cũ.

Điều này cho phép ghi đè lên các giá trị cũ bằng các giá trị mới.

Do đó, đoạn code dưới đây SẼ KHÔNG hoạt động:

```jsx
const data = {
    id: 1,
    age: 19
}
const wrongNewObj = {age: 20, ...data};
```

Nguyên nhân là vì `age: 19` từ đối tượng data sẽ ghi đè lên `age: 20`.

Bạn chỉ cần sửa đổi thành `{...data, age: 20}` và đoạn code sẽ hoạt động.

- **Loại bỏ key-value**

Để xóa cặp key/value khỏi đối tượng mà không làm thay đổi đối tượng gốc, chúng ta cũng cần sử dụng toán tử `spread` nhưng với một cách tiếp cận khác.

Trước tiên, hãy bắt đầu với phương thức làm thay đổi đối tượng:

```jsx
const obj = {
    id: 1,
    title: "Harry potter",
    year: 2017,
    rating: 4.5
}

// BAD: mutates
delete obj.year;
console.log(obj); // { id: 1, title: "Harry potter", rating: 4.5}
```

Để xóa `year` mà không làm thay đổi đối tượng, chúng ta sẽ phải sử dụng 2 tính năng của JavaScript: **destructuring đối tượng và toán tử spread**:

```jsx
const obj = {
    id: 1,
    title: "Harry potter",
    year: 2017,
    rating: 4.5
}

// GOOD: immutable
const {year, ...rest} = obj;
console.log(rest); // { id: 1, title: "Harry potter", rating: 4.5}
```

Đoạn code này hoạt động vì const `{year, ...rest} = obj` destructure giá trị của khóa year từ `obj`.

Điều này tương tự như việc đọc `obj.year`.

Tuy nhiên, chúng ta cũng yêu cầu JavaScript destructure phần còn lại của đối tượng với `...rest`; tương đương với việc kết hợp tất cả các key/value khác trong một đối tượng mới tên là `rest`.

Vì vậy, chúng ta có rest là một bản sao bất biến của `obj` nhưng không có khóa `year`!

- **Giá trị mặc định**

Khi khởi tạo một trạng thái mới, chúng ta cần cung cấp một giá trị mặc định. 

Dạng phổ biến nhất mà bạn thường thấy là đặt giá trị mặc định là một đối tượng rỗng:

```jsx
import {useState} from "react";

function App() {
    const [data, setData] = useState({});
}
```

- **Lặp qua đối tượng trong JSX**

Đôi khi chúng ta có thể cần lặp qua đối tượng. Tuy nhiên, thao tác này không phổ biến như việc lặp qua mảng. Cách thực hiện như sau:

```jsx
function App() {
    const settings = {
        title: "Blog",
        theme: "dark"
    }

    return <ul>{
        Object.entries(settings).map(item => {
            return <li key={item[0]}>{item[0]} with value {item[1]}</li>
        })
    }</ul>;
}
```

JSX kết quả sẽ là:

```jsx
<ul>
    <li key="title">title with value Blog</li>
    <li key="theme">theme with value dark</li>
</ul>
```

Đoạn code trên hoạt động vì `Object.entries(settings)` trả về mảng sau:

```jsx
[
    ["title", "Blog"],
    ["theme", "dark"],
]
```

### 7. Xử lý form
[:arrow_up: Mục lục](#mục-lục)

- **Thuộc tính value trong HTML**

Trong HTML, chúng ta thường cung cấp giá trị mặc định cho ô nhập liệu bằng cách chỉ định thuộc tính value, ví dụ:

```jsx
<!-- HTML example -->
<input type="text" name="address" value="Amsterdam">
```

Đoạn code trên sẽ hiển thị một trường nhập liệu chứa giá trị **Amsterdam** và người dùng **có thể chỉnh sửa văn bản**.

Tuy nhiên, trong React, cách hoạt động của phần tử này có chút khác biệt.

**defaultValue**

Khi bạn thiết lập value cho phần tử input trong React, **giá trị đó sẽ không bao giờ thay đổi** (trừ khi bạn chỉ định trình xử lý onChange).

Do đó, dòng code JSX dưới đây không nên được sử dụng:

```jsx
<input type="text" name="address" value="Amsterdam" />
```

Để ý code sử dụng cú pháp **tự đóng thẻ** vì chúng ta đang sử dụng JSX; điều này là bắt buộc.

Kết quả trả về một trường nhập liệu **chứa giá trị Amsterdam nhưng không thể thay đổi**, nghĩa là nó là một trường nhập liệu **chỉ đọc**.

Thay vào đó, khi bạn muốn cung cấp giá trị mặc định cho người dùng, bạn nên sử dụng thuộc tính `defaultValue` như sau:

```jsx
<input type="text" name="address" defaultValue="Amsterdam" />
```

- **Nhận giá trị đầu vào**

Để lấy văn bản do người dùng viết, chúng ta sử dụng trình xử lý sự kiện `onChange` trên thẻ `<input />`:

```jsx
function handleAddressChange(event) {
    //...
}

<input type="text" name="address" onChange={handleAddressChange} />
```

Hàm `handleAddressChange` sẽ được gọi mỗi khi người dùng nhập một ký tự mới, xóa một ký tự hoặc thực hiện bất kỳ chỉnh sửa nào trên ô văn bản. Hàm sẽ được kích hoạt mỗi khi giá trị của trường nhập liệu thay đổi.

**Đối số event**

Hàm được truyền vào `onChange` sẽ nhận đối số là một `event`, tương tự như khi làm việc với DOM.

Tuy nhiên, event này về mặt kỹ thuật là sự kiện tổng hợp (**synthetic event**)

Bạn có thể đọc giá trị được viết bởi người dùng bằng cách truy cập vào: `event.target.value`:

```jsx
function handleAddressChange(event) {
    console.log(event.target.value);
}

<input type="text" name="address" onChange={handleAddressChange} />
```

Trong ví dụ này, `event.target` **tham chiếu đến phần tử** (trong ví dụ này là `<input />`). Vì đó là một trường nhập liệu, bạn đọc nội dung bên trong nó bằng cách truy cập trường thuộc tính `.value`.

**target vs currentTarget**

Nếu bạn đã từng viết code JavaScript thuần túy, bạn có thể đã quen việc sử dụng `currentTarget` thay cho `target` (vì `currentTarget` luôn tham chiếu đến phần tử mà bạn gọi `addEventListener` trong khi `target` sẽ phụ thuộc vào vị trí chính xác mà người dùng nhấp chuột).

Khi sử dụng `onChange` của React, **không có sự khác biệt** giữa `target` và `currentTarget` vì **chỉ có một phần tử duy nhất mà không có phần tử con**. Do đó, cả **hai giá trị sẽ trỏ đến cùng một phần tử**.

Bạn sẽ thấy nhiều nhà phát triển sử dụng `target` và đó cũng là một thực hành mà bạn nên làm theo.

**Hàm nội tuyến**

Các hàm inline (nội tuyến) thường được sử dụng với biểu mẫu vì bạn thường cần có một trình xử lý sự kiện nhỏ, ví dụ:

```jsx
<input type="text" name="address" onChange={event => console.log(event.target.value)} />
```

- **Controlled component là gì?**

**Controlled component** là khi bạn theo dõi giá trị của một input dưới dạng state và cập nhật giá trị mỗi khi nó thay đổi.

Việc sử dụng controlled component là rất hữu ích trong các trường hợp có thẻ `<input />` (hoặc các thẻ `<select />` hoặc `<textarea />`) vì nó cho phép bạn lấy giá trị do người dùng viết và tự động thay đổi giá trị khi trạng thái thay đổi.

**Cách tạo một controlled component:**

- Bắt đầu bằng việc tạo biến state để lưu trữ giá trị
- Biến sẽ có giá trị mặc định là một chuỗi rỗng ""
- Thiết lập giá trị của input là biến state đó
- Cập nhật state mỗi khi nó thay đổi

**Cung cấp giá trị mặc định**

Để lấy một giá trị mặc định **khác chuỗi rỗng**, bạn có thể cập nhật giá trị mặc định của `useState`:

```jsx
import {useState} from "react";

function App() {
    const [address, setAddress] = useState("Amsterdam");

    return <input type="text" value={address} onChange={event => setAddress(event.target.value)} />;
}
```

Bạn **không cần sử dụng thuộc tính `defaultValue`** nữa vì đây là một **controlled component**.

- **Gửi biểu mẫu**

Phần tử Form trong React hoạt động tương tự như trong các ứng dụng không sử dụng React, tức là khi bạn submit biểu mẫu, nó sẽ gửi dữ liệu đến trang hiện tại và dẫn đến việc tải lại trang.

Khi làm việc với `fetch`, bạn cần ngăn biểu mẫu gửi dữ liệu để có thể gửi dữ liệu với [`fetch`](https://github.com/CUNGVANTHANG/Front-end/tree/master/Javascript%20Theory#c-fetch).

Cách thực hiện cũng tương tự trong React, chúng ta cần gọi [`event.preventDefault()`](https://github.com/CUNGVANTHANG/Front-end/tree/master/Javascript%20Theory#k-preventdefault-and-stoppropagation) trong sự kiện submit:

```jsx
function App() {

    function handleFormSubmit(event) {
        event.preventDefault();
    }

    return <form onSubmit={handleFormSubmit}>
        <input type="text" name="name" />
        <input type="submit" value="Add" />
    </form>;
}
```

- **Gán nhãn cho form**

Dưới đây là cách thêm label cho một input trong HTML (trong React sẽ khác một chút):

```jsx
<form>
    <label for="login-email">Email: </label>
    <input type="email" id="login-email" placeholder="alex@email.com">

    <label for="login-password">Password: </label>
    <input type="password" id="login-password" placeholder="Password">

    <input type="submit" >
</form>
```

Phần tử `<label>` cần một thuộc tính for trỏ tới id của trường nhập liệu/hộp chọn/vùng văn bản mà nó liên kết đến.

Để ý đoạn code làm cho phần tử HTML hoạt động bằng cách thêm: `id="login-email"` và sau đó tham chiếu đến nó bằng `for="login-email"`. Và đối với trường mật khẩu: `id="login-password"` và sau đó tham chiếu đến nó bằng `for="login-password"`.

Đảm bảo rằng `id` là duy nhất vì `id` đó chỉ nên được sử dụng một lần trên mỗi trang HTML.

**Nhãn trong React**

Trong React, cách sử dụng thẻ label có một số khác biệt nhỏ so với cách sử dụng thông thường, tương tự như việc sử dụng thuộc tính class trong React khác với cách sử dụng trong HTML thông thường.

Hãy nhớ rằng trong React, chúng ta phải sử dụng `className` thay vì `class`. React truyền tất cả những props này xuống DOM, DOM mong đợi `props` là các trường thuộc tính hợp lệ của một phần tử HTML.

Điều tương tự áp dụng cho thuộc tính `for`. Tên trường thuộc tính thực tế là `htmlFor`.

Vì vậy, đây là biểu mẫu tương tự nhưng được viết bằng JSX:

```jsx
<form>
    <label htmlFor="login-email">Email: </label>
    <input type="email" id="login-email" placeholder="alex@email.com" />

    <label htmlFor="login-password">Password: </label>
    <input type="password" id="login-password" placeholder="Password" />

    <input type="submit" />
</form>
```

`<label />` cần một trường thuộc tính `htmlFor` trỏ tới `id` của phần tử.

### 8. Truyền vào hàm
[:arrow_up: Mục lục](#mục-lục)

- **Phân biệt Stateless component và Stateful component?**

**Stateless component** KHÔNG quản lý trạng thái bên trong. (**Không** có lệnh gọi **useState** bên trong component)

**Stateful component** quản lý trạng thái bên trong (**Có ít nhất** một lệnh gọi **useState** bên trong component).

- **Truyền hàm vào props**

Ngoài ra, **props cũng có thể chứa hàm**. Dưới đây là một ví dụ (để thuận tiện, cả hai component được định nghĩa trong cùng một file):

```jsx
function App() {
    function handleWelcome() {
        console.log("Hello World");
    }
    return <StoreFront onWelcome={handleWelcome} />;
}

function StoreFront(props) {
    props.onWelcome();

    return <div>Store renders here</div>;
}
```

Cùng phân tích các bước:

Chúng ta định nghĩa phương thức `handleWelcome` trong component cha tên là `App`.

Sau đó, chúng ta hiển thị component `StoreFront` và truyền một prop có tên là `onWelcome`.

Prop `onWelcome` là một hàm (tham chiếu đến hàm `handleWelcome`)

Từ bên trong component `StoreFront`, chúng ta có thể gọi hàm đó bằng `props.onWelcome()`.

`Hello World` sẽ được in ra màn hình.

- **Quy ước đặt tên**

Khi truyền hàm, bạn cần tuân theo quy ước đặt tên sau:

1. Các hàm vẫn được gọi bằng cách sử dụng `handleSubjectEvent`. (Ví dụ trên đã được đơn giản hóa và không có Event nên ta đã bỏ qua nó)
2. Đối với props là hàm, bắt đầu chúng với `onSubjectEvent`. Điều này giúp phân biệt dễ dàng giữ các phần tử props là hàm.

Thêm một ví dụ:

```jsx
function App() {
    function handleStoreOpen() {

    }

    function handleItemClick() {

    }

    return <StoreFront
            onStoreOpen={handleStoreOpen}
            onItemClick={handleItemClick}
        />
}
```

Để ý `onStoreOpen` là một prop truyền một hàm và tương tự cho `onItemClick`.

### 9. Chuyển trạng thái lên
[:arrow_up: Mục lục](#mục-lục)

- **Phân biệt Stateless component và Stateful component?**

**Stateless component** KHÔNG quản lý trạng thái bên trong. (**Không** có lệnh gọi **useState** bên trong component)

**Stateful component** quản lý trạng thái bên trong (**Có ít nhất** một lệnh gọi **useState** bên trong component).

- **Cải tiến component Form**

Bây giờ chúng ta đã biết cách truyền hàm dưới dạng props trong React, hãy xem xét component React sau:

```jsx
// index.js
import {useState} from "react";

function App() {
    const [name, setName] = useState("");

    function handleNameChange(event) {
        setName(event.target.value);
    }

    return <div>
        <h2>Hello {name}</h2>
        <form>
            <label htmlFor="name">Name: </label>
            <input type="text" id="name" value={name} onChange={handleNameChange} />
        </form>
    </div>
}
```

Chúng ta muốn tái cấu trúc component thành:

```jsx
// index.js
import {useState} from "react";
import NameForm from "./NameForm.js";

function App() {
    const [name, setName] = useState("");

    function handleNameChange(event) {
        setName(event.target.value);
    }

    return <div>
        <h2>Hello {name}</h2>
        <NameForm />
    </div>
}
```

Để ý đoạn code đã tái cấu trúc component `<form>` thành component `NameForm`.

**Truyền "value" và "onChange"**

Component `NameForm` cần hiển thị một hộp văn bản và cập nhật giá trị của nó mỗi khi có thay đổi; do đó, nó cần thiết lập các prop `value` và `onChange`.

Để làm điều đó, chúng ta bắt đầu bằng cách truyền chúng từ component App xuống:

```jsx
// index.js
import NameForm from "./NameForm.js";

function App() {
    const [name, setName] = useState("");

    function handleNameChange(event) {
        setName(event.target.value);
    }

    return <div>
        <h2>Hello {name}</h2>
        <NameForm name={name} onNameChange={handleNameChange} />
    </div>
}
```

Một số điều cần lưu ý:

`name={name}` truyền biến trạng thái name xuống

`onNameChange={handleNameChange}` truyền hàm `handleNameChange`

`onNameChange` tuân theo quy ước đặt tên

Để ý trạng thái được tạo và duy trì trong component cha. Component App là **stateful component** vì nó **quản lý trạng thái**.

**Sử dụng "value" và "onChange"**

Bây giờ trong component `NameForm`, chúng ta có thể sử dụng 2 `prop` này:

```jsx
//NameForm.js
export default function NameForm(props) {

    return <form>
        <label htmlFor="name">Name: </label>
        <input type="text" id="name" value={props.name} onChange={props.onNameChange} />
    </form>
}
```

Một số điều cần lưu ý:

Component là **stateless** vì nó **KHÔNG quản lý trạng thái**. Mặc dù có một hộp văn bản, component này có một trình xử lý `onChange` gọi `props.onNameChange` thuộc về component cha của nó. Component cha xử lý trạng thái.

`value={name}` đã thay đổi thành `value={props.name}` vì `name` không còn là trạng thái nội bộ nữa mà là một `prop` **nhận được từ component cha**.

Bạn có nhận thấy rằng `App` là **stateful component** và `NameForm` là **stateless component** không?

- **Chia sẻ trạng thái giữa các component**

Giả sử chúng ta muốn xây dựng một Danh sách việc cần làm; chúng ta sẽ cần một form để thêm "todo" cũng như một danh sách ul để liệt kê các tác vụ.

```jsx
import {useState} from "react";

function TodoApp() {
    const [todos, setTodos] = useState([]);
    const [entry, setEntry] = useState("");

    function handleEntryChange(event) {
        setEntry(event.target.value);
    }

    function handleFormSubmit(event) {
        event.preventDefault();
        // add the new entry
        setTodos([...todos, entry]);
        // reset/empty the textbox
        setEntry("");
    }

    return <>
        <form onSubmit={handleFormSubmit}>
            <label htmlFor="todo">Enter To do: </label>
            <input type="text" id="todo" value={entry} onChange={handleEntryChange} />
        </form>
        <ul>
            {todos.map((todo, index) => <li key={index}>{todo}</li>)}
        </ul>
    </>;
}
```

Bây giờ hãy tách component này thành 2 component mới:

`<TodoForm />` chứa `<form>` và các component con của nó

`<TodoList />` chứa `<ul>` và các component con của nó

Vấn đề là cả hai component `TodoForm` và `TodoList` đều phụ thuộc vào cùng một trạng thái, đó là `todos` và `entry`.

Biểu mẫu cần trạng thái `todos` để có thể thêm `entry` mới vào mảng `todos`.

Vì vậy, chúng ta phải nâng trạng thái và định nghĩa trạng thái trong component cha, đó là `<TodoApp />`.

Sau đó, component `TodoApp` này sẽ truyền trạng thái và phương thức onChange xuống cả hai component con.

![image](https://github.com/CUNGVANTHANG/Front-end/assets/96326479/f8e6c191-5ccd-4856-aaa0-b7c1ed13e2e9)

Như vậy, trạng thái đã được định nghĩa trong component cha.

Code sau khi được tái cấu trúc:

```jsx
// TodoApp.js
import {useState} from "react";
import TodoForm from "./TodoForm.js";
import TodoList from "./TodoList.js";

function TodoApp() {
    const [todos, setTodos] = useState([]);
    const [entry, setEntry] = useState("");

    function handleEntryChange(event) {
        setEntry(event.target.value);
    }

    function handleFormSubmit(event) {
        event.preventDefault();
        setTodos([...todos, entry]);
        setEntry("");
    }

    return <>
        <TodoForm entry={entry} onEntryChange={handleEntryChange} onFormSubmit={handleFormSubmit} />
        <TodoList todos={todos} />
    </>;
}

// TodoForm.js
function TodoForm(props) {
    return <form onSubmit={props.onFormSubmit}>
        <label htmlFor="todo">Enter To do: </label>
        <input type="text" id="todo" value={props.entry} onChange={props.onEntryChange} />
    </form>;
}

// TodoList.js
function TodoList(props) {
    return <ul>
        {props.todos.map((todo, index) => <li key={index}>{todo}</li>)}
    </ul>;
}
```

Việc có trạng thái chung trong component cha chung gần nhất mang lại một số lợi ích nhất định (mặc dù code có thể dài hơn một chút). Cụ thể:

1. Component cha chung trở thành **nguồn dữ liệu duy nhất**. Điều này giúp dễ dàng việc tìm kiếm và sửa lỗi, vì bạn biết chỉ có một nơi duy nhất mà trạng thái sẽ được thay đổi.
2. Có một vị trí quản lý trạng thái chung giúp duy trì tính nhất quán trong ứng dụng. Nếu bạn tạo một số logic xác thực cho entry, bạn chỉ cần thực hiện một lần duy nhất trong component cha chung.

### 10. Cập nhật trạng thái bằng hàm
[:arrow_up: Mục lục](#mục-lục)

- **Cập nhật trạng thái có tính chất không đồng bộ**

Cập nhật trạng thái trong React là **hành vi bất đồng bộ**, tức là trạng thái không nhất thiết phải được cập nhật ngay lập tức.

Hành vi này được thiết kế như vậy nhằm giúp cải thiện hiệu suất của ứng dụng React.

Khi bạn cập nhật trạng thái trong React, điều này yêu cầu phải hiển thị lại component (và có thể cả các component khác), đó có thể là một hoạt động tốn kém. Đó là lý do tại sao React gom nhóm nhiều cập nhật trạng thái lại với nhau và kết hợp chúng thành một lần render để làm cho ứng dụng phản hồi nhanh hơn và giảm công việc mà trình duyệt phải thực hiện.

Hãy xem ví dụ sau:

```jsx
import React, {useState} from "react";

function App() {    
    const [date, setDate] = useState(new Date());
    const [counter, setCounter] = useState(0);

    console.log("rendered"); //allows us to visualize re-renders

    function handleButtonClick() {
        setDate(new Date());
        setCounter(counter + 1);
    }

    return <button onClick={handleButtonClick}>Click me</button>
}
```

Hàm `setDate()` thiết lập ngày hiện tại bằng cách gọi `new Date()`.

Bây giờ hãy trả lời những câu hỏi sau:

1. Có bao nhiêu cập nhật trạng thái xảy ra khi nhấp vào nút?
2. Component này sẽ được hiển thị lại bao nhiêu lần khi nhấp vào nút?

**Câu trả lời cho câu hỏi đầu tiên là:** có **hai** cập nhật trạng thái. Tuy nhiên, **component chỉ hiển thị lại một lần**.

Điều này là do React gom nhóm (kết hợp) hai thay đổi trạng thái này và thực hiện chúng cùng một lúc. Điều này giúp ứng dụng phản hồi nhanh hơn đối với tương tác của người dùng.

- **Cập nhật trạng thái bằng hàm**

Vì cập nhật trạng thái là hành vi bất đồng bộ, có một điều mà chúng ta cần phải để ý.

Để cho đơn giản, chúng ta sẽ xem xét component sau:

```jsx
import {useState} from "react";

function App() {
    const [counter, setCounter] = useState(0);

    function handleButtonClick() {
        setCounter(counter + 1);
        setCounter(counter + 1);
    }

    return <button onClick={handleButtonClick}>Click me {counter}</button>
}
```

Đây chỉ là code minh họa; tuy nhiên, code có **hai lệnh** gọi `setCounter` liên tiếp nhau.

Với đoạn code trên, bạn dự đoán giá trị của counter sẽ là bao nhiêu sau khi nhấp vào nút?

**Giá trị sẽ là 1**, không phải 2, lý do là:

```jsx
//assuming: counter is 0
setCounter(counter + 1);
setCounter(counter + 1);
```

Hai lần cập nhật trạng thái này sẽ được **gộp chung** và khi `counter = 0`, cuộc gọi `setCounter()` đầu tiên sẽ đặt giá trị của counter là `0 + 1 = 1`, nhưng việc cập nhật này không xảy ra ngay lập tức vì nó là **hành vi bất đồng bộ**.

Khi gọi **lần thứ hai** `setCounter(counter + 1)`, **giá trị của counter vẫn là 0** vì component chưa được hiển thị lại. Vì vậy, lần gọi thứ hai cũng sẽ cập nhật trạng thái thành 1.

Lưu ý rằng điều này xảy ra do các lần cập nhật trạng thái được gộp chung.

- **Cập nhật trạng thái bằng hàm**

Để giải quyết vấn đề này, React cung cấp khái niệm cập nhật trạng thái bằng hàm (**functional state updates**), đó là truyền một hàm vào hàm cập nhật trạng thái, dưới đây là một ví dụ:

```jsx
setCounter((previousCounter) => {
    return previousCounter + 1;
});
```

Phiên bản ngắn gọn hơn:

```jsx
setCounter(previousCounter => previousCounter + 1);
```

Chúng ta định nghĩa một hàm nhận giá trị trạng thái trước đó và trả về giá trị trạng thái mới. Trong ví dụ này, giá trị trạng thái mới là giá trị trạng thái trước đó + 1.

Dưới đây là cách bạn có thể sửa ví dụ trên để cộng vào trạng thái hai lần:

```jsx
import {useState} from "react";

function App() {
    const [counter, setCounter] = useState(0);

    function handleButtonClick() {
        setCounter(prevCounter => prevCounter + 1);
        setCounter(prevCounter => prevCounter + 1);
    }

    return <button onClick={handleButtonClick}>Click me {counter}</button>
}
```

**Giá trị trạng thái counter sẽ tăng thêm 2** mỗi lần bạn nhấp vào nút.

Bạn có thể chưa hiểu rõ nguồn gốc của `prevCounter`. Hãy nhớ rằng `prevCounter => prevCounter + 1` là **một định nghĩa hàm**. React sẽ gọi hàm này và truyền giá trị trạng thái trước đó vào làm đối số đầu tiên.

Điều này có nghĩa là bạn có thể đặt tên đối số đó thành bất cứ điều gì bạn muốn. Trong ví dụ này, ta sử dụng `prevCounter`.

## IV. Hook - useEffect
[:arrow_up: Mục lục](#mục-lục)

- **React.StrictMode**

React cung cấp component `StrictMode` giúp bạn tìm ra một số lỗi không mong muốn khi React đang chạy ở **chế độ phát triển**.

Bạn có thể giữ `StrictMode` khi chạy trong **chế độ sản xuất vì nó không có tác động đến ứng dụng**.

Thông qua đối tượng **React**, bạn có thể truy cập vào component `StrictMode`. Vì React là một đối tượng và `StrictMode` **là một khóa** của đối tượng đó, bạn có thể truy cập component đó bằng cách sử dụng cú pháp: `<React.StrictMode></React.StrictMode>` miễn là bạn đã thêm React vào file JavaScript.

```jsx
import React from "react";
import {createRoot} from "react-dom/client";

function App() {
}

const root = document.querySelector("#root");

createRoot(root).render(<React.StrictMode><App /></React.StrictMode>);
```

### 1. useEffect
[:arrow_up: Mục lục](#mục-lục)

Hook `useEffect` được dùng để triển khai hiệu ứng (effect) trong component. `useEffect` được **gọi sau khi component đã hiển thị**

Dưới đây là một số ví dụ về hiệu ứng:

- Gửi một yêu cầu đến nhà cung cấp dịch vụ phân tích
- Khởi tạo một plugin DOM ngoài React (ví dụ: vẽ bản đồ; sẽ được triển khai trong Dự án tiếp theo)
- Thay đổi tiêu đề trang (tiêu đề hiển thị trên thanh tab của trình duyệt)
- Đăng ký người dùng vào dịch vụ trò chuyện trực tiếp (với WebSockets)

Những hành động này được gọi là hiệu ứng vì chúng là các **chỉ thị chạy bên ngoài component hoặc là kết quả của component**.

- **Tiêu đề trang**

Trong JavaScript, bạn có thể cập nhật tiêu đề trang bằng cách thay đổi `document.title`, ví dụ:

```jsx
document.title = "React Tutorial App";
```

Bây giờ, giả sử chúng ta có một component React và chúng ta muốn đồng bộ tiêu đề với trạng thái hiện tại; ví dụ, chúng ta có biến trạng thái counter và chúng ta muốn hiển thị giá trị của bộ đếm đó trong tiêu đề; cách thực hiện như sau:

```jsx
import {useState, useEffect} from "react";

function Counter() {
    const [counter, setCounter] = useState(0);

    useEffect(() => {
        document.title = `Counter is ${counter}`;
    });

    function handleButtonClick() {
        setCounter(prevCounter => prevCounter + 1);
    }
    
    return <button onClick={handleButtonClick}>Click me {counter}</button>
}
```

Bây giờ hàm này:

```jsx
() => {
    document.title = `Counter is ${counter}`;
}
```

sẽ được gọi sau mỗi lần hiển thị lại của component `Counter`.

Vì vậy, sau mỗi lần component `Counter` hiển thị (hoặc hiển thị lại), hàm trên sẽ được gọi, từ đó cập nhật tiêu đề trang.

Điều này cho phép bạn đồng bộ tiêu đề của tài liệu với giá trị `counter`.

### 2. Các hiệu ứng yêu cầu phải dọn dẹp
[:arrow_up: Mục lục](#mục-lục)

- **Dọn dẹp là gì?**

Khi bạn tạo một bộ đếm thời gian bằng cách sử dụng `setTimeout`, bạn đang trì hoãn việc chạy một đoạn code trong tương lai, ví dụ:

```jsx
import {useEffect} from "react";

function App() {
    useEffect(() => {
        setTimeout(() => {
            console.log("This will run in 1 second");
        }, 1_000);
    });

    return <h1>App</h1>;
}
```

Nếu đoạn code này được đóng gói trong một hàm và hàm đó có thể được gọi nhiều lần, bạn có thể **gặp phải tình trạng rò rỉ bộ nhớ**. Điều này có nghĩa là bạn đang tăng dần bộ nhớ của ứng dụng vì bạn liên tục lên lịch cho một bộ đếm thời gian mới mỗi khi hàm được gọi.

- **Cách dọn dẹp hiệu ứng**

Để dọn dẹp một hiệu ứng, **bạn phải trả về một hàm** (dọn dẹp) từ bên trong cuộc gọi `useEffect`. Chúng ta sẽ bắt đầu với ví dụ đơn giản nhất:

```jsx
import {useEffect, useState} from "react";

function App() {
  const [counter, setCounter] = useState(0);

  useEffect(() => {
    console.log("effect running");
    return () => {
      console.log("effect cleaning up");
    }
  })

  return (
    <>
      <h2>{counter}</h2>
      <button onClick={() => setCounter(prevCounter => prevCounter + 1)}>Add</button>
    </>
  );
}
```

Vào lần đầu tiên component được hiển thị, chúng ta chỉ thấy `console.log`: "**effect running**".

Sau đó, mỗi khi component được hiển thị lại vì trạng thái của nó thay đổi (khi ta nhấp vào nút), nó bắt đầu bằng cách dọn dẹp component (chúng ta thấy "**effect cleaning up**") và sau đó là "**effect running**".

Kết luận là `return () => { console.log("effect running"); }` sẽ chạy mỗi khi component bị xóa (còn gọi là hủy gắn kết).

Một số phương thức JavaScript yêu cầu dọn dẹp để tránh rò rỉ bộ nhớ (ví dụ: `setTimeout`, `setInterval`)

Sử dụng `clearTimeout(timerId)` hủy bỏ bộ đếm thời gian được khởi tạo bởi `setTimeout`.

```jsx
useEffect(() => {
    const timerId = setTimeout(() => {
        console.log("This will run in 1 second");
    }, 1_000);
    return function cleanupTimer() {
        clearTimeout(timerId);
    };
});
```

### 3. Effect dependencies
[:arrow_up: Mục lục](#mục-lục)

Tất cả các cuộc gọi `useEffect` mà chúng ta đã thấy cho đến nay **đều chạy sau lần hiển thị đầu tiên của component và sau mỗi lần component hiển thị lại**. Nhưng đôi khi bạn không muốn `useEffect` hiển thị lại mỗi lần (đôi khi điều này sẽ tạo ra vòng lặp vô hạn). Đó là lý do tại sao hàm `useEffect` có đối số thứ hai.

```jsx
useEffect(effectCallback, dependencies)
```

**dependencies** trong `useEffect` là một mảng **quyết định khi nào hiệu ứng sẽ được chạy lại**. Dưới đây là cách nó hoạt động:

```jsx
import {useState, useEffect} from "react";

function App() {
    const [counter, setCounter] = useState(0);

    useEffect(() => {
        console.log("effect is running");
    }, [counter]);

    return <button onClick={() => setCounter(prev => prev + 1)}>Click me</button>;
}
```

Chúng ta đã truyền vào `useEffect` đối số thứ hai của `[counter]`. Đó là **mảng các phụ thuộc (dependencies)**.

Điều này cho React biết nó chỉ nên gọi lại `useEffect` khi giá trị của counter thay đổi. Điều này có nghĩa là nó sẽ gọi lại sau lần đầu tiên component hiển thị và mỗi lần giá trị counter thay đổi.

Vì vậy trong ví dụ này, `[counter]` bắt đầu là `[0]` (vì trạng thái counter bắt đầu từ 0).

React sẽ lưu trữ `[0]` và sau đó khi người dùng nhấp vào nút. Giá trị mới của `[counter]` trở thành `[1]`

React sẽ so sánh giá trị mới này với giá trị cũ (từng cái một). Và vì `1` trong `[1]` không giống như `0` trong `[0]` (từ lần chạy trước) nên React sẽ chạy lại useEffect.

- **Hiệu ứng chỉ chạy một lần**

Ta cũng có thể truyền mảng rỗng làm phụ thuộc: `[]`

Khi bạn truyền một mảng rỗng, so sánh giữa lần hiển thị trước và lần hiển thị tiếp theo **luôn trả về kết quả giống nhau** (vì React so sánh cùng một thực thể của `[]`, không có giá trị nào trong mảng đó có thể thay đổi). Điều này có nghĩa là việc truyền `[]` sẽ chỉ **chạy hiệu ứng một lần sau lần hiển thị đầu tiên.**

- **Bài tập vòng đời của Component**

Thêm các lệnh `console.log` sau vào component Countdown để hiệu ứng chạy vào thời điểm cụ thể trong vòng đời của component:

`console.log("first render")` khi component được gắn kết

`console.log("will be removed")` trước khi component bị hủy gắn kết

`console.log("count changed")` khi biến count thay đổi

`console.log("lives changed")` khi biến lives thay đổi

`console.log("count or lives changed")` khi count hoặc lives thay đổi

```jsx
import React, {useState, useEffect} from "react";
import {createRoot} from "react-dom/client";

function Countdown() {
    const [count, setCount] = useState(5);
    const [lives, setLives] = useState(3);
    
    useEffect(() => {
        console.log("first render")
        
        return () => {
          console.log("will be removed")
        }
    }, [])
    
    useEffect(() => {
      console.log("count changed")
    }, [count])
    
    useEffect(() => {
      console.log("lives changed")
    }, [lives])
    
    useEffect(() => {
      console.log("count or lives changed")
    }, [count, lives])

    function handleCountdownClick() {
        if (count > 0){
            setCount(count - 1);
        } else if (count === 0) {
            setCount(5);
            setLives(lives - 1);
        }
    }

    return <>
        <h2>Attempts remaining: {count}</h2>
        <button onClick={handleCountdownClick}>Count down</button>
        <h3>Lives remaining: {lives}</h3>
    </>;
}

createRoot(document.querySelector("#react-root")).render(<React.StrictMode><Countdown /></React.StrictMode>);
```

### 4. Local Storage
[:arrow_up: Mục lục](#mục-lục)

`localStorage` (hoặc `window.localStorage`) là một API của trình duyệt cho phép chúng ta lưu trữ dữ liệu dưới dạng các cặp khóa và giá trị.

Vấn đề với `localStorage` là **nó là một API đồng bộ**, tức là:

```jsx
console.log("A");
localStorage.setItem("key", "value");
console.log("B");
```

Trong đoạn code trên, chúng ta sẽ thấy `console.log("A")` được in ra trước, sau đó, nếu `localStorage.setItem()` **mất 200 mili giây để hoàn thành** thì `console.log("B")` **sẽ phải đợi** `localStorage.setItem()` hoàn thành trước khi nó được gọi.

Cú pháp:

```jsx
localStorage.setItem("key", "value")
```

Để lưu trữ trạng thái vào `localStorage`, bạn phải sử dụng API localStorage **bên trong** cuộc gọi useEffect:

```jsx
import {useState, useEffect} from "react";

function App() {
    const [random, setRandom] = useState(Math.random());

    useEffect(() => {
        // every time the value of random changes, save it to localStorage:
        localStorage.setItem("random", random);
    }, [random]);

    return <button onClick={() => setRandom(Math.random())}>Re-render</button>;
}
```

Mỗi khi trạng thái `random` thay đổi, hiệu ứng sẽ chạy, từ đó lưu giá trị mới vào `localStorage` với khóa là `random`

- **Lưu đối tượng vào localStorage**

Sau khi chuyển đổi mảng hoặc đối tượng thành chuỗi, bạn có thể lưu nó trong `localStorage`:

```jsx
const person = {
    id: 1,
    name: "Sam"
};

localStorage.setItem("person", JSON.stringify(person)); // '{"id":1,"name":"Sam"}'
```

Nếu bạn muốn khôi phục đối tượng đó từ `localStorage`, bạn cần chuyển đổi nó từ chuỗi thành đối tượng/mảng bằng cách sử dụng `JSON.parse()`

```jsx
let person = localStorage.getItem("person");
person = JSON.parse(person);
console.log(person); // {id: 1, name: "Sam"}
```

- **Khôi phục trạng thái từ localStorage**

**ĐỐI VỚI SỐ:**

Bởi vì localStorage luôn trả về chuỗi, chúng ta cần chuyển đổi chuỗi thành số một cách thủ công:

```jsx
let value = localStorage.getItem("key-here");
value = Number.parseInt(value, 10); // convert to number
```

Bạn cũng có thể sử dụng `Number.parseFloat (value, 10)` nếu muốn hiển thị phần thập phân (ví dụ: 12.5).

Số 10 chính là đối số thứ hai, gọi là cơ số.

**ĐỐI VỚI BOOLEAN:**

Giá trị boolean có thể là `true` hoặc `false`. Khi được lưu vào localStorage, chúng sẽ là `"true"` hoặc `"false"` (vì chúng được chuyển đổi thành chuỗi).

Cách chuyển đổi chuỗi trở lại thành boolean đơn giản nhất là so sánh mục trong `localStorage` với chuỗi `"true"`; sau đây là lý do:

```jsx
"true" === "true" // true (means original value was true)
"false" === "true" // false (means original value was false)
```

Dưới đây là cách viết khi đọc từ `localStorage`:

```jsx
const value = localStorage.getItem("key-here") === "true";
```

Bằng cách so sánh với chuỗi `"true"`, bạn đang chuyển đổi giá trị từ chuỗi thành kiểu boolean.

**GIÁ TRỊ MẶC ĐỊNH:**

Khi bạn đọc một khóa chưa được lưu trữ trong `localStorage`, kết quả sẽ trả về giá trị `null`.

Bạn có thể đặt giá trị mặc định cho biến theo nhiều cách như câu lệnh `if`, **toán tử ba ngôi** hoặc **toán tử coalescing nullish** (`??`). Dưới đây là một số ví dụ gán giá trị mặc định là mảng rỗng:

```jsx
// using an if condition
let value = []; // default value
if (localStorage.getItem("key-here")) {
    value = localStorage.getItem("key-here");
}

// OR: using the ternary operator
const value = localStorage.getItem("key-here") !== null ? localStorage.getItem("key-here") : [];

// OR: using the nullish coalescing operator
const value = localStorage.getItem("key-here") ?? [];
```

Chúng ta cần đặt giá trị mặc định cho mảng nếu mong đợi `localStorage` trả về mảng. Điều này đảm bảo rằng việc gọi `.map()` hoặc các phương thức mảng khác sẽ không gây lỗi nếu `localStorage.getItem()` trả về `null`.

**KHÔI PHỤC MẢNG VÀ ĐỐI TƯỢNG:**

Hãy nhớ rằng chúng ta có thể xử lý mảng và đối tượng theo cách tương tự nhau và chúng ta cần chuyển đổi mảng và đối tượng thành chuỗi trước khi lưu vào `localStorage`.

Điều này có nghĩa là khi **chúng ta muốn đọc lại giá trị của đối tượng từ localStorage**, chúng ta cần `parse` chuỗi trở lại thành đối tượng.

Dưới đây là cách thực hiện:

```jsx
import {useState, useEffect} from "react";

function App() {
    const [array, setArray] = useState(() => {
        return JSON.parse(localStorage.getItem("key-here"));
    });

    useEffect(() => {
        localStorage.setItem("key-here", JSON.stringify(array));
    }, [array]);
}
```

Đoạn code có thể được viết lại bằng cách sử dụng trả về ngầm định:

```jsx
const [array, setArray] = useState(() => JSON.parse(localStorage.getItem("key-here")));
```

### 5. Life cycle
[:arrow_up: Mục lục](#mục-lục)

Vòng đời của một component trong ReactJS bao gồm các giai đoạn chính sau: **Mounting**, **Updating**, và **Unmounting**.

_Ví dụ:_

```jsx
import React, { useState, useEffect } from 'react';
import { createRoot } from 'react-dom/client';

function Counter() {
  const [count, setCount] = useState(0);

  // Chạy một lần sau lần render đầu tiên
  useEffect(() => {
    console.log('componentDidMount: Component has been mounted.');

    // Hàm cleanup sẽ chạy khi component bị gỡ bỏ
    return () => {
      console.log('componentWillUnmount: Component will be unmounted.');
    };
  }, []);

  // Chạy mỗi khi 'count' thay đổi
  useEffect(() => {
    console.log('componentDidUpdate: count has been updated to', count);
  }, [count]);

  return (
    <div>
      <h1>Count: {count}</h1>
      <button onClick={() => setCount(count + 1)}>Increase</button>
    </div>
  );
}

createRoot(document.querySelector("#react-root")).render(<Counter />);
```

Khi ứng dụng bắt đầu chạy và component `Counter` được render lần đầu tiên:

```
componentDidMount: Component has been mounted.
```

Khi bạn nhấn nút "Increase" lần đầu tiên:

```
componentDidUpdate: count has been updated to 1
```

Khi bạn nhấn nút "Increase" lần thứ hai:

```
componentDidUpdate: count has been updated to 2
```

Khi component `Counter` bị gỡ bỏ (ví dụ, nếu bạn chuyển sang một trang khác hoặc gỡ bỏ component bằng cách nào đó):

```
componentWillUnmount: Component will be unmounted.
```

## V. Fetch
[:arrow_up: Mục lục](#mục-lục)

### 1. Fetch API
[:arrow_up: Mục lục](#mục-lục)

- [a. XỬ LÝ PROMISE](#a-xử-lý-promise)
- [b. FETCH API](#b-fetch-api)
- [c. GỌI FETCH Ở ĐÂU](#c-gọi-fetch-ở-đâu)
- [d. LẤY DỮ LIỆU](#d-lấy-dữ-liệu)
- [e. LIÊN KẾT FETCH VỚI STATE](#e-liên-kết-fetch-với-state)
- [f. Cannot read property X of undefined](#f-cannot-read-property-x-of-undefined)
- [g. SỬ DỤNG TOÁN TỬ &&](#g-sử-dụng-toán-tử-)
- [h. XỬ LÝ LỖI HTTP](#h-xử-lý-lỗi-http)
- [j. XỬ LÝ LỖI LIÊN QUAN ĐẾN MẠNG](#j-xử-lý-lỗi-liên-quan-đến-mạng)
- [k. XỬ LÝ TẢI DỮ LIỆU BẰNG FETCH](#k-xử-lý-tải-dữ-liệu-bằng-fetch)
- [l. Fetch khi click](#l-fetch-khi-click)
- [m. Fetch với async/await](#m-fetch-với-asyncawait)

Fetch API hay còn gọi là Fetch GET, chúng ta hay viết

```jsx
fetch("https://course-assets.tek4.vn/reactjs-assets/grades.json")
.then(response => response.json())
.then(data => {
    console.log(data);
});
```

tường minh hơn sẽ là như sau:

```jsx
fetch("https://course-assets.tek4.vn/reactjs-assets/grades.json", {
    method: "GET" // this is a default
})
.then(response => response.json())
.then(data => {
    console.log(data);
});
```

#### a. XỬ LÝ PROMISE
[:arrow_up: Fetch API](#1-fetch-api)

Việc sử dụng promise là một yêu cầu cơ bản khi làm việc với Fetch API. Xử lý promise có nghĩa là thực hiện một hành động khi promise đã hoàn thành công việc của nó.

Giả sử chúng ta có hàm `functionThatReturnsPromise`, sau đây là cách bạn xử lý hàm:

```jsx
functionThatReturnsPromise().then(result => {
    console.log(result);
});
```

Để xử lý Promise, bạn cần gọi `.then()` trên promise và truyền một **hàm callback**. Hàm callback đó sẽ được gọi khi promise đã hoàn thành công việc của nó.

Đối số đầu tiên được truyền vào hàm callback đó (trong ví dụ này là `result`) **sẽ là dữ liệu** mà hàm đó **đã tính toán**.

Promise cũng có thể gặp lỗi, trong trường hợp đó, hàm mà bạn truyền vào `.then()` **sẽ KHÔNG được gọi**. Bạn cần sử dụng `.catch()` để bắt lỗi. Đây là một ví dụ:

```jsx
functionThatReturnsPromise()
.then(result => {
    console.log(result); // when successful
})
.catch(error => {
    console.error(error); // when there's an error
})
```

#### b. FETCH API
[:arrow_up: Fetch API](#1-fetch-api)

```jsx
fetch(URL)
.then(response => response.json())
.then(data => {
    console.log(data);
});
```

Có bốn điều cần lưu ý ở đây:

1. Cuộc gọi `fetch()` trả về một promise, vì vậy ta xử lý nó bằng `.then()`.
2. `response` mà ta nhận được từ fetch là một phản hồi chung, vì vậy ta cần chuyển đổi nó thành đối tượng JSON bằng cách gọi `response.json()`.
3. `response.json()` cũng trả về một promise, vì vậy ta cần xử lý nó một lần nữa bằng `.then()`.
4. Luôn luôn bắt đầu bằng `console.log(data)` vì mỗi backend/API sẽ trả về dữ liệu khác nhau dựa trên mục đích của API đó.

#### c. GỌI FETCH Ở ĐÂU
[:arrow_up: Fetch API](#1-fetch-api)

Gọi `fetch` bên trong component được coi là một hiệu ứng phụ vì `fetch` thực hiện các kết nối mạng (bên ngoài component), vì vậy `fetch` cần được đặt bên trong một **hiệu ứng** (`useEffect`)

```jsx
useEffect(() => {
    // call fetch here
}, []);
```

#### d. LẤY DỮ LIỆU
[:arrow_up: Fetch API](#1-fetch-api)

```jsx
import {useEffect} from "react";

function App() {
    useEffect(() => {
        fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
        .then(response => response.json())
        .then(data => {
            console.log(data);
        });
    }, []);
}
```

Đoạn code này sẽ chạy cuộc gọi `fetch` **một lần bên trong component**.

#### e. LIÊN KẾT FETCH VỚI STATE
[:arrow_up: Fetch API](#1-fetch-api)

Để lưu trữ phản hồi từ `fetch` API vào biến trạng thái, bạn có thể làm theo 2 bước sau:

1. Tạo một biến trạng thái. Ví dụ: `const [users, setUsers] = useState()`.
2. Gọi hàm `setState` bên trong `.then(data => {})`. Ví dụ: `.then(data => { setUsers(data) })`.

```jsx
import {useEffect, useState} from "react";

function App() {
    const [users, setUsers] = useState();

    useEffect(() => {
        fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
        .then(response => response.json())
        .then(data => {
            console.log(data); // keep it for debugging
            setUsers(data);
        });
    }, []);
}
```

#### f. Cannot read property X of undefined
[:arrow_up: Fetch API](#1-fetch-api)

```jsx
import {useState, useEffect} from "react";

function App() {
    const [users, setUsers] = useState();

    useEffect(() => {
        fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
        .then(response => response.json())
        .then(data => {
            console.log(data);
            setUsers(data);
        });
    }, []);
    
    // ❌ This will throw an error
    return <h1>There are {users.length} users</h1>
}
```

Code trên sẽ đưa ra thông báo lỗi: **Cannot read property 'length' of undefined**.

Điều này có nghĩa là trong biểu thức `users.length`, `users` có giá trị là `undefined`, vì vậy chúng ta không thể truy cập `.length` trên nó vì điều đó tương đương với việc chạy `undefined.length`.

**KHẮC PHỤC BẰNG CÁCH:**

Trong ví dụ trên, chúng ta kiểm tra `if (!users)` (hoặc `if (users === undefined)`) và trả về `null` hoặc thông báo như Loading...:

```jsx
import {useState, useEffect} from "react";

function App() {
    const [users, setUsers] = useState();

    useEffect(() => {
        fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
        .then(response => response.json())
        .then(data => {
            console.log(data);
            setUsers(data);
        });
    }, []);
    
    if (!users) {
        return null;
    }

    return <h1>There are {users.length} users</h1>
}
```

#### g. SỬ DỤNG TOÁN TỬ &&
[:arrow_up: Fetch API](#1-fetch-api)

Đôi khi bạn không muốn hiển thị một JSX mới hoàn toàn mà chỉ muốn bỏ qua việc hiển thị một phần của JSX phụ thuộc vào `data` từ API. Ví dụ:

```jsx
import {useState, useEffect} from "react";

function App() {
    const [users, setUsers] = useState();

    useEffect(() => {
        fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
        .then(response => response.json())
        .then(data => {
            setUsers(data);
        });
    }, []);
    
    // This will throw an ERROR
    return <>
        <h1>Users</h1>
        <ul>
            {users.map(user => <li key={user.id}>{user.name}</li>)}
        </ul>
  </>
}
```

Chương trình sẽ đưa ra thông báo lỗi: **Cannot read property 'map' of undefined**.

Vậy nếu bạn muốn chặn thông báo lỗi mà không thay đổi phần hiển thị của component thì phải làm như thế nào? Giả sử trước khi `users` được tải, bạn chỉ muốn component hiển thị JSX sau:

```jsx
<>
    <h1>Users</h1>
    <ul>
    </ul>
</>
```

**KHẮC PHỤC BẰNG CÁCH:**

Bạn có thể thêm tiền tố `users && trước users.map()`, kết quả cuối cùng như sau:

```jsx
import {useState, useEffect} from "react";

function App() {
    const [users, setUsers] = useState();

    useEffect(() => {
        fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
        .then(response => response.json())
        .then(data => {
            setUsers(data);
        });
    }, []);
    
    // this will work without breaking 👍
    return <>
        <h1>Users</h1>
        <ul>
            {users && users.map(user => <li key={user.id}>{user.name}</li>)}
        </ul>
  </>
}
```

Đoạn code trên hoạt động là vì:

**Trước khi 'users' được tải**: biểu thức `users && users.map()` sẽ gặp xung đột tại `users`, có nghĩa là nó sẽ không tiếp tục thực thi sau `&&` vì `users` trả về `undefined`. Điều này sẽ ngăn chặn việc thực thi `users.map()`, tránh gây ra lỗi.

Vì vậy trước khi users được tải, component App sẽ hiển thị:

```jsx
<>
    <h1>Users</h1>
    <ul>
    </ul>
</>
```

**Sau khi 'users' được tải**: biểu thức `users && users.map()` sẽ được thực thi toàn bộ vì `users` không trả về một giá trị `falsy` (như `undefined` hoặc `false`). Do đó, `users.map()` sẽ được gọi.

Vì vậy sau khi users được tải, component App sẽ hiển thị:

```jsx
<>
    <h1>Users</h1>
    <ul>
        {users && users.map(user => <li key={user.id}>{user.name}</li>)}
    </ul>
</>
```

#### h. XỬ LÝ LỖI HTTP
[:arrow_up: Fetch API](#1-fetch-api)

Sử dụng `if` kiểm tra trước khi `setState`

```jsx
import {useEffect, useState} from "react";

function App() {
    const [users, setUsers] = useState();

    useEffect(() => {
        // this fetch request is designed to always fail
        fetch("https://course-assets.tek4.vn/reactjs-assets/validation-example.json", {
            method: "post"
        })
        .then(response => response.json())
        .then(data => {
            console.log(data);
            // only set the users when there's no error
            if (data && !data.error) {
                setUsers(data);
            }
        });

    }, []);
}
```

#### j. XỬ LÝ LỖI LIÊN QUAN ĐẾN MẠNG
[:arrow_up: Fetch API](#1-fetch-api)

Lỗi mạng xảy ra khi kết nối bị gián đoạn hoặc khi người dùng không kết nối mạng. Trong trường hợp này, cuộc gọi `fetch` sẽ đưa ra ngoại lệ thay vì trả về giá trị đã được xử lý. Điều này có nghĩa là bạn có thể bắt được lỗi này bằng cách thêm một khối `.catch()`, dưới đây là một ví dụ:

```jsx
fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
.then(response => response.json())
.then(data => {
    console.log(data);
})
.catch(error => {
    console.log(error); // or console.error(error)
});
```

Đoạn code trên đã thêm một khối `.catch`. Nếu kết nối internet bị gián đoạn trong khi yêu cầu này đang được gửi hoặc nếu người dùng không kết nối mạng thì `.then()` sẽ không chạy mà `.catch` sẽ được chạy, in thông báo lỗi ra console.

#### k. XỬ LÝ TẢI DỮ LIỆU BẰNG FETCH
[:arrow_up: Fetch API](#1-fetch-api)

Khi tải dữ liệu từ mạng bằng Fetch API, việc hiển thị trình tải (loader) là một phần quan trọng trong giao diện người dùng, đó là một chỉ báo hình ảnh cho người dùng biết rằng dữ liệu đang được tìm nạp từ mạng và họ nên đợi một chút.

<img src="https://github.com/CUNGVANTHANG/Front-end/assets/96326479/d4a3c7cb-25e5-43b4-a59d-fe6f308aa160" height="50px" />

**Làm thế nào để hiển thị trình tải?**

Chúng ta cần biết khi nào yêu cầu fetch bắt đầu và kết thúc để hiển thị trình tải. Chúng ta cần một biến trạng thái để theo dõi điều này.

Vì vậy, chúng ta bắt đầu bằng cách định nghĩa một biến trạng thái cho biết yêu cầu fetch có đang tải hay không; chúng ta sẽ gọi biến là `isLoading` và đặt giá trị mặc định là `false`:

```jsx
// inside a React component
const [isLoading, setIsLoading] = useState(false);
```

**Bắt đầu tải**

```jsx
import {useEffect, useState} from "react";

function App() {
    const [isLoading, setIsLoading] = useState(true); // create and start the loader

    useEffect(() => {
        fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
        .then(response => response.json())
        .then(data => {
            console.log(data);
        });
    }, []);
}
```

**Dừng tải**

Đoạn code trên sẽ thiết lập isLoading thành true và không bao giờ dừng trình tải. Đây là lý do tại sao chúng ta cần dừng trình tải khi nhận được phản hồi.

Tuy nhiên, chúng ta cũng nên dừng trình tải trong trường hợp yêu cầu `fetch` bị lỗi, vì vậy chúng ta cần gọi `setIsLoading(false)` trong `.then()` và `.catch()`.

```jsx
import {useEffect, useState} from "react";

function App() {
    const [isLoading, setIsLoading] = useState(true); // create and start the loader

    useEffect(() => {
        fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
        .then(response => response.json())
        .then(data => {
            setIsLoading(false); // stop the loader
            console.log(data);
        })
        .catch(error => {
            setIsLoading(false); // stop the loader
            console.error(error);
        });
    }, []);
}
```

Bạn có thể nhận thấy có một số câu lệnh trùng lặp trong các ví dụ trước khi chúng ta gọi `setIsLoading(false)` ở 2 nơi:

trong phần `.then()`

trong phần `.catch()`

Một phương án hiệu quả hơn là sử dụng `.finally()`. Callback được truyền vào `.finally()` sẽ chạy trong cả hai trường hợp: **fetch thành công và lỗi**.

```jsx
import {useEffect, useState} from "react";

function App() {
    const [isLoading, setIsLoading] = useState(true); // create and start the loader

    useEffect(() => {
        fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
        .then(response => response.json())
        .then(data => {
            console.log(data);
        })
        .catch(error => {
            console.log(error);
        })
        .finally(() => {
            setIsLoading(false); // stop the loader
        });
    }, []);
}
```

### l. Fetch khi click
[:arrow_up: Fetch API](#1-fetch-api)

Một trường hợp sử dụng phổ biến của `fetch` là tải dữ liệu khi người dùng nhấp chuột vào nút.

Bạn có thể làm điều đó bằng cách viết code `fetch` bên trong hàm `handleButtonClick`, ví dụ:

```jsx
function App() {
    const [isLoading, setIsLoading] = useState(false);

    function handleButtonClick() {
        setIsLoading(true);
        // fetch("...") as usual
    }

    return <button disabled={isLoading} onClick={handleButtonClick}>Load data</button>;
}
```

Vì vậy, nếu bạn muốn thực hiện yêu cầu `fetch` trên sự kiện `onClick`, bạn cần đặt cuộc gọi fetch bên trong hàm `handleButtonClick` thay vì trong `useEffect`.

Lưu ý rằng chúng ta thiết lập giá trị mặc định của `isLoading` là `false` vì nó chỉ bắt đầu tải khi người dùng nhấp vào nút. Chúng ta bắt đầu hiển thị trình tải bên trong `handleButtonClick` bằng `setIsLoading(true)`.

### m. Fetch với async/await
[:arrow_up: Fetch API](#1-fetch-api)

[async/await](https://github.com/CUNGVANTHANG/Front-end/tree/master/Javascript%20Theory#d-asyncawait) là cú pháp rút gọn cho promise, cho phép bạn biểu diễn logic của promise như một tập hợp các hoạt động chạy tuần tự theo từng dòng.

_Ví dụ:_

```jsx
import {useEffect, useState} from "react";

function App() {
    const [users, setUsers] = useState();

    useEffect(() => {
        fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
        .then(response => response.json())
        .then(data => {
            setUsers(data);
        });
    }, []);
}
```

Để sử dụng `async/await`, chúng ta cần đặt tiền tố `async` trước khai báo hàm để có thể sử dụng từ khóa `await`. Tuy nhiên, hàm `async` là một hàm trả về Promise.

Chúng ta cần giữ `useEffect` như một hàm thông thường và tạo một hàm khác bên trong nó có thể được gọi ngay lập tức (còn gọi là Immediately Invoked Function Expression ([IIFE](https://github.com/CUNGVANTHANG/Front-end/tree/master/Javascript%20Theory#a-iife)):

```jsx
useEffect(() => {
    (() => {
        // this is a function that will execute immediately
    })();
});
```

Bây giờ chúng ta cần làm cho hàm mới trở thành hàm `async` bằng cách thêm từ khóa `async` vào đầu hàm:

```jsx
useEffect(() => {
    (async () => {
        // we can use await here ✅
    })();
});
```

Và cuối cùng, với mọi hàm trả về promise (ví dụ: `fetch` và `response.json()`), chúng ta có thể thêm từ khóa `await` vào trước và loại bỏ `.then()`.

```jsx
import {useEffect, useState} from "react";

function App() {
    const [users, setUsers] = useState();

    useEffect(() => {
        (async () => {
            const response = await fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
            const data = await response.json()
            setUsers(data);
        })();
    }, []);
}
```

**XỬ LÝ LỖI:**

Khi sử dụng promise, chúng ta thường sử dụng `.catch` để xử lý lỗi. Với `async/await`, bạn cần đóng gói đoạn code sử dụng `await` bằng khối `try...catch`.

```jsx
import {useEffect, useState} from "react";

function App() {
    const [users, setUsers] = useState();
    const [isLoading, setIsLoading] = useState(true);

    useEffect(() => {
        (async () => {
          try {
            const response = await fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
            const data = await response.json();
            setIsLoading(false)
            setUsers(data);
          } catch (error) {
              console.log(error)
              setIsLoading(false);
          } 
        })()
    }, []);

    return null
}
```

Bạn cũng có thể sử dụng từ khóa `finally` để tái cấu trúc các câu lệnh chung giữa khối `try` và `catch`:

```jsx
import {useEffect, useState} from "react";

function App() {
    const [users, setUsers] = useState();
    const [isLoading, setIsLoading] = useState(true);

    useEffect(() => {
        (async () => {
          try {
            const response = await fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
            const data = await response.json();
            setUsers(data);
          } catch (error) {
              console.log(error)
          } finally {
            setIsLoading(false)
          }
        })()
    }, []);

    return null
}
```

### 2. Fetch POST
[:arrow_up: Mục lục](#mục-lục)

Để gửi một yêu cầu `POST`, chúng ta phải chỉ định method là `POST`.

```jsx
fetch("https://course-assets.tek4.vn/reactjs-assets/grades.json", {
    method: "POST"
})
.then(response => response.json())
.then(data => {
    console.log(data);
});
```

Tuy nhiên, trong hầu hết các trường hợp, bạn sẽ cần gửi một số dữ liệu cùng với yêu cầu. 

Trong ví dụ này, chúng ta cần gửi grade. Để làm điều đó, bạn cần thêm vào đối số thứ hai cặp khóa và giá trị sau: `JSON.stringify({grade: 10})` 

Một khuyến nghị dành cho bạn là khi làm việc với các API trả về dữ liệu dưới định dạng JSON, hãy luôn chỉ định header sau: `Content-Type: "application/json"`.

Nó giống như việc bạn đang thông báo cho API rằng: Tôi đang gửi cho bạn một số dữ liệu dưới định dạng JSON.

Tóm lại, dưới đây là cú pháp của `fetch POST`:

```jsx
fetch("https://course-assets.tek4.vn/reactjs-assets/grades.json", {
    method: "POST",
    headers: {
        "Content-Type": "application/json"
    },
    body: JSON.stringify({grade: 50})
})
.then(response => response.json())
.then(data => {
    console.log(data);
});
```

Cần chỉ định `method: "POST"` và thường phải gửi `body: JSON.stringify(dataObjectHere)`, header `"Content-Type": "application/json"`.

```jsx
import {useState} from "react";

function App() {
    const [number, setNumber] = useState(0);

    function handleFormSubmit(event) {
        event.preventDefault();

        fetch("https://course-assets.tek4.vn/reactjs-assets/grades.json", {
            method: "POST",
            headers: {
                "Content-Type": "application/json"
            },
            body: JSON.stringify({grade: number})
        })
        .then(response => response.json())
        .then(data => {
            console.log("Grade added");
            console.log(data);
        });
    }

    return <form onSubmit={handleFormSubmit}>
        <input type="number" value={number} name="grade" onChange={event => setNumber(event.target.value)} placeholder="Enter the grade" />
        <input type="submit" />
        </form>
    ;
}
```

`fetch POST` thường được đặt trong hàm `handleFormSubmit`, trong đó bạn gửi một trong các biến state trong body.

### 3. Axios
[:arrow_up: Mục lục](#mục-lục)

**Cài đặt Axios:**

```
npm install axios
```

**Sử dụng Axios để gọi API:**

```jsx
import React, { useState, useEffect } from 'react';
import axios from 'axios';

function DataFetching() {
  const [data, setData] = useState([]);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState('');

  useEffect(() => {
    axios.get('https://jsonplaceholder.typicode.com/posts')
      .then(response => {
        setData(response.data);
        setLoading(false);
      })
      .catch(error => {
        setError('Something went wrong!');
        setLoading(false);
      });
  }, []);

  return (
    <div>
      {loading ? 'Loading...' : null}
      {error ? error : null}
      <ul>
        {data.map(post => (
          <li key={post.id}>{post.title}</li>
        ))}
      </ul>
    </div>
  );
}

export default DataFetching;
```

- `useState`: Hook này được sử dụng để tạo và quản lý state trong function component. Ở đây, `data`, `loading`, và `error` được tạo để lưu trữ dữ liệu API, trạng thái tải, và lỗi nếu có.

- `useEffect`: Hook này được sử dụng để thực hiện các side effect trong function component. Ở đây, chúng ta gọi API khi component được `mount` lần đầu tiên.

- `axios.get`: Gửi một yêu cầu GET tới URL `https://jsonplaceholder.typicode.com/posts`. Khi yêu cầu thành công, chúng ta cập nhật state `data` và `loading`. Nếu yêu cầu thất bại, chúng ta cập nhật state `error` và `loading`.

**Tạo một yêu cầu POST với Axios:**

```jsx
import React, { useState } from 'react';
import axios from 'axios';

function PostData() {
  const [title, setTitle] = useState('');
  const [body, setBody] = useState('');
  const [response, setResponse] = useState(null);

  const handleSubmit = (e) => {
    e.preventDefault();
    axios.post('https://jsonplaceholder.typicode.com/posts', {
      title: title,
      body: body,
      userId: 1
    })
    .then(response => {
      setResponse(response.data);
    })
    .catch(error => {
      console.error('There was an error!', error);
    });
  };

  return (
    <div>
      <form onSubmit={handleSubmit}>
        <div>
          <label>Title</label>
          <input
            type="text"
            value={title}
            onChange={(e) => setTitle(e.target.value)}
          />
        </div>
        <div>
          <label>Body</label>
          <input
            type="text"
            value={body}
            onChange={(e) => setBody(e.target.value)}
          />
        </div>
        <button type="submit">Submit</button>
      </form>
      {response && (
        <div>
          <h3>Response</h3>
          <p>{JSON.stringify(response)}</p>
        </div>
      )}
    </div>
  );
}

export default PostData;
```

- `handleSubmit`: Hàm này được gọi khi form được submit. Nó ngăn hành động submit mặc định của form và gửi một yêu cầu POST tới API với dữ liệu từ form.

- `axios.post`: Gửi một yêu cầu POST tới URL `https://jsonplaceholder.typicode.com/posts` với dữ liệu title, body và userId. Khi yêu cầu thành công, state `response` được cập nhật với dữ liệu từ server.

## VI. Custom Hooks
[:arrow_up: Mục lục](#mục-lục)

Hook tùy chỉnh là một hàm JavaScript có tên bắt đầu bằng `use`. Ví dụ như `useHelloWorld`, `useAnalyticsEvent` ...

Mục tiêu của hook tùy chỉnh là tái sử dụng hook trong nhiều component. Việc đặt chúng vào một file riêng cũng giúp mã nguồn dễ đọc và dễ quản lý hơn. 

### 1. Custom hooks với useEffect
[:arrow_up: Mục lục](#mục-lục)

_Ví dụ:_

```jsx
// useHelloWorld.js
import {useEffect} from "react";

export default function useHelloWorld() {
    useEffect(() => {
        console.log("Hello World!");
    });
}
```

Bây giờ, quay trở lại component App, chúng ta có thể thêm nó vào như sau:

```jsx
import useHelloWorld from "./useHelloWorld.js";

function App() {
    useHelloWorld();

    return <h1>My App</h1>;
}
```

Bạn cũng có thể đặt tên file là `useHelloWorld.hook.js` để chỉ rõ rằng đây là một hook tùy chỉnh. Điều này phụ thuộc vào bạn.

**Các quy tắc làm việc với hook vẫn áp dụng cho hook tùy chỉnh.**

Quy tắc số 1: Chỉ gọi Hook từ các hàm React (component hoặc hook tùy chỉnh).

Quy tắc số 2: Chỉ gọi Hook ở cấp độ trên cùng

### 2. Custom hooks với useState
[:arrow_up: Mục lục](#mục-lục)

_Ví dụ:_

```jsx
import {useState} from "react";

function App() {
    const [counter, setCounter] = useState(0);

    function handleIncrementClick() {
        setCounter(prevCounter => prevCounter + 1);
    }

    function handleDecrementClick() {
        setCounter(prevCounter => {
            // only decrement if it's bigger than 0
            if (prevCounter > 0) {
                return prevCounter - 1;
            }
            // don't let it go below 0
            return 0;
        });
    }
}
```

Tái sử dụng logic trên, chúng ta có thể tối ưu hóa nó thành một hook tùy chỉnh tên là useProductCounter.

```jsx
// useProductCounter.js
import {useState} from "react";

export default function useProductCounter() {
    const [counter, setCounter] = useState(0);

    function increment() {
        setCounter(prevCounter => prevCounter + 1);
    }

    function decrement() {
        setCounter(prevCounter => {
            if (prevCounter > 0) {
                return prevCounter - 1;
            }
            return 0;
        });
    }

    return ; /* we need to return the counter and the two functions */
}
```

Chúng ta di chuyển khai báo `useState` và hai hàm và đặt chúng vào hook tùy chỉnh mới. Chúng ta cũng đổi tên `handleIncrementClick` thành `increment` vì đây là một hàm tăng giá trị có thể tái sử dụng và nó không nhất thiết phải được gọi khi nhấp chuột. Tương tự với hàm `handleDecrementClick`, giờ được gọi là `decrement`.

Bây giờ hook tùy chỉnh này cần trả về trạng thái `counter` cùng với các hàm `increment` và `decrement` để có thể sử dụng chúng bên ngoài component.

Có hai cách tiếp cận:

1. Array destructuring

Phương pháp đầu tiên là tiếp tục trả về mảng như ta đã học, nhưng lần này mảng sẽ có ba phần tử:

```jsx
return [counter, increment, decrement];
```

Sau đó, bên trong component, bạn sẽ sử dụng array destructuring:

```jsx
const [counter, increment, decrement] = useProductCounter();
```

2. Object destructuring (Hay dùng)

Phương pháp thứ hai là trả về một đối tượng chứa count và hai hàm:

```jsx
return {counter, increment, decrement};
```

Đây là cách sử dụng cú pháp rút gọn đối tượng ES2015. Nó tương đương với code dưới đây, nhưng ngắn hơn:

```jsx
return {
    counter: counter,
    increment: increment,
    decrement: decrement
};
```

Nhưng vì các khóa và giá trị có cùng tên, bạn chỉ cần viết là `return {counter, increment, decrement}`.

Với phương pháp này, bạn có thể sử dụng object destructuring trong component App, tương tự như array destructuring nhưng cho đối tượng:

```jsx
const {counter, increment, decrement} = useProductCounter();
```

### 3. Custom hooks với useFetch
[:arrow_up: Mục lục](#mục-lục)

Bạn có thể nhận thấy rằng code `fetch` thường rất dài, điều này làm cho component phức tạp hơn mức cần thiết. Đó là một trong những lý do tại sao chúng ta sẽ tạo hook tùy chỉnh `useFetch` để đơn giản hóa logic `fetch`.

Hook tùy chỉnh `useFetch` sẽ trả về một hàm `get` và một hàm `post`

_Ví dụ 1:_ Bắt đầu với "get"

Hàm `get` cho phép chúng ta thực hiện các yêu cầu `get`. Khi hook tùy chỉnh `useFetch` được xây dựng, đây là cách bạn sử dụng nó:

Thay vì viết code dưới đây:

```jsx
useEffect(() => {
    fetch("https://course-assets.tek4.vn/reactjs-assets/users.json")
    .then(response => response.json())
    .then(data => {
        console.log(data);
    })
    .catch(error => console.log(error));
}, []);
```

Bạn có thể viết code sau đây:

```jsx
const {get} = useFetch("https://course-assets.tek4.vn/reactjs-assets/users.json");

useEffect(() => {
    get("users.json")
    .then(data => {
        console.log(data);
    })
    .catch(error => console.log(error));
}, []);
```

Lưu ý rằng:

1. Hàm `useFetch` trả về một đối tượng với hàm `get`.

Chúng ta sử dụng object destructuring để truy cập vào hàm get.

2. Hàm `useFetch` nhận tham số `baseUrl`, cho phép ta gọi `get("users.json")` sau đó mà không cần lặp lại URL cơ sở dài.
3. `get("users.json")` tự động chuyển đổi phản hồi thành JSON. Chúng ta không cần phải làm điều đó nữa vì chúng ta có thể ngay lập tức xử lý promise và đọc `data`.

_Ví dụ 2:_ Bắt đầu với "post"

Phương thức `post` hoạt động tương tự như phương thức `get` nhưng nó cũng cần nhận tham số `body` để được gửi trong yêu cầu `fetch`.

Thay vì viết code dưới đây:

```jsx
fetch("https://course-api.tek4.vn/demo/react/grades", {
    method: "POST",
    headers: {
        "Content-Type": "application/json"
    },
    body: JSON.stringify({grade: 20})
})
.then(response => response.json())
.then(data => {
    console.log(data);
});
```

Bạn có thể viết code như sau:

```jsx
const {post} = useFetch("https://course-api.tek4.vn/demo/react/");

post("grades", {
    grade: 20
})
.then(data => {
    console.log(data);
})
.catch(error => console.log(error));
```

Lưu ý rằng hàm post nhận hai tham số: `url` và `body` được gửi cùng với yêu cầu post.

Yêu cầu `fetch` cũng nên thiết lập method là "post" và thiết lập các tiêu đề.

Hàm `post` sẽ nhận `url` mà bạn muốn gửi yêu cầu `fetch` và `url` này sẽ được thêm vào `baseUrl` và thực hiện yêu cầu `fetch` với `post`.

Hàm `post` cũng nhận tham số `body`, tham số này sẽ được chuyển thành chuỗi JSON và được gửi cùng với yêu cầu `fetch`.

Phiên bản nâng cao của hook tùy chỉnh trả về một đối tượng chứa ba mục: hàm `get`; hàm `post`; trạng thái loading, sẽ là một giá trị `boolean`.

```jsx
import { useState } from "react";

export default function useFetch(baseUrl) {
  const [loading, setLoading] = useState(true);

  function get(url) {
    return new Promise((resolve, reject) => {
      fetch(baseUrl + url)
        .then(response => response.json())
        .then(data => {
          if (!data) {
            setLoading(false);
            return reject(data);
          }
          setLoading(false);
          resolve(data);
        })
        .catch(error => {
          setLoading(false);
          reject(error);
        });
    });
  }

  function post(url, body) {
    return new Promise((resolve, reject) => {
      fetch(baseUrl + url, {
          method: "post",
          headers: {
            "Content-Type": "application/json",
          },
          body: JSON.stringify(body)
      })
        .then(response => response.json())
        .then(data => {
          if (!data) {
            setLoading(false);
            return reject(data);
          }
          setLoading(false);
          resolve(data);
        })
        .catch(error => {
          setLoading(false);
          reject(error);
        });
    });
  }

  return { get, post, loading };
};
```

Bạn cũng có thể destructure biến trạng thái `loading`, đây là một giá trị `boolean` cho biết `fetch` có đang trong trạng thái tải hay không. Ví dụ:

```jsx
import {useEffect} from "react";
import useFetch from "./useFetch.js";

function App() {
    const {get, loading} = useFetch("https://course-assets.tek4.vn/reactjs-assets/");

    useEffect(() => {
        get("users.json").then(data => {
            console.log(data);
        })
        .catch(error => console.error(error));
    }, []);

    return (<>
        <h2>{loading ? "Loading..." : ""}</h2>
    </>);
}
```

## VII. Hook - useRef
[:arrow_up: Mục lục](#mục-lục)

Trường hợp sử dụng useRef: `.play()` hoặc `.focus()`.

1. Tập trung vào một phần tử.
2. Phát video (`videoElement.play()`), tạm dừng video, v.v.
3. Chọn văn bản từ DOM.
4. Khởi tạo thư viện DOM.

Ví dụ, khi bạn mở [https://google.com](https://google.com), ô tìm kiếm sẽ được tập trung và trỏ nhắm tự động được đặt trong ô đó.

<img src="https://github.com/CUNGVANTHANG/Front-end/assets/96326479/cf39df37-85c2-40a6-bb11-e4942c9e97d9" height="200px" />

Phương thức `.focus()` trên các phần tử `<input>` là một phương thức đặt con trỏ của người dùng vào trường nhập liệu

Bạn có thể nghĩ đến việc sử dụng `document.querySelector()` để tìm `<input type="text" />` nhưng đây không phải là cách khuyên dùng vì một số lý do sau:

- Phương thức có thể không hoạt động (cụ thể là khi **trường nhập liệu chưa được hiển thị**, hãy nhớ rằng **React tạo ra các phần tử React tạo thành DOM ảo và sau đó hiển thị chúng lên DOM thực của trình duyệt**).

- Ngay cả khi phương thức hoạt động, bạn có thể nhận được **kết quả không đồng nhất** khi tiếp tục phát triển ứng dụng. Ví dụ: bạn sử dụng lại component đó nhiều lần trong ứng dụng.

Giải pháp cho vấn đề này là sử dụng `ref` của React. 

Ref cho phép bạn **giữ một tham chiếu đến phần tử DOM đã được hiển thị**. Sau khi tạo ra `ref` và gán nó cho một phần tử React trong JSX, bạn có thể gọi các phương thức mệnh lệnh trên phần tử DOM đã được hiển thị, chẳng hạn như `.focus()`.

Dưới đây là cách ref hoạt động:

```jsx
import {useRef} from "react";

function App() {
    const inputRef = useRef();

    return <input ref={inputRef} type="text" />;
}
```

Sau khi gán `inputRef` cho `<input />` bằng `ref={inputRef}`, chúng ta có thể truy cập vào phần tử DOM đã được hiển thị với `inputRef.current`.

Sau đó, bất cứ khi nào bạn muốn tập trung vào phần tử input, bạn có thể gọi `inputRef.current.focus()`. Vì vậy, kết quả cuối cùng sẽ như sau:

```jsx
import {useRef, useEffect} from "react";

function App() {
    const inputRef = useRef();

    useEffect(() => {
        inputRef.current.focus();
    }, []);

    return <input ref={inputRef} type="text" />;
}
```

Lời khuyên là hãy luôn kết thúc tên biến `ref` bằng từ Ref. Ví dụ:

- `inputRef` khi tham chiếu đến `input`
- `buttonRef` khi tham chiếu đến `button`
- `carouselRef` khi tham chiếu đến `carousel` (một plugin)

**Đối tượng được tạo ra bởi useRef:**

Khi bạn gọi `useRef()`, React sẽ tạo ra một đối tượng chứa **khóa** `current`. Vì vậy, việc gọi `const inputRef = useRef();` sẽ trả về một đối tượng có cấu trúc sau:

```jsx
{
    current: undefined
}
```

Sau đó, khi bạn gán `ref` cho phần tử JSX, React sẽ gán **khóa** `current` cho phần tử DOM đã được hiển thị. Ví dụ:

```jsx
{
    current: <input type="text" />
}
```

Điều này có nghĩa là mỗi khi bạn muốn truy cập vào phần tử đang tham chiếu, bạn phải sử dụng khóa `.current`. Đây là lý do tại sao trong ví dụ ở trên, chúng ta phải gọi `inputRef.current.focus()`. Đó là vì `inputRef.current` sẽ **cho phép bạn truy cập vào phần tử DOM được tham chiếu**.

Bạn phải nhớ rằng `inputRef.current` chỉ trả về phần tử DOM **sau khi component đã được hiển thị trên DOM**. Đây là lý do tại sao bạn chỉ nên sử dụng `ref` **bên trong** trình lý sự kiện (**useEffect**) hoặc cuộc gọi useEffect. Nguyên nhân là vì cả hai phương thức này đều chạy **sau** khi component đã được hiển thị trên DOM.

## VIII. Context
[:arrow_up: Mục lục](#mục-lục)

Trong lập trình, từ "context" có thể được hiểu là _thông tin liên quan_.

Giả sử ứng dụng có sẵn giao diện chủ đề tối và chủ đề sáng. Chủ đề của ứng dụng có thể được biểu diễn bằng một biến trạng thái trong component cao nhất, component `App`. `theme` được định nghĩa là một biến trạng thái trong component App như sau:

```jsx
import {useState} from "react";

function App() {
    const [theme, setTheme] = useState("dark");

    return <Nav />
}

function Nav() {
    return <Button>Login</Button>;
}

function Button(props) {
    return <button>{props.children}</button>;
}
```

Tuy nhiên, chúng ta cần biết `theme` hiện tại trong component Button vì chúng ta sẽ hiển thị một lớp khác nhau dựa trên chủ đề. Do đó, chúng ta sẽ phải truyền chủ đề xuống như một `prop` từ App đến Nav và từ Nav đến Button như sau:

```jsx
import React, {useState} from "react";

function App() {
    const [theme, setTheme] = useState("dark");

    return <Nav theme={theme} />
}

function Nav(props) {
    return <Button theme={props.theme}>Login</Button>;
}

function Button(props) {
    // render class depending on props.theme
    return <button>{props.children}</button>;
}
```

Để ý rằng mỗi component trong ứng dụng cần nhận `theme` như một `prop`. Điều này sẽ làm cho code trong các component **trở nên phức tạp và dài dòng.**

Đây là ví dụ minh họa một trường hợp sử dụng Context. Trường hợp sử dụng lý tưởng cho Context là **khi bạn muốn làm cho dữ liệu toàn cục có thể truy cập được từ nhiều component trong ứng dụng**.

### 1. Tạo Context
[:arrow_up: Mục lục](#mục-lục)

**Bước 1: Tạo Context**

Bước đầu tiên là tạo một Context mới. Để làm điều đó, chúng ta cần thêm một named export: `createContext` từ gói React, ví dụ: `import {createContext} from "react"`.

Sau đó, chúng ta cần gọi hàm `createContext()` và lưu kết quả trả về vào một biến.

```jsx
import React, {createContext} from "react";

const ThemeContext = createContext();
```

**Bước 2: Tạo Provider**

Mỗi **context đều cần một Provider**. Provider sẽ cung cấp dữ liệu cho context. Trong trường hợp này, chúng ta đang tạo `ThemeContext` và muốn cung cấp `theme` (ví dụ `"dark"` hoặc `"light"`).

```jsx
import { createContext } from "react";

const ThemeContext = createContext();

function ThemeProvider(props) {
  const theme = "dark";

  return (
    <ThemeContext.Provider value={theme}>
      {props.children}
    </ThemeContext.Provider>
  );
};
```

`ThemeProvider` là một component React nhận `props` và hiển thị `props.children` được đóng gói bởi `<ThemeContext.Provider>`.

`ThemeContext.Provider` nhận một `value`, đó là **giá trị mà tất cả các component con sẽ nhận được**. `ThemeContext` là một đối tượng và `Provider` là một khóa trong đối tượng đó

**Bước 3: Xuất Context & Provider**

Cuối cùng, chúng ta cần xuất `ThemeContext` và `ThemeProvider` bằng `export {ThemeContext, ThemeProvider}`.

```jsx
import { createContext } from "react";

const ThemeContext = createContext();

function ThemeProvider(props) {
  const theme = "dark";

  return (
    <ThemeContext.Provider value={theme}>
      {props.children}
    </ThemeContext.Provider>
  );
};

export { ThemeContext, ThemeProvider };
```

### 2. Sử dụng Context
[:arrow_up: Mục lục](#mục-lục)

**Bước 1. Đóng gói component với Provider**

Để có thể sử dụng `context` trong ứng dụng, bạn phải đóng gói các component bằng `Provider`.

Hãy xem xét component `App` hiển thị `<Nav />`:

```jsx
// index.js
function App() {
    return <Nav />;
}
```

Đầu tiên, chúng ta cần thêm `ThemeProvider` và đóng gói tất cả các component trong nó:

```jsx
// index.js
import {ThemeProvider} from "./ThemeContext.js";

function App() {
    return (<ThemeProvider>
        <Nav />
    </ThemeProvider>);
}
```

Điều này cho phép tất cả các component được lồng trong `ThemeProvider` có quyền truy cập vào `context` được cung cấp bởi `ThemeProvider`.

**Bước 2. Sử dụng context trong các component**

Bất kỳ component nào được lồng trong `ThemeProvider` bây giờ có thể truy cập vào `context` bằng cách thêm `ThemeContext` và truyền nó vào hook `useContext()`. 

```jsx
// Button.js
import {useContext} from "react";
import {ThemeContext} from "./ThemeContext.js";

function Button(props) {
    const theme = useContext(ThemeContext);
    console.log(theme); // "dark"
    return <button>{props.children}</button>;
}
```

Chúng ta đã thêm hook `useContext` và truyền `ThemeContext` cho nó. Điều này cho phép ta sử dụng `value` đã được truyền cho `provider` trong bước trên, trong ví dụ này là `"dark"`.

Cách làm này có vẻ phức tạp và rườm rà, nhưng lợi ích của việc này là chúng ta không cần phải truyền `props.theme` từ component cao nhất xuống tất cả các component con.

Vì vậy, chúng ta có thể tái cấu trúc chương trình trong bài học đầu chương như sau:

```jsx
import {useContext} from "react";
import {ThemeContext, ThemeProvider} from "./ThemeContext.js";

function App() {
    return (<ThemeProvider>
        <Nav />
    </ThemeProvider>);
}

function Nav() {
    return <Button>Login</Button>;
}

function Button(props) {
    const theme = useContext(ThemeContext);
    console.log(theme); // "dark"
    return <button>{props.children}</button>;
}
```

### 3. Giá trị Context
[:arrow_up: Mục lục](#mục-lục)

Ngoài trả về một giá trị chuỗi như sau:

```jsx
function ThemeProvider(props) {
  const theme = "dark";

  return (
    <ThemeContext.Provider value={theme}> /* value is a string (in this example) */
      {props.children}
    </ThemeContext.Provider>
  );
};
```

Thì ta có thể định nghĩa context trả về một mảng hoặc đối tượng!

```jsx
import { createContext } from "react";

const ThemeContext = createContext();

function ThemeProvider(props) {
  const theme = "dark";

  function toggleTheme() {
    // toggle the theme here
  }

  const value = {
    theme: theme,
    toggleTheme: toggleTheme
  }

  return (
    <ThemeContext.Provider value={value}>
      {props.children}
    </ThemeContext.Provider>
  );
};

export { ThemeContext, ThemeProvider };
```

Lưu ý `<ThemeContext.Provider />` vẫn nhận cùng `value={}`, nhưng thay vì truyền một chuỗi, chúng ta bây giờ đang truyền một đối tượng.

### 4. Cập nhật giá trị Context
[:arrow_up: Mục lục](#mục-lục)

Đôi khi chúng ta muốn thay đổi giá trị của `theme` tại một thời điểm nào đó, để làm điều đó, chúng ta cần tạo một biến trạng thái cho chủ đề thay vì sử dụng biến thông thường.

Chúng ta có thể sử dụng hook `useState` bên trong Context:

```jsx
import { createContext, useState } from "react";

const ThemeContext = createContext();

function ThemeProvider(props) {
  const [theme, setTheme] = useState("dark");

  function toggleTheme() {
    // toggle the theme here
  }

  const value = {
    theme: theme,
    toggleTheme: toggleTheme
  }

  return (
    <ThemeContext.Provider value={value}>
      {props.children}
    </ThemeContext.Provider>
  );
};

export { ThemeContext, ThemeProvider };
```

Và bây giờ chúng ta có thể triển khai hàm `toggleTheme`:

```jsx
function toggleTheme() {
    if (theme === "dark") {
      setTheme("light")
    } else {
      setTheme("dark")
    }
}
```

hàm sẽ chuyển đổi `theme` từ `"dark"` sang `"light"` và ngược lại.

Với `context` trên, chúng ta có thể cập nhật `theme` từ bất kỳ đâu trong ứng dụng, miễn là chúng ta sử dụng `ThemeContext`. Dưới đây là cách thực hiện:

```jsx
import {useContext} from "react";
import {ThemeContext} from "./ThemeContext.js";

function App() {
    const context = useContext(ThemeContext);
    console.log(context); // {theme: "dark", toggleTheme: Function}

    return <button onClick={() => context.toggleTheme()}>Toggle Theme</button>;
}
```

`useContext(ThemeContext)` bây giờ trả về một đối tượng chứa `theme` và hàm `toggleTheme`.

Sau đó, chúng ta gọi hàm `context.toggleTheme()` khi nút được nhấp (`onClick`).

## IX. React Router
[:arrow_up: Mục lục](#mục-lục)

Tên gói cho React Router là `react-router-dom`

Nhập gói:

```jsx
import {} from "react-router-dom";
```

Component phổ biến hay sử dụng `BrowserRouter`, `Routes`, `Route`, `Link`

### 1. Điều hướng cơ bản
[:arrow_up: Mục lục](#mục-lục)

**1. BrowserRouter**

Component `<BrowserRouter />` cho phép thay đổi `URL` của trang mà không kích hoạt hành vi làm mới trình duyệt

Để `BrowserRouter` hoạt động, bạn cần đóng gói toàn bộ ứng dụng trong component đó:

```jsx
import {BrowserRouter} from "react-router-dom";

function App() {
    return <BrowserRouter>
        <div>The rest of your app goes here</div>
    </BrowserRouter>;
}
```

**2. Route**

Component `<Route />` sẽ hiển thị một component khi trường thuộc tính `path` khớp với `URL` hiện tại trong trình duyệt.

Dưới đây là ví dụ về component `<Route />`:

```jsx
<Route path="/about" element={<About />}></Route>
```

Component `<About />`, được cung cấp cho Route thông qua trường thuộc tính `element`, chỉ được hiển thị khi `URL` của trình duyệt khớp với đường dẫn `/about`.

Hãy xem ví dụ đầy đủ:

```jsx
import {BrowserRouter, Route} from "react-router-dom";

function App() {
    return <BrowserRouter>
        <div>The rest of your app goes here</div>

        {/*We still need to wrap these two Route components with a <Routes />. Keep reading for now.*/}
        <Route path="/" element={<Home />}></Route>
        <Route path="/about" element={<About />}></Route>
    </BrowserRouter>;
}
```

Khi người dùng điều hướng đến `/`, component `<Home />` sẽ được hiển thị.

Tương tự, khi người dùng điều hướng đến `/about`, component `<About />` sẽ được hiển thị.

**3. Routes**

Component `<Routes />` sẽ đóng gói nhiều component `<Route />` và chỉ hiển thị `<Route />` khớp với URL hiện tại trong trình duyệt.

```jsx
import {BrowserRouter, Routes, Route} from "react-router-dom";

function App() {
    return <BrowserRouter>
        <div>The rest of your app goes here</div>

        <Routes>
            <Route path="/" element={<Home />}></Route>
            <Route path="/about" element={<About />}></Route>
        </Routes>
    </BrowserRouter>;
}
```

Điều quan trọng là phần tử `<Routes />` trực tiếp đóng gói các phần tử `<Route />`, tức là `<Route />` phải nằm trực tiếp bên trong trực tiếp `<Routes />`. Điều đó có nghĩa là bạn không nên có thành phần trung gian như `<div>` hoặc các phần tử khác ở giữa `<Routes />` và `<Route />`; nếu không, việc điều hướng có thể không hoạt động chính xác.

**4. Link**

Chúng ta thường sử dụng thẻ `anchor` để liên kết đến một trang mới. Ví dụ: `<a href="/about">About us</a>`. Tuy nhiên, liên kết này sẽ thực hiện điều hướng trang, điều đó có nghĩa là ứng dụng React sẽ phải khởi động lại. Điều này bởi vì trình duyệt nghĩ rằng chúng ta đang điều hướng đến một trang hoàn toàn mới, vì vậy nó thực hiện một yêu cầu HTTP tới `/about`, sau đó trình duyệt phải phân tích HTML và các đoạn mã script, v.v.

Ưu điểm của React Router là chúng ta có thể thực hiện điều hướng ngay tức thì. Đó là lý do tại sao chúng ta cần thay thế liên kết `<a>` bằng component `<Link />` do React Router cung cấp. Dưới đây là cách thực hiện:

```jsx
import {BrowserRouter, Routes, Route, Link} from "react-router-dom";

function App() {
  return (
    <BrowserRouter>
        <nav>
          <ul>
            <li>
              <Link to="/">Home</Link>
            </li>
            <li>
              <Link to="/contact">Contact</Link>
            </li>
          </ul>
        </nav>

        {/* Routes and Route goes here*/}
    </BrowserRouter>
  );
}
```

Component `<Link />` nhận một prop `to`. Khi người dùng nhấp vào liên kết, React Router sẽ chuyển hướng đến đường dẫn được cung cấp bởi prop `to`.

Phần tử `<Link />` này sẽ hiển thị một phần tử `<a>`, nhưng một số trình xử lý sự kiện sẽ chỉ định React Router thực hiện chuyển hướng ngay lập tức thay vì chuyển hướng trang.

### 2. Tham số URL
[:arrow_up: Mục lục](#mục-lục)

Bạn có một danh sách sản phẩm, bao gồm từ 2 sản phẩm cho đến hàng trăm (hoặc thậm chí nhiều hơn). Làm thế nào để tạo một trang riêng biệt cho từng sản phẩm?

Ta có thể suy ra rằng tất cả các sản phẩm đều có cấu trúc trang giống nhau, chỉ có dữ liệu là khác nhau. Để làm điều đó, ta sử dụng tham số `URL` của React Router.

Trước tiên hãy xem một ví dụ, sau đó ta sẽ phân tích cách nó hoạt động:

```jsx
<Route path="/products/:id" element={<Product />}>
</Route>
```

Để ý đường dẫn được định nghĩa là `/products/:id`. `:id` là trình giữ chỗ cho một giá trị `id` mà chúng ta có thể sử dụng như một biến trong bài học tiếp theo.

Dấu hai chấm (`:`) thông báo cho React Router biết rằng chúng ta không tìm kiếm `:id` chính xác mà là tìm kiếm bất kỳ văn bản nào xuất hiện sau `/products/`. Ví dụ, các route sau sẽ khớp với đường dẫn `/products/:id:`

`/products/1` => `:id` là `1`
`/products/2` => `:id` là `2`
`/products/30` => `:id` là `30`
`/products/abc` => `:id` là `abc`

Tất cả các route này sẽ hiển thị component `<Product />`.

Lưu ý rằng React Router sẽ nhận biết được bất kỳ chuỗi nào xuất hiện sau `/products/`, không chỉ giới hạn ở `id` (số).

### 3. Hook - useParams
[:arrow_up: Mục lục](#mục-lục)

Chúng ta đã định nghĩa một route nhận một tham số `URL` và hiển thị component tương ứng, ví dụ như component `<Product />`.

Nhưng làm thế nào component `Product` có thể biết tham số `URL` đó là gì?

Cho route sau:

```jsx
<Route path="/products/:id" element={<Product />}>
</Route>
```

Trong component `<Product />`, bạn có thể trích xuất tham số `:id` từ `URL` bằng cách sử dụng hook `useParams()`.

Hook `useParams` là một hook mà chúng ta cần thêm từ `"react-router-dom"`. Hook này trả về một đối tượng chứa tất cả các tham số `URL` từ `URL`:

```jsx
// Product.js
import {useParams} from "react-router-dom";

function Product() {
  const params = useParams();
  console.log(params); // object containing params

  return <h2>Product</h2>;
}
```

Bắt đầu bằng việc thêm `useParams` dưới dạng named import từ `react-router-dom`. Sau đó, bạn gọi hook đó ở đầu component với `const params = useParams()`.

Nó luôn trả về một đối tượng chứa tất cả các tham số `URL` từ `URL`. Sử dụng ví dụ hiện tại, giả sử người dùng truy cập trang: `/products/10`, khi đó đối tượng `params` sẽ chứa:

```jsx
{
    id: "10"
}
```

Điều này có nghĩa là nếu chúng ta muốn lấy `id` của sản phẩm từ `URL`, chúng ta sẽ truy cập `params.id`.

- **Một điều quan trọng cần lưu ý là giá trị của các tham số URL luôn là chuỗi.**

- **Nhiều tham số URL**

Cho đến nay, tất cả các ví dụ chỉ có một tham số `URL`. Tuy nhiên, bạn có thể sử dụng nhiều hơn một tham số `URL`. Hãy xem một ví dụ:

```jsx
<Route path="/products/:type/:id" element={<Product />}>
</Route>
```

Giả sử người dùng truy cập `URL` sau: `/products/food/42`, tham số `:type` tương ứng với `"food"` và tham số `:id` tương ứng với `"42"`.

Chúng ta có thể cập nhật component để đọc cả hai tham số vì hook `useParams()` trả về một đối tượng chứa tất cả các tham số `URL` này:

```jsx
// Product.js
import {useParams} from "react-router-dom";

function Product() {
  const params = useParams();
  const id = params.id; // "42"
  const type = params.type; // "food"

  return <h2>Product</h2>;
}
```

### 4. Nested routes
[:arrow_up: Mục lục](#mục-lục)

_Ví dụ trực quan:_ Thông thường trên một số trang web, khi chọn trang about (giới thiệu), bạn sẽ được chuyển hướng đến route `/about`, sau đó trang sẽ hiển thị ảnh bìa, tiêu đề `About`, và bạn có thể chọn một trong hai trang con:

Chọn `About us` (Về chúng tôi) sẽ chuyển hướng bạn đến `/about/us/`

Chọn `About the Team` (Về Đội ngũ) sẽ chuyển hướng bạn đến `/about/team/`

Trang Về chúng tôi sẽ hiển thị nội dung giống như trang `/about` nhưng có thêm phần Về chúng tôi ở dưới nội dung hiện tại.

Tương tự, trang Về Đội ngũ sẽ hiển thị nội dung giống như trang `/about` nhưng có thêm phần Về Đội ngũ ở dưới nội dung hiện tại.

Đây là một ví dụ về các route lồng nhau (nested routes). Điều này là bởi vì trang `/about/us` đang hiển thị hai route cùng một lúc. Nó đang hiển thị nội dung từ route `/about` cũng như nội dung từ route `/about/us`.

_Khái niệm:_ Các route lồng nhau cho phép bạn hiển thị nhiều route cùng một lúc. Ví dụ, `/about/us` sẽ hiển thị cả route `/about` và `/about/us` cùng một lúc.

**Quá trình làm việc:**

Quá trình làm việc với các route lồng nhau trong React Router bao gồm ba bước:

1. Khai báo các `<Route />` lồng nhau.
2. Sử dụng `<Outlet />` để xác định vị trí mà các route lồng nhau sẽ hiển thị trong component cha.
3. Thêm các phần tử `<Link />` để xem và kiểm thử các route lồng nhau.

Hãy bắt đầu bằng một ví dụ có component `<About />` được hiển thị trên `/about`:

```jsx
import {BrowserRouter, Routes, Route} from "react-router-dom";

function About() {
  return <>
        <h1>About</h1>

    </>;
}

function App() {
    return (
        <BrowserRouter>
            <Routes>
                <Route path="/about/" element={<About />}>
                </Route>
            </Routes>
        </BrowserRouter>
    );
}
```

Chúng ta muốn làm cho component `<About />` hiển thị các route lồng nhau. Nghĩa là mỗi khi đường dẫn bắt đầu bằng `/about`, chúng ta muốn hiển thị component `<About />` cùng với một số component con. Điều này cho phép ta luôn hiển thị `<h1>About</h1>` trên các trang con như `/about/us` và `/about/team`.

**1. Khai báo các `<Route />` lồng nhau**

Đầu tiên, chúng ta cần định nghĩa hai route lồng nhau nằm trong route cha `/about`. Đó là `<Route path="us" />` và `<Route path="team" />`. Chú ý rằng các đường dẫn là tương đối vì chúng ta sẽ nhúng chúng trong `<Route path="/about/" />`. Hai component `<Route />` này trở thành component con của `<Route path="/about" />` như sau:

```jsx
<Route path="/about/" element={<About />}>
    {/* about/us */}
    <Route path="us" element={<h2>About us</h2>}>
    </Route>
    {/* about/team */}
    <Route path="team" element={<h2>About the Team</h2>}>
    </Route>
</Route>
```

Comment ở trên cho thấy rằng `path="us"` được lồng trong `path="/about/"` tạo thành đường dẫn cuối cùng của route đó là `/about/us`. Tương tự, `path="team"` trở thành `/about/team`.

**2. Sử dụng <Outlet />**

Bây giờ, chúng ta cần chỉ định cho component `<About />` hiển thị các route lồng nhau. Để làm điều đó, chúng ta cần thêm component `Outlet` từ `react-router-dom` và sử dụng nó trong `<About />`. Điều này sẽ xác định vị trí mà các route lồng nhau sẽ hiển thị trong JSX:

```jsx
import {BrowserRouter, Routes, Route, Outlet} from "react-router-dom";

function About() {
  return <>
        <h1>About</h1>

        {/* Render nested routes for /about/... here */}
        <Outlet />
    </>;
}

function App() {
    return (
        <BrowserRouter>
            <Routes>
                <Route path="/about/" element={<About />}>
                    {/* about/us */}
                    <Route path="us" element={<h2>About us</h2>}>
                    </Route>
                    {/* about/team */}
                    <Route path="team" element={<h2>About the Team</h2>}>
                </Route>
            </Route>
          </Routes>
        </BrowserRouter>
    );
}
```

Giả sử bạn đặt `<Outlet />` trước `<h1>About</h1>`. Trong trường hợp đó, nội dung của các route lồng nhau (`<h2>About us</h2>` hoặc `<h2>About the Team</h2>`) sẽ hiển thị **trước** `h1`.

**3. Thêm các phần tử <Link />**

Cuối cùng, chúng ta cần thêm các phần tử `<Link />` để xem và kiểm thử các route lồng nhau:

```jsx
import {BrowserRouter, Routes, Route, Outlet, Link} from "react-router-dom";

function About() {
  return <>
      {/* Content always rendered when the URL starts with /about */}
      <h1>About</h1>
      <Link to="us">About us</Link> | 
      <Link to="team">About the team</Link>

      <Outlet />
    </>;
}

function App() {
    return (
        <BrowserRouter>
          <Routes>
            <Route path="/about/" element={<About />}>
                {/* about/us */}
                <Route path="us" element={<h2>About us</h2>}>
                </Route>
                {/* about/team */}
                <Route path="team" element={<h2>About the Team</h2>}>
                </Route>
            </Route>
            </Route>
          </Routes>
        </BrowserRouter>
    );
}
```

### 5. Hook - useOutletContext
[:arrow_up: Mục lục](#mục-lục)

Có những tình huống mà chúng ta **cần truyền dữ liệu từ component cha chứa Outlet xuống cho các component con**. Hiện tại, chúng ta sẽ bắt đầu với một ví dụ cơ bản với biến `data`, chúng ta muốn truyền biến này cho các component con được hiển thị trong `<Outlet />`.

```jsx
function About() {
    // we want to make this available to the <Outlet /> sub-components
    const data = {
        someValue: 123
    };

    return <>
        {/* Content always rendered when the URL starts with /about */}
        <h1>About</h1>
        <Link to="us">About us</Link> | 
        <Link to="team">About the team</Link>

        <Outlet />
    </>;
}
```

Để làm điều đó, chúng ta có thể sử dụng thuộc tính `context` trên component `<Outlet />`, nó sẽ tự động tạo ra `context`. Đây là một trường hợp sử dụng phổ biến, vì vậy nhóm React Router đã tích hợp tính năng này vào thư viện.

```jsx
function About() {
    // we want to make this available to the <Outlet /> sub-components
    const data = {
        someValue: 123
    };

    return <>
        {/* Content always rendered when the URL starts with /about */}
        <h1>About</h1>
        <Link to="us">About us</Link> | 
        <Link to="team">About the team</Link>

        // pass it to Outlet as a context
        <Outlet context={data} />
    </>;
}
```

**Hook useOutletContext**

Đây là lúc hook `useOutletContext` trở nên hữu ích. Chúng ta có thể sử dụng nó trong bất kỳ component nào cần được hiển thị bên trong `<Outlet />`. Ví dụ, trong component `AboutUs`:

```jsx
import {useOutletContext} from "react-router-dom";

function AboutUs() {
    const context = useOutletContext();
    console.log(context); // {someValue: 123}
    console.log(context.someValue); // 123

    // ...
}
```

### 6. Xử lý lỗi 404
[:arrow_up: Mục lục](#mục-lục)

Đối với các dự án lớn, việc xử lý các route không tồn tại là rất quan trọng. Đôi khi chúng được gọi là “404 route” vì mã trạng thái HTTP 404 được trả về khi không tìm thấy tài liệu trên máy chủ. 

Khi không có route nào khớp với `URL` hiện tại của trình duyệt, chúng ta sẽ tạo một route đại diện cho các trường hợp không khớp như sau:

```jsx
import {BrowserRouter, Routes, Route} from "react-router-dom";

function App() {
    return <BrowserRouter>
        <Routes>
            <Route path="/" element={<p>Landing page here</p>}></Route>
            <Route path="/products" element={<p>Products page here</p>}></Route>
            <Route path="*" element={<p>404 page here</p>}></Route>
        </Routes>
    </BrowserRouter>
}
```

Bây giờ khi người dùng truy cập vào `/`, họ sẽ thấy Landing page here. Tương tự, khi họ truy cập vào `/products`, họ sẽ thấy `Products page here`. Và đối với tất cả các liên kết khác, họ sẽ thấy `404 page here`.

Tại sao lại như vậy? Đó là vì `<Route>` mà chúng ta đã tạo cho trang 404 có trường thuộc tính path được đặt thành `*`. React Router sẽ kích hoạt route này chỉ **khi không có route nào khớp với URL hiện tại**.

### 7. Trang hoạt động NavLink
[:arrow_up: Mục lục](#mục-lục)

Giả sử bạn có một menu điều hướng với hai liên kết:

1. `Home` chuyển hướng người dùng đến `/`
2. `About` chuyển hướng người dùng đến `/about`

Bạn có thể tự động làm nổi bật liên kết `About` với React Router khi người dùng đang truy cập route `/about`. Tương tự, bạn có thể làm nổi bật liên kết `Home` khi người dùng đang truy cập route `/`.

```jsx
import {NavLink} from "react-router-dom";

function getClassName({isActive}) {
    if (isActive) {
        return "active"; // CSS class
    }
}

function App() {
    return <ul>
        <li>
            <NavLink to="/" className={getClassName}>Home</NavLink>
        </li>
        <li>
            <NavLink to="/about" className={getClassName}>About</NavLink>
        </li>
    </ul>
}
```

Đoạn code trên yêu cầu viết một số code CSS cho lớp `active`. Hãy làm cho liên kết của trang hiện tại trong menu được làm nổi bật bằng chữ đậm:

```css
.active {
    font-weight: bold;
}
```

Bạn có thể nhận thấy là ở đây chúng ta đang sử dụng `NavLink` thay vì `Link`.

Điều này rất quan trọng vì component `<Link />` **không hỗ trợ truyền một định nghĩa hàm vào trường thuộc tính** `className`.

Một lỗi phổ biến là **sử dụng ClassName với định nghĩa hàm trên component** `<Link />`, nhưng điều đó sẽ làm **code không hoạt động**!

### 8. Hook - useNavigate
[:arrow_up: Mục lục](#mục-lục)

_Ví dụ_: bạn gửi một yêu cầu `fetch` và dựa trên kết quả đó, bạn muốn chuyển hướng người dùng đến một trang cụ thể.

Sau đây là một số ví dụ khác:

1. Chuyển hướng người dùng đến trang `/login` nếu họ chưa đăng nhập.
2. Chuyển hướng người dùng đến trang `/dashboard` sau khi yêu cầu `fetch()` cho đăng nhập thành công.

Để làm điều đó, bạn cần sử dụng hook `useNavigate()`, nó trả về một phương thức mà bạn có thể gọi để điều hướng đến một route mới một cách tự động. Hãy xem ví dụ sau:

```jsx
import React, {useEffect} from "react";
import {useNavigate} from "react-router-dom";

function HelpPage() {
    const navigate = useNavigate();

    useEffect(() => {
        const isLoggedIn = window.localStorage.getItem("isLoggedIn");
        if (!isLoggedIn) {
            navigate("/login");
        }
    }, []);

    return <h2>Help page</h2>;
}
```

Trong ví dụ này, chúng ta kiểm tra xem `localStorage` có chứa giá trị cho khóa `isLoggedIn` hay không. Nếu không, chúng ta điều hướng người dùng trở lại trang `/login` bằng cách gọi `navigate("/login")`.

**Hook `useNavigate` chỉ hoạt động trong `BrowserRouter`**

Bạn cần gọi hook `useNavigate()` **trong một component được lồng** trong `<BrowserRouter />`, nếu không, hook sẽ không hoạt động.

Do đó đoạn code dưới đây SẼ KHÔNG hoạt động:

```jsx
import React from "react";
import {BrowserRouter, useNavigate} from "react-router-dom";

function App() {
    // ❌ This breaks because the component was not wrapped by BrowserRouter, but its children are.
    const history = useNavigate();

    return <BrowserRouter>
        {/* ... */}
    </BrowserRouter>;
}
```

Như bạn thấy, hook `useNavigate()` sẽ không hoạt động trong component `App()` vì nó không được đóng gói bởi `<BrowserRouter/>`. Tuy nhiên, tất cả các component con bên trong App sẽ được đóng gói bởi `<BrowserRouter />`, vì vậy bạn có thể sử dụng `useNavigate()` trong các component con đó.

### 9. Hook - useLocation
[:arrow_up: Mục lục](#mục-lục)

Nếu bạn **muốn chạy một đoạn code mỗi khi React Router điều hướng đến một URL mới** thì bạn sẽ làm như thế nào?

Bạn có thể làm điều đó bằng cách sử dụng hook `useLocation`.

Hook `useLocation` trả về thông tin liên quan đến route hiện đang hoạt động.

Dưới đây là cách bạn sử dụng hook `useLocation`:

```jsx
import {BrowserRouter, Routes, Route, useLocation} from "react-router-dom";
import {createRoot} from "react-dom/client";

function App() {
    const location = useLocation();
    console.log(location.pathname);

    return <Routes>
        {/* routes here... */}
    </Routes>
}

createRoot(document.querySelector("#react-root")).render(<BrowserRouter><App /></BrowserRouter>);
```

Biến `location` sẽ là một đối tượng chứa `pathname`.

Sau đó, bạn có thể sử dụng `location.pathname` để biết **route hiện tại mà người dùng đang duyệt**. Ví dụ: `/` hoặc `/about`, v.v., tùy thuộc vào các route hiện có.

Giống như hook `useNavigate`, bạn cần đảm bảo rằng code **được chạy trong một component được đóng gói bởi** `<BrowserRouter />`, nếu không, hook sẽ không hoạt động.

**Thay đổi vị trí**

Bằng cách sử dụng `useLocation` và cách lấy `pathname` hiện tại, bạn có thể chạy một đoạn code mỗi khi React Router điều hướng đến một `URL` mới bằng cách đóng gói code bằng `useEffect` với một phụ thuộc trên `location`. Cách triển khai như sau:

```jsx
import React, {useEffect} from "react";
import {BrowserRouter, Routes, Route, useLocation} from "react-router-dom";
import {createRoot} from "react-dom/client";

function App() {
    const location = useLocation();

    // run a piece of code on location change
    useEffect(() => {
        console.log(location.pathname);
        // send it to analytic, or do some conditional logic here
    }, [location]);

    return <Routes>
        {/* routes here... */}
    </Routes>
}

createRoot(document.querySelector("#react-root")).render(<BrowserRouter><App /></BrowserRouter>);
```

Code trong hook `useEffect` sẽ chạy mỗi khi đối tượng `location` thay đổi, điều này xảy ra mỗi khi người dùng điều hướng đến một route mới.

## X. Redux
[:arrow_up: Mục lục](#mục-lục)

### 1. Redux là gì
[:arrow_up: Mục lục](#mục-lục)

Lí do dùng Redux:

  - Nhiều thành viên tham gia vào dự án.

  - Bạn có nhiều biến state đang được sử dụng trong nhiều component.

  - Bạn đã rất quen thuộc với Redux và việc sử dụng nó sẽ giúp tăng năng suất thay vì gây trở ngại.

  - Ứng dụng có nhiều trạng thái cần cập nhật nhiều lần (liên quan đến trạng thái được sử dụng trong nhiều component).

- **Redux so với Chuyển trạng thái lên trên**

**Việc chuyển trạng thái** lên cấp độ cao hơn có thể nhanh chóng trở nên phức tạp khi số biến lượng trạng thái cần di chuyển ngày càng tăng lên. Đôi khi, bạn cần chuyển trạng thái qua nhiều cấp component (5 cấp độ), quá trình này càng trở nên cồng kềnh và phức tạp.

Bạn sẽ không gặp vấn đề này với `redux`, vì mỗi component sẽ lựa chọn dữ liệu cụ thể mà nó cần và cập nhật trạng thái.

- **Redux so với Context**

Đối với các cập nhật trạng thái toàn cục diễn ra thường xuyên, việc sử dụng Context **sẽ gây ra vấn đề về hiệu suất**. Trong trường hợp này, việc sử dụng Redux sẽ hợp lý hơn. Ngoài ra, với số lượng lớn trạng thái được cập nhật, Redux **giúp dễ dàng theo dõi** các thay đổi và quản lý mọi thứ.

Nhìn chung, ứng dụng **càng nhỏ/đơn giản thì bạn càng ít cần sử dụng Redux.**

### 2. State, Store và Reducer
[:arrow_up: Mục lục](#mục-lục)

#### 1. Trạng thái (State)

Trong React, chúng ta có thể tạo một trạng thái lưu trữ giá trị **boolean, số, chuỗi, v.v.**

Tuy nhiên trong Redux, trạng thái luôn luôn là **một đối tượng**

_Ví dụ:_ Đối với ứng dụng đếm, ta sẽ tạo đối tượng trạng thái sau:

```jsx
const state = {
    value: 0 // starting value of the counter
};
```

Tên của biến không quan trọng. Điều quan trọng là `state` **là một đối tượng**. Và trong trường hợp này, đối tượng có **khóa** `value` với **giá trị** ban đầu là `0`.

#### 2. Reducer

Reducer là một hàm nhận 2 tham số: **trạng thái hiện tại** và **một hành động (action)**

Dựa vào hành động nhận được, nó có thể trả về một trạng thái mới. Nếu không, nó sẽ trả về trạng thái hiện tại mà không thay đổi gì.

_Ví dụ 1:_ Hãy xem xét ví dụ chưa hoàn chỉnh sau đây:

```jsx
const initialState = {
    value: 0,
};

const counterReducer = (state = initialState, action = {}) => {
  return state; // return the state as is
};
```

Đây là reducer cơ bản nhất. Nó nhận trạng thái hiện tại và trả về chính xác trạng thái đó như nó đã nhận. Để ý tham số `state = initialState`. Điều này có nghĩa là nếu chúng ta gọi `counterReducer` mà không có tham số nào, nó sẽ mặc định là `initialState`. Điều này sẽ xảy ra vào lần đầu tiên chúng ta gọi reducer này.

Sử dụng code trên, dưới đây là cách chúng ta sử dụng reducer này:

```jsx
const state = counterReducer(); // state will default to initialState
console.log(state); // {value: 0}
```

_Ví dụ 2:_ 

Bây giờ, hãy cùng **tăng giá trị của bộ đếm**. Để làm điều đó, chúng ta sẽ **truyền một hành động** là `{type: "counter/increment"}`. Action (hành động) là một **đối tượng** được **sử dụng** để thực hiện **thay đổi trạng thái**.

Vì vậy, chúng ta cần cập nhật reducer để xử lý hành động này với `if (action.type === "counter/increment")`:

```jsx
const initialState = {
    value: 0,
};

const counterReducer = (state = initialState, action = {}) => {
  if (action.type === "counter/increment") {
    return {
        value: state.value + 1 // important: do NOT mutate the state.
    };
  }

  return state; // return the state as is (in all other cases)
};
```

Dưới đây là cách sử dụng reducer này:

```jsx
const state = counterReducer(); // state will default to initialState
console.log(state); // {value: 0}
const newState = counterReducer(state, {type: "counter/increment"});
console.log(newState); // {value: 1}
```

#### 3. Cửa hàng (Store)

Cửa hàng là một **đối tượng chứa reducer và trạng thái (state)**. 

Muốn cập nhật trạng thái, chúng ta sẽ phải **yêu cầu cửa hàng** thực hiện cập nhật (**gửi hành động**).

Cửa hàng sau đó sẽ sử dụng phương thức reducer để tính toán trạng thái mới.

Giả sử chúng ta có hàm `counterReducer` như ở trên, dưới đây là cách tạo một cửa hàng trong Redux:

```jsx
import { createStore } from "redux";

const store = createStore(counterReducer);
```

**Chương trình hoàn chỉnh:**

```jsx
import { createStore } from "redux";

const initialState = {
    value: 0
};

const counterReducer = (state = initialState, action = {}) => {
  if (action.type === "counter/increment") {
    return {
        value: state.value + 1 // important: do NOT mutate the state.
    };
  }

  return state; // return the state as is (in all other cases)
};

const store = createStore(counterReducer);
```

### 3. Thực hiện dispatch một action
[:arrow_up: Mục lục](#mục-lục)

Chúng ta **không được phép thay đổi trạng thái** được lưu trữ trong cửa hàng bằng cách **thủ công**. Thay vào đó, chúng ta phải **yêu cầu** cửa hàng **thực hiện thay đổi** bằng cách gửi một **hành động**.

Chúng ta đã học rằng các hành động là các đối tượng với cấu trúc sau:

```jsx
{
    type: "counter/increment", // example of an action
}
```

Để gửi hành động, bạn phải sử dụng hàm `store.dispatch(action)`:

```jsx
store.dispatch({type: "counter/increment"});
// another example
store.dispatch({type: "counter/reset"});
```

Gọi phương thức `store.dispatch()` sẽ **yêu cầu** cửa hàng gọi reducer để tính toán trạng thái mới. Nếu trạng thái **đã thay đổi**, giao diện người dùng sẽ được kích hoạt để **cập nhật**

**Gửi hành động khi nhấp chuột**

Bạn có thể **gửi hành động ở bất kỳ đâu** trong code. Một trường hợp sử dụng phổ biến là gửi hành động khi nhấp chuột vào nút. Đây là điều mà chúng ta đã làm trong ứng dụng đếm:

```jsx
const addButton = document.querySelector("#add-button");

addButton.addEventListener("click", () => {
    store.dispatch({ type: "counter/increment" });
});
```

_Ví dụ:_ Chương trình hoàn chỉnh

```jsx
import { createStore } from "redux";

const initialState = { value: 0 };

const counterReducer = (state = initialState, action) => {
    if (action.type === "counter/increment") {
        return {
            value: state.value + 1 // important: do NOT mutate the state.
        };
    }

    return state; // return the state as is (in all other cases)
};

const store = createStore(counterReducer);

const addButton = document.querySelector("#add-button");

addButton.addEventListener("click", () => {
    store.dispatch({ type: "counter/increment" });
});
```

## XI. Redux Toolkit
[:arrow_up: Mục lục](#mục-lục)

Mặc dù tên gói redux là `redux` nhưng tên gói Redux Toolkit là `@reduxjs/toolkit`.

**Tính bất biến với immer**

**immer** là một thư viện JavaScript cho phép bạn **cập nhật trạng thái theo cách bất biến** trong khi vẫn viết code JavaScript theo cách truyền thống.

Điều này làm cho cú pháp trở nên đơn giản hơn khi làm việc với các cấu trúc dữ liệu phức tạp như đối tượng, mảng và mảng đối tượng.

### 1. Slices
[:arrow_up: Mục lục](#mục-lục)

Khi bạn cấu hình một Redux store mới, đôi khi quá trình này có thể hơi phức tạp, đặc biệt khi store mở rộng để chứa nhiều hơn một loại hành động. Tuy nhiên, việc xử lý thêm các hành động cho app có thể làm cho quá trình trở nên phức tạp hơn. Đó là lý do tại sao Redux Toolkit giới thiệu khái niệm `slice`.

Redux Slice là một tập hợp **các reducer và hành động** liên quan đến một tính năng cụ thể của ứng dụng.

_Ví dụ:_ Chúng ta có slice `counter` và sau đó là slice `app`. Hai slice này sẽ được cấu hình riêng biệt nhưng được cung cấp cho cùng một store.

Hãy xem cách tạo một slice và cấu hình store trong Redux Toolkit:

```jsx
import { createSlice } from "@reduxjs/toolkit";

const counterSlice = createSlice({
  name: "counter",
  initialState: {
    value: 0,
  },
  reducers: {
    increment: (state) => {
      // TODO: write reducer code here
    }
  },
});
```

Chúng ta đã thêm hàm `createSlice` từ `@reduxjs/toolkit` và sau đó gọi hàm này và cung cấp `name`, `initialState` và `reducers`.

Chúng ta không cần thêm tiền tố `counter/` cho reducer như đã làm trước đây (ví dụ: `counter/increment`, `counter/decrement`, vv). Điều này bởi vì `slice` này chỉ cung cấp các hành động liên quan đến `counter` mà ta đã cung cấp trong `name`.

- **Viết reducer (và sử dụng immer)**

Trong đoạn code trên, chúng ta đã tạo một hàm reducer gọi là `increment`. Trong hàm reducer này, chúng ta được phép viết code như thể ta đang thay đổi trạng thái trực tiếp. Điều này bởi vì Redux Toolkit đã tải **immer**. Trong đoạn code trên, dù có vẻ như chúng ta đang thay đổi trực tiếp trạng thái, thực tế là code này đang **chạy theo cách bất biến**

**Immer** tạo ra một **phiên bản tạm thời** của **trạng thái hiện tại từ các thay đổi** và sau đó **tạo ra một trạng thái bất biến** hoàn toàn mới **dựa trên những thay đổi** đó.

Vì vậy, code reducer `increment` sẽ trông như sau:

```jsx
// ...
  reducers: {
    increment: (state) => {
      // While this looks like it's mutating the state, immer creates a draft state and then produces immutable state changes
      state.value += 1;
    }
  },
  // ...
```

- **Cấu hình store**

Để tạo `store`, bạn phải thêm hàm `configureStore` và truyền reducer cho hàm:

```jsx
import { configureStore, createSlice } from "@reduxjs/toolkit";

const counterSlice = createSlice({
  name: "counter",
  initialState: {
    value: 0,
  },
  reducers: {
    increment: (state) => {
      // While this looks like it's mutating the state, immer creates a draft state and then produces immutable state changes
      state.value += 1;
    },
  },
});

const store = configureStore({
  reducer: counterSlice.reducer,
});
```

Để ý chúng ta đã truyền `counterSlice.reducer` (không phải `reducers`). Nó khác với `reducers` mà bạn đã định nghĩa trong hàm `createSlice()`.

### 2. Actions & payloads
[:arrow_up: Mục lục](#mục-lục)

- **Hành động (Action)**

Trước đây với `redux`, chúng ta gửi một hành động bằng cách sử dụng code sau:

```jsx
store.dispatch({type: "counter/increment"});
```

Với Redux Toolkit, chúng ta nhận được một hàm mà chúng ta có thể trích xuất từ `slice.actions`. Sau đó, chúng ta có thể sử dụng hàm này kết hợp với `store.dispatch()`. Hãy cùng xem cách thức hoạt động.

Chúng ta bắt đầu với đoạn code trong bài học trước và mở rộng bằng code `dispatch`:

```jsx
import { configureStore, createSlice } from "@reduxjs/toolkit";

const counterSlice = createSlice({
  name: "counter",
  initialState: {
    value: 0,
  },
  reducers: {
    increment: (state) => {
      // While this looks like it's mutating the state, immer creates a draft state and then produces immutable state changes
      state.value += 1;
    },
  },
});

const store = configureStore({
  reducer: counterSlice.reducer,
});

// extract the increment function from counterSlice.actions
const { increment } = counterSlice.actions;

document.querySelector("#add").addEventListener("click", () => {
  // dispatch an increment() action
  store.dispatch(increment());
});
```

Hàm `increment` có thể được truy cập bên trong `counterSlice.actions`. **Tên** của nó **trùng khớp** với tên của hàm mà ta đã cung cấp trong **reducers** ở trên.

Bạn có thể sử dụng **object destructuring** như trong ví dụ trên hoặc truy cập hàm bằng cách sử dụng `counterSlice.actions.increment`.

Nếu bạn có nhiều hàm (có nhiều reducers trong slice), bạn có thể trích xuất chúng theo cùng một cách:

```jsx
const { increment, decrement } = counterSlice.actions;
```

- **Cung cấp payload**

Cho đến nay, chúng ta chủ yếu làm việc với các hành động không nhận bất kỳ payload nào. Chúng luôn thực hiện cùng một hành động (ví dụ: tăng 1 hoặc giảm 1).

Tuy nhiên, đôi khi, bạn muốn tạo một hành động mà **giá trị** của nó **tăng theo số đơn vị cụ thể** (có thể là 1, 5 hoặc một số khác). Giá trị này được gọi là **payload**.

Mọi reducer đều **nhận một đối số thứ 2** gọi là `action`. Bạn có thể truy cập `action.payload` để có quyền truy cập vào giá trị đã được truyền cho `action` khi nó được gọi. Hãy xem một ví dụ triển khai tính năng `incrementBy(value)`:

```jsx
import { configureStore, createSlice } from "@reduxjs/toolkit";

const counterSlice = createSlice({
  name: "counter",
  initialState: {
    value: 0,
  },
  reducers: {
    incrementBy: (state, action) => {
        console.log(action.payload); // visualize payload
        state.value += action.payload;
    }
  },
});

const store = configureStore({
  reducer: counterSlice.reducer,
});

const { incrementBy } = counterSlice.actions;

document.querySelector("#add").addEventListener("click", () => {
  // the payload is 1
  store.dispatch(incrementBy(1));
});

document.querySelector("#add-five").addEventListener("click", () => {
  // the payload is 5
  store.dispatch(incrementBy(5));
});
```

Chúng ta có thể gọi `incrementBy(1)`, `incrementBy(5)` hoặc bất kỳ giá trị nào khác ở đây. Giá trị này sẽ được nhận dưới dạng `action.payload` mà bạn sau đó có thể sử dụng để cập nhật trạng thái.

### 3. Provider
[:arrow_up: Mục lục](#mục-lục)

Trong ứng dụng React, bạn có thể làm cho `store` có thể được **truy cập bởi bất kỳ component con nào** bằng cách **đóng gói toàn bộ** ứng dụng bằng **component Provider**

Để làm điều đó, bạn cần thêm `Provider` từ `react-redux` (dưới dạng named import) và sau đó đóng gói toàn bộ ứng dụng bằng `Provider`. Giả sử bạn có đoạn code sau:

```jsx
import { createRoot } from 'react-dom/client';
import { store } from './store.js';

render(<App />, document.querySelector('#react-root'));
```

Trong ví dụ này, ta giả định rằng ta đang thêm một `store` (được tạo bằng phương thức `configureStore` của `@reduxjs/toolkit`).

Bây giờ, ta sẽ thêm `Provider` và đóng gói toàn bộ ứng dụng bằng `Provider` và truyền `store` dưới dạng `prop store`:

```jsx
import { createRoot } from 'react-dom/client';
import { store } from './store.js';
import { Provider } from 'react-redux';

const root = document.querySelector('#react-root');

createRoot(root).render(<Provider store={store}>
    <App />
</Provider>);
```

Đừng quên `store={store}`. Nó cho phép chúng ta truyền `store` vào ứng dụng, làm cho `store` có thể được **truy cập bởi tất cả các component con** của **component Provider**.

### 4. Hook - useSelector
[:arrow_up: Mục lục](#mục-lục)

Hook `useSelector` cho phép bạn **trích xuất dữ liệu** từ `store` của redux.

Nó nhận một hàm callback, hàm này nhận toàn bộ `state` làm đối số. Sau đó, bạn có thể quyết định dữ liệu mà bạn muốn lấy. Hãy xem một ví dụ với store được tạo từ `slice` sau:

```jsx
const counterSlice = createSlice({
  name: "counter",
  initialState: {
    value: 0,
  },
  reducers: {
    increment: (state) => {
      state.value += 1;
    },
  },
});
```

Component `<Counter />` sẽ cần hiển thị giá trị của `counter`. Hãy quan sát `initialState`. Đó là một đối tượng có khóa `value` mà chúng ta cần trích xuất.

```jsx
import {useSelector} from "react-redux";

function Counter() {
    const counter = useSelector(state => state.value);

    return <h1>Counter: {counter}</h1>
}
```

Đoạn code trên thêm hook `useSelector` từ gói `react-redux`.

Sau đó, nó sử dụng hook này và truyền hàm callback sau:

```jsx
state => state.value
```

Đây là một hàm mũi tên trích xuất giá trị của `counter` từ `state`.

### 5. Hook - useDispatch
[:arrow_up: Mục lục](#mục-lục)

Hook `useDispatch` **trả về** một **tham chiếu** đến hàm `dispatch` từ `store` của Redux. Khi bạn sử dụng `useDispatch`, bạn có thể **gọi** hàm `dispatch()` để **gửi một hành động** đến `store`.

Hãy xem một ví dụ với store `counter` và hành động `increment` đã được định nghĩa trong `store.js`:

```jsx
import { configureStore, createSlice } from "@reduxjs/toolkit";

const counterSlice = createSlice({
  name: "counter",
  initialState: {
    value: 0,
  },
  reducers: {
    increment: (state) => {
      state.value += 1;
    },
  },
});

const store = configureStore({
  reducer: counterSlice.reducer,
});

const { increment } = counterSlice.actions;

export {store, increment};
```

Dưới đây là cách chúng ta hoàn thiện component `Counter` để component tăng giá trị biến đếm khi nhấp vào nút:

```jsx
import {useDispatch} from "react-redux";
import {increment} from "./store.js";

export default function Counter() {
    const dispatch = useDispatch();

    return <button onClick={() => dispatch(increment())}>Add 1</button>;
}
```

Ta bắt đầu bằng cách thêm hook `useDispatch` từ `react-redux`.

Sau đó, ta sử dụng hook đó để trích xuất hàm dispatch: `const dispatch = useDispatch()`. 

Ta cũng đã thêm hàm (hành động) `increment` từ store.

Cuối cùng, khi người dùng nhấp vào nút, ta gọi `dispatch(increment())`

## 1. error:0308010C:digital envelope routines::unsupported
[:arrow_up: Mục lục](#mục-lục)

```
Error: error:0308010C:digital envelope routines::unsupported
    at new Hash (node:internal/crypto/hash:67:19)
    at Object.createHash (node:crypto:130:10)
    at module.exports (/Users/user/Programming Documents/WebServer/untitled/node_modules/webpack/lib/util/createHash.js:135:53)
    at NormalModule._initBuildHash (/Users/user/Programming Documents/WebServer/untitled/node_modules/webpack/lib/NormalModule.js:417:16)
    at handleParseError (/Users/user/Programming Documents/WebServer/untitled/node_modules/webpack/lib/NormalModule.js:471:10)
    at /Users/user/Programming Documents/WebServer/untitled/node_modules/webpack/lib/NormalModule.js:503:5
    at /Users/user/Programming Documents/WebServer/untitled/node_modules/webpack/lib/NormalModule.js:358:12
    at /Users/user/Programming Documents/WebServer/untitled/node_modules/loader-runner/lib/LoaderRunner.js:373:3
    at iterateNormalLoaders (/Users/user/Programming Documents/WebServer/untitled/node_modules/loader-runner/lib/LoaderRunner.js:214:10)
    at iterateNormalLoaders (/Users/user/Programming Documents/WebServer/untitled/node_modules/loader-runner/lib/LoaderRunner.js:221:10)
/Users/user/Programming Documents/WebServer/untitled/node_modules/react-scripts/scripts/start.js:19
  throw err;
  ^
```

**Khắc phục:**

On Unix-like (Linux, macOS, Git bash, etc.):

```
export NODE_OPTIONS=--openssl-legacy-provider
```

On Windows command prompt:

```
set NODE_OPTIONS=--openssl-legacy-provider
```

On PowerShell:

```
$env:NODE_OPTIONS = "--openssl-legacy-provider"
```

