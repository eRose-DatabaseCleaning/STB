ALL QSD files.

analyse structure fichier QSD (à partir de QN-021.QSD)

0c 00 00 00  = type de fichier

01 00 00 00 = 1 block
  08 00 = longueur id_nom
  	32 31 -	20 -	C6 DF C5 B2 00 = id - séparateur (20:espace) - nom

01 00 00 00 = 1 block
  09 00 = longueur info
    b9 df b5 bf c3 bc c5 a9 00 = info
    
00 = SEPARATOR

02 00 00 00  = # condition

02 00 00 00 = # action

07 00 = longueur quest-ID
	31 30 35 2D 33 31 00 = quest-ID

## CONDITION ##

0c 00 00 00 = size (incluant size : 12 octet)
	00 00 00 00 = TYPE : Check QUEST
	69 00 00 00 = quest (105)

1c 00 00 00 = size (incluant size : 28 octet)
	04 00 00 00 = TYPE : Check QUEST ITEM
	01 00 00 00 = quantity
	49 33 00 00 = object (13129)
	0D 00 00 00 = type object (13)
	0A 00 00 00 = amount (10)
	03 CC CC CC = condition ( < )

## ACTION ##

10 00 00 00 = size (incluant size : 16 octet)
	00 00 00 01 = TYPE : Select QUEST
	69 00 00 00 = quest (105)
	04 CD CD CD = Action (???)

14 00 00 00 = size (incluant size : 20 octet)
	01 00 00 01 = TYPE : Update QUEST ITEM
	49 33 00 00 = object (13129)
	01 CD 01 00 = 01:GIVE / CD:??? / 0100:AMOUNT
	00 CD CD CD = PARTY???
