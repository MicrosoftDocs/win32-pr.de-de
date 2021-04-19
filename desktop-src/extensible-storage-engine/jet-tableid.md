---
description: 'Weitere Informationen finden Sie hier: JET_TABLEID'
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
ms.openlocfilehash: e2eae9590d0151bcdb2dc5621ae6df9e41e068a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355288"
---
# <a name="jet_tableid"></a>JET_TABLEID


_**Gilt für:** Windows | Windows Server_

## <a name="jet_tableid"></a>JET_TABLEID

Der JET_TABLEID-Datentyp enthält ein Handle für den Daten Bank Cursor, der für einen aufzurufenden Jet-API-Befehl verwendet wird. Ein Cursor kann nur mit der Sitzung verwendet werden, die zum Öffnen dieses Cursors verwendet wurde.

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a>Datentypen

JET_TABLEID

Entweder **null** oder [JET_tableidNil](./invalid-handle-constants.md) kann verwendet werden, um ein ungültiges Cursor Handle anzugeben.

### <a name="remarks"></a>Bemerkungen

Ein Cursor verwaltet die Verwendung einer Tabelle für die Datenbank-Engine. Ein Cursor kann die folgenden Aufgaben ausführen:

  - Datensätze überprüfen

  - Suchen nach Datensätzen

  - Effektive Sortierreihenfolge und Sichtbarkeit dieser Datensätze auswählen

  - Erstellen, aktualisieren oder Löschen von Datensätzen

  - Ändern des Schemas der Tabelle

Die unterstützten Funktionen des Cursors können sich ändern, wenn sich der Status oder der Typ der zugrunde liegenden Tabelle ändert. Eine temporäre Tabelle kann z. b. die Suche nach Daten nicht zulassen, wenn Sie mit bestimmten Optionen geöffnet wird. Der Cursor ist immer vollständig mit der zugrunde liegenden Tabelle verbunden und interagiert ohne Zwischenspeichern direkt mit diesen Daten. Fast alle Kernfunktionen von ISAM, die von dieser Datenbank-Engine verfügbar gemacht werden, funktionieren über den Cursor.

Ein Cursor kann mit [jetopentable](./jetopentable-function.md) oder [jetopumtemptable](./jetopentemptable-function.md)erstellt werden. Ein Cursor kann mithilfe von [jetdupcursor](./jetdupcursor-function.md)dupliziert werden. Ein Cursor kann mithilfe von [jetclosetable](./jetclosetable-function.md) explizit geschlossen oder mithilfe von [jetendsession](./jetendsession-function.md) oder [jetterm](./jetterm-function.md)implizit geschlossen werden. Ein Cursor kann auch implizit von [jetrollback](./jetrollback-function.md) geschlossen werden, wenn er in der abgebrochenen Transaktion geöffnet wurde. Die maximale Anzahl von Cursorn, die zu einem beliebigen Zeitpunkt erstellt werden können, wird von [JET_paramMaxCursors](./resource-parameters.md)gesteuert, die mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md)konfiguriert werden können.

### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_paramMaxSessions](./resource-parameters.md)  
[Jetclosetable](./jetclosetable-function.md)  
[Jetdupcursor](./jetdupcursor-function.md)  
[Jetendsession](./jetendsession-function.md)  
[Jetopentable](./jetopentable-function.md)  
[Jetopumtemptable](./jetopentemptable-function.md)  
[Jetrollback](./jetrollback-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[Jetterm](./jetterm-function.md)
