import csv
import MySQLdb

mydb = MySQLdb.connect(host='localhost',
                       user='root',
                       passwd='mls1000',
                       db='mls_t1_master')
cursor = mydb.cursor()

csv_data = csv.reader(file('C:\Users\vtika\Desktop\Valon T\leaseco_to_sprint_20151201_B.csv'))
for row in csv_data:
    cursor.execute('INSERT INTO testcsv(names, \
          classes, mark )' |
                   'VALUES("%s", "%s", "%s")',
                   row)
mydb.commit()
cursor.close()
print "Done"
