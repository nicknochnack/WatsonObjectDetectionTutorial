
## 1. Create an IBM Cloud Account
Head on over to [https://cloud.ibm.com/registration](https://cloud.ibm.com/registration) to create an IBM Cloud Account.  This will allow you to try out all the services and APIs available on the IBM Cloud. 
![enter image description here](https://i.imgur.com/qd5dRP1.png)

Once you've entered your email you'll be prompted to confirm your email address. Head on over and confirm it. 
![enter image description here](https://i.imgur.com/kT9vZul.png)

Login once you're redirected to the IBM Cloud account, you'll be prompted to proceed. Hit Proceed. From here you'll end up at your IBM Dashboard. 

![enter image description here](https://i.imgur.com/c4qtn99.png)

## 2. Create a Watson Studio Service
The next bit of setup involves creating a Watson Studio service. To do this hit Catalog at the top of the screen. 
![enter image description here](https://i.imgur.com/hP81gYd.png)

Hit AI from the menu on the right hand side. Then select Watson Studio. 

![enter image description here](https://i.imgur.com/roDM6NQ.png)
Then hit Create from the right hand side of the screen.
![enter image description here](https://i.imgur.com/PGtjkBh.png)

Awesome! You've now created a Watson Studio environment. Next hit get started to create a Watson Studio Project. 
![enter image description here](https://i.imgur.com/BpCNvJH.png)

## 3. Create a New Project in Watson Studio
First thing’s first, the easiest way to work with the Object Detection API is to create a new project inside of Watson Studio. Start out by selecting Create a project.

![enter image description here](https://i.imgur.com/gxXOcsP.png)

Then select Create an empty project.
![enter image description here](https://i.imgur.com/R1RfZvB.png)

<b>IMPORTANT</b>
Adding Cloud Object Storage: you need to add this so you can upload images.

Select Add, you'll be taken away from your screen so that you can attach some storage.
![enter image description here](https://i.imgur.com/3dn5MdJ.png)

 Choose the Lite Plan then hit Create.
![enter image description here](https://i.imgur.com/9LM3j8d.png)

Then come back into your project and Select Create. 
![enter image description here](https://i.imgur.com/RHxqFAT.png)


Once your project is created select Add to Project and Object Detection model (Beta) to add the Object Detection API into your project.

![](https://lh4.googleusercontent.com/pq7LBxaYiu8dZqO3jUVQhrzxlpDlsMhRS8saLy0ZykuqHc1k9MmJBfzg8DlXSlHEc8wuRw-x5bmxzi2ALQJSfJohjv20gKVJfA2DYIprpCZ4LnAtN2jFN8mIxQnGDrLx6XvfrNlr)

You’ll then be prompted to associate a Vision Recognition service. ![](https://lh4.googleusercontent.com/5kVBTZxdx6ilcLbtY_2iNKsjiODgR2dQAPMpjEKpQzGZ4SREkpd5UY_mifVQz-b8RMfSMSmpEwyytPpqp1uM5s4UIZ2V3qPjYbEtaDM6dHalJPXDfjgJa22KYk_QyAlYigc12YSd)

If you have an existing Vision Recognition service, simply select the service from the list of available services.

![](https://lh4.googleusercontent.com/owrDLRmyxL_q6F7STxnq7-brhYOrRAcglUqysuBOwwO5YGUMAx7jbmyNH7WXtIdJMTPyEWRQyFOvbUjCoYMbcNgwGyFKi-jNcclrsE4G2jsjExfKZQPbPiPWexwIpwemp_8ZzBJC)

If you don’t have a service available, select New from the top of the page and choose an appropriate plan. The Lite Plan is more than sufficient to get up and running with a proof of concept. If you plan on building out a beefier application then take a look at the Standard Plan.

![](https://lh5.googleusercontent.com/QYcLnk6M7t_saczsBLok552BwX5sst27U8rzkEor19XQgs7joxqOaL-B9dXi9VJk1o63FmygH2HUSHfrmj44V-0iGTCo-QL6ME3rX2p3MsM-zRTNiYXsl2cyyxnMzeSMh3nUWSOa)

  

## 4. Load Up Your Images

Alright, that’s the boring stuff out of the way. You can now get to loading and training our model. Once you’ve associated your Vision Recognition service you’ll be redirected to the Collections page where you’re able to load images to train your model on.

Click Browse from the right hand side of the page to start uploading images.

![](https://lh4.googleusercontent.com/QiER6lq02ZpB_rrQUdkLhaQ1FKaJZ5WTsU9H60XDXxjtBOJKkV6pDdLvCcI4ru9R1Lr1q0sPvlzeZM40L_FC4b_CQLKRdQqxP-xrBf_3Aal99fbgQwiXCUyuiE_6EPSG1_2CQwuP)

  

In this case there’s a bunch of space shuttle images that will be used to train the model. These images are available from the GitHub repository inside the folder called IMAGES. Choose whichever images you’d like to use to build your own model.

![enter image description here](https://i.imgur.com/JmeOg7v.png)
Once you’ve selected the images to upload, they’ll start processing and eventually will be loaded into the project.

![](https://lh5.googleusercontent.com/yTVh-uhiQtoR7WsGMczLKsymmRwCdvr8SJgXkbJVgi-r6U49llcOFgx5eyMNVKETQC7ZRrqIj1XWyppP1qb_TXdaa_etuRbRRl341FncDdOn5ToBOndL-Aprhbo_FcS4smmF8DQI)

Once that’s done, you can start labelling your images!

## 5. Label Your Objects

The next part of this journey requires you to label the objects within your images. This is actually pretty straight forward inside of Watson Studio. All you have to do is select the image and drag a square around the object you’re trying to train on.

To add images to your training data, select the checkbox next to each image you’d like to use as part of the training set then select Add to Model.


![](https://lh4.googleusercontent.com/OIx3tSXv5EM7VrPEixHQh0ig0ZPYYyz7syj72JsTnRtCHNcetnU-fvzp0OAFqvTf0gh5Ikm05ZAqiQCMovn8HIOEH6cuI90aMKBCgTszNWr1DfsMFXjESpQ-VWRydsANcGR2OBrF)

This will load the images into the collection in preparation for training.
![enter image description here](https://i.imgur.com/pllX8nQ.png)

Once the image is loaded into the collection you’re able to start labelling it. Click into the image, then select Add new object.
![enter image description here](https://i.imgur.com/azMu0Jr.png)


You’ll then be able to draw squares (aka labels) over the objects within the image. Once you’ve selected Add new object all you have to do is draw a square over the object you’re labelling.  In this case label the External Tank (Orange thing), the Boosters (white things next to the orange thing) and the Shuttle (the big white thing sitting on top of the others). 

![enter image description here](https://i.imgur.com/x3GnkQI.png)

Once this has been done, write the name of the object you’re labelling. And hit Add. Repeat the same process for the other parts of the image. Once you’ve labelled all objects required. Select Done in the top right of the image labelled area.

![enter image description here](https://i.imgur.com/cZZifJ3.png)

To label the next set of images just hit the left and right arrows next to the current image to start labelling process again on the next image.

![enter image description here](https://i.imgur.com/fZSwImj.png)

Anddd….you can label this image too!

![enter image description here](https://i.imgur.com/zK0aBFa.png)
Once you’ve labelled all your images, select View all images to see the results of your labelling process.

![](https://lh4.googleusercontent.com/k5_VEHr3f1M1cy-l3jWOgNJJeQZGVA0iOACKYjq25ndmrTTnU80xerAGkCej6t1KYZF50BwEHgLuqGMhZ31uZi_qWsQzsyUxiS_l2Byd8WoFIdH5aFz9jAbsAlrGaLbyNIDfnyOU)

At this stage the deep learning model hasn’t been trained yet. To kick off this process select Train Model in the top right hand corner. This will commence the training process for your visual recognition model.

![enter image description here](https://i.imgur.com/oiY1mjm.png)

Once the training has finished, you’ll be able to test out your model with new images and view the results!

## 6. Testing Your Model

Now that you’ve labelled your images and trained the model you can then start the fun bit and commence testing your model. As soon as the model has finished training you’ll be redirected to an overview.

From here you can test out the model by selecting Test from the menu bar.

![enter image description here](https://i.imgur.com/YfJWSDV.png)

 
Then upload an image to test out your model.

![enter image description here](https://i.imgur.com/1iegCgw.png)

The results of the detection will be visible once each image has been processed.

![enter image description here](https://i.imgur.com/QhYd5ft.png)