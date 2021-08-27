---
description: 'Weitere Informationen finden Sie unter: JET_RECSIZE2 Struktur'
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
ms.openlocfilehash: c187d57149b7f0589d56439bfacbf7129ab4fe4a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987833"
---
# <a name="jet_recsize2-structure"></a>JET_RECSIZE2 Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_recsize2-structure"></a>JET_RECSIZE2 Struktur

Die **JET_RECSIZE2-Struktur** wird von [JetGetRecordSize2](./jetgetrecordsize2-function.md) verwendet, um Informationen über die Nutzungsanforderungen eines Datensatzes im Benutzerdatenbereich, die Anzahl der festgelegten Spalten, die Anzahl der Werte und den Mehraufwand für die ESE-Datensatzstruktur zurück zu geben.

**Windows 7:** Die **JET_RECSIZE2-Struktur** wird im Windows 7-Betriebssystem eingeführt.

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

**cCompressedColumns**

Die Gesamtzahl der komprimierten Spalten.

**cbDataCompressed**

Die komprimierte Größe der Benutzerdaten in diesem Datensatz. Dies ist identisch mit cbData, wenn keine systeminternen Long-Werte komprimiert sind.

**cbLongValueDataCompressed**

Die komprimierte Größe der Benutzerdaten in der Long-Value-Struktur. Dies ist identisch mit cbLongValue-Daten, wenn keine getrennten long-Werte komprimiert werden.

### <a name="remarks"></a>Bemerkungen

Die Gesamtzahl der Werte im Datensatz wäre **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

Die logischen Daten im Datensatz sind (cbData+cbLongValueData), und die physische Größe der Daten ist (cbDataCompressed+cbLongValueDataCompressed). Dies kann verwendet werden, um das Komprimierungsverhältnis gespeicherter Daten zu berechnen.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista-Betriebssystem.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008-Betriebssystem.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetGetRecordSize](./jetgetrecordsize-function.md)  
[JetGetRecordSize2](./jetgetrecordsize2-function.md)
