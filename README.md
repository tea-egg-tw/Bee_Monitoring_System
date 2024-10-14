### ToBeeOrNotToBee

1. 建立虛擬環境 (For window)
    
    ```jsx
    python -m venv venv
    .\venv\Scripts\activate
    ```
    
2. 開啟 mongodb sever
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/da3d35b3-8639-4f83-8fe5-0f8bfaa2c8ee/9146a59c-05ee-4a0a-a1ca-b0af8817c1e5/image.png)
    
3. 安裝依賴包、建立mongodb資料庫
    
    ```jsx
    pip install pandas
    pip install pymongo
    pip install openpyxl
    python .\DBSoundBasicInfo.py
    ```
    
4. 安裝依賴包，確定機器學習預測的程式能運行 (儲存進mongodb的過程被我註解掉了)
    
    ```jsx
    pip install scipy
    pip install librosa
    python .\Beepre_mongo.py
    ```
    
5. 進到kedro
    
    ```jsx
    cd .\audio-classification\
    pip install kedro
    # 在 ToBeeOrNotTobee\audio-classification\conf\base\parameters.yml
    裡面更改knn_model_path 位置 
    #更改完畢以後
    kedro run
    ```
    

### bee_monitoring

1. 先連上網路
2. 開啟建立完成的mongodb
3. 安裝配件、開啟後端
    
    ```jsx
    	cd ../..
    	cd .\bee_monitoring_system\
    	pip install flask
    	pip install flask_cors
    ```
    
4. 開網頁
