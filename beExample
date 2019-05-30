import sqlite3

def konnect():
    con = sqlite3.connect('emps.db')
    cur = con.cursor()
    cur.execute("create table if not exists emp (id integer primary key, \
                                                 fn text, ln text, dept text, \
                                                 sal integer)")
    con.commit()
    con.close()

def addrec(fn,ln,dept,sal):
    con = sqlite3.connect('emps.db')
    cur = con.cursor()
    cur.execute("insert into emp values(null,?,?,?,?)",(fn,ln,dept,sal))
    print("Just put this in:",fn,ln,dept,sal)
    con.commit()
    con.close()

konnect()
