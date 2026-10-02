-	How big is the dataset?
    < wc -l clean_dialog.csv >
o	36860 clean_dialog.csv

-	What’s the structure of the data? (i.e., what are the fields and what are values in them)
    < head -n 1 clean_dialog.csv >
o	"title","writer","pony","dialog"

-	How many episodes does it cover?
    tail -n +2 clean_dialog.csv | cut -d',' -f1 | sort -u | wc -l
o	197

-	During the exploration phase, find at least one aspect of the dataset that is unexpected – meaning that it seems like it could create issues for later analysis.
    Manually checking through less clean_dialog.csv
o	Non-dialog audio such as [yawn], or [sigh]
