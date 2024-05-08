# Proj_MRI-air-motor
# readme

% ========================== GENERAL INFO ============================== %

Authors: 
 - Zhijie Pan & Mengtang Li, Ph.D.
 - Institution: Sun Yat-Sen University, China.
 - Date: 2024 05 08 (first release)

 Description:
  - Please read the published Journal ariticle for more info: Pan, Z., et al. Cornerstone for MRI-compatible robots: A continuous pneumatic actuator
with easy-to-connect prismatic/revolute and bidirectional encoder modules, MEASRUEMENT, 2024. https://doi.org/10.1016/j.measurement.2024.114685
  - Supp. Vid can be found at: https://www.youtube.com/watch?v=GabAmfBLwVU&t=7s
  - This guihub repo contains the open sourced CAD files for the proposed MRI-compatible pneumatic motor, and PCB files for the optical fiber encoder (will update later).



% ========================== Detailed INFO - ENG ============================== %
## Three-dimensional Design Software and Versions

SolidWorks Version: 2019 and above. Files cannot be opened in versions lower than this.

## Modification of Part Dimensions

Models in the `Vanetype_AirMotor_V2` folder are designed with perfect dimensions. However, due to manufacturing tolerances and assembly requirements, some parts need slight modifications.

Models in the `Vanetype_AirMotor_V2_prototype` folder account for manufacturing tolerances and assembly requirements. However, their accuracy depends on the precision of the 3D printer or CNC machine used. The "Parts list" file provides the types and quantities of parts needed to assemble the prototype.

The table below indicates key modifications made to parts in this prototype for reference only. Actual modifications should be based on the precision of your 3D printer and CNC machine.

| Part Name          |                           Modifications                           |
| :----------------- | :---------------------------------------------------------------: |
| output_shaft       |      Reduced the cylinder diameter for positioning planetary gears by 0.2mm, decreased disk thickness by 0.1mm      |
| carrier_thick      | Reduced the cylinder diameter for positioning planetary gears by 0.2mm, decreased disk thickness by 0.1mm, reduced thickness of middle gear by 0.2mm |
| carrier_thin       | Reduced the cylinder diameter for positioning planetary gears by 0.2mm, decreased disk thickness by 0.1mm, reduced thickness of middle gear by 0.2mm |
| input_gear         |                        Reduced thickness by 0.2mm                         |
| reducer_cover_back |                      Decreased disk thickness by 0.5mm                       |
| rotor              |          Increased blade slot width by 0.15mm, shortened output shaft length by 0.2mm           |
| motor_back_cover   |               Increased outer diameter of guide rail by 0.2mm, decreased inner diameter by 0.1mm               |
| motor_front_cover  |               Increased outer diameter of guide rail by 0.2mm, decreased inner diameter by 0.1mm               |
| motor_housing      |           Increased overall thickness by 0.3mm, enlarged diameter of middle through-hole by 0.2mm           |
| encoder_disk       |                      Reduced overall thickness by 0.2mm                       |

## Notes

- Due to frequent relative sliding between vanes, rotor, and two covers (motor_back_cover and motor_front_cover), it's recommended to use materials with low friction coefficients for these parts. Teflon material was used here, machined through CNC. Ensure smooth movement between these parts and apply plastic-specific lubricant if necessary.
- The sealing of the motor chamber significantly affects motor output performance. Here, two O-ring rubber seals are used to ensure the motor housing remains airtight.
- When the output shaft of the reducer experiences axial force, it significantly affects the torque performance of the actuator, as mentioned in the paper showing the performance graph with the linear module. This is likely due to the structure of the reducer, where axial pressure increases the resistance experienced by the input gear of the reducer, directly affecting rotor rotation.
- Plastic-specific lubricant should be added inside the reducer to reduce friction.
- Experimental testing revealed that the actuator prototype does not initially perform at its best. As the testing progresses and internal parts wear in over time, the performance of the actuator prototype improves.



% ========================== Detailed INFO - CHN ============================== %
## 三维制图软件及版本

SolidWorks版本：2019及以上，低于此版本则打不开SW源文件。

## 零件尺寸修改

`Vanetype_AirMotor_V2`文件夹中的模型为完美尺寸模型，由于需要考虑制造误差以及配合公差，因此需要对一些零件稍作修改。

`Vanetype_AirMotor_V2_prototype` 文件夹中的模型考虑了制造误差以及配合公差，由于3D打印和CNC加工的精度取决于所操作的机器，因此仅作参考。`Parts list`文件给出了制作样机所需要零件的种类及数量。

下表列举了本样机中的零件已修改了哪些关键的地方，仅作参考，需要根据自己的3D打印机和CNC机器的制造精度进行修改。

| 零件名称           |                           修改选型                           |
| :----------------- | :----------------------------------------------------------: |
| output_shaft       |      定位行星齿轮的圆柱直径减小0.2mm，圆盘厚度减小0.1mm         |
| carrier_thick      | 定位行星齿轮的圆柱直径减小0.2mm，圆盘厚度减小0.1mm，中间齿轮厚度减小0.2mm |
| carrier_thin       | 定位行星齿轮的圆柱直径减小0.2mm，圆盘厚度减小0.1mm，中间齿轮厚度减小0.2mm |
| input_gear         |                        厚度减小0.2mm                         |
| reducer_cover_back |                      圆盘厚度减小0.5mm                       |
| rotor              |          叶片槽宽度增加0.15mm，输出轴长度缩短0.2mm             |
| motor_back_cover   |               导轨外径增加0.2mm，内径减小0.1mm               |
| motor_front_cover  |               导轨外径增加0.2mm，内径减小0.1mm               |
| motor_housing      |           整体厚度增加0.3mm，中间通孔直径增大0.2mm            |
| encoder_disk       |                      整体厚度减小0.2mm                       |

## 注意事项

- 由于叶片 (vane) 与转子 (rotor)、叶片 (vane) 与两个封盖 (motor_back_cover and motor_front_cover) 之间存在频繁的相对滑动，因此建议使用摩擦系数低的材料制作这些零件，这里使用了特氟龙 (teflon)材料通过CNC加工得到。需要确保这些零件之间能够顺畅地滑动，必要时可添加塑料专用润滑脂。
- 马达 (motor) 腔室的密封性对马达的输出性能影响较大，这里通过两个O型弹性橡胶圈进行密封，确保马达外壳不会漏气。
- 减速器的输出轴受到轴向力时，会显著影响执行器的扭矩性能的输出，这点论文中在展示搭配直线模块性能图时有提及到。原因猜测应该与减速器的结构有关，受到轴向压力时，会增大减速器的输入齿轮所受到的阻力，从而直接影响转子转动。
- 减速器内部需要添加塑料专用的润滑脂，从而降低摩擦。
- 实验测试时发现，刚装配完成执行器样机并没有发挥出最好的性能，随着测试进行，内部零件磨合一段时间后，执行器样机的性能会提升。

