---
description: 'Weitere Informationen finden Sie hier: JET_RECSIZE2 Struktur'
title: JET_RECSIZE2 Struktur
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
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
ms.openlocfilehash: 2fd16480f0ec059c977d07f8e445a35094c5f2fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362355"
---
# <a name="jet_recsize2-structure"></a>JET_RECSIZE2 Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_recsize2-structure"></a>JET_RECSIZE2 Struktur

Die **JET_RECSIZE2** Struktur wird von [JetGetRecordSize2](./jetgetrecordsize2-function.md) verwendet, um Informationen über die Verwendungs Anforderungen eines Datensatzes im Benutzerdaten Bereich, die Anzahl der Satz Spalten, die Anzahl der Werte und den mehr Aufwand für die ESE-Daten Satzstruktur zurückzugeben.

**Windows 7:** Die **JET_RECSIZE2** Struktur wird im Windows 7-Betriebssystem eingeführt.

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
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
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

**ccompressedcolumns**

Die Gesamtanzahl der komprimierten Spalten.

**cbdatacompressed**

Die komprimierte Größe der Benutzerdaten in diesem Datensatz. Dies ist das gleiche wie bei cbData, wenn keine systeminternen langen Werte komprimiert werden.

**cblongvaluedatacompressed**

Die komprimierte Größe von Benutzerdaten in der Struktur mit langem Wert. Dies entspricht den cblongvalue-Daten, wenn keine getrennten Long-Werte komprimiert werden.

### <a name="remarks"></a>Bemerkungen

Die Gesamtanzahl der Werte im Datensatz wäre **cmultivalues**  +  **cnontaggedcolumns**  +  **ctaggedcolumns**.

Die logischen Daten im Datensatz sind (cbData + cblongvaluedata), und die physische Größe der Daten ist (cbdatacompressed + cblongvaluedatacompressed). Dies kann zum Berechnen des Komprimierungs Verhältnisses gespeicherter Daten verwendet werden.

### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert das Windows Vista-Betriebssystem.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert das Betriebssystem Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[Jetgetrecordsize](./jetgetrecordsize-function.md)  
[JetGetRecordSize2](./jetgetrecordsize2-function.md)
