# School_District_Analysis

## Overview of the school district analysis:
To help Maria to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact.

## Results: 
# District summarize using through DataFrame (per_school_types) per module 4.8.1 knowing the school district.
district_summary_df = pd.DataFrame(
          [{"Total Schools": school_count, 
          "Total Students": student_count, 
          "Total Budget": total_budget,
          "Average Math Score": average_math_score, 
          "Average Reading Score": average_reading_score,
          "% Passing Math": passing_math_percentage,
         "% Passing Reading": passing_reading_percentage,
        "% Overall Passing": overall_passing_percentage}])



# Format the "Total Students" to have the comma for a thousands separator.
district_summary_df["Total Students"] = district_summary_df["Total Students"].map("{:,}".format)
# Format the "Total Budget" to have the comma for a thousands separator, a decimal separator and a "$".
district_summary_df["Total Budget"] = district_summary_df["Total Budget"].map("${:,.2f}".format)
# Format the columns.
district_summary_df["Average Math Score"] = district_summary_df["Average Math Score"].map("{:.1f}".format)
district_summary_df["Average Reading Score"] = district_summary_df["Average Reading Score"].map("{:.1f}".format)
district_summary_df["% Passing Math"] = district_summary_df["% Passing Math"].map("{:.1f}".format)
district_summary_df["% Passing Reading"] = district_summary_df["% Passing Reading"].map("{:.1f}".format)
district_summary_df["% Overall Passing"] = district_summary_df["% Overall Passing"].map("{:.1f}".format)

# Display the data frame
district_summary_df
"District Summary.png" file in "Resource" folder.

# School summary been DataFrame after establish the spending bins(4.11.1)
and the Categorize spending based on the bins(4.11.2) through Spending Range per Student.
per_school_summary_df = pd.DataFrame({
    "School Type": per_school_types,
    "Total Students": per_school_counts,
    "Total School Budget": per_school_budget,
    "Per Student Budget": per_school_capita,
    "Average Math Score": per_school_math,
    "Average Reading Score": per_school_reading,
    "% Passing Math": per_school_passing_math,
    "% Passing Reading": per_school_passing_reading,
    "% Overall Passing": per_overall_passing_percentage})


per_school_summary_df.head()
"School Summary.png" file in "Resource" folder.

## Scores by school size
# Formatting. (4.12.4)
size_summary_df["Average Math Score"] = size_summary_df["Average Math Score"].map("{:.1f}".format)
size_summary_df["Average Reading Score"] = size_summary_df["Average Reading Score"].map("{:.1f}".format)
size_summary_df["% Passing Math"] = size_summary_df["% Passing Math"].map("{:.0f}".format)
size_summary_df["% Passing Reading"] = size_summary_df["% Passing Reading"].map("{:.0f}".format)
size_summary_df["% Overall Passing"] = size_summary_df["% Overall Passing"].map("{:.0f}".format)
size_summary_df
"Size Summary.png" file in "Resource" folder.

## Scores by school type
# Formatting (4.13.2)
type_summary_df["Average Math Score"] = type_summary_df["Average Math Score"].map("{:.1f}".format)
type_summary_df["Average Reading Score"] = type_summary_df["Average Reading Score"].map("{:.1f}".format)
type_summary_df["% Passing Math"] = type_summary_df["% Passing Math"].map("{:.0f}".format)
type_summary_df["% Passing Reading"] = type_summary_df["% Passing Reading"].map("{:.0f}".format)
type_summary_df["% Overall Passing"] = type_summary_df["% Overall Passing"].map("{:.0f}".format)
type_summary_df
"Type Summary.png" file in "Resource" folder.

## Summary:

1) Count the total number of students.
2) Count the number of students in 9th grade at Thomas High School of math and reading.
3) Calculate the number of student's scores of math and reading at Thomas High School.
4) Calculate budget per students at Thomas High School.
