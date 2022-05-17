(base) PS C:\Users\nakas> conda test5

CommandNotFoundError: No command 'conda test5'.

(base) PS C:\Users\nakas> conda activate test5
(test5) PS C:\Users\nakas>
(test5) PS C:\Users\nakas>
(test5) PS C:\Users\nakas>
(test5) PS C:\Users\nakas>
(test5) PS C:\Users\nakas> cd ../..
(test5) PS C:\> ls


    ディレクトリ: C:\


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        2022/05/07     22:39                CMakeFiles
d-----        2022/04/26      7:23                cygwin64
d-----        2022/05/07     21:53                Git
d-----        2022/03/10     20:57                Intel
d-----        2022/05/07     22:27                Microsoft
d-----        2022/05/07     12:52                MinGW
d-----        2021/06/05     21:10                PerfLogs
d-r---        2022/05/07     22:26                Program Files
d-r---        2022/05/07     22:24                Program Files (x86)
d-----        2022/05/12     22:31                SWSetup
d-----        2022/05/11     18:01                Windows


(test5) PS C:\> cd Git
(test5) PS C:\Git>
(test5) PS C:\Git>
(test5) PS C:\Git>
(test5) PS C:\Git> ld
C:\MinGW\bin\ld.exe: no input files
(test5) PS C:\Git>
(test5) PS C:\Git> ;d
d : 用語 'd' は、コマンドレット、関数、スクリプト ファイル、または操作可能なプログラムの名前として認識されません。名前
が正しく記述されていることを確認し、パスが含まれている場合はそのパスが正しいことを確認してから、再試行してください。
発生場所 行:1 文字:2
+ ;d
+  ~
    + CategoryInfo          : ObjectNotFound: (d:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException

(test5) PS C:\Git> ls


    ディレクトリ: C:\Git


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        2022/04/26      6:50                frustum-pointnets
d-----        2022/05/11      5:26                frustum-pointnets-pytorch
d-----        2022/05/11      6:25                MachineLearning
d-----        2022/05/07     22:01                vtk


(test5) PS C:\Git>
(test5) PS C:\Git>
(test5) PS C:\Git> ls


    ディレクトリ: C:\Git


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        2022/04/26      6:50                frustum-pointnets
d-----        2022/05/11      5:26                frustum-pointnets-pytorch
d-----        2022/05/11      6:25                MachineLearning
d-----        2022/05/07     22:01                vtk


(test5) PS C:\Git>
(test5) PS C:\Git>
(test5) PS C:\Git>
(test5) PS C:\Git> cd .\frustum-pointnets-pytorch\
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch> ls


    ディレクトリ: C:\Git\frustum-pointnets-pytorch


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        2022/04/27      1:34                .ipynb_checkpoints
d-----        2022/04/27      1:04                cfgs
d-----        2022/05/11      5:20                configs
d-----        2022/05/07     13:23                dataset
d-----        2022/04/27      1:04                doc
d-----        2022/05/07     21:53                kitti
d-----        2022/05/12      8:02                log
d-----        2022/05/08     23:07                mayavi
d-----        2022/05/08      0:11                models
d-----        2022/04/27      1:04                nuscenes
d-----        2022/04/27      1:04                nuscenes2kitti
d-----        2022/04/27      1:04                ops
d-----        2022/05/11     22:24                runs
d-----        2022/05/08      0:15                train
-a----        2022/04/27      1:04           7857 README.md
-a----        2022/04/27      1:34             72 Untitled.ipynb


(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch> python train/train_fpointnets.py --log_dir log
pid: 23092
Your FLAGS:
Namespace(batch_size=32, ckpt=None, dataset='kitti', debug=False, decay_rate=0.7, decay_step=20, learning_rate=0.001, log_dir='log', max_epoch=150, model='frustum_pointnets_v1_old', momentum=0.9, name='default', no_intensity=False, num_point=1024, objtype='caronly', optimizer='adam', restore_model_path=None, return_all_loss=False, sensor='CAM_FRONT', train_sets='train', val_sets='val', weight_decay=0.0)
**** EPOCH 001 ****
Epoch 1/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:44<00:00,  6.50it/s]
[1: 1849/1850] train loss: 0.438186
segmentation accuracy: 0.815605
box IoU(ground/3D): 0.544721/0.484656
box estimation accuracy (IoU=0.7): 0.213361
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.96it/s]
[1] test loss: 0.272573
test segmentation accuracy: 0.821079
test box IoU(ground/3D): 0.602224/0.550743
test box estimation accuracy (IoU=0.7): 0.325251
learning rate: 0.001000
Best Test acc: 0.325251(Epoch 1)
**** EPOCH 002 ****
Epoch 2/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:26<00:00,  6.94it/s]
[2: 1849/1850] train loss: 0.265257
segmentation accuracy: 0.864547
box IoU(ground/3D): 0.639100/0.580228
box estimation accuracy (IoU=0.7): 0.364949
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.00it/s]
[2] test loss: 0.219399
test segmentation accuracy: 0.868115
test box IoU(ground/3D): 0.678338/0.610921
test box estimation accuracy (IoU=0.7): 0.429016
learning rate: 0.001000
Best Test acc: 0.429016(Epoch 2)
**** EPOCH 003 ****
Epoch 3/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.05it/s]
[3: 1849/1850] train loss: 0.215389
segmentation accuracy: 0.876394
box IoU(ground/3D): 0.665403/0.605965
box estimation accuracy (IoU=0.7): 0.420642
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[3] test loss: 0.181617
test segmentation accuracy: 0.864114
test box IoU(ground/3D): 0.724104/0.660468
test box estimation accuracy (IoU=0.7): 0.586776
learning rate: 0.001000
Best Test acc: 0.586776(Epoch 3)
**** EPOCH 004 ****
Epoch 4/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.01it/s]
[4: 1849/1850] train loss: 0.192500
segmentation accuracy: 0.883926
box IoU(ground/3D): 0.686007/0.627142
box estimation accuracy (IoU=0.7): 0.478074
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.16it/s]
[4] test loss: 0.251521
test segmentation accuracy: 0.841607
test box IoU(ground/3D): 0.624277/0.574539
test box estimation accuracy (IoU=0.7): 0.398070
learning rate: 0.001000
Best Test acc: 0.586776(Epoch 3)
**** EPOCH 005 ****
Epoch 5/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.06it/s]
[5: 1849/1850] train loss: 0.176717
segmentation accuracy: 0.889874
box IoU(ground/3D): 0.701749/0.643379
box estimation accuracy (IoU=0.7): 0.522939
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.04it/s]
[5] test loss: 0.160132
test segmentation accuracy: 0.879502
test box IoU(ground/3D): 0.723864/0.671132
test box estimation accuracy (IoU=0.7): 0.598261
learning rate: 0.001000
Best Test acc: 0.598261(Epoch 5)
**** EPOCH 006 ****
Epoch 6/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.01it/s]
[6: 1849/1850] train loss: 0.165020
segmentation accuracy: 0.893917
box IoU(ground/3D): 0.712903/0.654153
box estimation accuracy (IoU=0.7): 0.553784
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.01it/s]
[6] test loss: 0.150965
test segmentation accuracy: 0.874348
test box IoU(ground/3D): 0.719525/0.665031
test box estimation accuracy (IoU=0.7): 0.583347
learning rate: 0.001000
Best Test acc: 0.598261(Epoch 5)
**** EPOCH 007 ****
Epoch 7/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.05it/s]
[7: 1849/1850] train loss: 0.159986
segmentation accuracy: 0.897763
box IoU(ground/3D): 0.720938/0.662245
box estimation accuracy (IoU=0.7): 0.573547
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.90it/s]
[7] test loss: 0.145704
test segmentation accuracy: 0.884650
test box IoU(ground/3D): 0.731742/0.679033
test box estimation accuracy (IoU=0.7): 0.619557
learning rate: 0.001000
Best Test acc: 0.619557(Epoch 7)
**** EPOCH 008 ****
Epoch 8/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.05it/s]
[8: 1849/1850] train loss: 0.144537
segmentation accuracy: 0.901042
box IoU(ground/3D): 0.729752/0.670654
box estimation accuracy (IoU=0.7): 0.594476
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.93it/s]
[8] test loss: 0.149807
test segmentation accuracy: 0.889953
test box IoU(ground/3D): 0.736361/0.680409
test box estimation accuracy (IoU=0.7): 0.607912
learning rate: 0.001000
Best Test acc: 0.619557(Epoch 7)
**** EPOCH 009 ****
Epoch 9/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.03it/s]
[9: 1849/1850] train loss: 0.142251
segmentation accuracy: 0.904084
box IoU(ground/3D): 0.736765/0.677663
box estimation accuracy (IoU=0.7): 0.611706
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.02it/s]
[9] test loss: 0.134024
test segmentation accuracy: 0.892693
test box IoU(ground/3D): 0.745689/0.687770
test box estimation accuracy (IoU=0.7): 0.636465
learning rate: 0.001000
Best Test acc: 0.636465(Epoch 9)
**** EPOCH 010 ****
Epoch 10/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.02it/s]
[10: 1849/1850] train loss: 0.133034
segmentation accuracy: 0.906529
box IoU(ground/3D): 0.742549/0.683634
box estimation accuracy (IoU=0.7): 0.629882
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.97it/s]
[10] test loss: 0.124290
test segmentation accuracy: 0.881541
test box IoU(ground/3D): 0.756796/0.696191
test box estimation accuracy (IoU=0.7): 0.662626
learning rate: 0.001000
Best Test acc: 0.662626(Epoch 10)
**** EPOCH 011 ****
Epoch 11/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:27<00:00,  6.91it/s]
[11: 1849/1850] train loss: 0.130005
segmentation accuracy: 0.908570
box IoU(ground/3D): 0.747431/0.688333
box estimation accuracy (IoU=0.7): 0.640574
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.99it/s]
[11] test loss: 0.149325
test segmentation accuracy: 0.892189
test box IoU(ground/3D): 0.757202/0.702448
test box estimation accuracy (IoU=0.7): 0.669963
learning rate: 0.001000
Best Test acc: 0.669963(Epoch 11)
**** EPOCH 012 ****
Epoch 12/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:24<00:00,  7.00it/s]
[12: 1849/1850] train loss: 0.124353
segmentation accuracy: 0.910672
box IoU(ground/3D): 0.753422/0.694184
box estimation accuracy (IoU=0.7): 0.655861
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.95it/s]
[12] test loss: 0.118848
test segmentation accuracy: 0.896837
test box IoU(ground/3D): 0.759994/0.696535
test box estimation accuracy (IoU=0.7): 0.644361
learning rate: 0.001000
Best Test acc: 0.669963(Epoch 11)
**** EPOCH 013 ****
Epoch 13/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:26<00:00,  6.94it/s]
[13: 1849/1850] train loss: 0.119111
segmentation accuracy: 0.912588
box IoU(ground/3D): 0.758062/0.699062
box estimation accuracy (IoU=0.7): 0.671470
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.03it/s]
[13] test loss: 0.121280
test segmentation accuracy: 0.893140
test box IoU(ground/3D): 0.756103/0.704850
test box estimation accuracy (IoU=0.7): 0.687111
learning rate: 0.001000
Best Test acc: 0.687111(Epoch 13)
**** EPOCH 014 ****
Epoch 14/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.03it/s]
[14: 1849/1850] train loss: 0.116009
segmentation accuracy: 0.913836
box IoU(ground/3D): 0.760645/0.701926
box estimation accuracy (IoU=0.7): 0.676723
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [01:11<00:00,  5.50it/s]
[14] test loss: 0.122377
test segmentation accuracy: 0.894577
test box IoU(ground/3D): 0.759540/0.697552
test box estimation accuracy (IoU=0.7): 0.653852
learning rate: 0.001000
Best Test acc: 0.687111(Epoch 13)
**** EPOCH 015 ****
Epoch 15/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:38<00:00,  6.63it/s]
[15: 1849/1850] train loss: 0.109457
segmentation accuracy: 0.915448
box IoU(ground/3D): 0.764482/0.705696
box estimation accuracy (IoU=0.7): 0.685169
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.93it/s]
[15] test loss: 0.128944
test segmentation accuracy: 0.894402
test box IoU(ground/3D): 0.763821/0.707200
test box estimation accuracy (IoU=0.7): 0.681688
learning rate: 0.001000
Best Test acc: 0.687111(Epoch 13)
**** EPOCH 016 ****
Epoch 16/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:25<00:00,  6.98it/s]
[16: 1849/1850] train loss: 0.109330
segmentation accuracy: 0.916513
box IoU(ground/3D): 0.767296/0.708500
box estimation accuracy (IoU=0.7): 0.694764
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[16] test loss: 0.124413
test segmentation accuracy: 0.892237
test box IoU(ground/3D): 0.765933/0.713952
test box estimation accuracy (IoU=0.7): 0.709443
learning rate: 0.001000
Best Test acc: 0.709443(Epoch 16)
**** EPOCH 017 ****
Epoch 17/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:32<00:00,  6.78it/s]
[17: 1849/1850] train loss: 0.108211
segmentation accuracy: 0.918164
box IoU(ground/3D): 0.770731/0.711615
box estimation accuracy (IoU=0.7): 0.697432
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.91it/s]
[17] test loss: 0.117086
test segmentation accuracy: 0.895516
test box IoU(ground/3D): 0.754303/0.696245
test box estimation accuracy (IoU=0.7): 0.643404
learning rate: 0.001000
Best Test acc: 0.709443(Epoch 16)
**** EPOCH 018 ****
Epoch 18/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:24<00:00,  6.99it/s]
[18: 1849/1850] train loss: 0.105471
segmentation accuracy: 0.919225
box IoU(ground/3D): 0.772147/0.712964
box estimation accuracy (IoU=0.7): 0.701706
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.86it/s]
[18] test loss: 0.141783
test segmentation accuracy: 0.893383
test box IoU(ground/3D): 0.761308/0.706895
test box estimation accuracy (IoU=0.7): 0.690301
learning rate: 0.001000
Best Test acc: 0.709443(Epoch 16)
**** EPOCH 019 ****
Epoch 19/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.04it/s]
[19: 1849/1850] train loss: 0.101918
segmentation accuracy: 0.920155
box IoU(ground/3D): 0.773232/0.714496
box estimation accuracy (IoU=0.7): 0.706588
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.91it/s]
[19] test loss: 0.123721
test segmentation accuracy: 0.892962
test box IoU(ground/3D): 0.764065/0.706130
test box estimation accuracy (IoU=0.7): 0.692854
learning rate: 0.001000
Best Test acc: 0.709443(Epoch 16)
**** EPOCH 020 ****
Epoch 20/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.06it/s]
[20: 1849/1850] train loss: 0.103074
segmentation accuracy: 0.921684
box IoU(ground/3D): 0.776368/0.717873
box estimation accuracy (IoU=0.7): 0.714341
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[20] test loss: 0.131791
test segmentation accuracy: 0.890180
test box IoU(ground/3D): 0.769071/0.714281
test box estimation accuracy (IoU=0.7): 0.702584
learning rate: 0.001000
Best Test acc: 0.709443(Epoch 16)
**** EPOCH 021 ****
Epoch 21/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:33<00:00,  6.75it/s]
[21: 1849/1850] train loss: 0.088468
segmentation accuracy: 0.925788
box IoU(ground/3D): 0.787531/0.728987
box estimation accuracy (IoU=0.7): 0.737956
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.81it/s]
[21] test loss: 0.105150
test segmentation accuracy: 0.900536
test box IoU(ground/3D): 0.771396/0.716686
test box estimation accuracy (IoU=0.7): 0.706572
learning rate: 0.000700
Best Test acc: 0.709443(Epoch 16)
**** EPOCH 022 ****
Epoch 22/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:25<00:00,  6.97it/s]
[22: 1849/1850] train loss: 0.090817
segmentation accuracy: 0.926735
box IoU(ground/3D): 0.788591/0.730246
box estimation accuracy (IoU=0.7): 0.743260
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.94it/s]
[22] test loss: 0.113841
test segmentation accuracy: 0.901310
test box IoU(ground/3D): 0.760182/0.707730
test box estimation accuracy (IoU=0.7): 0.674350
learning rate: 0.000700
Best Test acc: 0.709443(Epoch 16)
**** EPOCH 023 ****
Epoch 23/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:24<00:00,  7.00it/s]
[23: 1849/1850] train loss: 0.088860
segmentation accuracy: 0.927640
box IoU(ground/3D): 0.790308/0.731992
box estimation accuracy (IoU=0.7): 0.746368
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[23] test loss: 0.123028
test segmentation accuracy: 0.896997
test box IoU(ground/3D): 0.780331/0.727298
test box estimation accuracy (IoU=0.7): 0.736003
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 024 ****
Epoch 24/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.02it/s]
[24: 1849/1850] train loss: 0.087842
segmentation accuracy: 0.929052
box IoU(ground/3D): 0.793245/0.735000
box estimation accuracy (IoU=0.7): 0.754848
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.87it/s]
[24] test loss: 0.111044
test segmentation accuracy: 0.899694
test box IoU(ground/3D): 0.766496/0.713032
test box estimation accuracy (IoU=0.7): 0.690860
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 025 ****
Epoch 25/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.01it/s]
[25: 1849/1850] train loss: 0.084356
segmentation accuracy: 0.929323
box IoU(ground/3D): 0.793498/0.735528
box estimation accuracy (IoU=0.7): 0.754848
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.84it/s]
[25] test loss: 0.112850
test segmentation accuracy: 0.895889
test box IoU(ground/3D): 0.781392/0.726744
test box estimation accuracy (IoU=0.7): 0.725953
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 026 ****
Epoch 26/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:24<00:00,  7.00it/s]
[26: 1849/1850] train loss: 0.084289
segmentation accuracy: 0.930571
box IoU(ground/3D): 0.795431/0.737719
box estimation accuracy (IoU=0.7): 0.761774
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.93it/s]
[26] test loss: 0.122078
test segmentation accuracy: 0.896603
test box IoU(ground/3D): 0.778656/0.723468
test box estimation accuracy (IoU=0.7): 0.717658
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 027 ****
Epoch 27/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.02it/s]
[27: 1849/1850] train loss: 0.083514
segmentation accuracy: 0.930807
box IoU(ground/3D): 0.796264/0.738166
box estimation accuracy (IoU=0.7): 0.761503
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.95it/s]
[27] test loss: 0.113604
test segmentation accuracy: 0.898700
test box IoU(ground/3D): 0.783281/0.729018
test box estimation accuracy (IoU=0.7): 0.731297
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 028 ****
Epoch 28/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.02it/s]
[28: 1849/1850] train loss: 0.080966
segmentation accuracy: 0.931554
box IoU(ground/3D): 0.796745/0.738972
box estimation accuracy (IoU=0.7): 0.764240
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.87it/s]
[28] test loss: 0.114779
test segmentation accuracy: 0.900098
test box IoU(ground/3D): 0.780844/0.727963
test box estimation accuracy (IoU=0.7): 0.732493
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 029 ****
Epoch 29/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.02it/s]
[29: 1849/1850] train loss: 0.082864
segmentation accuracy: 0.932392
box IoU(ground/3D): 0.798236/0.740690
box estimation accuracy (IoU=0.7): 0.766622
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.85it/s]
[29] test loss: 0.118837
test segmentation accuracy: 0.897759
test box IoU(ground/3D): 0.774994/0.721791
test box estimation accuracy (IoU=0.7): 0.713989
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 030 ****
Epoch 30/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:24<00:00,  6.99it/s]
[30: 1849/1850] train loss: 0.079958
segmentation accuracy: 0.933218
box IoU(ground/3D): 0.799170/0.741289
box estimation accuracy (IoU=0.7): 0.770963
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.92it/s]
[30] test loss: 0.110533
test segmentation accuracy: 0.899341
test box IoU(ground/3D): 0.782017/0.729373
test box estimation accuracy (IoU=0.7): 0.730818
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 031 ****
Epoch 31/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:28<00:00,  6.89it/s]
[31: 1849/1850] train loss: 0.079282
segmentation accuracy: 0.933688
box IoU(ground/3D): 0.800123/0.742368
box estimation accuracy (IoU=0.7): 0.772703
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.88it/s]
[31] test loss: 0.104294
test segmentation accuracy: 0.900424
test box IoU(ground/3D): 0.780179/0.725564
test box estimation accuracy (IoU=0.7): 0.725475
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 032 ****
Epoch 32/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:33<00:00,  6.76it/s]
[32: 1849/1850] train loss: 0.082608
segmentation accuracy: 0.934089
box IoU(ground/3D): 0.801027/0.742986
box estimation accuracy (IoU=0.7): 0.774307
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.94it/s]
[32] test loss: 0.122391
test segmentation accuracy: 0.899048
test box IoU(ground/3D): 0.764013/0.707090
test box estimation accuracy (IoU=0.7): 0.697878
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 033 ****
Epoch 33/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:29<00:00,  6.88it/s]
[33: 1849/1850] train loss: 0.080015
segmentation accuracy: 0.934970
box IoU(ground/3D): 0.801568/0.743930
box estimation accuracy (IoU=0.7): 0.774527
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.94it/s]
[33] test loss: 0.103288
test segmentation accuracy: 0.898760
test box IoU(ground/3D): 0.779809/0.723827
test box estimation accuracy (IoU=0.7): 0.721726
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 034 ****
Epoch 34/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.02it/s]
[34: 1849/1850] train loss: 0.083351
segmentation accuracy: 0.935227
box IoU(ground/3D): 0.801994/0.744153
box estimation accuracy (IoU=0.7): 0.777331
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.97it/s]
[34] test loss: 0.119473
test segmentation accuracy: 0.896680
test box IoU(ground/3D): 0.774898/0.720336
test box estimation accuracy (IoU=0.7): 0.715585
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 035 ****
Epoch 35/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:24<00:00,  6.98it/s]
[35: 1849/1850] train loss: 0.080967
segmentation accuracy: 0.935634
box IoU(ground/3D): 0.803266/0.745633
box estimation accuracy (IoU=0.7): 0.780608
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.99it/s]
[35] test loss: 0.102529
test segmentation accuracy: 0.897632
test box IoU(ground/3D): 0.780583/0.728673
test box estimation accuracy (IoU=0.7): 0.734487
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 036 ****
Epoch 36/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:25<00:00,  6.97it/s]
[36: 1849/1850] train loss: 0.081377
segmentation accuracy: 0.935817
box IoU(ground/3D): 0.803902/0.745842
box estimation accuracy (IoU=0.7): 0.780051
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.03it/s]
[36] test loss: 0.102632
test segmentation accuracy: 0.900640
test box IoU(ground/3D): 0.780265/0.727354
test box estimation accuracy (IoU=0.7): 0.724836
learning rate: 0.000700
Best Test acc: 0.736003(Epoch 23)
**** EPOCH 037 ****
Epoch 37/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:34<00:00,  6.74it/s]
[37: 1849/1850] train loss: 0.077710
segmentation accuracy: 0.936918
box IoU(ground/3D): 0.805294/0.747923
box estimation accuracy (IoU=0.7): 0.785220
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.93it/s]
[37] test loss: 0.108153
test segmentation accuracy: 0.900788
test box IoU(ground/3D): 0.786448/0.732025
test box estimation accuracy (IoU=0.7): 0.745175
learning rate: 0.000700
save to:log/default_caronly_kitti_2022-05-15-21/acc0.745175-epoch036.pth
Saving model to log/default_caronly_kitti_2022-05-15-21/acc0.745175-epoch036.pth
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 038 ****
Epoch 38/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.01it/s]
[38: 1849/1850] train loss: 0.076506
segmentation accuracy: 0.936763
box IoU(ground/3D): 0.804926/0.747391
box estimation accuracy (IoU=0.7): 0.784155
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.95it/s]
[38] test loss: 0.112364
test segmentation accuracy: 0.896687
test box IoU(ground/3D): 0.780647/0.726261
test box estimation accuracy (IoU=0.7): 0.735285
learning rate: 0.000700
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 039 ****
Epoch 39/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:25<00:00,  6.96it/s]
[39: 1849/1850] train loss: 0.076790
segmentation accuracy: 0.937801
box IoU(ground/3D): 0.806429/0.748945
box estimation accuracy (IoU=0.7): 0.788615
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.94it/s]
[39] test loss: 0.104492
test segmentation accuracy: 0.897126
test box IoU(ground/3D): 0.784275/0.730865
test box estimation accuracy (IoU=0.7): 0.737518
learning rate: 0.000700
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 040 ****
Epoch 40/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:28<00:00,  6.90it/s]
[40: 1849/1850] train loss: 0.078869
segmentation accuracy: 0.937923
box IoU(ground/3D): 0.807125/0.749579
box estimation accuracy (IoU=0.7): 0.788750
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.39it/s]
[40] test loss: 0.105665
test segmentation accuracy: 0.898961
test box IoU(ground/3D): 0.779097/0.727093
test box estimation accuracy (IoU=0.7): 0.736242
learning rate: 0.000700
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 041 ****
Epoch 41/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[41: 1849/1850] train loss: 0.073728
segmentation accuracy: 0.940711
box IoU(ground/3D): 0.812208/0.755197
box estimation accuracy (IoU=0.7): 0.800878
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.42it/s]
[41] test loss: 0.102624
test segmentation accuracy: 0.900365
test box IoU(ground/3D): 0.785762/0.734168
test box estimation accuracy (IoU=0.7): 0.737837
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 042 ****
Epoch 42/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.20it/s]
[42: 1849/1850] train loss: 0.070295
segmentation accuracy: 0.941089
box IoU(ground/3D): 0.813971/0.756597
box estimation accuracy (IoU=0.7): 0.804155
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.44it/s]
[42] test loss: 0.130486
test segmentation accuracy: 0.895783
test box IoU(ground/3D): 0.753107/0.701636
test box estimation accuracy (IoU=0.7): 0.684080
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 043 ****
Epoch 43/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.18it/s]
[43: 1849/1850] train loss: 0.068019
segmentation accuracy: 0.941747
box IoU(ground/3D): 0.815067/0.757910
box estimation accuracy (IoU=0.7): 0.807551
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.43it/s]
[43] test loss: 0.107419
test segmentation accuracy: 0.902117
test box IoU(ground/3D): 0.781666/0.729752
test box estimation accuracy (IoU=0.7): 0.734806
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 044 ****
Epoch 44/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:16<00:00,  7.21it/s]
[44: 1849/1850] train loss: 0.072581
segmentation accuracy: 0.942010
box IoU(ground/3D): 0.815312/0.758426
box estimation accuracy (IoU=0.7): 0.808530
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.44it/s]
[44] test loss: 0.100743
test segmentation accuracy: 0.901680
test box IoU(ground/3D): 0.778149/0.725226
test box estimation accuracy (IoU=0.7): 0.724916
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 045 ****
Epoch 45/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.23it/s]
[45: 1849/1850] train loss: 0.068675
segmentation accuracy: 0.942616
box IoU(ground/3D): 0.816675/0.759843
box estimation accuracy (IoU=0.7): 0.811334
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.34it/s]
[45] test loss: 0.099679
test segmentation accuracy: 0.903185
test box IoU(ground/3D): 0.781140/0.727520
test box estimation accuracy (IoU=0.7): 0.723321
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 046 ****
Epoch 46/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.25it/s]
[46: 1849/1850] train loss: 0.069100
segmentation accuracy: 0.942850
box IoU(ground/3D): 0.816471/0.759632
box estimation accuracy (IoU=0.7): 0.810946
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.31it/s]
[46] test loss: 0.118076
test segmentation accuracy: 0.895721
test box IoU(ground/3D): 0.769390/0.715436
test box estimation accuracy (IoU=0.7): 0.712474
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 047 ****
Epoch 47/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:18<00:00,  7.16it/s]
[47: 1849/1850] train loss: 0.071577
segmentation accuracy: 0.943259
box IoU(ground/3D): 0.816784/0.760018
box estimation accuracy (IoU=0.7): 0.812061
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.43it/s]
[47] test loss: 0.110246
test segmentation accuracy: 0.899979
test box IoU(ground/3D): 0.773501/0.720766
test box estimation accuracy (IoU=0.7): 0.720211
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 048 ****
Epoch 48/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:16<00:00,  7.21it/s]
[48: 1849/1850] train loss: 0.069585
segmentation accuracy: 0.943105
box IoU(ground/3D): 0.817284/0.760504
box estimation accuracy (IoU=0.7): 0.813649
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.37it/s]
[48] test loss: 0.100036
test segmentation accuracy: 0.899621
test box IoU(ground/3D): 0.786004/0.732905
test box estimation accuracy (IoU=0.7): 0.744377
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 049 ****
Epoch 49/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.18it/s]
[49: 1849/1850] train loss: 0.069340
segmentation accuracy: 0.943498
box IoU(ground/3D): 0.816026/0.759556
box estimation accuracy (IoU=0.7): 0.811284
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.48it/s]
[49] test loss: 0.116906
test segmentation accuracy: 0.900527
test box IoU(ground/3D): 0.759234/0.706455
test box estimation accuracy (IoU=0.7): 0.679454
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 050 ****
Epoch 50/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.24it/s]
[50: 1849/1850] train loss: 0.067688
segmentation accuracy: 0.943984
box IoU(ground/3D): 0.818098/0.761337
box estimation accuracy (IoU=0.7): 0.814003
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.48it/s]
[50] test loss: 0.104664
test segmentation accuracy: 0.902726
test box IoU(ground/3D): 0.782094/0.726243
test box estimation accuracy (IoU=0.7): 0.723241
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 051 ****
Epoch 51/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.24it/s]
[51: 1849/1850] train loss: 0.070230
segmentation accuracy: 0.944250
box IoU(ground/3D): 0.818348/0.761683
box estimation accuracy (IoU=0.7): 0.814949
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.38it/s]
[51] test loss: 0.103743
test segmentation accuracy: 0.903164
test box IoU(ground/3D): 0.782016/0.729345
test box estimation accuracy (IoU=0.7): 0.741586
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 052 ****
Epoch 52/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.25it/s]
[52: 1849/1850] train loss: 0.070194
segmentation accuracy: 0.944703
box IoU(ground/3D): 0.819037/0.762398
box estimation accuracy (IoU=0.7): 0.818666
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.43it/s]
[52] test loss: 0.105159
test segmentation accuracy: 0.899416
test box IoU(ground/3D): 0.770837/0.718426
test box estimation accuracy (IoU=0.7): 0.704179
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 053 ****
Epoch 53/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:16<00:00,  7.20it/s]
[53: 1849/1850] train loss: 0.069174
segmentation accuracy: 0.944679
box IoU(ground/3D): 0.818806/0.762104
box estimation accuracy (IoU=0.7): 0.817517
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.38it/s]
[53] test loss: 0.126127
test segmentation accuracy: 0.898651
test box IoU(ground/3D): 0.762630/0.708803
test box estimation accuracy (IoU=0.7): 0.689185
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 054 ****
Epoch 54/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.23it/s]
[54: 1849/1850] train loss: 0.065885
segmentation accuracy: 0.945431
box IoU(ground/3D): 0.820815/0.764204
box estimation accuracy (IoU=0.7): 0.820912
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.32it/s]
[54] test loss: 0.108785
test segmentation accuracy: 0.899563
test box IoU(ground/3D): 0.773389/0.721238
test box estimation accuracy (IoU=0.7): 0.717419
learning rate: 0.000490
Best Test acc: 0.745175(Epoch 37)
**** EPOCH 055 ****
Epoch 55/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:16<00:00,  7.21it/s]
[55: 1849/1850] train loss: 0.069146
segmentation accuracy: 0.945448
box IoU(ground/3D): 0.819826/0.763297
box estimation accuracy (IoU=0.7): 0.819780
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.39it/s]
[55] test loss: 0.111566
test segmentation accuracy: 0.899372
test box IoU(ground/3D): 0.785247/0.733411
test box estimation accuracy (IoU=0.7): 0.745972
learning rate: 0.000490
save to:log/default_caronly_kitti_2022-05-15-21/acc0.745972-epoch054.pth
Saving model to log/default_caronly_kitti_2022-05-15-21/acc0.745972-epoch054.pth
Best Test acc: 0.745972(Epoch 55)
**** EPOCH 056 ****
Epoch 56/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:16<00:00,  7.22it/s]
[56: 1849/1850] train loss: 0.069401
segmentation accuracy: 0.945769
box IoU(ground/3D): 0.820563/0.764048
box estimation accuracy (IoU=0.7): 0.817331
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.45it/s]
[56] test loss: 0.107034
test segmentation accuracy: 0.902818
test box IoU(ground/3D): 0.773602/0.721021
test box estimation accuracy (IoU=0.7): 0.712155
learning rate: 0.000490
Best Test acc: 0.745972(Epoch 55)
**** EPOCH 057 ****
Epoch 57/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:14<00:00,  7.26it/s]
[57: 1849/1850] train loss: 0.068818
segmentation accuracy: 0.945975
box IoU(ground/3D): 0.820851/0.763945
box estimation accuracy (IoU=0.7): 0.821115
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.35it/s]
[57] test loss: 0.106959
test segmentation accuracy: 0.900330
test box IoU(ground/3D): 0.789437/0.735521
test box estimation accuracy (IoU=0.7): 0.751795
learning rate: 0.000490
save to:log/default_caronly_kitti_2022-05-15-21/acc0.751795-epoch056.pth
Saving model to log/default_caronly_kitti_2022-05-15-21/acc0.751795-epoch056.pth
Best Test acc: 0.751795(Epoch 57)
**** EPOCH 058 ****
Epoch 58/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.23it/s]
[58: 1849/1850] train loss: 0.066800
segmentation accuracy: 0.946198
box IoU(ground/3D): 0.821081/0.764773
box estimation accuracy (IoU=0.7): 0.823176
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.38it/s]
[58] test loss: 0.112145
test segmentation accuracy: 0.898383
test box IoU(ground/3D): 0.791493/0.738107
test box estimation accuracy (IoU=0.7): 0.752752
learning rate: 0.000490
save to:log/default_caronly_kitti_2022-05-15-21/acc0.752752-epoch057.pth
Saving model to log/default_caronly_kitti_2022-05-15-21/acc0.752752-epoch057.pth
Best Test acc: 0.752752(Epoch 58)
**** EPOCH 059 ****
Epoch 59/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.20it/s]
[59: 1849/1850] train loss: 0.066727
segmentation accuracy: 0.946170
box IoU(ground/3D): 0.821339/0.764756
box estimation accuracy (IoU=0.7): 0.822821
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.31it/s]
[59] test loss: 0.113860
test segmentation accuracy: 0.901907
test box IoU(ground/3D): 0.764118/0.711075
test box estimation accuracy (IoU=0.7): 0.686792
learning rate: 0.000490
Best Test acc: 0.752752(Epoch 58)
**** EPOCH 060 ****
Epoch 60/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.25it/s]
[60: 1849/1850] train loss: 0.067948
segmentation accuracy: 0.946786
box IoU(ground/3D): 0.821676/0.765323
box estimation accuracy (IoU=0.7): 0.823598
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.39it/s]
[60] test loss: 0.104654
test segmentation accuracy: 0.901725
test box IoU(ground/3D): 0.786349/0.734020
test box estimation accuracy (IoU=0.7): 0.742224
learning rate: 0.000490
Best Test acc: 0.752752(Epoch 58)
**** EPOCH 061 ****
Epoch 61/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:16<00:00,  7.22it/s]
[61: 1849/1850] train loss: 0.065557
segmentation accuracy: 0.948496
box IoU(ground/3D): 0.825380/0.769443
box estimation accuracy (IoU=0.7): 0.834240
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.44it/s]
[61] test loss: 0.117377
test segmentation accuracy: 0.903019
test box IoU(ground/3D): 0.753417/0.697965
test box estimation accuracy (IoU=0.7): 0.655527
learning rate: 0.000343
Best Test acc: 0.752752(Epoch 58)
**** EPOCH 062 ****
Epoch 62/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.24it/s]
[62: 1849/1850] train loss: 0.062572
segmentation accuracy: 0.949013
box IoU(ground/3D): 0.826512/0.770697
box estimation accuracy (IoU=0.7): 0.836537
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.28it/s]
[62] test loss: 0.095634
test segmentation accuracy: 0.905160
test box IoU(ground/3D): 0.789051/0.736373
test box estimation accuracy (IoU=0.7): 0.746052
learning rate: 0.000343
Best Test acc: 0.752752(Epoch 58)
**** EPOCH 063 ****
Epoch 63/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.19it/s]
[63: 1849/1850] train loss: 0.062453
segmentation accuracy: 0.948822
box IoU(ground/3D): 0.826957/0.770795
box estimation accuracy (IoU=0.7): 0.837095
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.36it/s]
[63] test loss: 0.102770
test segmentation accuracy: 0.901138
test box IoU(ground/3D): 0.771570/0.717821
test box estimation accuracy (IoU=0.7): 0.706652
learning rate: 0.000343
Best Test acc: 0.752752(Epoch 58)
**** EPOCH 064 ****
Epoch 64/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.19it/s]
[64: 1849/1850] train loss: 0.064668
segmentation accuracy: 0.949123
box IoU(ground/3D): 0.826678/0.770777
box estimation accuracy (IoU=0.7): 0.835693
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.45it/s]
[64] test loss: 0.099254
test segmentation accuracy: 0.903009
test box IoU(ground/3D): 0.788680/0.736373
test box estimation accuracy (IoU=0.7): 0.744696
learning rate: 0.000343
Best Test acc: 0.752752(Epoch 58)
**** EPOCH 065 ****
Epoch 65/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.25it/s]
[65: 1849/1850] train loss: 0.064385
segmentation accuracy: 0.949425
box IoU(ground/3D): 0.827092/0.770907
box estimation accuracy (IoU=0.7): 0.835456
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.40it/s]
[65] test loss: 0.094401
test segmentation accuracy: 0.903058
test box IoU(ground/3D): 0.790003/0.737928
test box estimation accuracy (IoU=0.7): 0.752911
learning rate: 0.000343
save to:log/default_caronly_kitti_2022-05-15-21/acc0.752911-epoch064.pth
Saving model to log/default_caronly_kitti_2022-05-15-21/acc0.752911-epoch064.pth
Best Test acc: 0.752911(Epoch 65)
**** EPOCH 066 ****
Epoch 66/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:14<00:00,  7.26it/s]
[66: 1849/1850] train loss: 0.063972
segmentation accuracy: 0.949734
box IoU(ground/3D): 0.828190/0.772288
box estimation accuracy (IoU=0.7): 0.839730
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.37it/s]
[66] test loss: 0.099865
test segmentation accuracy: 0.902021
test box IoU(ground/3D): 0.793821/0.742269
test box estimation accuracy (IoU=0.7): 0.762243
learning rate: 0.000343
save to:log/default_caronly_kitti_2022-05-15-21/acc0.762243-epoch065.pth
Saving model to log/default_caronly_kitti_2022-05-15-21/acc0.762243-epoch065.pth
Best Test acc: 0.762243(Epoch 66)
**** EPOCH 067 ****
Epoch 67/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:14<00:00,  7.27it/s]
[67: 1849/1850] train loss: 0.064154
segmentation accuracy: 0.949645
box IoU(ground/3D): 0.827762/0.772088
box estimation accuracy (IoU=0.7): 0.837905
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.43it/s]
[67] test loss: 0.099663
test segmentation accuracy: 0.903181
test box IoU(ground/3D): 0.791920/0.739669
test box estimation accuracy (IoU=0.7): 0.749322
learning rate: 0.000343
Best Test acc: 0.762243(Epoch 66)
**** EPOCH 068 ****
Epoch 68/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:16<00:00,  7.21it/s]
[68: 1849/1850] train loss: 0.061620
segmentation accuracy: 0.950073
box IoU(ground/3D): 0.828028/0.772238
box estimation accuracy (IoU=0.7): 0.839324
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.34it/s]
[68] test loss: 0.099011
test segmentation accuracy: 0.901421
test box IoU(ground/3D): 0.791677/0.740126
test box estimation accuracy (IoU=0.7): 0.754985
learning rate: 0.000343
Best Test acc: 0.762243(Epoch 66)
**** EPOCH 069 ****
Epoch 69/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.13it/s]
[69: 1849/1850] train loss: 0.063510
segmentation accuracy: 0.950297
box IoU(ground/3D): 0.828695/0.772861
box estimation accuracy (IoU=0.7): 0.840524
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.15it/s]
[69] test loss: 0.108204
test segmentation accuracy: 0.900632
test box IoU(ground/3D): 0.788051/0.736481
test box estimation accuracy (IoU=0.7): 0.751316
learning rate: 0.000343
Best Test acc: 0.762243(Epoch 66)
**** EPOCH 070 ****
Epoch 70/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.25it/s]
[70: 1849/1850] train loss: 0.062341
segmentation accuracy: 0.950224
box IoU(ground/3D): 0.829066/0.773067
box estimation accuracy (IoU=0.7): 0.841943
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.37it/s]
[70] test loss: 0.099372
test segmentation accuracy: 0.902247
test box IoU(ground/3D): 0.786440/0.735035
test box estimation accuracy (IoU=0.7): 0.748365
learning rate: 0.000343
Best Test acc: 0.762243(Epoch 66)
**** EPOCH 071 ****
Epoch 71/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:16<00:00,  7.20it/s]
[71: 1849/1850] train loss: 0.063587
segmentation accuracy: 0.950545
box IoU(ground/3D): 0.828565/0.772717
box estimation accuracy (IoU=0.7): 0.840253
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.40it/s]
[71] test loss: 0.100690
test segmentation accuracy: 0.900381
test box IoU(ground/3D): 0.793016/0.741454
test box estimation accuracy (IoU=0.7): 0.755782
learning rate: 0.000343
Best Test acc: 0.762243(Epoch 66)
**** EPOCH 072 ****
Epoch 72/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.20it/s]
[72: 1849/1850] train loss: 0.060116
segmentation accuracy: 0.950637
box IoU(ground/3D): 0.829309/0.773302
box estimation accuracy (IoU=0.7): 0.841520
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.38it/s]
[72] test loss: 0.101247
test segmentation accuracy: 0.901471
test box IoU(ground/3D): 0.790564/0.739232
test box estimation accuracy (IoU=0.7): 0.758654
learning rate: 0.000343
Best Test acc: 0.762243(Epoch 66)
**** EPOCH 073 ****
Epoch 73/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:16<00:00,  7.22it/s]
[73: 1849/1850] train loss: 0.062847
segmentation accuracy: 0.951123
box IoU(ground/3D): 0.829441/0.773932
box estimation accuracy (IoU=0.7): 0.845777
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.32it/s]
[73] test loss: 0.103672
test segmentation accuracy: 0.903717
test box IoU(ground/3D): 0.795913/0.743691
test box estimation accuracy (IoU=0.7): 0.769580
learning rate: 0.000343
save to:log/default_caronly_kitti_2022-05-15-21/acc0.769580-epoch072.pth
Saving model to log/default_caronly_kitti_2022-05-15-21/acc0.769580-epoch072.pth
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 074 ****
Epoch 74/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.19it/s]
[74: 1849/1850] train loss: 0.062555
segmentation accuracy: 0.951007
box IoU(ground/3D): 0.829971/0.774274
box estimation accuracy (IoU=0.7): 0.843733
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.33it/s]
[74] test loss: 0.100734
test segmentation accuracy: 0.902210
test box IoU(ground/3D): 0.787467/0.735153
test box estimation accuracy (IoU=0.7): 0.742941
learning rate: 0.000343
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 075 ****
Epoch 75/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.20it/s]
[75: 1849/1850] train loss: 0.060455
segmentation accuracy: 0.951330
box IoU(ground/3D): 0.830083/0.773834
box estimation accuracy (IoU=0.7): 0.843361
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.43it/s]
[75] test loss: 0.093518
test segmentation accuracy: 0.901827
test box IoU(ground/3D): 0.793502/0.741368
test box estimation accuracy (IoU=0.7): 0.757936
learning rate: 0.000343
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 076 ****
Epoch 76/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:16<00:00,  7.21it/s]
[76: 1849/1850] train loss: 0.061201
segmentation accuracy: 0.951397
box IoU(ground/3D): 0.830998/0.774858
box estimation accuracy (IoU=0.7): 0.845389
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.37it/s]
[76] test loss: 0.106551
test segmentation accuracy: 0.903585
test box IoU(ground/3D): 0.788288/0.735568
test box estimation accuracy (IoU=0.7): 0.750837
learning rate: 0.000343
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 077 ****
Epoch 77/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:16<00:00,  7.22it/s]
[77: 1849/1850] train loss: 0.060538
segmentation accuracy: 0.951358
box IoU(ground/3D): 0.829894/0.773951
box estimation accuracy (IoU=0.7): 0.844003
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.38it/s]
[77] test loss: 0.103191
test segmentation accuracy: 0.901596
test box IoU(ground/3D): 0.789619/0.734804
test box estimation accuracy (IoU=0.7): 0.742224
learning rate: 0.000343
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 078 ****
Epoch 78/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.19it/s]
[78: 1849/1850] train loss: 0.059417
segmentation accuracy: 0.951759
box IoU(ground/3D): 0.830397/0.774812
box estimation accuracy (IoU=0.7): 0.847111
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.39it/s]
[78] test loss: 0.106518
test segmentation accuracy: 0.900505
test box IoU(ground/3D): 0.790355/0.736483
test box estimation accuracy (IoU=0.7): 0.757697
learning rate: 0.000343
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 079 ****
Epoch 79/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.13it/s]
[79: 1849/1850] train loss: 0.060551
segmentation accuracy: 0.951819
box IoU(ground/3D): 0.830917/0.775169
box estimation accuracy (IoU=0.7): 0.845591
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.31it/s]
[79] test loss: 0.102978
test segmentation accuracy: 0.899720
test box IoU(ground/3D): 0.788151/0.735742
test box estimation accuracy (IoU=0.7): 0.748126
learning rate: 0.000343
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 080 ****
Epoch 80/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:18<00:00,  7.17it/s]
[80: 1849/1850] train loss: 0.061673
segmentation accuracy: 0.951764
box IoU(ground/3D): 0.830752/0.774983
box estimation accuracy (IoU=0.7): 0.844713
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.42it/s]
[80] test loss: 0.098965
test segmentation accuracy: 0.901512
test box IoU(ground/3D): 0.792327/0.739934
test box estimation accuracy (IoU=0.7): 0.759850
learning rate: 0.000343
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 081 ****
Epoch 81/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:14<00:00,  7.26it/s]
[81: 1849/1850] train loss: 0.060696
segmentation accuracy: 0.953126
box IoU(ground/3D): 0.833781/0.778424
box estimation accuracy (IoU=0.7): 0.852145
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.41it/s]
[81] test loss: 0.099576
test segmentation accuracy: 0.903570
test box IoU(ground/3D): 0.795703/0.743750
test box estimation accuracy (IoU=0.7): 0.763519
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 082 ****
Epoch 82/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.14it/s]
[82: 1849/1850] train loss: 0.057043
segmentation accuracy: 0.953071
box IoU(ground/3D): 0.834667/0.779153
box estimation accuracy (IoU=0.7): 0.853970
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.30it/s]
[82] test loss: 0.095529
test segmentation accuracy: 0.903386
test box IoU(ground/3D): 0.797442/0.745362
test box estimation accuracy (IoU=0.7): 0.768703
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 083 ****
Epoch 83/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[83: 1849/1850] train loss: 0.061058
segmentation accuracy: 0.953705
box IoU(ground/3D): 0.834704/0.779436
box estimation accuracy (IoU=0.7): 0.855355
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.38it/s]
[83] test loss: 0.098454
test segmentation accuracy: 0.902567
test box IoU(ground/3D): 0.790275/0.738544
test box estimation accuracy (IoU=0.7): 0.755623
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 084 ****
Epoch 84/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.23it/s]
[84: 1849/1850] train loss: 0.057397
segmentation accuracy: 0.953766
box IoU(ground/3D): 0.835127/0.779634
box estimation accuracy (IoU=0.7): 0.855693
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.40it/s]
[84] test loss: 0.096032
test segmentation accuracy: 0.903885
test box IoU(ground/3D): 0.794252/0.742430
test box estimation accuracy (IoU=0.7): 0.764715
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 085 ****
Epoch 85/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.19it/s]
[85: 1849/1850] train loss: 0.055260
segmentation accuracy: 0.953712
box IoU(ground/3D): 0.835286/0.779822
box estimation accuracy (IoU=0.7): 0.855659
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.13it/s]
[85] test loss: 0.104658
test segmentation accuracy: 0.902376
test box IoU(ground/3D): 0.792539/0.740991
test box estimation accuracy (IoU=0.7): 0.760648
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 086 ****
Epoch 86/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.19it/s]
[86: 1849/1850] train loss: 0.057831
segmentation accuracy: 0.953702
box IoU(ground/3D): 0.834660/0.779307
box estimation accuracy (IoU=0.7): 0.854358
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.44it/s]
[86] test loss: 0.101195
test segmentation accuracy: 0.901523
test box IoU(ground/3D): 0.791995/0.739886
test box estimation accuracy (IoU=0.7): 0.757776
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 087 ****
Epoch 87/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.24it/s]
[87: 1849/1850] train loss: 0.059238
segmentation accuracy: 0.953747
box IoU(ground/3D): 0.834942/0.779726
box estimation accuracy (IoU=0.7): 0.855693
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.41it/s]
[87] test loss: 0.099799
test segmentation accuracy: 0.902881
test box IoU(ground/3D): 0.790597/0.738867
test box estimation accuracy (IoU=0.7): 0.754586
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 088 ****
Epoch 88/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.17it/s]
[88: 1849/1850] train loss: 0.061061
segmentation accuracy: 0.954223
box IoU(ground/3D): 0.835962/0.780563
box estimation accuracy (IoU=0.7): 0.857635
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.44it/s]
[88] test loss: 0.099886
test segmentation accuracy: 0.902495
test box IoU(ground/3D): 0.791736/0.740073
test box estimation accuracy (IoU=0.7): 0.761605
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 089 ****
Epoch 89/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[89: 1849/1850] train loss: 0.058619
segmentation accuracy: 0.954428
box IoU(ground/3D): 0.836080/0.780727
box estimation accuracy (IoU=0.7): 0.857787
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.40it/s]
[89] test loss: 0.103488
test segmentation accuracy: 0.902000
test box IoU(ground/3D): 0.786386/0.734808
test box estimation accuracy (IoU=0.7): 0.743819
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 090 ****
Epoch 90/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:18<00:00,  7.17it/s]
[90: 1849/1850] train loss: 0.060139
segmentation accuracy: 0.954401
box IoU(ground/3D): 0.835734/0.780309
box estimation accuracy (IoU=0.7): 0.857348
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.36it/s]
[90] test loss: 0.105306
test segmentation accuracy: 0.902360
test box IoU(ground/3D): 0.793884/0.742010
test box estimation accuracy (IoU=0.7): 0.763280
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 091 ****
Epoch 91/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[91: 1849/1850] train loss: 0.057550
segmentation accuracy: 0.954215
box IoU(ground/3D): 0.835670/0.780140
box estimation accuracy (IoU=0.7): 0.857061
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.20it/s]
[91] test loss: 0.101891
test segmentation accuracy: 0.902719
test box IoU(ground/3D): 0.792457/0.739832
test box estimation accuracy (IoU=0.7): 0.761046
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 092 ****
Epoch 92/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:18<00:00,  7.17it/s]
[92: 1849/1850] train loss: 0.058030
segmentation accuracy: 0.954499
box IoU(ground/3D): 0.836125/0.780820
box estimation accuracy (IoU=0.7): 0.857128
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.41it/s]
[92] test loss: 0.098564
test segmentation accuracy: 0.903130
test box IoU(ground/3D): 0.794954/0.743258
test box estimation accuracy (IoU=0.7): 0.765593
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 093 ****
Epoch 93/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.18it/s]
[93: 1849/1850] train loss: 0.057414
segmentation accuracy: 0.954653
box IoU(ground/3D): 0.836644/0.781361
box estimation accuracy (IoU=0.7): 0.858699
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.42it/s]
[93] test loss: 0.100004
test segmentation accuracy: 0.902452
test box IoU(ground/3D): 0.790547/0.738437
test box estimation accuracy (IoU=0.7): 0.754506
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 094 ****
Epoch 94/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.23it/s]
[94: 1849/1850] train loss: 0.057443
segmentation accuracy: 0.954904
box IoU(ground/3D): 0.836296/0.781230
box estimation accuracy (IoU=0.7): 0.860456
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.26it/s]
[94] test loss: 0.098893
test segmentation accuracy: 0.900625
test box IoU(ground/3D): 0.790465/0.739431
test box estimation accuracy (IoU=0.7): 0.753390
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 095 ****
Epoch 95/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[95: 1849/1850] train loss: 0.055730
segmentation accuracy: 0.955026
box IoU(ground/3D): 0.837487/0.782236
box estimation accuracy (IoU=0.7): 0.861064
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.38it/s]
[95] test loss: 0.098831
test segmentation accuracy: 0.901533
test box IoU(ground/3D): 0.795459/0.743518
test box estimation accuracy (IoU=0.7): 0.764795
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 096 ****
Epoch 96/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[96: 1849/1850] train loss: 0.058444
segmentation accuracy: 0.954998
box IoU(ground/3D): 0.836652/0.781410
box estimation accuracy (IoU=0.7): 0.859780
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.36it/s]
[96] test loss: 0.100068
test segmentation accuracy: 0.900788
test box IoU(ground/3D): 0.790591/0.739028
test box estimation accuracy (IoU=0.7): 0.757298
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 097 ****
Epoch 97/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.14it/s]
[97: 1849/1850] train loss: 0.059718
segmentation accuracy: 0.955142
box IoU(ground/3D): 0.836923/0.781830
box estimation accuracy (IoU=0.7): 0.860439
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.38it/s]
[97] test loss: 0.100190
test segmentation accuracy: 0.902116
test box IoU(ground/3D): 0.794285/0.742461
test box estimation accuracy (IoU=0.7): 0.763439
learning rate: 0.000240
Best Test acc: 0.769580(Epoch 73)
**** EPOCH 098 ****
Epoch 98/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[98: 1849/1850] train loss: 0.057494
segmentation accuracy: 0.955390
box IoU(ground/3D): 0.837164/0.781631
box estimation accuracy (IoU=0.7): 0.858986
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.32it/s]
[98] test loss: 0.100709
test segmentation accuracy: 0.902353
test box IoU(ground/3D): 0.796255/0.744404
test box estimation accuracy (IoU=0.7): 0.771814
learning rate: 0.000240
save to:log/default_caronly_kitti_2022-05-15-21/acc0.771814-epoch097.pth
Saving model to log/default_caronly_kitti_2022-05-15-21/acc0.771814-epoch097.pth
Best Test acc: 0.771814(Epoch 98)
**** EPOCH 099 ****
Epoch 99/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:16<00:00,  7.21it/s]
[99: 1849/1850] train loss: 0.059570
segmentation accuracy: 0.955180
box IoU(ground/3D): 0.836981/0.781833
box estimation accuracy (IoU=0.7): 0.860642
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.40it/s]
[99] test loss: 0.099957
test segmentation accuracy: 0.900217
test box IoU(ground/3D): 0.788318/0.737092
test box estimation accuracy (IoU=0.7): 0.748205
learning rate: 0.000240
Best Test acc: 0.771814(Epoch 98)
**** EPOCH 100 ****
Epoch 100/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.14it/s]
[100: 1849/1850] train loss: 0.056713
segmentation accuracy: 0.955395
box IoU(ground/3D): 0.837402/0.782223
box estimation accuracy (IoU=0.7): 0.861453
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.50it/s]
[100] test loss: 0.094691
test segmentation accuracy: 0.902308
test box IoU(ground/3D): 0.792949/0.740389
test box estimation accuracy (IoU=0.7): 0.755942
learning rate: 0.000240
Best Test acc: 0.771814(Epoch 98)
**** EPOCH 101 ****
Epoch 101/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[101: 1849/1850] train loss: 0.055153
segmentation accuracy: 0.956174
box IoU(ground/3D): 0.839445/0.784551
box estimation accuracy (IoU=0.7): 0.865980
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.21it/s]
[101] test loss: 0.098477
test segmentation accuracy: 0.903995
test box IoU(ground/3D): 0.795702/0.743951
test box estimation accuracy (IoU=0.7): 0.763678
learning rate: 0.000168
Best Test acc: 0.771814(Epoch 98)
**** EPOCH 102 ****
Epoch 102/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:15<00:00,  7.25it/s]
[102: 1849/1850] train loss: 0.056829
segmentation accuracy: 0.956439
box IoU(ground/3D): 0.840008/0.785232
box estimation accuracy (IoU=0.7): 0.865270
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.33it/s]
[102] test loss: 0.099980
test segmentation accuracy: 0.904108
test box IoU(ground/3D): 0.795460/0.743941
test box estimation accuracy (IoU=0.7): 0.768384
learning rate: 0.000168
Best Test acc: 0.771814(Epoch 98)
**** EPOCH 103 ****
Epoch 103/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.05it/s]
[103: 1849/1850] train loss: 0.053759
segmentation accuracy: 0.956485
box IoU(ground/3D): 0.839644/0.784532
box estimation accuracy (IoU=0.7): 0.864375
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.43it/s]
[103] test loss: 0.099598
test segmentation accuracy: 0.902824
test box IoU(ground/3D): 0.794628/0.742284
test box estimation accuracy (IoU=0.7): 0.760169
learning rate: 0.000168
Best Test acc: 0.771814(Epoch 98)
**** EPOCH 104 ****
Epoch 104/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.19it/s]
[104: 1849/1850] train loss: 0.056629
segmentation accuracy: 0.956570
box IoU(ground/3D): 0.839461/0.784772
box estimation accuracy (IoU=0.7): 0.866368
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:41<00:00,  9.49it/s]
[104] test loss: 0.102077
test segmentation accuracy: 0.900877
test box IoU(ground/3D): 0.797343/0.745811
test box estimation accuracy (IoU=0.7): 0.773010
learning rate: 0.000168
save to:log/default_caronly_kitti_2022-05-15-21/acc0.773010-epoch103.pth
Saving model to log/default_caronly_kitti_2022-05-15-21/acc0.773010-epoch103.pth
Best Test acc: 0.773010(Epoch 104)
**** EPOCH 105 ****
Epoch 105/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:25<00:00,  6.98it/s]
[105: 1849/1850] train loss: 0.052917
segmentation accuracy: 0.956667
box IoU(ground/3D): 0.840881/0.785837
box estimation accuracy (IoU=0.7): 0.868615
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.23it/s]
[105] test loss: 0.104739
test segmentation accuracy: 0.903305
test box IoU(ground/3D): 0.793220/0.741072
test box estimation accuracy (IoU=0.7): 0.759052
learning rate: 0.000168
Best Test acc: 0.773010(Epoch 104)
**** EPOCH 106 ****
Epoch 106/150:
Traceback (most recent call last):
  File "train/train_fpointnets.py", line 572, in <module>
    train()
  File "train/train_fpointnets.py", line 330, in train
    for i, data in tqdm(enumerate(train_dataloader),\
  File "C:\Users\nakas\.conda\envs\test5\lib\site-packages\torch\utils\data\dataloader.py", line 368, in __iter__
    return self._get_iterator()
  File "C:\Users\nakas\.conda\envs\test5\lib\site-packages\torch\utils\data\dataloader.py", line 314, in _get_iterator
    return _MultiProcessingDataLoaderIter(self)
  File "C:\Users\nakas\.conda\envs\test5\lib\site-packages\torch\utils\data\dataloader.py", line 927, in __init__
    w.start()
  File "C:\Users\nakas\.conda\envs\test5\lib\multiprocessing\process.py", line 112, in start
    self._popen = self._Popen(self)
  File "C:\Users\nakas\.conda\envs\test5\lib\multiprocessing\context.py", line 223, in _Popen
    return _default_context.get_context().Process._Popen(process_obj)
  File "C:\Users\nakas\.conda\envs\test5\lib\multiprocessing\context.py", line 322, in _Popen
    return Popen(process_obj)
  File "C:\Users\nakas\.conda\envs\test5\lib\multiprocessing\popen_spawn_win32.py", line 89, in __init__
    reduction.dump(process_obj, to_child)
  File "C:\Users\nakas\.conda\envs\test5\lib\multiprocessing\reduction.py", line 60, in dump
    ForkingPickler(file, protocol).dump(obj)
OSError: [Errno 22] Invalid argument
Traceback (most recent call last):
  File "<string>", line 1, in <module>
  File "C:\Users\nakas\.conda\envs\test5\lib\multiprocessing\spawn.py", line 105, in spawn_main
    exitcode = _main(fd)
  File "C:\Users\nakas\.conda\envs\test5\lib\multiprocessing\spawn.py", line 115, in _main
    self = reduction.pickle.load(from_parent)
_pickle.UnpicklingError: pickle data was truncated
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch> python train/train_fpointnets.py --log_dir log
pid: 20556
Your FLAGS:
Namespace(batch_size=32, ckpt=None, dataset='kitti', debug=False, decay_rate=0.7, decay_step=20, learning_rate=0.001, log_dir='log', max_epoch=150, model='frustum_pointnets_v1_old', momentum=0.9, name='default', no_intensity=False, num_point=1024, objtype='caronly', optimizer='adam', restore_model_path=None, return_all_loss=False, sensor='CAM_FRONT', train_sets='train', val_sets='val', weight_decay=0.0)
**** EPOCH 001 ****
Epoch 1/150:
 22%|████████████████▉                                                              | 398/1850 [01:17<04:36,  5.26it/s]forrtl: error (200): program aborting due to control-C event
Image              PC                Routine            Line        Source
libifcoremd.dll    00007FF8DB463B58  Unknown               Unknown  Unknown
KERNELBASE.dll     00007FF95AAF59E5  Unknown               Unknown  Unknown
KERNEL32.DLL       00007FF95B6154E0  Unknown               Unknown  Unknown
ntdll.dll          00007FF95CFC485B  Unknown               Unknown  Unknown
 22%|█████████████████                                                              | 399/1850 [01:17<04:22,  5.54it/s]forrtl: error (200): program aborting due to control-C event
Image              PC                Routine            Line        Source
libifcoremd.dll    00007FF8DB463B58  Unknown               Unknown  Unknown
KERNELBASE.dll     00007FF95AAF59E5  Unknown               Unknown  Unknown
KERNEL32.DLL       00007FF95B6154E0  Unknown               Unknown  Unknown
ntdll.dll          00007FF95CFC485B  Unknown               Unknown  Unknown
forrtl: error (200): program aborting due to control-C event
Image              PC                Routine            Line        Source
libifcoremd.dll    00007FF8DB463B58  Unknown               Unknown  Unknown
KERNELBASE.dll     00007FF95AAF59E5  Unknown               Unknown  Unknown
KERNEL32.DLL       00007FF95B6154E0  Unknown               Unknown  Unknown
ntdll.dll          00007FF95CFC485B  Unknown               Unknown  Unknown
forrtl: error (200): program aborting due to control-C event
Image              PC                Routine            Line        Source
libifcoremd.dll    00007FF8DB463B58  Unknown               Unknown  Unknown
KERNELBASE.dll     00007FF95AAF59E5  Unknown               Unknown  Unknown
KERNEL32.DLL       00007FF95B6154E0  Unknown               Unknown  Unknown
ntdll.dll          00007FF95CFC485B  Unknown               Unknown  Unknown
 22%|█████████████████▏                                                             | 403/1850 [01:18<03:56,  6.12it/s]forrtl: error (200): program aborting due to control-C event
Image              PC                Routine            Line        Source
libifcoremd.dll    00007FF8DB463B58  Unknown               Unknown  Unknown
KERNELBASE.dll     00007FF95AAF59E5  Unknown               Unknown  Unknown
KERNEL32.DLL       00007FF95B6154E0  Unknown               Unknown  Unknown
ntdll.dll          00007FF95CFC485B  Unknown               Unknown  Unknown
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> ^C
(test5) PS C:\Git\frustum-pointnets-pytorch> python train/train_fpointnets.py --log_dir log
pid: 27100
Your FLAGS:
Namespace(batch_size=32, ckpt=None, dataset='kitti', debug=False, decay_rate=0.7, decay_step=20, learning_rate=0.001, log_dir='log', max_epoch=150, model='frustum_pointnets_v1_old', momentum=0.9, name='default', no_intensity=False, num_point=1024, objtype='caronly', optimizer='adam', restore_model_path=None, return_all_loss=False, sensor='CAM_FRONT', train_sets='train', val_sets='val', weight_decay=0.0)
name has been existed
**** EPOCH 001 ****
Epoch 1/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.05it/s]
[1: 1849/1850] train loss: 0.437064
segmentation accuracy: 0.814267
box IoU(ground/3D): 0.541869/0.482275
box estimation accuracy (IoU=0.7): 0.213514
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.15it/s]
[1] test loss: 0.271259
test segmentation accuracy: 0.801847
test box IoU(ground/3D): 0.613418/0.557590
test box estimation accuracy (IoU=0.7): 0.352050
learning rate: 0.001000
Best Test acc: 0.352050(Epoch 1)
**** EPOCH 002 ****
Epoch 2/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.03it/s]
[2: 1849/1850] train loss: 0.263530
segmentation accuracy: 0.865388
box IoU(ground/3D): 0.638623/0.578938
box estimation accuracy (IoU=0.7): 0.362787
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[2] test loss: 0.192058
test segmentation accuracy: 0.876448
test box IoU(ground/3D): 0.682398/0.627124
test box estimation accuracy (IoU=0.7): 0.489472
learning rate: 0.001000
Best Test acc: 0.489472(Epoch 2)
**** EPOCH 003 ****
Epoch 3/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[3: 1849/1850] train loss: 0.224060
segmentation accuracy: 0.876674
box IoU(ground/3D): 0.666558/0.606843
box estimation accuracy (IoU=0.7): 0.427044
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.12it/s]
[3] test loss: 0.185127
test segmentation accuracy: 0.867499
test box IoU(ground/3D): 0.687754/0.629366
test box estimation accuracy (IoU=0.7): 0.463710
learning rate: 0.001000
Best Test acc: 0.489472(Epoch 2)
**** EPOCH 004 ****
Epoch 4/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:17<00:00,  7.18it/s]
[4: 1849/1850] train loss: 0.191720
segmentation accuracy: 0.884865
box IoU(ground/3D): 0.687283/0.627891
box estimation accuracy (IoU=0.7): 0.484105
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.21it/s]
[4] test loss: 0.191418
test segmentation accuracy: 0.871686
test box IoU(ground/3D): 0.689377/0.634101
test box estimation accuracy (IoU=0.7): 0.514596
learning rate: 0.001000
Best Test acc: 0.514596(Epoch 4)
**** EPOCH 005 ****
Epoch 5/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:18<00:00,  7.15it/s]
[5: 1849/1850] train loss: 0.180000
segmentation accuracy: 0.890659
box IoU(ground/3D): 0.702876/0.644124
box estimation accuracy (IoU=0.7): 0.523801
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.99it/s]
[5] test loss: 0.153194
test segmentation accuracy: 0.886810
test box IoU(ground/3D): 0.735686/0.684101
test box estimation accuracy (IoU=0.7): 0.629446
learning rate: 0.001000
Best Test acc: 0.629446(Epoch 5)
**** EPOCH 006 ****
Epoch 6/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:18<00:00,  7.15it/s]
[6: 1849/1850] train loss: 0.162520
segmentation accuracy: 0.895404
box IoU(ground/3D): 0.713199/0.654376
box estimation accuracy (IoU=0.7): 0.552280
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.10it/s]
[6] test loss: 0.128388
test segmentation accuracy: 0.893996
test box IoU(ground/3D): 0.746396/0.691658
test box estimation accuracy (IoU=0.7): 0.658558
learning rate: 0.001000
Best Test acc: 0.658558(Epoch 6)
**** EPOCH 007 ****
Epoch 7/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.14it/s]
[7: 1849/1850] train loss: 0.155853
segmentation accuracy: 0.899121
box IoU(ground/3D): 0.723719/0.664533
box estimation accuracy (IoU=0.7): 0.579341
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.11it/s]
[7] test loss: 0.138296
test segmentation accuracy: 0.886223
test box IoU(ground/3D): 0.736086/0.681760
test box estimation accuracy (IoU=0.7): 0.635588
learning rate: 0.001000
Best Test acc: 0.658558(Epoch 6)
**** EPOCH 008 ****
Epoch 8/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:18<00:00,  7.14it/s]
[8: 1849/1850] train loss: 0.143444
segmentation accuracy: 0.902437
box IoU(ground/3D): 0.733990/0.674648
box estimation accuracy (IoU=0.7): 0.606892
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.12it/s]
[8] test loss: 0.132945
test segmentation accuracy: 0.888252
test box IoU(ground/3D): 0.741826/0.685422
test box estimation accuracy (IoU=0.7): 0.641729
learning rate: 0.001000
Best Test acc: 0.658558(Epoch 6)
**** EPOCH 009 ****
Epoch 9/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.12it/s]
[9: 1849/1850] train loss: 0.136389
segmentation accuracy: 0.905435
box IoU(ground/3D): 0.740582/0.681106
box estimation accuracy (IoU=0.7): 0.623429
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.14it/s]
[9] test loss: 0.123400
test segmentation accuracy: 0.893627
test box IoU(ground/3D): 0.747169/0.692446
test box estimation accuracy (IoU=0.7): 0.660711
learning rate: 0.001000
Best Test acc: 0.660711(Epoch 9)
**** EPOCH 010 ****
Epoch 10/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.04it/s]
[10: 1849/1850] train loss: 0.133633
segmentation accuracy: 0.907655
box IoU(ground/3D): 0.745320/0.685888
box estimation accuracy (IoU=0.7): 0.636351
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.07it/s]
[10] test loss: 0.134007
test segmentation accuracy: 0.891398
test box IoU(ground/3D): 0.749841/0.694455
test box estimation accuracy (IoU=0.7): 0.659356
learning rate: 0.001000
Best Test acc: 0.660711(Epoch 9)
**** EPOCH 011 ****
Epoch 11/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.12it/s]
[11: 1849/1850] train loss: 0.129687
segmentation accuracy: 0.910192
box IoU(ground/3D): 0.749019/0.689716
box estimation accuracy (IoU=0.7): 0.646030
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[11] test loss: 0.145325
test segmentation accuracy: 0.891148
test box IoU(ground/3D): 0.744666/0.687673
test box estimation accuracy (IoU=0.7): 0.637183
learning rate: 0.001000
Best Test acc: 0.660711(Epoch 9)
**** EPOCH 012 ****
Epoch 12/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[12: 1849/1850] train loss: 0.124673
segmentation accuracy: 0.912120
box IoU(ground/3D): 0.754137/0.694571
box estimation accuracy (IoU=0.7): 0.659307
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.93it/s]
[12] test loss: 0.117987
test segmentation accuracy: 0.894800
test box IoU(ground/3D): 0.763921/0.709867
test box estimation accuracy (IoU=0.7): 0.681050
learning rate: 0.001000
Best Test acc: 0.681050(Epoch 12)
**** EPOCH 013 ****
Epoch 13/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.13it/s]
[13: 1849/1850] train loss: 0.118318
segmentation accuracy: 0.914031
box IoU(ground/3D): 0.757985/0.698696
box estimation accuracy (IoU=0.7): 0.669341
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.77it/s]
[13] test loss: 0.122204
test segmentation accuracy: 0.896091
test box IoU(ground/3D): 0.756661/0.701978
test box estimation accuracy (IoU=0.7): 0.676184
learning rate: 0.001000
Best Test acc: 0.681050(Epoch 12)
**** EPOCH 014 ****
Epoch 14/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:18<00:00,  7.16it/s]
[14: 1849/1850] train loss: 0.113008
segmentation accuracy: 0.916255
box IoU(ground/3D): 0.762097/0.702986
box estimation accuracy (IoU=0.7): 0.678209
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[14] test loss: 0.119275
test segmentation accuracy: 0.897464
test box IoU(ground/3D): 0.763601/0.704836
test box estimation accuracy (IoU=0.7): 0.666773
learning rate: 0.001000
Best Test acc: 0.681050(Epoch 12)
**** EPOCH 015 ****
Epoch 15/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[15: 1849/1850] train loss: 0.114317
segmentation accuracy: 0.917207
box IoU(ground/3D): 0.765559/0.706368
box estimation accuracy (IoU=0.7): 0.688074
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.12it/s]
[15] test loss: 0.125054
test segmentation accuracy: 0.898569
test box IoU(ground/3D): 0.744427/0.690791
test box estimation accuracy (IoU=0.7): 0.625937
learning rate: 0.001000
Best Test acc: 0.681050(Epoch 12)
**** EPOCH 016 ****
Epoch 16/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[16: 1849/1850] train loss: 0.108246
segmentation accuracy: 0.918099
box IoU(ground/3D): 0.768760/0.709376
box estimation accuracy (IoU=0.7): 0.695456
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.96it/s]
[16] test loss: 0.110245
test segmentation accuracy: 0.898693
test box IoU(ground/3D): 0.767133/0.713990
test box estimation accuracy (IoU=0.7): 0.697719
learning rate: 0.001000
Best Test acc: 0.697719(Epoch 16)
**** EPOCH 017 ****
Epoch 17/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[17: 1849/1850] train loss: 0.104207
segmentation accuracy: 0.920058
box IoU(ground/3D): 0.772108/0.712466
box estimation accuracy (IoU=0.7): 0.699848
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.01it/s]
[17] test loss: 0.121243
test segmentation accuracy: 0.897715
test box IoU(ground/3D): 0.768023/0.711730
test box estimation accuracy (IoU=0.7): 0.695725
learning rate: 0.001000
Best Test acc: 0.697719(Epoch 16)
**** EPOCH 018 ****
Epoch 18/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[18: 1849/1850] train loss: 0.103013
segmentation accuracy: 0.921896
box IoU(ground/3D): 0.774542/0.715066
box estimation accuracy (IoU=0.7): 0.706976
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.12it/s]
[18] test loss: 0.128597
test segmentation accuracy: 0.896579
test box IoU(ground/3D): 0.761987/0.708149
test box estimation accuracy (IoU=0.7): 0.690142
learning rate: 0.001000
Best Test acc: 0.697719(Epoch 16)
**** EPOCH 019 ****
Epoch 19/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[19: 1849/1850] train loss: 0.098745
segmentation accuracy: 0.922570
box IoU(ground/3D): 0.776172/0.717343
box estimation accuracy (IoU=0.7): 0.714797
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.13it/s]
[19] test loss: 0.123762
test segmentation accuracy: 0.895499
test box IoU(ground/3D): 0.765082/0.707945
test box estimation accuracy (IoU=0.7): 0.697878
learning rate: 0.001000
Best Test acc: 0.697878(Epoch 19)
**** EPOCH 020 ****
Epoch 20/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.12it/s]
[20: 1849/1850] train loss: 0.097091
segmentation accuracy: 0.923575
box IoU(ground/3D): 0.778524/0.719459
box estimation accuracy (IoU=0.7): 0.717348
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[20] test loss: 0.120986
test segmentation accuracy: 0.899702
test box IoU(ground/3D): 0.775488/0.720270
test box estimation accuracy (IoU=0.7): 0.714069
learning rate: 0.001000
Best Test acc: 0.714069(Epoch 20)
**** EPOCH 021 ****
Epoch 21/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[21: 1849/1850] train loss: 0.088731
segmentation accuracy: 0.927686
box IoU(ground/3D): 0.787744/0.729397
box estimation accuracy (IoU=0.7): 0.741301
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.12it/s]
[21] test loss: 0.116820
test segmentation accuracy: 0.900842
test box IoU(ground/3D): 0.772717/0.718861
test box estimation accuracy (IoU=0.7): 0.709523
learning rate: 0.000700
Best Test acc: 0.714069(Epoch 20)
**** EPOCH 022 ****
Epoch 22/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.09it/s]
[22: 1849/1850] train loss: 0.086742
segmentation accuracy: 0.928774
box IoU(ground/3D): 0.790815/0.732240
box estimation accuracy (IoU=0.7): 0.748243
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[22] test loss: 0.112803
test segmentation accuracy: 0.900126
test box IoU(ground/3D): 0.773802/0.720146
test box estimation accuracy (IoU=0.7): 0.717658
learning rate: 0.000700
Best Test acc: 0.717658(Epoch 22)
**** EPOCH 023 ****
Epoch 23/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[23: 1849/1850] train loss: 0.087288
segmentation accuracy: 0.929670
box IoU(ground/3D): 0.792494/0.734144
box estimation accuracy (IoU=0.7): 0.753243
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[23] test loss: 0.116226
test segmentation accuracy: 0.899745
test box IoU(ground/3D): 0.778652/0.726306
test box estimation accuracy (IoU=0.7): 0.727468
learning rate: 0.000700
Best Test acc: 0.727468(Epoch 23)
**** EPOCH 024 ****
Epoch 24/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[24: 1849/1850] train loss: 0.084605
segmentation accuracy: 0.930595
box IoU(ground/3D): 0.794113/0.735817
box estimation accuracy (IoU=0.7): 0.756064
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.07it/s]
[24] test loss: 0.110040
test segmentation accuracy: 0.900687
test box IoU(ground/3D): 0.773490/0.721154
test box estimation accuracy (IoU=0.7): 0.712394
learning rate: 0.000700
Best Test acc: 0.727468(Epoch 23)
**** EPOCH 025 ****
Epoch 25/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:18<00:00,  7.14it/s]
[25: 1849/1850] train loss: 0.082303
segmentation accuracy: 0.931464
box IoU(ground/3D): 0.794772/0.736584
box estimation accuracy (IoU=0.7): 0.758125
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.12it/s]
[25] test loss: 0.110114
test segmentation accuracy: 0.899217
test box IoU(ground/3D): 0.781357/0.729358
test box estimation accuracy (IoU=0.7): 0.738555
learning rate: 0.000700
Best Test acc: 0.738555(Epoch 25)
**** EPOCH 026 ****
Epoch 26/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:18<00:00,  7.15it/s]
[26: 1849/1850] train loss: 0.080520
segmentation accuracy: 0.932279
box IoU(ground/3D): 0.797231/0.739405
box estimation accuracy (IoU=0.7): 0.764595
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.07it/s]
[26] test loss: 0.117986
test segmentation accuracy: 0.900658
test box IoU(ground/3D): 0.781338/0.727908
test box estimation accuracy (IoU=0.7): 0.731377
learning rate: 0.000700
Best Test acc: 0.738555(Epoch 25)
**** EPOCH 027 ****
Epoch 27/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:30<00:00,  6.84it/s]
[27: 1849/1850] train loss: 0.081463
segmentation accuracy: 0.932699
box IoU(ground/3D): 0.798259/0.740172
box estimation accuracy (IoU=0.7): 0.767196
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.11it/s]
[27] test loss: 0.099032
test segmentation accuracy: 0.900032
test box IoU(ground/3D): 0.778822/0.726646
test box estimation accuracy (IoU=0.7): 0.729064
learning rate: 0.000700
Best Test acc: 0.738555(Epoch 25)
**** EPOCH 028 ****
Epoch 28/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[28: 1849/1850] train loss: 0.080119
segmentation accuracy: 0.932905
box IoU(ground/3D): 0.798407/0.740029
box estimation accuracy (IoU=0.7): 0.764848
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[28] test loss: 0.105146
test segmentation accuracy: 0.902678
test box IoU(ground/3D): 0.781253/0.728589
test box estimation accuracy (IoU=0.7): 0.728346
learning rate: 0.000700
Best Test acc: 0.738555(Epoch 25)
**** EPOCH 029 ****
Epoch 29/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[29: 1849/1850] train loss: 0.082880
segmentation accuracy: 0.934238
box IoU(ground/3D): 0.799954/0.741912
box estimation accuracy (IoU=0.7): 0.771064
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.07it/s]
[29] test loss: 0.110732
test segmentation accuracy: 0.899538
test box IoU(ground/3D): 0.780431/0.726479
test box estimation accuracy (IoU=0.7): 0.733849
learning rate: 0.000700
Best Test acc: 0.738555(Epoch 25)
**** EPOCH 030 ****
Epoch 30/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[30: 1849/1850] train loss: 0.079472
segmentation accuracy: 0.934221
box IoU(ground/3D): 0.800690/0.742476
box estimation accuracy (IoU=0.7): 0.771875
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.97it/s]
[30] test loss: 0.121557
test segmentation accuracy: 0.900993
test box IoU(ground/3D): 0.777782/0.726432
test box estimation accuracy (IoU=0.7): 0.738076
learning rate: 0.000700
Best Test acc: 0.738555(Epoch 25)
**** EPOCH 031 ****
Epoch 31/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:24<00:00,  6.99it/s]
[31: 1849/1850] train loss: 0.080034
segmentation accuracy: 0.934804
box IoU(ground/3D): 0.800704/0.742663
box estimation accuracy (IoU=0.7): 0.771824
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.88it/s]
[31] test loss: 0.111317
test segmentation accuracy: 0.895468
test box IoU(ground/3D): 0.775450/0.723215
test box estimation accuracy (IoU=0.7): 0.719971
learning rate: 0.000700
Best Test acc: 0.738555(Epoch 25)
**** EPOCH 032 ****
Epoch 32/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[32: 1849/1850] train loss: 0.082463
segmentation accuracy: 0.935600
box IoU(ground/3D): 0.801822/0.743647
box estimation accuracy (IoU=0.7): 0.773919
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[32] test loss: 0.107605
test segmentation accuracy: 0.894786
test box IoU(ground/3D): 0.784333/0.728910
test box estimation accuracy (IoU=0.7): 0.745653
learning rate: 0.000700
save to:log/default_caronly_kitti_2022-05-16-07/acc0.745653-epoch031.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.745653-epoch031.pth
Best Test acc: 0.745653(Epoch 32)
**** EPOCH 033 ****
Epoch 33/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[33: 1849/1850] train loss: 0.077336
segmentation accuracy: 0.936288
box IoU(ground/3D): 0.803115/0.745255
box estimation accuracy (IoU=0.7): 0.778446
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[33] test loss: 0.111027
test segmentation accuracy: 0.903085
test box IoU(ground/3D): 0.783506/0.730326
test box estimation accuracy (IoU=0.7): 0.734806
learning rate: 0.000700
Best Test acc: 0.745653(Epoch 32)
**** EPOCH 034 ****
Epoch 34/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[34: 1849/1850] train loss: 0.081078
segmentation accuracy: 0.936492
box IoU(ground/3D): 0.804096/0.746353
box estimation accuracy (IoU=0.7): 0.782855
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.04it/s]
[34] test loss: 0.123260
test segmentation accuracy: 0.899790
test box IoU(ground/3D): 0.783981/0.731076
test box estimation accuracy (IoU=0.7): 0.738236
learning rate: 0.000700
Best Test acc: 0.745653(Epoch 32)
**** EPOCH 035 ****
Epoch 35/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[35: 1849/1850] train loss: 0.080743
segmentation accuracy: 0.937148
box IoU(ground/3D): 0.804198/0.746285
box estimation accuracy (IoU=0.7): 0.780236
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.10it/s]
[35] test loss: 0.103205
test segmentation accuracy: 0.894717
test box IoU(ground/3D): 0.769912/0.716654
test box estimation accuracy (IoU=0.7): 0.701787
learning rate: 0.000700
Best Test acc: 0.745653(Epoch 32)
**** EPOCH 036 ****
Epoch 36/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[36: 1849/1850] train loss: 0.077761
segmentation accuracy: 0.937503
box IoU(ground/3D): 0.805660/0.747669
box estimation accuracy (IoU=0.7): 0.783666
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[36] test loss: 0.105402
test segmentation accuracy: 0.900969
test box IoU(ground/3D): 0.786098/0.733026
test box estimation accuracy (IoU=0.7): 0.746052
learning rate: 0.000700
save to:log/default_caronly_kitti_2022-05-16-07/acc0.746052-epoch035.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.746052-epoch035.pth
Best Test acc: 0.746052(Epoch 36)
**** EPOCH 037 ****
Epoch 37/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.05it/s]
[37: 1849/1850] train loss: 0.077258
segmentation accuracy: 0.938199
box IoU(ground/3D): 0.805904/0.748477
box estimation accuracy (IoU=0.7): 0.786098
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.93it/s]
[37] test loss: 0.112284
test segmentation accuracy: 0.899765
test box IoU(ground/3D): 0.767243/0.707394
test box estimation accuracy (IoU=0.7): 0.694210
learning rate: 0.000700
Best Test acc: 0.746052(Epoch 36)
**** EPOCH 038 ****
Epoch 38/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.04it/s]
[38: 1849/1850] train loss: 0.075681
segmentation accuracy: 0.938449
box IoU(ground/3D): 0.806419/0.748475
box estimation accuracy (IoU=0.7): 0.786132
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.85it/s]
[38] test loss: 0.115546
test segmentation accuracy: 0.896376
test box IoU(ground/3D): 0.779966/0.723737
test box estimation accuracy (IoU=0.7): 0.721327
learning rate: 0.000700
Best Test acc: 0.746052(Epoch 36)
**** EPOCH 039 ****
Epoch 39/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[39: 1849/1850] train loss: 0.076774
segmentation accuracy: 0.939013
box IoU(ground/3D): 0.806441/0.748897
box estimation accuracy (IoU=0.7): 0.785980
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.12it/s]
[39] test loss: 0.114761
test segmentation accuracy: 0.898836
test box IoU(ground/3D): 0.780167/0.727318
test box estimation accuracy (IoU=0.7): 0.729622
learning rate: 0.000700
Best Test acc: 0.746052(Epoch 36)
**** EPOCH 040 ****
Epoch 40/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[40: 1849/1850] train loss: 0.075658
segmentation accuracy: 0.939391
box IoU(ground/3D): 0.807509/0.749974
box estimation accuracy (IoU=0.7): 0.788615
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.10it/s]
[40] test loss: 0.106414
test segmentation accuracy: 0.902527
test box IoU(ground/3D): 0.783071/0.731324
test box estimation accuracy (IoU=0.7): 0.741665
learning rate: 0.000700
Best Test acc: 0.746052(Epoch 36)
**** EPOCH 041 ****
Epoch 41/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[41: 1849/1850] train loss: 0.069408
segmentation accuracy: 0.942241
box IoU(ground/3D): 0.813702/0.756664
box estimation accuracy (IoU=0.7): 0.803294
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[41] test loss: 0.106283
test segmentation accuracy: 0.900429
test box IoU(ground/3D): 0.786374/0.734913
test box estimation accuracy (IoU=0.7): 0.746212
learning rate: 0.000490
save to:log/default_caronly_kitti_2022-05-16-07/acc0.746212-epoch040.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.746212-epoch040.pth
Best Test acc: 0.746212(Epoch 41)
**** EPOCH 042 ****
Epoch 42/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[42: 1849/1850] train loss: 0.072207
segmentation accuracy: 0.942392
box IoU(ground/3D): 0.813975/0.756673
box estimation accuracy (IoU=0.7): 0.802382
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[42] test loss: 0.118716
test segmentation accuracy: 0.903401
test box IoU(ground/3D): 0.785012/0.730591
test box estimation accuracy (IoU=0.7): 0.737917
learning rate: 0.000490
Best Test acc: 0.746212(Epoch 41)
**** EPOCH 043 ****
Epoch 43/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[43: 1849/1850] train loss: 0.070530
segmentation accuracy: 0.942937
box IoU(ground/3D): 0.815202/0.758044
box estimation accuracy (IoU=0.7): 0.806588
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.84it/s]
[43] test loss: 0.113972
test segmentation accuracy: 0.902106
test box IoU(ground/3D): 0.786652/0.735343
test box estimation accuracy (IoU=0.7): 0.749083
learning rate: 0.000490
save to:log/default_caronly_kitti_2022-05-16-07/acc0.749083-epoch042.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.749083-epoch042.pth
Best Test acc: 0.749083(Epoch 43)
**** EPOCH 044 ****
Epoch 44/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.14it/s]
[44: 1849/1850] train loss: 0.072709
segmentation accuracy: 0.943476
box IoU(ground/3D): 0.816121/0.759358
box estimation accuracy (IoU=0.7): 0.809916
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.18it/s]
[44] test loss: 0.106297
test segmentation accuracy: 0.900822
test box IoU(ground/3D): 0.786719/0.733531
test box estimation accuracy (IoU=0.7): 0.749402
learning rate: 0.000490
save to:log/default_caronly_kitti_2022-05-16-07/acc0.749402-epoch043.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.749402-epoch043.pth
Best Test acc: 0.749402(Epoch 44)
**** EPOCH 045 ****
Epoch 45/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[45: 1849/1850] train loss: 0.067621
segmentation accuracy: 0.944022
box IoU(ground/3D): 0.816793/0.759793
box estimation accuracy (IoU=0.7): 0.810693
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[45] test loss: 0.102931
test segmentation accuracy: 0.901816
test box IoU(ground/3D): 0.782193/0.728931
test box estimation accuracy (IoU=0.7): 0.731217
learning rate: 0.000490
Best Test acc: 0.749402(Epoch 44)
**** EPOCH 046 ****
Epoch 46/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.06it/s]
[46: 1849/1850] train loss: 0.067756
segmentation accuracy: 0.944218
box IoU(ground/3D): 0.816937/0.759865
box estimation accuracy (IoU=0.7): 0.810625
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.02it/s]
[46] test loss: 0.104917
test segmentation accuracy: 0.898912
test box IoU(ground/3D): 0.777677/0.724965
test box estimation accuracy (IoU=0.7): 0.730260
learning rate: 0.000490
Best Test acc: 0.749402(Epoch 44)
**** EPOCH 047 ****
Epoch 47/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.12it/s]
[47: 1849/1850] train loss: 0.069445
segmentation accuracy: 0.944657
box IoU(ground/3D): 0.817592/0.760680
box estimation accuracy (IoU=0.7): 0.813412
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[47] test loss: 0.098740
test segmentation accuracy: 0.904578
test box IoU(ground/3D): 0.783517/0.731129
test box estimation accuracy (IoU=0.7): 0.738794
learning rate: 0.000490
Best Test acc: 0.749402(Epoch 44)
**** EPOCH 048 ****
Epoch 48/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.12it/s]
[48: 1849/1850] train loss: 0.066967
segmentation accuracy: 0.944239
box IoU(ground/3D): 0.817726/0.760872
box estimation accuracy (IoU=0.7): 0.814020
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.98it/s]
[48] test loss: 0.101989
test segmentation accuracy: 0.901837
test box IoU(ground/3D): 0.786851/0.736278
test box estimation accuracy (IoU=0.7): 0.750518
learning rate: 0.000490
save to:log/default_caronly_kitti_2022-05-16-07/acc0.750518-epoch047.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.750518-epoch047.pth
Best Test acc: 0.750518(Epoch 48)
**** EPOCH 049 ****
Epoch 49/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.05it/s]
[49: 1849/1850] train loss: 0.068923
segmentation accuracy: 0.945112
box IoU(ground/3D): 0.817568/0.760720
box estimation accuracy (IoU=0.7): 0.813497
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.99it/s]
[49] test loss: 0.105625
test segmentation accuracy: 0.899709
test box IoU(ground/3D): 0.784026/0.732379
test box estimation accuracy (IoU=0.7): 0.749163
learning rate: 0.000490
Best Test acc: 0.750518(Epoch 48)
**** EPOCH 050 ****
Epoch 50/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.09it/s]
[50: 1849/1850] train loss: 0.067223
segmentation accuracy: 0.945213
box IoU(ground/3D): 0.818639/0.761725
box estimation accuracy (IoU=0.7): 0.814578
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.13it/s]
[50] test loss: 0.109784
test segmentation accuracy: 0.901877
test box IoU(ground/3D): 0.792428/0.738100
test box estimation accuracy (IoU=0.7): 0.753948
learning rate: 0.000490
save to:log/default_caronly_kitti_2022-05-16-07/acc0.753948-epoch049.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.753948-epoch049.pth
Best Test acc: 0.753948(Epoch 50)
**** EPOCH 051 ****
Epoch 51/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[51: 1849/1850] train loss: 0.068736
segmentation accuracy: 0.945302
box IoU(ground/3D): 0.819346/0.762205
box estimation accuracy (IoU=0.7): 0.816132
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.04it/s]
[51] test loss: 0.113222
test segmentation accuracy: 0.905177
test box IoU(ground/3D): 0.761956/0.706617
test box estimation accuracy (IoU=0.7): 0.685596
learning rate: 0.000490
Best Test acc: 0.753948(Epoch 50)
**** EPOCH 052 ****
Epoch 52/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[52: 1849/1850] train loss: 0.066456
segmentation accuracy: 0.945868
box IoU(ground/3D): 0.819956/0.763292
box estimation accuracy (IoU=0.7): 0.817855
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.08it/s]
[52] test loss: 0.109616
test segmentation accuracy: 0.899912
test box IoU(ground/3D): 0.769750/0.714589
test box estimation accuracy (IoU=0.7): 0.700112
learning rate: 0.000490
Best Test acc: 0.753948(Epoch 50)
**** EPOCH 053 ****
Epoch 53/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.04it/s]
[53: 1849/1850] train loss: 0.068806
segmentation accuracy: 0.945937
box IoU(ground/3D): 0.819447/0.762570
box estimation accuracy (IoU=0.7): 0.817905
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.08it/s]
[53] test loss: 0.111854
test segmentation accuracy: 0.900346
test box IoU(ground/3D): 0.784135/0.733292
test box estimation accuracy (IoU=0.7): 0.744377
learning rate: 0.000490
Best Test acc: 0.753948(Epoch 50)
**** EPOCH 054 ****
Epoch 54/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[54: 1849/1850] train loss: 0.069278
segmentation accuracy: 0.946426
box IoU(ground/3D): 0.820083/0.763449
box estimation accuracy (IoU=0.7): 0.819611
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.08it/s]
[54] test loss: 0.103617
test segmentation accuracy: 0.898957
test box IoU(ground/3D): 0.783287/0.731704
test box estimation accuracy (IoU=0.7): 0.743899
learning rate: 0.000490
Best Test acc: 0.753948(Epoch 50)
**** EPOCH 055 ****
Epoch 55/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[55: 1849/1850] train loss: 0.067026
segmentation accuracy: 0.946619
box IoU(ground/3D): 0.820012/0.763202
box estimation accuracy (IoU=0.7): 0.817416
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.04it/s]
[55] test loss: 0.102553
test segmentation accuracy: 0.901091
test box IoU(ground/3D): 0.782064/0.728833
test box estimation accuracy (IoU=0.7): 0.739352
learning rate: 0.000490
Best Test acc: 0.753948(Epoch 50)
**** EPOCH 056 ****
Epoch 56/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.05it/s]
[56: 1849/1850] train loss: 0.064853
segmentation accuracy: 0.947072
box IoU(ground/3D): 0.821595/0.764836
box estimation accuracy (IoU=0.7): 0.821605
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.04it/s]
[56] test loss: 0.110458
test segmentation accuracy: 0.901783
test box IoU(ground/3D): 0.772748/0.719699
test box estimation accuracy (IoU=0.7): 0.715585
learning rate: 0.000490
Best Test acc: 0.753948(Epoch 50)
**** EPOCH 057 ****
Epoch 57/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[57: 1849/1850] train loss: 0.065467
segmentation accuracy: 0.947139
box IoU(ground/3D): 0.821344/0.764182
box estimation accuracy (IoU=0.7): 0.820929
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.14it/s]
[57] test loss: 0.110381
test segmentation accuracy: 0.896594
test box IoU(ground/3D): 0.784615/0.732811
test box estimation accuracy (IoU=0.7): 0.747567
learning rate: 0.000490
Best Test acc: 0.753948(Epoch 50)
**** EPOCH 058 ****
Epoch 58/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.04it/s]
[58: 1849/1850] train loss: 0.066785
segmentation accuracy: 0.947472
box IoU(ground/3D): 0.821134/0.764769
box estimation accuracy (IoU=0.7): 0.822500
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[58] test loss: 0.116557
test segmentation accuracy: 0.896590
test box IoU(ground/3D): 0.789160/0.737002
test box estimation accuracy (IoU=0.7): 0.756660
learning rate: 0.000490
save to:log/default_caronly_kitti_2022-05-16-07/acc0.756660-epoch057.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.756660-epoch057.pth
Best Test acc: 0.756660(Epoch 58)
**** EPOCH 059 ****
Epoch 59/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[59: 1849/1850] train loss: 0.065802
segmentation accuracy: 0.947238
box IoU(ground/3D): 0.822129/0.765116
box estimation accuracy (IoU=0.7): 0.825507
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[59] test loss: 0.111934
test segmentation accuracy: 0.902622
test box IoU(ground/3D): 0.790468/0.739442
test box estimation accuracy (IoU=0.7): 0.758414
learning rate: 0.000490
save to:log/default_caronly_kitti_2022-05-16-07/acc0.758414-epoch058.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.758414-epoch058.pth
Best Test acc: 0.758414(Epoch 59)
**** EPOCH 060 ****
Epoch 60/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.06it/s]
[60: 1849/1850] train loss: 0.066521
segmentation accuracy: 0.947846
box IoU(ground/3D): 0.822367/0.765976
box estimation accuracy (IoU=0.7): 0.824122
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[60] test loss: 0.113417
test segmentation accuracy: 0.900610
test box IoU(ground/3D): 0.793336/0.741063
test box estimation accuracy (IoU=0.7): 0.763120
learning rate: 0.000490
save to:log/default_caronly_kitti_2022-05-16-07/acc0.763120-epoch059.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.763120-epoch059.pth
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 061 ****
Epoch 61/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.05it/s]
[61: 1849/1850] train loss: 0.064363
segmentation accuracy: 0.949297
box IoU(ground/3D): 0.825812/0.769710
box estimation accuracy (IoU=0.7): 0.831250
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.04it/s]
[61] test loss: 0.100989
test segmentation accuracy: 0.901647
test box IoU(ground/3D): 0.790449/0.739439
test box estimation accuracy (IoU=0.7): 0.758414
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 062 ****
Epoch 62/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.04it/s]
[62: 1849/1850] train loss: 0.063557
segmentation accuracy: 0.950192
box IoU(ground/3D): 0.826926/0.770597
box estimation accuracy (IoU=0.7): 0.835473
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.98it/s]
[62] test loss: 0.103889
test segmentation accuracy: 0.901566
test box IoU(ground/3D): 0.788946/0.737304
test box estimation accuracy (IoU=0.7): 0.750598
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 063 ****
Epoch 63/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:25<00:00,  6.96it/s]
[63: 1849/1850] train loss: 0.061244
segmentation accuracy: 0.949946
box IoU(ground/3D): 0.827760/0.771694
box estimation accuracy (IoU=0.7): 0.837162
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.01it/s]
[63] test loss: 0.104783
test segmentation accuracy: 0.901676
test box IoU(ground/3D): 0.781984/0.728867
test box estimation accuracy (IoU=0.7): 0.729462
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 064 ****
Epoch 64/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[64: 1849/1850] train loss: 0.063504
segmentation accuracy: 0.950504
box IoU(ground/3D): 0.827727/0.771622
box estimation accuracy (IoU=0.7): 0.836419
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.10it/s]
[64] test loss: 0.109538
test segmentation accuracy: 0.902813
test box IoU(ground/3D): 0.777299/0.722428
test box estimation accuracy (IoU=0.7): 0.718855
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 065 ****
Epoch 65/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.09it/s]
[65: 1849/1850] train loss: 0.062326
segmentation accuracy: 0.950672
box IoU(ground/3D): 0.827757/0.771501
box estimation accuracy (IoU=0.7): 0.835811
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[65] test loss: 0.097166
test segmentation accuracy: 0.901838
test box IoU(ground/3D): 0.791538/0.739987
test box estimation accuracy (IoU=0.7): 0.757697
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 066 ****
Epoch 66/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[66: 1849/1850] train loss: 0.062982
segmentation accuracy: 0.950723
box IoU(ground/3D): 0.828307/0.772080
box estimation accuracy (IoU=0.7): 0.837399
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[66] test loss: 0.106278
test segmentation accuracy: 0.901984
test box IoU(ground/3D): 0.789503/0.738616
test box estimation accuracy (IoU=0.7): 0.754666
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 067 ****
Epoch 67/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[67: 1849/1850] train loss: 0.059764
segmentation accuracy: 0.950910
box IoU(ground/3D): 0.828357/0.772318
box estimation accuracy (IoU=0.7): 0.838057
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[67] test loss: 0.101939
test segmentation accuracy: 0.902203
test box IoU(ground/3D): 0.776213/0.724055
test box estimation accuracy (IoU=0.7): 0.723481
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 068 ****
Epoch 68/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[68: 1849/1850] train loss: 0.061874
segmentation accuracy: 0.951050
box IoU(ground/3D): 0.829533/0.773586
box estimation accuracy (IoU=0.7): 0.840270
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.07it/s]
[68] test loss: 0.102088
test segmentation accuracy: 0.901291
test box IoU(ground/3D): 0.789671/0.738963
test box estimation accuracy (IoU=0.7): 0.754905
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 069 ****
Epoch 69/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[69: 1849/1850] train loss: 0.060380
segmentation accuracy: 0.951344
box IoU(ground/3D): 0.828928/0.773027
box estimation accuracy (IoU=0.7): 0.839865
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.00it/s]
[69] test loss: 0.110420
test segmentation accuracy: 0.902100
test box IoU(ground/3D): 0.790405/0.739802
test box estimation accuracy (IoU=0.7): 0.760089
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 070 ****
Epoch 70/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.06it/s]
[70: 1849/1850] train loss: 0.058831
segmentation accuracy: 0.951302
box IoU(ground/3D): 0.829731/0.773406
box estimation accuracy (IoU=0.7): 0.841926
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.91it/s]
[70] test loss: 0.107716
test segmentation accuracy: 0.898979
test box IoU(ground/3D): 0.791924/0.738450
test box estimation accuracy (IoU=0.7): 0.756181
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 071 ****
Epoch 71/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[71: 1849/1850] train loss: 0.062009
segmentation accuracy: 0.951392
box IoU(ground/3D): 0.829418/0.773404
box estimation accuracy (IoU=0.7): 0.840557
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[71] test loss: 0.096762
test segmentation accuracy: 0.902639
test box IoU(ground/3D): 0.792882/0.740960
test box estimation accuracy (IoU=0.7): 0.758813
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 072 ****
Epoch 72/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.13it/s]
[72: 1849/1850] train loss: 0.059264
segmentation accuracy: 0.951889
box IoU(ground/3D): 0.829882/0.774001
box estimation accuracy (IoU=0.7): 0.843361
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.97it/s]
[72] test loss: 0.100538
test segmentation accuracy: 0.900167
test box IoU(ground/3D): 0.791883/0.740429
test box estimation accuracy (IoU=0.7): 0.758893
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 073 ****
Epoch 73/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.09it/s]
[73: 1849/1850] train loss: 0.059900
segmentation accuracy: 0.952048
box IoU(ground/3D): 0.830311/0.774637
box estimation accuracy (IoU=0.7): 0.844983
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.07it/s]
[73] test loss: 0.097025
test segmentation accuracy: 0.902642
test box IoU(ground/3D): 0.788858/0.737092
test box estimation accuracy (IoU=0.7): 0.753469
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 074 ****
Epoch 74/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[74: 1849/1850] train loss: 0.060180
segmentation accuracy: 0.951855
box IoU(ground/3D): 0.830381/0.774280
box estimation accuracy (IoU=0.7): 0.843564
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.93it/s]
[74] test loss: 0.102991
test segmentation accuracy: 0.902032
test box IoU(ground/3D): 0.789982/0.739656
test box estimation accuracy (IoU=0.7): 0.760408
learning rate: 0.000343
Best Test acc: 0.763120(Epoch 60)
**** EPOCH 075 ****
Epoch 75/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.09it/s]
[75: 1849/1850] train loss: 0.057197
segmentation accuracy: 0.952179
box IoU(ground/3D): 0.830817/0.774697
box estimation accuracy (IoU=0.7): 0.843125
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.89it/s]
[75] test loss: 0.099625
test segmentation accuracy: 0.902218
test box IoU(ground/3D): 0.793962/0.742907
test box estimation accuracy (IoU=0.7): 0.766709
learning rate: 0.000343
save to:log/default_caronly_kitti_2022-05-16-07/acc0.766709-epoch074.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.766709-epoch074.pth
Best Test acc: 0.766709(Epoch 75)
**** EPOCH 076 ****
Epoch 76/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[76: 1849/1850] train loss: 0.061349
segmentation accuracy: 0.952375
box IoU(ground/3D): 0.830570/0.774619
box estimation accuracy (IoU=0.7): 0.845152
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.02it/s]
[76] test loss: 0.117243
test segmentation accuracy: 0.902161
test box IoU(ground/3D): 0.755284/0.702458
test box estimation accuracy (IoU=0.7): 0.673313
learning rate: 0.000343
Best Test acc: 0.766709(Epoch 75)
**** EPOCH 077 ****
Epoch 77/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[77: 1849/1850] train loss: 0.060721
segmentation accuracy: 0.952292
box IoU(ground/3D): 0.830837/0.774991
box estimation accuracy (IoU=0.7): 0.845068
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.08it/s]
[77] test loss: 0.107981
test segmentation accuracy: 0.902158
test box IoU(ground/3D): 0.779299/0.727299
test box estimation accuracy (IoU=0.7): 0.728745
learning rate: 0.000343
Best Test acc: 0.766709(Epoch 75)
**** EPOCH 078 ****
Epoch 78/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.06it/s]
[78: 1849/1850] train loss: 0.061191
segmentation accuracy: 0.952835
box IoU(ground/3D): 0.831053/0.775281
box estimation accuracy (IoU=0.7): 0.846301
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.10it/s]
[78] test loss: 0.112345
test segmentation accuracy: 0.898872
test box IoU(ground/3D): 0.786956/0.735501
test box estimation accuracy (IoU=0.7): 0.750120
learning rate: 0.000343
Best Test acc: 0.766709(Epoch 75)
**** EPOCH 079 ****
Epoch 79/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[79: 1849/1850] train loss: 0.061751
segmentation accuracy: 0.952619
box IoU(ground/3D): 0.831022/0.775181
box estimation accuracy (IoU=0.7): 0.845541
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[79] test loss: 0.097385
test segmentation accuracy: 0.899126
test box IoU(ground/3D): 0.790048/0.737918
test box estimation accuracy (IoU=0.7): 0.753230
learning rate: 0.000343
Best Test acc: 0.766709(Epoch 75)
**** EPOCH 080 ****
Epoch 80/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[80: 1849/1850] train loss: 0.058795
segmentation accuracy: 0.952776
box IoU(ground/3D): 0.831421/0.775452
box estimation accuracy (IoU=0.7): 0.846791
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.01it/s]
[80] test loss: 0.099641
test segmentation accuracy: 0.900853
test box IoU(ground/3D): 0.793389/0.741221
test box estimation accuracy (IoU=0.7): 0.763758
learning rate: 0.000343
Best Test acc: 0.766709(Epoch 75)
**** EPOCH 081 ****
Epoch 81/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[81: 1849/1850] train loss: 0.058274
segmentation accuracy: 0.953986
box IoU(ground/3D): 0.834521/0.779009
box estimation accuracy (IoU=0.7): 0.852483
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.02it/s]
[81] test loss: 0.101401
test segmentation accuracy: 0.901668
test box IoU(ground/3D): 0.793859/0.742707
test box estimation accuracy (IoU=0.7): 0.762402
learning rate: 0.000240
Best Test acc: 0.766709(Epoch 75)
**** EPOCH 082 ****
Epoch 82/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[82: 1849/1850] train loss: 0.057385
segmentation accuracy: 0.953935
box IoU(ground/3D): 0.834817/0.779188
box estimation accuracy (IoU=0.7): 0.853598
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.89it/s]
[82] test loss: 0.100929
test segmentation accuracy: 0.902640
test box IoU(ground/3D): 0.796401/0.744612
test box estimation accuracy (IoU=0.7): 0.766071
learning rate: 0.000240
Best Test acc: 0.766709(Epoch 75)
**** EPOCH 083 ****
Epoch 83/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.06it/s]
[83: 1849/1850] train loss: 0.058047
segmentation accuracy: 0.954575
box IoU(ground/3D): 0.835328/0.779957
box estimation accuracy (IoU=0.7): 0.855236
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[83] test loss: 0.104010
test segmentation accuracy: 0.900674
test box IoU(ground/3D): 0.793247/0.742005
test box estimation accuracy (IoU=0.7): 0.765353
learning rate: 0.000240
Best Test acc: 0.766709(Epoch 75)
**** EPOCH 084 ****
Epoch 84/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[84: 1849/1850] train loss: 0.058531
segmentation accuracy: 0.954492
box IoU(ground/3D): 0.834898/0.779330
box estimation accuracy (IoU=0.7): 0.855743
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[84] test loss: 0.102425
test segmentation accuracy: 0.903231
test box IoU(ground/3D): 0.796036/0.744591
test box estimation accuracy (IoU=0.7): 0.771574
learning rate: 0.000240
save to:log/default_caronly_kitti_2022-05-16-07/acc0.771574-epoch083.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.771574-epoch083.pth
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 085 ****
Epoch 85/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.05it/s]
[85: 1849/1850] train loss: 0.058702
segmentation accuracy: 0.954660
box IoU(ground/3D): 0.835369/0.779727
box estimation accuracy (IoU=0.7): 0.855507
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.97it/s]
[85] test loss: 0.104511
test segmentation accuracy: 0.902756
test box IoU(ground/3D): 0.791692/0.740863
test box estimation accuracy (IoU=0.7): 0.761445
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 086 ****
Epoch 86/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[86: 1849/1850] train loss: 0.055951
segmentation accuracy: 0.954900
box IoU(ground/3D): 0.836370/0.780755
box estimation accuracy (IoU=0.7): 0.858395
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.04it/s]
[86] test loss: 0.103237
test segmentation accuracy: 0.904199
test box IoU(ground/3D): 0.793636/0.742338
test box estimation accuracy (IoU=0.7): 0.761764
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 087 ****
Epoch 87/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[87: 1849/1850] train loss: 0.057665
segmentation accuracy: 0.954688
box IoU(ground/3D): 0.835129/0.779678
box estimation accuracy (IoU=0.7): 0.854764
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.11it/s]
[87] test loss: 0.104749
test segmentation accuracy: 0.903175
test box IoU(ground/3D): 0.790823/0.740429
test box estimation accuracy (IoU=0.7): 0.763997
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 088 ****
Epoch 88/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[88: 1849/1850] train loss: 0.055124
segmentation accuracy: 0.954896
box IoU(ground/3D): 0.836431/0.780963
box estimation accuracy (IoU=0.7): 0.858378
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.07it/s]
[88] test loss: 0.117189
test segmentation accuracy: 0.901916
test box IoU(ground/3D): 0.793928/0.742876
test box estimation accuracy (IoU=0.7): 0.768703
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 089 ****
Epoch 89/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.12it/s]
[89: 1849/1850] train loss: 0.056968
segmentation accuracy: 0.955301
box IoU(ground/3D): 0.836305/0.780847
box estimation accuracy (IoU=0.7): 0.857483
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.11it/s]
[89] test loss: 0.107647
test segmentation accuracy: 0.901118
test box IoU(ground/3D): 0.791710/0.741039
test box estimation accuracy (IoU=0.7): 0.762881
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 090 ****
Epoch 90/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[90: 1849/1850] train loss: 0.059433
segmentation accuracy: 0.955231
box IoU(ground/3D): 0.836981/0.781368
box estimation accuracy (IoU=0.7): 0.858851
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.02it/s]
[90] test loss: 0.105569
test segmentation accuracy: 0.900796
test box IoU(ground/3D): 0.788074/0.736006
test box estimation accuracy (IoU=0.7): 0.753230
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 091 ****
Epoch 91/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[91: 1849/1850] train loss: 0.057501
segmentation accuracy: 0.955171
box IoU(ground/3D): 0.836310/0.780929
box estimation accuracy (IoU=0.7): 0.857416
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.15it/s]
[91] test loss: 0.105768
test segmentation accuracy: 0.901025
test box IoU(ground/3D): 0.790146/0.738910
test box estimation accuracy (IoU=0.7): 0.755224
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 092 ****
Epoch 92/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[92: 1849/1850] train loss: 0.056335
segmentation accuracy: 0.955389
box IoU(ground/3D): 0.836619/0.781019
box estimation accuracy (IoU=0.7): 0.857264
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.07it/s]
[92] test loss: 0.102768
test segmentation accuracy: 0.903867
test box IoU(ground/3D): 0.792928/0.741421
test box estimation accuracy (IoU=0.7): 0.762402
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 093 ****
Epoch 93/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[93: 1849/1850] train loss: 0.055386
segmentation accuracy: 0.955522
box IoU(ground/3D): 0.837153/0.781806
box estimation accuracy (IoU=0.7): 0.861081
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.12it/s]
[93] test loss: 0.098990
test segmentation accuracy: 0.902419
test box IoU(ground/3D): 0.795385/0.743734
test box estimation accuracy (IoU=0.7): 0.769182
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 094 ****
Epoch 94/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.12it/s]
[94: 1849/1850] train loss: 0.055726
segmentation accuracy: 0.955603
box IoU(ground/3D): 0.837047/0.781509
box estimation accuracy (IoU=0.7): 0.857500
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[94] test loss: 0.104316
test segmentation accuracy: 0.903889
test box IoU(ground/3D): 0.795135/0.743594
test box estimation accuracy (IoU=0.7): 0.768863
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 095 ****
Epoch 95/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[95: 1849/1850] train loss: 0.055012
segmentation accuracy: 0.955824
box IoU(ground/3D): 0.837525/0.781918
box estimation accuracy (IoU=0.7): 0.860422
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.10it/s]
[95] test loss: 0.105023
test segmentation accuracy: 0.900516
test box IoU(ground/3D): 0.792194/0.741075
test box estimation accuracy (IoU=0.7): 0.762402
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 096 ****
Epoch 96/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[96: 1849/1850] train loss: 0.054919
segmentation accuracy: 0.955723
box IoU(ground/3D): 0.837844/0.782224
box estimation accuracy (IoU=0.7): 0.861639
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.10it/s]
[96] test loss: 0.106925
test segmentation accuracy: 0.901819
test box IoU(ground/3D): 0.793324/0.742609
test box estimation accuracy (IoU=0.7): 0.762721
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 097 ****
Epoch 97/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.12it/s]
[97: 1849/1850] train loss: 0.055772
segmentation accuracy: 0.955924
box IoU(ground/3D): 0.837345/0.782003
box estimation accuracy (IoU=0.7): 0.859797
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.10it/s]
[97] test loss: 0.109855
test segmentation accuracy: 0.898722
test box IoU(ground/3D): 0.796216/0.744550
test box estimation accuracy (IoU=0.7): 0.768783
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 098 ****
Epoch 98/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.02it/s]
[98: 1849/1850] train loss: 0.056769
segmentation accuracy: 0.956113
box IoU(ground/3D): 0.837679/0.781912
box estimation accuracy (IoU=0.7): 0.859274
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.98it/s]
[98] test loss: 0.100210
test segmentation accuracy: 0.902532
test box IoU(ground/3D): 0.794565/0.743146
test box estimation accuracy (IoU=0.7): 0.764795
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 099 ****
Epoch 99/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[99: 1849/1850] train loss: 0.055439
segmentation accuracy: 0.956216
box IoU(ground/3D): 0.837621/0.782404
box estimation accuracy (IoU=0.7): 0.861132
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.07it/s]
[99] test loss: 0.096952
test segmentation accuracy: 0.903696
test box IoU(ground/3D): 0.793102/0.741760
test box estimation accuracy (IoU=0.7): 0.759052
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 100 ****
Epoch 100/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.06it/s]
[100: 1849/1850] train loss: 0.056561
segmentation accuracy: 0.956232
box IoU(ground/3D): 0.837776/0.782504
box estimation accuracy (IoU=0.7): 0.860828
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.12it/s]
[100] test loss: 0.104434
test segmentation accuracy: 0.903150
test box IoU(ground/3D): 0.794644/0.743294
test box estimation accuracy (IoU=0.7): 0.765912
learning rate: 0.000240
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 101 ****
Epoch 101/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.02it/s]
[101: 1849/1850] train loss: 0.054023
segmentation accuracy: 0.956832
box IoU(ground/3D): 0.839376/0.784344
box estimation accuracy (IoU=0.7): 0.865034
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.02it/s]
[101] test loss: 0.101064
test segmentation accuracy: 0.903149
test box IoU(ground/3D): 0.795769/0.744223
test box estimation accuracy (IoU=0.7): 0.768703
learning rate: 0.000168
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 102 ****
Epoch 102/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[102: 1849/1850] train loss: 0.057075
segmentation accuracy: 0.957136
box IoU(ground/3D): 0.839934/0.784795
box estimation accuracy (IoU=0.7): 0.866639
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.11it/s]
[102] test loss: 0.102307
test segmentation accuracy: 0.902735
test box IoU(ground/3D): 0.795440/0.744040
test box estimation accuracy (IoU=0.7): 0.767427
learning rate: 0.000168
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 103 ****
Epoch 103/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[103: 1849/1850] train loss: 0.054238
segmentation accuracy: 0.957146
box IoU(ground/3D): 0.840390/0.785202
box estimation accuracy (IoU=0.7): 0.867027
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.04it/s]
[103] test loss: 0.101822
test segmentation accuracy: 0.903913
test box IoU(ground/3D): 0.792408/0.741526
test box estimation accuracy (IoU=0.7): 0.760727
learning rate: 0.000168
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 104 ****
Epoch 104/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[104: 1849/1850] train loss: 0.054142
segmentation accuracy: 0.957336
box IoU(ground/3D): 0.840561/0.785461
box estimation accuracy (IoU=0.7): 0.866453
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.10it/s]
[104] test loss: 0.102289
test segmentation accuracy: 0.902533
test box IoU(ground/3D): 0.794938/0.743289
test box estimation accuracy (IoU=0.7): 0.766709
learning rate: 0.000168
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 105 ****
Epoch 105/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[105: 1849/1850] train loss: 0.052356
segmentation accuracy: 0.957549
box IoU(ground/3D): 0.841050/0.786214
box estimation accuracy (IoU=0.7): 0.869054
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.86it/s]
[105] test loss: 0.097068
test segmentation accuracy: 0.903831
test box IoU(ground/3D): 0.798077/0.746849
test box estimation accuracy (IoU=0.7): 0.771415
learning rate: 0.000168
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 106 ****
Epoch 106/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.02it/s]
[106: 1849/1850] train loss: 0.055490
segmentation accuracy: 0.957570
box IoU(ground/3D): 0.840800/0.785676
box estimation accuracy (IoU=0.7): 0.866554
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[106] test loss: 0.101896
test segmentation accuracy: 0.903161
test box IoU(ground/3D): 0.792977/0.741794
test box estimation accuracy (IoU=0.7): 0.763359
learning rate: 0.000168
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 107 ****
Epoch 107/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[107: 1849/1850] train loss: 0.052415
segmentation accuracy: 0.957489
box IoU(ground/3D): 0.841422/0.786542
box estimation accuracy (IoU=0.7): 0.869139
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.16it/s]
[107] test loss: 0.101655
test segmentation accuracy: 0.902626
test box IoU(ground/3D): 0.792173/0.740134
test box estimation accuracy (IoU=0.7): 0.758494
learning rate: 0.000168
Best Test acc: 0.771574(Epoch 84)
**** EPOCH 108 ****
Epoch 108/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[108: 1849/1850] train loss: 0.051491
segmentation accuracy: 0.957508
box IoU(ground/3D): 0.841365/0.786334
box estimation accuracy (IoU=0.7): 0.869831
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:44<00:00,  8.79it/s]
[108] test loss: 0.101123
test segmentation accuracy: 0.902195
test box IoU(ground/3D): 0.796995/0.745824
test box estimation accuracy (IoU=0.7): 0.772133
learning rate: 0.000168
save to:log/default_caronly_kitti_2022-05-16-07/acc0.772133-epoch107.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.772133-epoch107.pth
Best Test acc: 0.772133(Epoch 108)
**** EPOCH 109 ****
Epoch 109/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.12it/s]
[109: 1849/1850] train loss: 0.055415
segmentation accuracy: 0.957492
box IoU(ground/3D): 0.841351/0.786466
box estimation accuracy (IoU=0.7): 0.868497
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[109] test loss: 0.096937
test segmentation accuracy: 0.903030
test box IoU(ground/3D): 0.797552/0.746045
test box estimation accuracy (IoU=0.7): 0.768544
learning rate: 0.000168
Best Test acc: 0.772133(Epoch 108)
**** EPOCH 110 ****
Epoch 110/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[110: 1849/1850] train loss: 0.052353
segmentation accuracy: 0.957832
box IoU(ground/3D): 0.841531/0.786277
box estimation accuracy (IoU=0.7): 0.868429
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.14it/s]
[110] test loss: 0.110788
test segmentation accuracy: 0.897875
test box IoU(ground/3D): 0.794259/0.743109
test box estimation accuracy (IoU=0.7): 0.766709
learning rate: 0.000168
Best Test acc: 0.772133(Epoch 108)
**** EPOCH 111 ****
Epoch 111/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[111: 1849/1850] train loss: 0.052773
segmentation accuracy: 0.957826
box IoU(ground/3D): 0.841590/0.786817
box estimation accuracy (IoU=0.7): 0.870203
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.08it/s]
[111] test loss: 0.107333
test segmentation accuracy: 0.903588
test box IoU(ground/3D): 0.794378/0.743145
test box estimation accuracy (IoU=0.7): 0.767666
learning rate: 0.000168
Best Test acc: 0.772133(Epoch 108)
**** EPOCH 112 ****
Epoch 112/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[112: 1849/1850] train loss: 0.055448
segmentation accuracy: 0.957972
box IoU(ground/3D): 0.841234/0.786079
box estimation accuracy (IoU=0.7): 0.870693
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[112] test loss: 0.099275
test segmentation accuracy: 0.902857
test box IoU(ground/3D): 0.792702/0.741176
test box estimation accuracy (IoU=0.7): 0.761046
learning rate: 0.000168
Best Test acc: 0.772133(Epoch 108)
**** EPOCH 113 ****
Epoch 113/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[113: 1849/1850] train loss: 0.053511
segmentation accuracy: 0.957906
box IoU(ground/3D): 0.841566/0.786762
box estimation accuracy (IoU=0.7): 0.868801
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.07it/s]
[113] test loss: 0.100319
test segmentation accuracy: 0.901674
test box IoU(ground/3D): 0.792978/0.741862
test box estimation accuracy (IoU=0.7): 0.760169
learning rate: 0.000168
Best Test acc: 0.772133(Epoch 108)
**** EPOCH 114 ****
Epoch 114/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[114: 1849/1850] train loss: 0.054977
segmentation accuracy: 0.958005
box IoU(ground/3D): 0.841508/0.786494
box estimation accuracy (IoU=0.7): 0.871740
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[114] test loss: 0.105496
test segmentation accuracy: 0.903173
test box IoU(ground/3D): 0.795083/0.744401
test box estimation accuracy (IoU=0.7): 0.771176
learning rate: 0.000168
Best Test acc: 0.772133(Epoch 108)
**** EPOCH 115 ****
Epoch 115/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[115: 1849/1850] train loss: 0.052004
segmentation accuracy: 0.958091
box IoU(ground/3D): 0.842079/0.787122
box estimation accuracy (IoU=0.7): 0.870659
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.01it/s]
[115] test loss: 0.107036
test segmentation accuracy: 0.900605
test box IoU(ground/3D): 0.789342/0.737190
test box estimation accuracy (IoU=0.7): 0.754427
learning rate: 0.000168
Best Test acc: 0.772133(Epoch 108)
**** EPOCH 116 ****
Epoch 116/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.02it/s]
[116: 1849/1850] train loss: 0.052261
segmentation accuracy: 0.957931
box IoU(ground/3D): 0.841594/0.786873
box estimation accuracy (IoU=0.7): 0.870693
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.97it/s]
[116] test loss: 0.102206
test segmentation accuracy: 0.900920
test box IoU(ground/3D): 0.795261/0.744152
test box estimation accuracy (IoU=0.7): 0.767666
learning rate: 0.000168
Best Test acc: 0.772133(Epoch 108)
**** EPOCH 117 ****
Epoch 117/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.09it/s]
[117: 1849/1850] train loss: 0.050391
segmentation accuracy: 0.958419
box IoU(ground/3D): 0.842996/0.788026
box estimation accuracy (IoU=0.7): 0.872889
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.97it/s]
[117] test loss: 0.106103
test segmentation accuracy: 0.902509
test box IoU(ground/3D): 0.795575/0.744419
test box estimation accuracy (IoU=0.7): 0.771973
learning rate: 0.000168
Best Test acc: 0.772133(Epoch 108)
**** EPOCH 118 ****
Epoch 118/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[118: 1849/1850] train loss: 0.053884
segmentation accuracy: 0.958243
box IoU(ground/3D): 0.842177/0.787093
box estimation accuracy (IoU=0.7): 0.870321
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[118] test loss: 0.103991
test segmentation accuracy: 0.902605
test box IoU(ground/3D): 0.796255/0.745440
test box estimation accuracy (IoU=0.7): 0.772053
learning rate: 0.000168
Best Test acc: 0.772133(Epoch 108)
**** EPOCH 119 ****
Epoch 119/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[119: 1849/1850] train loss: 0.052181
segmentation accuracy: 0.958391
box IoU(ground/3D): 0.842569/0.787532
box estimation accuracy (IoU=0.7): 0.872145
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.02it/s]
[119] test loss: 0.104204
test segmentation accuracy: 0.903865
test box IoU(ground/3D): 0.797342/0.745243
test box estimation accuracy (IoU=0.7): 0.772212
learning rate: 0.000168
save to:log/default_caronly_kitti_2022-05-16-07/acc0.772212-epoch118.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.772212-epoch118.pth
Best Test acc: 0.772212(Epoch 119)
**** EPOCH 120 ****
Epoch 120/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[120: 1849/1850] train loss: 0.049876
segmentation accuracy: 0.958330
box IoU(ground/3D): 0.841623/0.786853
box estimation accuracy (IoU=0.7): 0.870557
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.10it/s]
[120] test loss: 0.103962
test segmentation accuracy: 0.902994
test box IoU(ground/3D): 0.795613/0.744600
test box estimation accuracy (IoU=0.7): 0.771893
learning rate: 0.000168
Best Test acc: 0.772212(Epoch 119)
**** EPOCH 121 ****
Epoch 121/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[121: 1849/1850] train loss: 0.050616
segmentation accuracy: 0.958940
box IoU(ground/3D): 0.843762/0.788771
box estimation accuracy (IoU=0.7): 0.875220
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.11it/s]
[121] test loss: 0.104093
test segmentation accuracy: 0.902078
test box IoU(ground/3D): 0.797858/0.747052
test box estimation accuracy (IoU=0.7): 0.775802
learning rate: 0.000118
save to:log/default_caronly_kitti_2022-05-16-07/acc0.775802-epoch120.pth
Saving model to log/default_caronly_kitti_2022-05-16-07/acc0.775802-epoch120.pth
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 122 ****
Epoch 122/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[122: 1849/1850] train loss: 0.052094
segmentation accuracy: 0.959046
box IoU(ground/3D): 0.844176/0.789595
box estimation accuracy (IoU=0.7): 0.875321
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.07it/s]
[122] test loss: 0.102609
test segmentation accuracy: 0.903287
test box IoU(ground/3D): 0.795212/0.743919
test box estimation accuracy (IoU=0.7): 0.765274
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 123 ****
Epoch 123/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[123: 1849/1850] train loss: 0.051761
segmentation accuracy: 0.958929
box IoU(ground/3D): 0.843951/0.789321
box estimation accuracy (IoU=0.7): 0.875709
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.10it/s]
[123] test loss: 0.097001
test segmentation accuracy: 0.902452
test box IoU(ground/3D): 0.799000/0.747653
test box estimation accuracy (IoU=0.7): 0.771415
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 124 ****
Epoch 124/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[124: 1849/1850] train loss: 0.051679
segmentation accuracy: 0.959156
box IoU(ground/3D): 0.843763/0.788753
box estimation accuracy (IoU=0.7): 0.874510
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.03it/s]
[124] test loss: 0.109805
test segmentation accuracy: 0.901481
test box IoU(ground/3D): 0.795770/0.744338
test box estimation accuracy (IoU=0.7): 0.770059
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 125 ****
Epoch 125/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.05it/s]
[125: 1849/1850] train loss: 0.051230
segmentation accuracy: 0.959204
box IoU(ground/3D): 0.844435/0.789692
box estimation accuracy (IoU=0.7): 0.877095
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.07it/s]
[125] test loss: 0.105586
test segmentation accuracy: 0.902509
test box IoU(ground/3D): 0.796597/0.745463
test box estimation accuracy (IoU=0.7): 0.770617
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 126 ****
Epoch 126/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.12it/s]
[126: 1849/1850] train loss: 0.052632
segmentation accuracy: 0.959385
box IoU(ground/3D): 0.843618/0.788851
box estimation accuracy (IoU=0.7): 0.874780
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.18it/s]
[126] test loss: 0.106539
test segmentation accuracy: 0.902297
test box IoU(ground/3D): 0.794966/0.743676
test box estimation accuracy (IoU=0.7): 0.768942
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 127 ****
Epoch 127/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[127: 1849/1850] train loss: 0.051930
segmentation accuracy: 0.959294
box IoU(ground/3D): 0.844464/0.789947
box estimation accuracy (IoU=0.7): 0.877618
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.10it/s]
[127] test loss: 0.106821
test segmentation accuracy: 0.902541
test box IoU(ground/3D): 0.796088/0.745325
test box estimation accuracy (IoU=0.7): 0.769182
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 128 ****
Epoch 128/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.13it/s]
[128: 1849/1850] train loss: 0.053076
segmentation accuracy: 0.959590
box IoU(ground/3D): 0.845081/0.790366
box estimation accuracy (IoU=0.7): 0.877838
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.08it/s]
[128] test loss: 0.098784
test segmentation accuracy: 0.902838
test box IoU(ground/3D): 0.796447/0.745226
test box estimation accuracy (IoU=0.7): 0.769820
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 129 ****
Epoch 129/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[129: 1849/1850] train loss: 0.050829
segmentation accuracy: 0.959511
box IoU(ground/3D): 0.844507/0.790161
box estimation accuracy (IoU=0.7): 0.877297
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[129] test loss: 0.104168
test segmentation accuracy: 0.902888
test box IoU(ground/3D): 0.798588/0.747628
test box estimation accuracy (IoU=0.7): 0.773489
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 130 ****
Epoch 130/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[130: 1849/1850] train loss: 0.050053
segmentation accuracy: 0.959363
box IoU(ground/3D): 0.844676/0.789979
box estimation accuracy (IoU=0.7): 0.876858
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.01it/s]
[130] test loss: 0.110211
test segmentation accuracy: 0.903092
test box IoU(ground/3D): 0.796422/0.745293
test box estimation accuracy (IoU=0.7): 0.770298
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 131 ****
Epoch 131/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.09it/s]
[131: 1849/1850] train loss: 0.050422
segmentation accuracy: 0.959494
box IoU(ground/3D): 0.844733/0.790315
box estimation accuracy (IoU=0.7): 0.877111
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.95it/s]
[131] test loss: 0.109086
test segmentation accuracy: 0.902206
test box IoU(ground/3D): 0.797714/0.745649
test box estimation accuracy (IoU=0.7): 0.773648
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 132 ****
Epoch 132/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[132: 1849/1850] train loss: 0.051248
segmentation accuracy: 0.959526
box IoU(ground/3D): 0.844859/0.790327
box estimation accuracy (IoU=0.7): 0.878649
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.11it/s]
[132] test loss: 0.102585
test segmentation accuracy: 0.901910
test box IoU(ground/3D): 0.796558/0.745497
test box estimation accuracy (IoU=0.7): 0.770697
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 133 ****
Epoch 133/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:24<00:00,  7.01it/s]
[133: 1849/1850] train loss: 0.051929
segmentation accuracy: 0.959470
box IoU(ground/3D): 0.844714/0.789874
box estimation accuracy (IoU=0.7): 0.876622
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[133] test loss: 0.107515
test segmentation accuracy: 0.902512
test box IoU(ground/3D): 0.794875/0.744162
test box estimation accuracy (IoU=0.7): 0.770538
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 134 ****
Epoch 134/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.04it/s]
[134: 1849/1850] train loss: 0.050771
segmentation accuracy: 0.959465
box IoU(ground/3D): 0.844994/0.790300
box estimation accuracy (IoU=0.7): 0.877534
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[134] test loss: 0.108947
test segmentation accuracy: 0.903491
test box IoU(ground/3D): 0.795899/0.744532
test box estimation accuracy (IoU=0.7): 0.772212
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 135 ****
Epoch 135/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[135: 1849/1850] train loss: 0.051809
segmentation accuracy: 0.959561
box IoU(ground/3D): 0.845260/0.790389
box estimation accuracy (IoU=0.7): 0.878547
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.12it/s]
[135] test loss: 0.111892
test segmentation accuracy: 0.902757
test box IoU(ground/3D): 0.796240/0.745183
test box estimation accuracy (IoU=0.7): 0.772053
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 136 ****
Epoch 136/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.09it/s]
[136: 1849/1850] train loss: 0.050217
segmentation accuracy: 0.959693
box IoU(ground/3D): 0.844877/0.790454
box estimation accuracy (IoU=0.7): 0.876284
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[136] test loss: 0.105375
test segmentation accuracy: 0.903806
test box IoU(ground/3D): 0.795689/0.745064
test box estimation accuracy (IoU=0.7): 0.770219
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 137 ****
Epoch 137/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[137: 1849/1850] train loss: 0.051484
segmentation accuracy: 0.959775
box IoU(ground/3D): 0.844807/0.790339
box estimation accuracy (IoU=0.7): 0.877128
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[137] test loss: 0.108757
test segmentation accuracy: 0.902135
test box IoU(ground/3D): 0.795371/0.744371
test box estimation accuracy (IoU=0.7): 0.766948
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 138 ****
Epoch 138/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.07it/s]
[138: 1849/1850] train loss: 0.049945
segmentation accuracy: 0.959859
box IoU(ground/3D): 0.845147/0.790604
box estimation accuracy (IoU=0.7): 0.878328
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[138] test loss: 0.103990
test segmentation accuracy: 0.900264
test box IoU(ground/3D): 0.795713/0.744628
test box estimation accuracy (IoU=0.7): 0.769580
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 139 ****
Epoch 139/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.09it/s]
[139: 1849/1850] train loss: 0.052536
segmentation accuracy: 0.959874
box IoU(ground/3D): 0.845000/0.790474
box estimation accuracy (IoU=0.7): 0.877990
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.11it/s]
[139] test loss: 0.102670
test segmentation accuracy: 0.900508
test box IoU(ground/3D): 0.797028/0.745542
test box estimation accuracy (IoU=0.7): 0.772053
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 140 ****
Epoch 140/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.09it/s]
[140: 1849/1850] train loss: 0.047585
segmentation accuracy: 0.959817
box IoU(ground/3D): 0.845507/0.791027
box estimation accuracy (IoU=0.7): 0.879223
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.13it/s]
[140] test loss: 0.100489
test segmentation accuracy: 0.902271
test box IoU(ground/3D): 0.798592/0.747272
test box estimation accuracy (IoU=0.7): 0.772611
learning rate: 0.000118
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 141 ****
Epoch 141/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[141: 1849/1850] train loss: 0.050116
segmentation accuracy: 0.960219
box IoU(ground/3D): 0.846561/0.792023
box estimation accuracy (IoU=0.7): 0.879274
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[141] test loss: 0.101077
test segmentation accuracy: 0.903695
test box IoU(ground/3D): 0.795817/0.744494
test box estimation accuracy (IoU=0.7): 0.767666
learning rate: 0.000082
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 142 ****
Epoch 142/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.11it/s]
[142: 1849/1850] train loss: 0.049630
segmentation accuracy: 0.960238
box IoU(ground/3D): 0.846386/0.792045
box estimation accuracy (IoU=0.7): 0.880693
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:42<00:00,  9.13it/s]
[142] test loss: 0.107863
test segmentation accuracy: 0.902755
test box IoU(ground/3D): 0.797068/0.746122
test box estimation accuracy (IoU=0.7): 0.771415
learning rate: 0.000082
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 143 ****
Epoch 143/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:19<00:00,  7.12it/s]
[143: 1849/1850] train loss: 0.049674
segmentation accuracy: 0.960435
box IoU(ground/3D): 0.846535/0.792185
box estimation accuracy (IoU=0.7): 0.882280
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.96it/s]
[143] test loss: 0.106715
test segmentation accuracy: 0.903482
test box IoU(ground/3D): 0.798165/0.746514
test box estimation accuracy (IoU=0.7): 0.773249
learning rate: 0.000082
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 144 ****
Epoch 144/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.06it/s]
[144: 1849/1850] train loss: 0.047941
segmentation accuracy: 0.960461
box IoU(ground/3D): 0.846571/0.792147
box estimation accuracy (IoU=0.7): 0.882095
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  8.94it/s]
[144] test loss: 0.107436
test segmentation accuracy: 0.902754
test box IoU(ground/3D): 0.797818/0.745989
test box estimation accuracy (IoU=0.7): 0.771176
learning rate: 0.000082
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 145 ****
Epoch 145/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.10it/s]
[145: 1849/1850] train loss: 0.047255
segmentation accuracy: 0.960468
box IoU(ground/3D): 0.846737/0.792581
box estimation accuracy (IoU=0.7): 0.882990
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.04it/s]
[145] test loss: 0.107938
test segmentation accuracy: 0.902600
test box IoU(ground/3D): 0.797257/0.746024
test box estimation accuracy (IoU=0.7): 0.772452
learning rate: 0.000082
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 146 ****
Epoch 146/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:20<00:00,  7.09it/s]
[146: 1849/1850] train loss: 0.049693
segmentation accuracy: 0.960438
box IoU(ground/3D): 0.846919/0.792577
box estimation accuracy (IoU=0.7): 0.884510
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.09it/s]
[146] test loss: 0.103295
test segmentation accuracy: 0.902762
test box IoU(ground/3D): 0.799139/0.747605
test box estimation accuracy (IoU=0.7): 0.772930
learning rate: 0.000082
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 147 ****
Epoch 147/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:23<00:00,  7.03it/s]
[147: 1849/1850] train loss: 0.049833
segmentation accuracy: 0.960474
box IoU(ground/3D): 0.846660/0.792184
box estimation accuracy (IoU=0.7): 0.880693
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.05it/s]
[147] test loss: 0.105401
test segmentation accuracy: 0.902101
test box IoU(ground/3D): 0.798034/0.746666
test box estimation accuracy (IoU=0.7): 0.774127
learning rate: 0.000082
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 148 ****
Epoch 148/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.06it/s]
[148: 1849/1850] train loss: 0.048305
segmentation accuracy: 0.960373
box IoU(ground/3D): 0.846787/0.792174
box estimation accuracy (IoU=0.7): 0.881014
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.02it/s]
[148] test loss: 0.108570
test segmentation accuracy: 0.902202
test box IoU(ground/3D): 0.797686/0.745998
test box estimation accuracy (IoU=0.7): 0.773010
learning rate: 0.000082
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 149 ****
Epoch 149/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:21<00:00,  7.08it/s]
[149: 1849/1850] train loss: 0.049809
segmentation accuracy: 0.960516
box IoU(ground/3D): 0.847190/0.792370
box estimation accuracy (IoU=0.7): 0.882889
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.12it/s]
[149] test loss: 0.106203
test segmentation accuracy: 0.903433
test box IoU(ground/3D): 0.797995/0.747134
test box estimation accuracy (IoU=0.7): 0.774525
learning rate: 0.000082
Best Test acc: 0.775802(Epoch 121)
**** EPOCH 150 ****
Epoch 150/150:
100%|██████████████████████████████████████████████████████████████████████████████| 1850/1850 [04:22<00:00,  7.05it/s]
[150: 1849/1850] train loss: 0.048380
segmentation accuracy: 0.960663
box IoU(ground/3D): 0.847451/0.792994
box estimation accuracy (IoU=0.7): 0.883260
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [00:43<00:00,  9.06it/s]
[150] test loss: 0.110449
test segmentation accuracy: 0.901969
test box IoU(ground/3D): 0.797034/0.746115
test box estimation accuracy (IoU=0.7): 0.772133
learning rate: 0.000082
Best Test acc: 0.775802(Epoch 121)
Time 13.903520217305557 hours
model saved to log/default_caronly_kitti_2022-05-16-07/acc0.775802-epoch120.pth
(test5) PS C:\Git\frustum-pointnets-pytorch> python train/test_fpointnets.py --model_path <log/.../xx.pth> --output test_results
発生場所 行:1 文字:46
+ python train/test_fpointnets.py --model_path <log/.../xx.pth> --outpu ...
+                                              ~
演算子 '<' は、今後の使用のために予約されています。
    + CategoryInfo          : ParserError: (:) [], ParentContainsErrorRecordException
    + FullyQualifiedErrorId : RedirectionNotSupported

(test5) PS C:\Git\frustum-pointnets-pytorch> python train/test_fpointnets.py --model_path "C:\Git\frustum-pointnets-pytorch\log\default_caronly_kitti_2022-05-16-07\acc0.775802-epoch120.pth" --output test_results
100%|████████████████████████████████████████████████████████████████████████████████| 392/392 [01:02<00:00,  6.24it/s]
Number of point clouds: 12538
Average pos ratio: 0.436390
Average pos prediction ratio: 0.471979
Average npoints: 1024.000000
Mean points: x0.025830 y0.987077 z24.957537
Max points: x15.590100 y9.347202 z79.730591
Min points: x-20.224794 y-3.882158 z0.000000
test from 2d gt: Done
test loss: 0.103065
test segmentation accuracy: 0.902165
test box IoU(ground/3D): 0.797544/0.746511
test box estimation accuracy (IoU=0.7): 0.773329
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch>
(test5) PS C:\Git\frustum-pointnets-pytorch> python kitti/kitti_object.py
