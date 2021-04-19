Finds position if exists, #VALUE! if not.
=FIND("ADD/ADHD",J1)

This gives YES if exists, but #Value! if not
=IF((FIND("ADD/ADHD",J1) > 0),"YES","NO")

If term does not exists, returns TRUE because it is an error. Returns FALSE if not present.
=ISERROR(FIND("ADD/ADHD",J1))

This returns Y if term exists, N if it doesn't. Only works on one term.
=IF(ISERROR(FIND("ADD/ADHD",J1)),"N","Y")

Post-Traumatic Stress Syndrome##ADD/ADHD


.str.contains("Hello|Britain")

def process(table):
    table['CAMPUS'] = table['CAMPUS'].astype(str).str.replace(',', '').str.zfill(9)
    return table

This creates a new column based on contents of old one
def process(table):
    table['New'] = table['Diagnoses']
    return table

This worked ... found Infant T if there.
def process(table):
  table['Test_Flag'] = np.where(table['Diagnoses'].str.contains("Infant", case=False, na=False), 'T', '')
  return table

def process(table):
  table['Test_Flag'] = np.where(table['Diagnoses'].str.contains("Infant|Oppositional", case=False, na=False), 'T', '')
  return table

