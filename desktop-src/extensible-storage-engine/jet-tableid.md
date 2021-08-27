---
description: 'Weitere Informationen finden Sie unter: JET_TABLEID'
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
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
ms.openlocfilehash: 04e59ddada8715872978ccc21da11a349e1b7c43
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983573"
---
# <a name="jet_tableid"></a>JET_TABLEID


_**Gilt für:** Windows | Windows Server_

## <a name="jet_tableid"></a>JET_TABLEID

Der JET_TABLEID datentyp enthält ein Handle für den Datenbankcursor, das für einen Aufruf der JET-API verwendet werden soll. Ein Cursor kann nur mit der Sitzung verwendet werden, die zum Öffnen dieses Cursors verwendet wurde.

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a>Datentypen

JET_TABLEID

Entweder **NULL** oder [JET_tableidNil](./invalid-handle-constants.md) kann verwendet werden, um ein ungültiges Cursorhand handle anzugeben.

### <a name="remarks"></a>Bemerkungen

Ein Cursor verwaltet die Verwendung einer Tabelle für die Datenbank-Engine. Ein Cursor kann die folgenden Aufgaben ausführen:

  - Überprüfen von Datensätzen

  - Suchen nach Datensätzen

  - Auswählen der effektiven Sortierreihenfolge und Sichtbarkeit dieser Datensätze

  - Erstellen, Aktualisieren oder Löschen von Datensätzen

  - Ändern des Schemas der Tabelle

Die unterstützte Funktionalität des Cursors kann sich ändern, wenn sich der Status oder Typ der zugrunde liegenden Tabelle ändert. Beispielsweise könnte eine temporäre Tabelle die Suche nach Daten nicht nach sichten, wenn sie mit bestimmten Optionen geöffnet wird. Der Cursor ist immer vollständig mit der zugrunde liegenden Tabelle verbunden und interagiert direkt mit diesen Daten, ohne zwischenspeichern zu müssen. Fast alle isam-Kernfunktionen, die von dieser Datenbank-Engine verfügbar gemacht werden, werden über den Cursor verwendet.

Ein Cursor kann mit [JetOpenTable](./jetopentable-function.md) oder [JetOpenTempTable erstellt werden.](./jetopentemptable-function.md) Ein Cursor kann mit [JetDupCursor dupliziert werden.](./jetdupcursor-function.md) Ein Cursor kann explizit mit [JetCloseTable](./jetclosetable-function.md) oder implizit mit [JetEndSession](./jetendsession-function.md) oder [JetTerm geschlossen werden.](./jetterm-function.md) Ein Cursor kann auch implizit von [JetRollback geschlossen](./jetrollback-function.md) werden, wenn er in der abgebrochenen Transaktion geöffnet wurde. Die maximale Anzahl von Cursorn, die zu einem [](./resource-parameters.md)beliebigen Zeitpunkt erstellt werden können, wird durch JET_paramMaxCursors gesteuert, die mit [JetSetSystemParameter konfiguriert werden kann.](./jetsetsystemparameter-function.md)

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_paramMaxSessions](./resource-parameters.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)
