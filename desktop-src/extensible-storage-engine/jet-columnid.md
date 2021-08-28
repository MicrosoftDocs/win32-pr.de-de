---
description: 'Weitere Informationen zu: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: fbdc03342187cfc2adfa1dcd3ed650f532e1dbc0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982943"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**Gilt für:** Windows | Windows Server_

## <a name="jet_columnid"></a>JET_COLUMNID

Der **JET_COLUMNID** Datentyp identifiziert eine Spalte innerhalb einer Tabelle.

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a>Datentypen

JET_COLUMNID

Identifiziert eine Spalte innerhalb einer Tabelle.

### <a name="remarks"></a>Bemerkungen

Spalten-IDs sind innerhalb einer einzelnen Tabelle eindeutig. Sobald bekannt ist, dass eine Spalte eine bestimmte Spalten-ID hat, hat sie immer diese Spalten-ID. Bei der Wiederherstellung aus einer Sicherung wird der Wert einer Spalten-ID nicht geändert. Wenn jedoch eine oder mehrere Tabellenspalten vor einer bestimmten Tabellenspalte gelöscht werden, kann eine kompakte Datenbank den Wert einer Spalten-ID ändern.

In einigen Fällen sind Spalten-IDs die einzige Möglichkeit zum Identifizieren von Spalten. Wenn eine temporäre Tabelle erstellt wird, haben die Spalten keine Namen, aber ein Array von Spalten-IDs wird von der create-Funktion zurückgegeben.

Spalten in verschiedenen Tabellen können die gleiche Spalten-ID aufweisen.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 


