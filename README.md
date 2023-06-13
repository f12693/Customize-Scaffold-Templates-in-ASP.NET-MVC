# Customize-Scaffold-Templates-in-ASP.NET-MVC
(筆者當初是裝Visual Studio 17.5.3版本，目前還未測試其他版本是否可行)
1. 如果當初在安裝Visual Studio時，沒有更改安裝路徑
那麼就去以下路徑：  
C:\Program Files\Microsoft Visual Studio\2022\Community\Common7\IDE\Extensions\Microsoft\Web\Mvc\Scaffolding
![image](https://github.com/f12693/Customize-Scaffold-Templates-in-ASP.NET-MVC/assets/121540001/fdc90d64-8dc4-4cd4-bfc1-e43bdc8235db)
2. 複製 Templates 資料夾到桌面(或者任何你想暫時存放的地方)  
![image](https://github.com/f12693/Customize-Scaffold-Templates-in-ASP.NET-MVC/assets/121540001/ff3998f6-0efc-46b4-8baa-0d4d35c41689)
3. 將其改名為 CodeTemplates  
![image](https://github.com/f12693/Customize-Scaffold-Templates-in-ASP.NET-MVC/assets/121540001/ab84327f-dff0-413c-9b03-4e788bc8c7a1)
4. 打開 CodeTemplates\MvcView 裡面的 Create.cs.t4 做一些修改  
筆者是用了Visual Studio Code來開啟(可以顯示行數)  
 81行 form-horizontal改成row  
105行 form-group改成mb-3  
109行 control-label col-md-2改成form-label  
113行 control-label col-md-2改成form-label  
117行 &lt;div class="col-md-10">刪掉(留行,不要讓下面的程式碼上移,免得後續行數有誤)  
177行 &lt;/div>刪掉  
184行 form-group改成mb-3  
185行 &lt;div class="col-md-offset-2 col-md-10">刪掉  
186行 btn-default改成btn-primary  
187行 &lt;/div>刪掉  
整個刪完，根據需求，再做縮排  

4. 開啟想要改變模板的專案->專案上右鍵->在檔案總管中開啟資料夾  
![1](https://github.com/f12693/Customize-Scaffold-Templates-in-ASP.NET-MVC/assets/121540001/a632aaa7-2bd1-457d-ae24-93c7c975549b)
5. 整個CodeTemplates資料夾丟到專案資料夾裡面  
6. 方案總管上方工具列點選"顯示所有檔案"  
![2](https://github.com/f12693/Customize-Scaffold-Templates-in-ASP.NET-MVC/assets/121540001/f451d2f8-2e14-43aa-9ab0-c67263cacbaa)
7. 在CodeTemplates上右鍵"加入至專案"  
![image](https://github.com/f12693/Customize-Scaffold-Templates-in-ASP.NET-MVC/assets/121540001/ead5ca58-2206-4dac-b4cd-2daf61e4646b)
8. 完成！  
此時再去xxxController.cs裡  
在要新增檢視的action中  
右鍵->新增檢視 -> MVC 5 檢視 -> 範本選擇"Create"就有囉~
