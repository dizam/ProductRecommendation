Generate previous month user data
python cf.py -s --select-date=2016-04-28 --output-file=prevmonth.csv

Generate current month user data
python cf.py -s --select-date=2016-05-28 --output-file=curmonth.csv

Calculate added products
python cf.py -l --input-file=prevmonth.csv --aux-input-file=curmonth.csv --output-file=addedproducts.csv

Calculate MAP (your predictions should be stored in output.csv)
python cf.py -e --input-file=output.csv --aux-input-file=addedproducts.csv