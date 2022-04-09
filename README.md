# git-challenge

### คำสั่ง CLI

ก่อนจะไปใช้คำสั่ง git คำสั่ง CLI ก็เป็นสิ่งที่ต้องรู้ด้วย ไม่งั้นเราจะไปต่อกันไม่ได้ ถ้าใครรู้แล้วก็ข้ามไปคำสั่ง git ได้เลย คำสั่งที่ต้องรู้คือ

  - `pwd` (print working directory (dir)) ใช้เมื่ออยากรู้ว่าตอนนี้เราอยู่ที่ dir ไหน
  - `cd` (change dir) เพื่อเปลี่ยนไปยัง dir อื่น
  - `ls` (list) ดูว่าใน dir ที่เราอยู่มีไฟล์หรือโฟลเดอร์อะไรบ้าง
  - `mkdir` (make dir) สร้างโฟลเดอร์ใหม่ขึ้นมา
  - `touch` สร้างไฟล์ใหม่

### คำสั่ง git

โดยพื้นฐานแล้ว git มีคำสั่งที่หลากหลายมากมายมหาศาลมาก แต่เราจะเริ่มกันด้วยคำสั่งเบื้องต้นที่ทำให้เราสามารถใช้งานได้ก่อนอันได้แก่

  - `git init` ใช้สร้าง local repo ขึ้นมา
  - `git add` ใช้ stage เพื่อติดตามตามความเปลี่ยนแปลงของไฟล์
  - `git commit -m <git_commit_message>` -m (ย่อมาจาก Message) ใช้เพื่อบันทึกความเปลี่ยนแปลงที่เกิดขึ้นสู่ local repo
  - `git push` ใช้เพื่อส่ง commit ไปยัง remote repo
  - `git clone` ใช้เพื่อคัดลอก repo จาก remote มายัง local
  - `git fetch` ใช้ดึงความเปลี่ยนแปลงจาก remote มายัง local แต่ยังไม่รวมเข้าด้วยกัน
  - `git merge` ใช้รวมความเปลี่ยนแปลงที่ได้มาจาก fetch เข้ากับ local
  - `git pull` ใช้ดึงความเปลี่ยนแปลงจาก remote มายัง local และรวมเข้าด้วยกัน (มีค่าเท่ากับ fetch+merge)
  - `git log` ใช้เพื่อดูว่า git repo มี commit อะไรแล้วบ้าง
  - `git tag -a <tag_name> -m <tag_message>` Annotated Tag คือ Tag ที่มีชื่อที่เราใส่ให้ Tag พร้อมทั้งมีข้อมูลเพิ่มเติม
  - `git tag <tag_name>` Lightweight Tag คือ Tag ที่มีแค่ชื่อที่เราตั้งให้ Tag แต่ไม่มีข้อมูลเพิ่มเติม
  - `git checkout -b <branch_name>` Creating a Branch (การสร้าง Branch ใหม่)
  - `git restore --staged <file>` Removing changes in staging area
  - `git stash` เก็บบันทึกการเปลี่ยนแปลงใน Working Area และ Staging Area ไว้ก่อน
    -  `git stash list` แสดงรายการ Stash
    -  `git stash pop <stash_id>` นำการเปลี่ยนแปลงที่อยู่ใน Stash ออกมาใช้ แล้วจะลบ Stash ทิ้งหลังจากเอาของออกมาแล้ว
    -  `git stash apply <stash_id>` นำการเปลี่ยนแปลงที่อยู่ใน Stash ออกมาใช้โดยที่ยังเก็บ Stash นั้นไว้อยู่
    -  `git stash drop <stash_id>` ใช้ลบ Stash ที่ไม่ใช้
