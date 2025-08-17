# Data Folder

This folder is a placeholder for the **six CourseKata textbook datasets** used during ASA DataFest 2024 at SMU.  
Due to privacy restrictions, the raw data is **not included** in this repository.  

Instead, this README provides a description of the data files and their purpose in the project.

---

## Provided Datasets

- **items.csv**  
  Metadata about textbook items (questions, videos, activities, and more).  
  *Example columns*: `item_id`, `item_type`, `chapter`, `page`, `lrn_type`.

- **media_views.csv**  
  Student interactions with videos or media objects.  
  *Example columns*: `student_id`, `chapter_number`, `time_on_page`, `time_video`.

- **page_views.csv**  
  Records of student page visits.  
  *Example columns*: `student_id`, `chapter_number`, `time_on_page`, `scroll_count`, `idle_long`.

- **responses.csv**  
  Student responses to textbook questions (multiple choice, open response, etc.).  
  *Example columns*: `student_id`, `item_id`, `correct`, `attempt`, `time_spent`.

- **checkpoints_eoc.csv**  
  End-of-chapter checkpoint quiz results.  
  *Example columns*: `student_id`, `chapter_number`, `n_possible`, `n_correct`.

- **checkpoints_pulse.csv**  
  Shorter “pulse” checkpoint assessments within the chapters.  
  *Example columns*: `student_id`, `chapter_number`, `construct`, `response`.

---

**Note:** These files are described here for reproducibility purposes, but the actual data cannot be published.
