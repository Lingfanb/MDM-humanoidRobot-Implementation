# Vision 1
```
Editted by Lingfan Bao

Edit date: Jan/05/2025

Update:
1. common linux shell operation comments
```

## update ur code to the github
Push ur code to the Github
```shell
git add .
git commit -m "你的修改信息"
git push
```

## Remove autogenerate file
This is to delete the model or file you do not need

```shell
rm -r save/"your file name"
```

## Processing the trained model
For the already trained model, 

1. We need to try it through generate.py
2. Move it outside the folder
3. Upload to onedrive
4. Delete the model from the file 

```shell
mv MDM-humanoidRobot-Implementation/dataset/{HumanAct12Poses,HumanML3D,KIT-ML,uestc} dataset
mv dataset/{HumanAct12Poses,HumanML3D,KIT-ML,uestc} MDM-humanoidRobot-Implementation/dataset/
```

Move ur model to outside the folder and storage the model to the cloud
```shell
mv MDM-humanoidRobot-Implementation/save/humanml_trans_enc_512 model_storage
mv model_storage/humanml_trans_enc_512 MDM-humanoidRobot-Implementation/save/ 
rclone copy model_storage onedrive:/Documents/model_storage --progress
```