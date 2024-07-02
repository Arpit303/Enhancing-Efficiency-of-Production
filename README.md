# Enhancing Efficiency of Production
Data analyst at ABC Garments, feeling the pressure of work inconsistency as orders  were pilling up, but production was falling behind schedule. Frustration filled the air as supervisors scrambled to meet deadlines, and the sewing floor buzzed with a frenetic energy. The company prided itself on its efficient operations, but lately, things felt different. Operators were complaining about long periods of inactivity, while others were rushing to keep up with the workload. You suspected that the problem lay in the way task’s were distributed and the sequence of the operation in which they were carried out. You are keen to find out the root cause of the problem as to take any conclusive decision, assumptions need to be backed by a solid understand of the current operator working data in  production line before you present your findings to the plant’s General Manager.

Process 
1. Cutting and Bundling - After fabric is cut into individual pieces, they are bundled for each garment. A unique QR code is attached to each bundle. - need to write it well 
2. Line Setup: Production lines are set up based on the style's operation list, ensuring the correct sequence of tasks.
3. Scanning and Production: An operator starts working on a bundle by scanning the QR code using a dedicated application. This initiates production tracking for that specific set of garments.
4. Operations: The operator performs the designated tasks (sewing, pressing etc.) as per the style's operation list.
5. Completion Scanning: Upon completing the bundle, the operator scans the QR code again,  signifying the completion of work on that specific set of garments. This updates the  production tracking system.
6. Repeat: The process repeats for subsequent bundles until the production order is complete.

To understand the problem you started collecting operator production data in the following format 
from your current production management system (see Data Provided), along with your Industrial 
Engineer prepared for the required operation break down of the currently running style.



Data Provided: 

• Table 1: operator_tracking 
1. id - primary key for the database
2. operator_id - unique identification number of operator
3. operation_id - unique identification number of operation (task from the style operation list), operator is working on.
4. date - date of production 
5. bundle_number - the unique number of the bundle he has worked on
6. style_id - unique identification of the style
7. floor_id - unique identification of the floor (use to identify on which building floor the production was done)
8. line_id - unique identification of the line (use to identify on the floor which exact production line the piece is stitched)
9. complete_piece - number of good piece produced from this bundle
10. total_time - Total amount of time taken to complete the bundle (in seconds)
11. break_time - Total break taken during working on bundle (in seconds)
12. off_standard_time - Total time lost due to some unavoidable problems on production floor like power outage. (in seconds)

    
• Table 2: styles_operation_list 
1. id - primary key for the database
2. style_id - unique identification of the style
3. operation_id - unique identification number of operation
4. sort_order - sequence of the operation in which they are being performed on the production floor
5. sam - standard allowed time (time require to perform the operation on a single piece)
6. rate - amount in INR earned by an operator for completing operation
7. machine_id - machine on which this operation is performed

   
Based on data provided summit your finds in the way suitable to be presented for actionable decision making
