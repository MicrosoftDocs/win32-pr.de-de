---
description: 'Weitere Informationen finden Sie hier: JET_TUPLELIMITS Struktur'
title: JET_TUPLELIMITS Struktur
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960863"
---
# <a name="jet_tuplelimits-structure"></a>JET_TUPLELIMITS Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_tuplelimits-structure"></a>JET_TUPLELIMITS Struktur

Die **JET_TUPLELIMITS** -Struktur ermöglicht die Anpassung der tupelindexmerkmale auf Index Basis und nicht pro Instanz mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md).

**Windows Server 2003:** Die **JET_TUPLELIMITS** Struktur wird in Windows Server 2003 eingeführt.

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a>Member

**chverlängert**

Die minimale Länge eines Tupels. Der Standardwert ist 3.

**chlängen Max**

Die maximale Länge eines Tupels. Der Standardwert ist 10.

**Chum indexmax**

Die maximale Länge einer Zeichenfolge, die indiziert werden soll. Wenn eine Spalte z. b. 100 Zeichen lang ist und **chchanindexmax** auf 60 festgelegt ist, werden nur die ersten 60 Zeichen der Spalte indiziert. Der Standardwert ist 32767.

**cchincrement**

Dadurch kann der Stride auf Index Basis konfiguriert werden.

**Windows Vista:** Der **cchincrement** -Member wird in Windows Vista eingeführt. Vor Windows Vista war der Betrag zum Verschieben des Fensters ("stride") immer 1, wie im Beispiel im Abschnitt "Hinweise" gezeigt.

**ichstart**

Der Offset im Wert, mit dem das Abrufen von Tupeln aus dem Wert begonnen werden soll.

**Windows Vista:** Das Mitglied " **ichstart** " wird in Windows Vista eingeführt.

### <a name="remarks"></a>Bemerkungen

Ein Tupelindex durchläuft eine Zeichenfolge und indiziert alle möglichen Teil Zeichenfolgen von **chlängen Max**. Am Ende der Zeichenfolge (oder an der Position **chinindexmax**, je nachdem, welcher Wert zuerst auftritt) werden die Teil Zeichenfolgen von mindestens **chlängen min** indiziert.

Ein Tupelindex kann verwendet werden, um Zeichen folgen mit führenden und nachfolgenden Platzhaltern zu suchen.

Wenn in einer Zeile mit dem Textfeld "Regen in Spanien \! " ein Tupelindex mit den Parametern " **chverlänmin**= 2" und " **chlängen Max**= 3" erstellt wird, werden die folgenden Einträge im Index erstellt:

Darstellt  
Porzellan  
IN  
"N I"  
IN  
IN  
"N S"  
El  
Hotel  
Kampagnen  
Porzellan  
"In \! "  
"N \! "

Beachten Sie, dass "in" zweimal auftritt und dass der letzte Eintrag ("N \! ") kürzer als 3 (**chlängen Max**) ist. Beachten Sie außerdem, dass der Teilungs Algorithmus keine Leerzeichen oder Wörter kennt und alle Zeichen identisch behandelt.

**Windows XP:** Windows XP unterstützt tupelindizes, verfügt jedoch nicht über **JET_TUPLELIMITS**. Die Datenbank-Engine verwendet die Standardwerte (**chverlänmin**= 3, **chlängen Max**= 10, **chdeindexmax**= 32767). Es ist immer noch möglich, diese Werte zu ändern, aber Sie werden auf instanzbasis mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)und [JET_paramIndexTuplesToIndexMax](./index-parameters.md)festgelegt.

### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS]()  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)
