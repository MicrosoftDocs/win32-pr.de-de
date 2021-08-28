---
description: 'Weitere Informationen finden Sie unter: JET_RECSIZE Struktur'
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
ms.openlocfilehash: a7ea4520a75e83c77a6403a583e9131a15df337b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988228"
---
# <a name="jet_recsize-structure"></a>JET_RECSIZE Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_recsize-structure"></a>JET_RECSIZE Struktur

Die **JET_RECSIZE-Struktur** wird von [JetGetRecordSize](./jetgetrecordsize-function.md) verwendet, um Informationen über die Nutzungsanforderungen eines Datensatzes im Benutzerdatenbereich, die Anzahl der festgelegten Spalten, die Anzahl von Werten und den Mehraufwand für die ESE-Datensatzstruktur zurück zu geben.

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

**Hinweis:**  Die Schlüsselgröße ist in dieser nicht enthalten.

**cbLongValueData**

Benutzerdaten, die dem Datensatz zugeordnet sind, aber in der Long-Value-Struktur gespeichert sind.

**Hinweis:**  Dies zählt keine systeminternen Long-Werte.

**cbOverhead**

Der Mehraufwand der ESE-Datensatzstruktur für diesen Datensatz. Dies schließt die Schlüsselgröße des Datensatzes ein.

**cbLongValueOverhead**

Der Mehraufwand der Long-Value-Daten.

**Hinweis:**  Dies zählt keine systeminternen Long-Werte.

**cNonTaggedColumns**

Die Gesamtanzahl der festen und variablen Spalten, die in diesem Datensatz festgelegt sind.

**cTaggedColumns**

Gesamtanzahl der in diesem Datensatz festgelegten markierten Spalten.

**cLongValues**

Gesamtanzahl der long-Werte, die in der Long-Value-Struktur für diesen Datensatz gespeichert sind.

**Hinweis:**  Dies zählt keine systeminternen Long-Werte.

**cMultiValues**

Die Akkumulation der Gesamtzahl von Werten, die über die erste für alle Spalten im Datensatz hinausgehen.

### <a name="remarks"></a>Bemerkungen

Die Gesamtzahl der Werte im Datensatz wäre **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetGetRecordSize](./jetgetrecordsize-function.md)
