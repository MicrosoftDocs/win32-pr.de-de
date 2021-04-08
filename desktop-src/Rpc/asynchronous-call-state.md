---
title: Asynchroner Aufrufstatus
description: Auf dieser Seite wird der asynchrone Aufruf Status für RPC-Aufrufe beschrieben.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856971"
---
# <a name="asynchronous-call-state"></a>Asynchroner Aufrufstatus

Auf dieser Seite wird der asynchrone Aufruf Status für RPC-Aufrufe beschrieben.

## <a name="client-behavior"></a>Client Verhalten



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Name des Zustands</th>
<th>Aktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Ausführen des Aufrufes</td>
<td>Erstellen des RPC
<ul>
<li>Bei Erfolg gehe zu Status wcomp</li>
<li>Bei Ausnahme gehe zu Ende</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="even">
<td>Kann</td>
<td>Abbrechen des Aufrufes</td>
<td>Aufrufen von <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>rpcasynccancelcallgo</strong></a>zu wcomp<br/></td>
</tr>
<tr class="odd">
<td>Wcomp</td>
<td>Auf Abschluss warten</td>
<td>Warten Sie, bis notificationcall\benachrichtigungs Benachrichtigung empfangen wurde.<br/> Gehe zu Comp<br/></td>
</tr>
<tr class="even">
<td>Zuschreiben</td>
<td>Completion</td>
<td>Problem " <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcasynccompletecallgo</strong></a>to End"<br/></td>
</tr>
<tr class="odd">
<td>Ende</td>


</tr>
</tbody>
</table>



 

## <a name="server-behavior"></a>Server Verhalten



| State | Name des Zustands     | Aktion                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | Dispatch       | Der Aufruf wird vom RPC-runtimeprocess gesendet.<br/> Gehe zu Comp<br/> So führen Sie einen fehlerhaften Fehler (während der Ausführung im RPC-Thread) aus: Ausnahme auslösen; Gehe zu Ende<br/> So führen Sie einen fehlerhaften Fehler aus: Gehe zu A<br/> |
| A     | Abbrechen des Aufrufes | Aufrufen von [**rpcasyncabortcallgo**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)zum Ende<br/>                                                                                                                                             |
| Zuschreiben  | Completion     | Problem " [**rpcasynccompletecallgo**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)to End"<br/>                                                                                                                                      |
| Ende   |                |                                                                                                                                                                                                                     |



 

 

 





