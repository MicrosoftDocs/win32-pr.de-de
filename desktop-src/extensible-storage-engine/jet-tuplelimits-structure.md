---
description: 'Weitere Informationen finden Sie unter: JET_TUPLELIMITS Struktur'
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
ms.openlocfilehash: 7155763f68a74333fc71db1054fb0ecffcca862e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983763"
---
# <a name="jet_tuplelimits-structure"></a>JET_TUPLELIMITS Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_tuplelimits-structure"></a>JET_TUPLELIMITS Struktur

Die **JET_TUPLELIMITS-Struktur** ermöglicht die Anpassung der Tupelindexmerkmale pro Index und nicht auf Instanzbasis mithilfe von [JetSetSystemParameter](./jetsetsystemparameter-function.md).

**Windows Server 2003:** Die **JET_TUPLELIMITS-Struktur** wird in Windows Server 2003 eingeführt.

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

**chLengthMin**

Die Mindestlänge eines Tupels. Der Standardwert ist 3.

**chLengthMax**

Die maximale Länge eines Tupels. Der Standardwert ist 10.

**chToIndexMax**

Die maximale Länge einer zu indizierenden Zeichenfolge. Wenn eine Spalte beispielsweise 100 Zeichen lang ist und **chToIndexMax** auf 60 festgelegt ist, werden nur die ersten 60 Zeichen der Spalte indiziert. Der Standardwert ist 32767.

**cchIncrement**

Dadurch kann der Schritt pro Index konfiguriert werden.

**Windows Vista:** Das **cchIncrement-Member** wird in Windows Vista eingeführt. Vor Windows Vista war der Betrag zum Verschieben des Fensters (der "Stride") immer 1, wie im Beispiel im Abschnitt "Hinweise" gezeigt.

**ichStart**

Der Offset in den Wert, um mit dem Abrufen von Tupeln aus dem Wert zu beginnen.

**Windows Vista:** Das **ichStart-Mitglied** wird in Windows Vista eingeführt.

### <a name="remarks"></a>Bemerkungen

Ein Tupelindex durchgibt eine Zeichenfolge und indiziert alle möglichen Teilzeichenfolgen von **chLengthMax.** Am Ende der Zeichenfolge (oder an der Position **chToIndexMax**, je nachdem, was zuerst eintritt), werden die Teilzeichenfolgen von **mindestens chLengthMin** indiziert.

Ein Tupelindex kann zum Durchsuchen von Zeichenfolgen mit führenden und nachdenkenden Platzhaltern verwendet werden.

Angenommen, eine Zeile mit dem Textfeld "RAIN IN SPANIEN" wird, wenn ein Tupelindex mit den Parametern \! **chLengthMin**=2 und **chLengthMax**=3 erstellt wird, werden die folgenden Einträge im Index erstellt:

"RAI"  
"AIN"  
"IN"  
"N I"  
" IN"  
"IN"  
"N S"  
" SP"  
"SPA"  
"PAI"  
"AIN"  
\!"IN"  
\!"N"

Beachten Sie, dass "IN" zweimal auftritt und dass der letzte Eintrag ("N ") kürzer \! als 3 (**chLengthMax**) ist. Beachten Sie auch, dass der Aufteilungsalgorithmus Leerzeichen oder Wörter nicht kennt und alle Zeichen identisch behandelt.

**Windows XP:** Windows XP unterstützt Tupelindizes, verfügt jedoch nicht über **JET_TUPLELIMITS.** Die Datenbank-Engine verwendet die Standardwerte (**chLengthMin**=3, **chLengthMax**=10, **chToIndexMax**=32767). Es ist weiterhin [möglich,](./index-parameters.md)diese Werte zu ändern, aber sie werden auf Instanzbasis mit [JetSetSystemParameter](./jetsetsystemparameter-function.md) mit JET_paramIndexTuplesLengthMin , [JET_paramIndexTuplesLengthMax](./index-parameters.md)und JET_paramIndexTuplesToIndexMax [.](./index-parameters.md)

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
