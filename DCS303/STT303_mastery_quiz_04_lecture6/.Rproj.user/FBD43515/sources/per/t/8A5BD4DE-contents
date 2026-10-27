# STT303: R for Data Science
# In-Class Mastery Quiz 4
# Lecture 6: Importing and Inspecting Data
#
# Name:Osvaldo Perez Eslava
# Date:9/11/2026
#
# Suggested time: about 20 minutes
#
# Work in THIS SCRIPT.
# Save before running the grader.
#
# Run the grader from the Console:
#
#   source("grade_this.R")
#   grade_this()
#
# You may revise, save, and rerun the grader during the quiz.
# Do NOT edit grade_this.R.
#
# The quiz focuses on the Lecture 6 workflow:
#
# locate file -> import -> inspect names/dimensions/types
#             -> check missingness -> count categories -> skim
#
# The data for this quiz are different from the lecture example.

# =============================================================================
# Problem 1. Locate and import the CSV file                                 [20]
# =============================================================================

# The file is:
#   data/fitness_checkins.csv
#
# A. Create checkin_file using here::here() with separate path components.
checkin_file <- here::here("data", "fitness_checkins.csv")

# B. Create file_found using file.exists(checkin_file).
file_found <- file.exists(checkin_file)

# C. Import the CSV and save it as checkins.
#    Use readr::read_csv().
#    You may use show_col_types = FALSE if you want quieter output.
checkins <- readr::read_csv(checkin_file)


# =============================================================================
# Problem 2. Inspect names and dimensions                                   [15]
# =============================================================================

# Create checkin_names using names(checkins).
checkin_names <- names(checkins)

# Create checkin_dim using dim(checkins).
checkin_dim <- dim(checkins)

# Create n_checkins using nrow(checkins).
n_checkins <- nrow(checkins)

# Create n_variables using ncol(checkins).
n_variables <- ncol(checkins)


# =============================================================================
# Problem 3. Inspect column types with glimpse()                            [10]
# =============================================================================

# Run dplyr::glimpse(checkins) as a standalone expression below.
# Do not assign it to an object.
dplyr::glimpse(checkins)


# =============================================================================
# Problem 4. Check missing values                                           [15]
# =============================================================================

# Create total_missing using is.na() and sum() to count ALL missing cells
# in checkins.
total_missing <- sum(is.na(checkins))

# Create missing_by_variable using is.na() and colSums() to count missing
# values separately for each column.
missing_by_variable <- colSums(is.na(checkins))


# =============================================================================
# Problem 5. Count a categorical variable                                  [15]
# =============================================================================

# Create activity_counts using dplyr::count().
#
# Count the values of activity and sort the result from most frequent to
# least frequent using sort = TRUE.
activity_counts <- dplyr::count(checkins, activity, sort = TRUE)


# =============================================================================
# Problem 6. Create a broad summary with skim()                             [10]
# =============================================================================

# Create skim_result by applying skimr::skim() to checkins.
skim_result <- skimr::skim(checkins)


# =============================================================================
# Problem 7. Inspect the Excel workbook                                     [15]
# =============================================================================

# The Excel file is:
#   data/fitness_checkins.xlsx
#
# A. Create excel_file using here::here() with separate path components.
excel_file <- here::here("data", "fitness_checkins.xlsx")

# B. Create sheet_names using readxl::excel_sheets(excel_file).
sheet_names <- readxl::excel_sheets(excel_file)

# C. Import the sheet named "checkins" using readxl::read_excel().
#    Save the result as checkins_excel.
checkins_excel <- readxl::read_excel(excel_file, sheet = "checkins")

# D. Create excel_dim using dim(checkins_excel).
excel_dim <- dim(checkins_excel)


# =============================================================================
# Finish
# =============================================================================

# Save this script, then run:
#
#   source("grade_this.R")
#   grade_this()
#
# Read the feedback problem by problem.
# Revise, SAVE, and rerun if needed.
