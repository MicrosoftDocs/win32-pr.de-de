---
description: 'Weitere Informationen finden Sie hier: JET_RECSIZE Struktur'
title: JET_RECSIZE Struktur
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749856"
---
# <a name="jet_recsize-structure"></a>JET_RECSIZE Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_recsize-structure"></a>JET_RECSIZE Struktur

Die **JET_RECSIZE** Struktur wird von [jetgetrecordsize](./jetgetrecordsize-function.md) verwendet, um Informationen über die Verwendungs Anforderungen eines Datensatzes im Benutzerdaten Bereich, die Anzahl der Mengen Spalten, die Anzahl der Werte und den mehr Aufwand der ESE-Daten Satzstruktur zurückzugeben.

**Windows Vista:** Die **JET_RECSIZE** Struktur wird in Windows Vista eingeführt.

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
    } JET_RECSIZE;
```

### <a name="members"></a>Member

**cbData**

Benutzer DataSet im Datensatz.

**Hinweis**  Die Schlüsselgröße ist in diesem nicht enthalten.

**cblongvaluedata**

Benutzerdaten, die dem Datensatz zugeordnet sind, aber in der Struktur mit langem Wert gespeichert sind.

**Hinweis**  Dabei werden keine systeminternen langen Werte gezählt.

**cboverhead**

Der Aufwand der ESE-Daten Satzstruktur für diesen Datensatz. Dazu gehört auch die Schlüsselgröße des Datensatzes.

**cblongvalueoverhead**

Der Aufwand für die Daten mit langen Werten.

**Hinweis**  Dabei werden keine systeminternen langen Werte gezählt.

**cnontaggedcolumns**

Die Gesamtanzahl der in diesem Datensatz festgelegten Fixed-und variable-Spalten.

**ctaggedcolumns**

Die Gesamtanzahl der in diesem Datensatz festgelegten markierten Spalten.

**clongvalues**

Gesamtzahl der langen Werte, die in der Struktur mit langem Wert für diesen Datensatz gespeichert sind.

**Hinweis**  Dabei werden keine systeminternen langen Werte gezählt.

**cmultivalues**

Die Ansammlung der Gesamtzahl der Werte, die über den ersten für alle Spalten im Datensatz hinausgehen.

### <a name="remarks"></a>Bemerkungen

Die Gesamtanzahl der Werte im Datensatz wäre **cmultivalues**  +  **cnontaggedcolumns**  +  **ctaggedcolumns**.

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
<td><p>Erfordert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[Jetgetrecordsize](./jetgetrecordsize-function.md)
