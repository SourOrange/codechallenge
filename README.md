# codechallenge 我只是想做点什么而已，并没有多么远大的梦想
may be 100days, now is better than never
# day2
Bite 5. Parse a list of names
In this bite you will work with a list of names.
First you will write a function to take out duplicates and title case them.
Then you will sort the list in alphabetical descending order by surname and lastly determine what the shortest first name is. 
For this exercise you can assume there is always one name and one surname.
With some handy Python builtins you can write this in a pretty concise way. Get it sorted :)
<pre>
# 以下是我的代码，看了答案后，人家的可真是简洁！！
NAMES = ['arnold schwarzenegger', 'alec baldwin', 'bob belderbos',
         'julian sequeira', 'sandra bullock', 'keanu reeves',
         'julbob pybites', 'bob belderbos', 'julian sequeira',
         'al pacino', 'brad pitt', 'matt damon', 'brad pitt']


def dedup_and_title_case_names(names):
    """Should return a list of names, each name appears only once"""
    names = list(set(names))
    names_title_case = []
    for name in names:
        names_title_case.append(name.title())
    return names_title_case


def sort_by_surname_desc(names):
    """Returns names list sorted desc by surname"""
    names = dedup_and_title_case_names(names)
    sorted_desc_by_surname = sorted(
            names, key=lambda fullName: fullName.split()[1], reverse=True
        )
    return sorted_desc_by_surname
    # ...


def shortest_first_name(names):
    """Returns the shortest first name (str).
       You can assume there is only one shortest name.
    """
    names = dedup_and_title_case_names(names)
    shortest_first_name = min(names, key=lambda x:x.split()[0]).split()[0]
    return shortest_first
</pre>
