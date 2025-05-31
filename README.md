# Day-11

🧩 Additional Tasks & Scripts
These tasks showcase basic scripting and command-line skills in both Bash and Windows Command Prompt.

7. 🆚 String Length Comparator
📄 File: answer3.sh
📘 Description:
Compares the length of two strings entered by the user and prints which one is longer.

📥 Sample Run:
arduino
Copy
Edit
Enter the first word:
hello
Enter the second word:
worldwide
worldwide is larger than hello
✨ Enhanced Version:
Also handles the case when both strings have equal length:

bash
Copy
Edit
read -p "Enter string_1: " str1
read -p "Enter string_2: " str2

len1=${#str1}
len2=${#str2}

if [ "$len1" -gt "$len2" ]; then
  echo "The longer string is: $str1"
elif [ "$len2" -gt "$len1" ]; then
  echo "The longer string is: $str2"
else
  echo "Both lengths are equal"
fi
8. 🗂️ File & Folder Management (Windows CMD)
📘 Description:
A script to create subject folders and exam resources on a Windows desktop.

📂 Structure Created:
sql
Copy
Edit
Desktop\
└── CSC2244\
    ├── practical\
    │   ├── practical.docx
    │   ├── practical.txt
    │   └── practical.pptx
    ├── theory\
    │   ├── theory.txt
    │   ├── theory.docx
    │   └── theory.pptx
    └── exam papers\
        ├── exam.txt
        ├── exam.docx
        └── exam.pptx

Also creates:
├── Icae Marks.xlsx
├── Final Exam Marks.xlsx → moved to "Marks" folder
🔐 Final Commands:
cmd
Copy
Edit
xcopy /E /I Marks Exam\Marks
attrib +h Exam
Hides the Exam directory.

9. 📊 CSV Data Analysis using awk
📘 Description: Processes data.csv with comma-separated fields to filter and compute GPA statistics.

✅ Print entries with GPA > 3.5:
bash
Copy
Edit
awk -F, 'NR==1 || $4 > 3.5' data.csv
📈 Calculate average GPA:
bash
Copy
Edit
awk -F, 'NR>1 {sum+=$4; count++} END {if (count > 0) print "Average GPA:", sum/count}' data.csv
📌 Summary of Scripts
Script / Task	Description
answer3.sh	Compare string lengths
Windows CMD Task	Create folders and move/hide exam files
awk commands	GPA filtering and average from data.csv
