All assisted by the `grep --help` command in the terminal

# Grep -v

    grep -v [What to exclude] [files]

This command for is meant to take the input by the user and find all lines within the file that do not match with it. Those lines are what would be output into the terminal.

## Showcase
1st Example

    [cs15lsp23rj@ieng6-202]:plos:160$ grep -v a pmed.0010051.txt

  
    
      
        PRESENTATION of CASE 
        count (WBC), 2.9 × 10
        6 /l (4.8–10.8 × 10  
        6 /l (1.5–6.2 × 10   
        6 /l (150–350 × 10   
        6 /l).
        6 /l.
      
      
        Discussion
        nutrient supply.     
        elements.
      
    

    [cs15lsp23rj@ieng6-202]:plos:161$
    
2nd Example

    [cs15lsp23rj@ieng6-202]:plos:161$ grep -v it pmed.0020281.txt





        Whistleblowers serve no function if they cannot tell their stories. The present story of
        whistleblowing—as discussed, in part, in
        PLoS Medicine —that involves the pharmaceutical industry, pharmaceutical
        courageous men and women [1, 2] For that reason, those of us who congregated in Washington,
        Amendment work of responsible journalists, who exemplify the best in investigatory
        research.
        For me, whistleblowing is not a theoretical exercise. It has a human face and tangible
        features. It is the face of children and adults who have been injured or killed by
        misrepresented pharmaceuticals; clinical research trial results that have been sequestered
        pharmaceuticals that are detailed to physicians, not to save lives or necessarily improve
        the health or welfare of the recipients, but to make money.
        In the lonely and, at times, discouraging world of whistleblowing, we whistleblowers are
        passionate, and often successful, because our efforts have a different goal than the
        is to tell the truth. That honest effort is the source of any ethical difference we can or
        expediency, and money.
        A whistleblower's success depends upon competent and articulate media. The debate to
        Ralph Waldo Emerson, American essayist and philosopher (1803–1882), commented about
        success (I have adapted his comments for all of us who gathered in Washington in mid-May
        this is to have succeeded [as a whistleblower].”



    [cs15lsp23rj@ieng6-202]:plos:162$

# Grep -m

    grep -m [number of desired matches] [string to match] [files]
    
Stops displaying lines that match after the number of lines given reaches the input. If it does not reach the number, it will just print all matching lines.

## Showcase
1st Example

    [cs15lsp23rj@ieng6-202]:plos:162$ grep -m 10 a pmed.0010047.txt
        A malaria vaccine called ME-TRAP, which targets the pre-erythrocytic stage of the
        disease, was not effective at reducing natural infection rates in semi-immune African
        adults, according to the report of a randomized controlled trial published this month in
        PLoS Medicine . “This first field efficacy trial was an important
        milestone in the progression of new recombinant vectored vaccines to deployable products,”
        says Adrian Hill (University of Oxford, United Kingdom), the lead investigator of the
        study. “The safety profile was excellent and the efficacy data provide a first indication
        of the levels of cellular immunogenicity that will be required for preventing infection,”
        he says.
        Hill and his co-workers used a heterologous prime–boost vaccination technique. They gave
    [cs15lsp23rj@ieng6-202]:plos:163$

2nd Example

    [cs15lsp23rj@ieng6-202]:plos:163$ grep -m 20 it pmed.0010013.txt
        In 1996, Richard Horton, editor of the
        a decade later, it is important for surgeons and non-surgeons alike to revisit Horton's
        trials attempt to obtain an unbiased randomization of patients with respect to known and
        unknown baseline conditions and to assess the effects of an intervention. However, only a
        minority of surgical studies involve a valid randomization scheme. The case series remains
        consider Dennis Burkitt's report on jaw tumors in African children, Alfred Blalock's
        initial efforts in cardiac surgery, or, more recently, Starzl and colleagues' observations,
        that the complexities of human disease in surgical patients makes them a more difficult
        non-surgical patients. So it would be inherently easier, for example, to study a new
        medication for generally healthy young adults with essential hypertension than a surgical
        technique for older patients with hepatic failure needing transplantation.
        In addition, while there may be value in studying patients from multiple centers, there
        may be important differences in the skill levels of different surgeons, either between
        carotid endarterectomy may be greater than those across the surgical community as a whole.
        This makes the applicability of some surgical RCTs to the wider community less certain than
        So when it comes to surgical research, for both researchers and funding agencies, it is
        easier to grapple with a difficult, but ultimately soluble, basic science question than to
        face the uncertainty of clinical research. Investigators understand these implicit issues
        would seem that improvements are required from within and beyond the surgical world.
        begin within the field itself [1,5,6,7]. Both during surgical training and in the early
    [cs15lsp23rj@ieng6-202]:plos:164$

# Grep -n

    grep -n [string to match] [files]

Displays the line numbers of each output's original line location from the file. It can be useful when trying to reference back to the text to search for the output.

## Showcase
1st Example

    [cs15lsp23rj@ieng6-202]:plos:164$ grep -n -v it pmed.0020281.txt
    1:
    2:
    3:
    4:
    5:
    6:        Whistleblowers serve no function if they cannot tell their stories. The present story of
    7:        whistleblowing—as discussed, in part, in
    8:        PLoS Medicine —that involves the pharmaceutical industry, pharmaceutical
    11:        courageous men and women [1, 2] For that reason, those of us who congregated in Washington,
    15:        Amendment work of responsible journalists, who exemplify the best in investigatory
    16:        research.
    17:        For me, whistleblowing is not a theoretical exercise. It has a human face and tangible
    18:        features. It is the face of children and adults who have been injured or killed by
    19:        misrepresented pharmaceuticals; clinical research trial results that have been sequestered
    21:        pharmaceuticals that are detailed to physicians, not to save lives or necessarily improve
    22:        the health or welfare of the recipients, but to make money.
    23:        In the lonely and, at times, discouraging world of whistleblowing, we whistleblowers are
    24:        passionate, and often successful, because our efforts have a different goal than the
    26:        is to tell the truth. That honest effort is the source of any ethical difference we can or
    29:        expediency, and money.
    30:        A whistleblower's success depends upon competent and articulate media. The debate to
    33:        Ralph Waldo Emerson, American essayist and philosopher (1803–1882), commented about
    34:        success (I have adapted his comments for all of us who gathered in Washington in mid-May
    37:        this is to have succeeded [as a whistleblower].”
    38:
    39:
    40:
    [cs15lsp23rj@ieng6-202]:plos:165$

2nd Example

    [cs15lsp23rj@ieng6-202]:plos:165$ grep -n -m 10 a pmed.0010047.txt
    6:        A malaria vaccine called ME-TRAP, which targets the pre-erythrocytic stage of the
    7:        disease, was not effective at reducing natural infection rates in semi-immune African
    8:        adults, according to the report of a randomized controlled trial published this month in
    9:        PLoS Medicine . “This first field efficacy trial was an important
    10:        milestone in the progression of new recombinant vectored vaccines to deployable products,”
    11:        says Adrian Hill (University of Oxford, United Kingdom), the lead investigator of the
    12:        study. “The safety profile was excellent and the efficacy data provide a first indication
    13:        of the levels of cellular immunogenicity that will be required for preventing infection,”
    14:        he says.
    15:        Hill and his co-workers used a heterologous prime–boost vaccination technique. They gave
    [cs15lsp23rj@ieng6-202]:plos:166$

# Grep -l

    grep -l [string to match] [files]

This will output all files that contain the given string. There will be no output however if none of the files contain the string. This is very useful for quick searches between files.

## Showcase
1st Example

    [cs15lsp23rj@ieng6-202]:plos:166$ grep -l Whistleblowers pmed.0020281.txt pmed.0010047.txt pmed.0010013.txt
    pmed.0020281.txt
    [cs15lsp23rj@ieng6-202]:plos:167$

2nd Example

    [cs15lsp23rj@ieng6-202]:plos:167$ grep -l noneHaveThisString pmed.0020281.txt pmed.0010047.txt pmed.0010013.txt
    [cs15lsp23rj@ieng6-202]:plos:168$
