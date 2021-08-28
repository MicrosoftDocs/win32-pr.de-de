---
description: 'Weitere Informationen zu: JET_RECSIZE-Struktur'
title: JET_RECSIZE-Struktur
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
ms.openlocfilehash: 4fd0f59c821fa80d8de46f97e05aa1944354018e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475946"
---
# <a name="jet_recsize-structure"></a>JET_RECSIZE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_recsize-structure"></a>JET_RECSIZE-Struktur

Die **JET_RECSIZE-Struktur** wird von [JetGetRecordSize](./jetgetrecordsize-function.md) verwendet, um Informationen über die Verwendungsanforderungen eines Datensatzes im Benutzerdatenbereich, die Anzahl der festgelegten Spalten, die Anzahl der Werte und den Mehraufwand für die ESE-Datensatzstruktur zurückzugeben.

**Windows Vista:** Die **JET_RECSIZE-Struktur** wird in Windows Vista eingeführt.

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

Benutzerdatensatz im Datensatz.

**Hinweis**  Die Schlüsselgröße ist hier nicht enthalten.

**cbLongValueData**

Benutzerdaten, die dem Datensatz zugeordnet sind, aber in der Struktur mit langen Werten gespeichert sind.

**Hinweis**  Dies zählt keine systeminternen Long-Werte.

**cbOverhead**

Der Mehraufwand der ESE-Datensatzstruktur für diesen Datensatz. Dies schließt die Schlüsselgröße des Datensatzes ein.

**cbLongValueOverhead**

Der Mehraufwand der Daten mit langen Werten.

**Hinweis**  Dies zählt keine systeminternen Long-Werte.

**cNonTaggedColumns**

Gesamtanzahl der festen und variablen Spalten, die in diesem Datensatz festgelegt sind.

**cTaggedColumns**

Gesamtanzahl der markierten Spalten, die in diesem Datensatz festgelegt sind.

**cLongValues**

Gesamtanzahl von long-Werten, die in der Long-Value-Struktur für diesen Datensatz gespeichert sind.

**Hinweis**  Dies zählt keine systeminternen Long-Werte.

**cMultiValues**

Die Akkumulation der Gesamtanzahl von Werten nach dem ersten für alle Spalten im Datensatz.

### <a name="remarks"></a>Hinweise

Die Gesamtzahl der Werte im Datensatz wäre **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetGetRecordSize](./jetgetrecordsize-function.md)
