---
description: Auf dieser Seite wird das Verhalten von Multicastsocketoptionen basierend auf verschiedenen Socketoptionseinstellungszuständen beschrieben.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Multicastsocket-Optionsverhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367487d12a6c54c8aaf5ce623c717ed229a001875c68a6b782dde0739a328ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993660"
---
# <a name="multicast-socket-option-behavior"></a>Multicastsocket-Optionsverhalten

Auf dieser Seite wird das Verhalten von Multicastsocketoptionen basierend auf verschiedenen Socketoptionseinstellungszuständen beschrieben.

Auf dieser Seite wird beispielsweise das Verhalten beschrieben, wenn die IP ADD \_ \_ SOURCE \_ MEMBERSHIP-Socketoption für einen Socket festgelegt ist, für den die OPTION IP \_ ADD SOURCE MEMBERSHIP bereits mit dem \_ \_ angegebenen Gruppen-/Quellpaar auf derselben Netzwerkschnittstelle festgelegt wurde. Es ist zulässig, IP \_ ADD SOURCE MEMBERSHIP für dieselbe Gruppe auf einer anderen Netzwerkschnittstelle \_ aufzurufen. \_

Diese Seite unterstützt Sie bei der ordnungsgemäßen Entwicklung und Problembehandlung Windows Sockets-Multicastanwendungen. 

<table>
<thead>
<tr class="header">
<th>Anfängliche Socketoption</th>
<th>In Konfliktstehende nachfolgende Socketoption</th>
<th>Zurückgegebener Fehler</th>
<th>Hinweise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">IP_ADD_MEMBERSHIP${REMOVE}$<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Rufen Sie IP_ADD_MEMBERSHIP mit derselben Gruppe nicht mehr als einmal auf derselben Netzwerkschnittstelle auf.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Rufen Sie nicht IP_ADD_SOURCE_MEMBERSHIP mit derselben Gruppe auf, die zuvor mit IP_ADD_MEMBERSHIP auf derselben Netzwerkschnittstelle aufgerufen wurde.</td>

</tr>
<tr class="odd">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Verwenden Sie stattdessen IP_BLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Gibt einen Fehler zurück, wenn versucht wird, die Blockierung eines Gruppen-/Quellpaars aufzuheben, das zuvor nicht auf derselben Netzwerkschnittstelle blockiert wurde.</td>

</tr>
<tr class="odd">
<td>IP_DROP_MEMBERSHIP</td>
<td>Alle nachfolgenden Aufrufe für dieselbe Gruppe oder Gruppe bzw. das gleiche Quellpaar</td>
<td>WSAEINVAL</td>
<td>Socketoptionsaufrufe für eine Gruppe oder ein Gruppen-/Quellpaar, die derzeit nicht in der Aufnahmeliste enthalten sind (aufgrund des Löschens der Mitgliedschaft oder anderweitig), führen zu einem Fehler.</td>
</tr>
<tr class="even">
<td rowspan="3">IP_ADD_SOURCE_MEMBERSHIP${REMOVE}$<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Rufen Sie nicht IP_ADD_MEMBERSHIP mit derselben Gruppe auf, die zuvor mit IP_ADD_SOURCE_MEMBERSHIP auf derselben Netzwerkschnittstelle aufgerufen wurde.</td>
</tr>
<tr class="odd">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Rufen Sie IP_ADD_SOURCE_MEMBERSHIP nicht mit demselben Gruppen-/Quellpaar auf, das zuvor mit IP_ADD_SOURCE_MEMBERSHIP auf derselben Netzwerkschnittstelle aufgerufen wurde.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Gibt einen Fehler zurück, wenn versucht wird, die Blockierung eines Gruppen-/Quellpaars aufzuheben, das zuvor nicht auf derselben Netzwerkschnittstelle blockiert wurde.</td>

</tr>
<tr class="odd">
<td rowspan="2">IP_DROP_SOURCE_MEMBERSHIP${REMOVE}$<br />
</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Gibt einen Fehler zurück, wenn versucht wird, die Blockierung eines Gruppen-/Quellpaars aufzuheben, das zuvor nicht auf derselben Netzwerkschnittstelle blockiert wurde.</td>
</tr>
<tr class="even">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Gibt einen Fehler zurück, wenn versucht wird, ein Gruppen-/Quellpaar zu löschen, das nicht in der Aufnahmeliste derselben Netzwerkschnittstelle enthalten ist.</td>

</tr>
<tr class="odd">
<td rowspan="3">IP_BLOCK_SOURCE${REMOVE}$<br />
</td>
<td>IP_BLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Gibt einen Fehler zurück, wenn versucht wird, ein Gruppen-/Quellpaar zu blockieren, das bereits auf derselben Netzwerkschnittstelle blockiert ist.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Verwenden Sie stattdessen IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="odd">
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Verwenden Sie stattdessen IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Gibt einen Fehler zurück, wenn versucht wird, die Blockierung eines Gruppen-/Quellpaars aufzuheben, das nicht in der Sperrliste auf derselben Netzwerkschnittstelle enthalten ist.</td>
</tr>
</tbody>
</table>



 

 

 



