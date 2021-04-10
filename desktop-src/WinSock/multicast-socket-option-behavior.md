---
description: Auf dieser Seite wird das Verhalten von Multicast Socketoptionen basierend auf verschiedenen Einstellungen für Socketoptionen beschrieben.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Multicast-socketoptionsverhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041726"
---
# <a name="multicast-socket-option-behavior"></a>Multicast-socketoptionsverhalten

Auf dieser Seite wird das Verhalten von Multicast Socketoptionen basierend auf verschiedenen Einstellungen für Socketoptionen beschrieben.

Auf dieser Seite wird z. b. das Verhalten beschrieben, wenn die IP- \_ \_ \_ Option Quell Mitgliedschafts Socket hinzufügen für einen Socket festgelegt ist, für den die IP- \_ \_ Option Quell- \_ Mitgliedschaftsoption bereits mit dem angegebenen Gruppen-/quellpaar auf derselben Netzwerkschnittstelle festgelegt wurde. Es ist zulässig, IP- \_ Add- \_ Source- \_ Mitgliedschaft in derselben Gruppe auf einer anderen Netzwerkschnittstelle aufzurufen.

Diese Seite hilft bei der ordnungsgemäßen Entwicklung und Problembehandlung von Windows Sockets-Multicast Anwendungen. 

<table>
<thead>
<tr class="header">
<th>Anfängliche Socketoption</th>
<th>Widersprüchliche nachfolgende Socketoption</th>
<th>Fehler zurückgegeben</th>
<th>Bemerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">IP_ADD_MEMBERSHIP $ {Remove} $<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Nennen Sie IP_ADD_MEMBERSHIP nicht mehr als einmal in derselben Netzwerkschnittstelle.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Nennen Sie IP_ADD_SOURCE_MEMBERSHIP nicht mit derselben Gruppe, die zuvor mit IP_ADD_MEMBERSHIP auf derselben Netzwerkschnittstelle aufgerufen wurde.</td>

</tr>
<tr class="odd">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>Wsaabval</td>
<td>Verwenden Sie stattdessen IP_BLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>Wsaabval</td>
<td>Gibt einen Fehler zurück, wenn versucht wird, die Blockierung eines Gruppen-/Quell-Paars aufzuheben, das zuvor nicht an derselben Netzwerkschnittstelle blockiert wurde.</td>

</tr>
<tr class="odd">
<td>IP_DROP_MEMBERSHIP</td>
<td>Alle nachfolgenden Aufrufe für dasselbe Gruppen-oder Gruppen-/quellpaar</td>
<td>Wsaabval</td>
<td>Das Erstellen von socketoptionsaufrufen für eine Gruppe oder ein Gruppen-/Quell-Paar, das sich derzeit nicht in der Aufnahme Liste (aufgrund der Löschung der Mitgliedschaft oder anderweitig), führt zu einem Fehler.</td>
</tr>
<tr class="even">
<td rowspan="3">IP_ADD_SOURCE_MEMBERSHIP $ {Remove} $<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Nennen Sie IP_ADD_MEMBERSHIP nicht mit derselben Gruppe, die zuvor mit IP_ADD_SOURCE_MEMBERSHIP auf derselben Netzwerkschnittstelle aufgerufen wurde.</td>
</tr>
<tr class="odd">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Sie sollten IP_ADD_SOURCE_MEMBERSHIP nicht mit demselben Gruppen-/quellpaar aufrufen, das zuvor mit IP_ADD_SOURCE_MEMBERSHIP auf derselben Netzwerkschnittstelle aufgerufen wurde.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>Wsaabval</td>
<td>Gibt einen Fehler zurück, wenn versucht wird, die Blockierung eines Gruppen-/Quell-Paars aufzuheben, das zuvor nicht an derselben Netzwerkschnittstelle blockiert wurde.</td>

</tr>
<tr class="odd">
<td rowspan="2">IP_DROP_SOURCE_MEMBERSHIP $ {Remove} $<br />
</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>Wsaabval</td>
<td>Gibt einen Fehler zurück, wenn versucht wird, die Blockierung eines Gruppen-/Quell-Paars aufzuheben, das zuvor nicht an derselben Netzwerkschnittstelle blockiert wurde.</td>
</tr>
<tr class="even">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Gibt einen Fehler zurück, wenn versucht wird, ein Gruppen-/quellpaar zu löschen, das sich nicht in der Aufnahme Liste auf derselben Netzwerkschnittstelle befindet.</td>

</tr>
<tr class="odd">
<td rowspan="3">IP_BLOCK_SOURCE $ {Remove} $<br />
</td>
<td>IP_BLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Gibt einen Fehler zurück, wenn versucht wird, ein Gruppen-/Quell-paar zu blockieren, das bereits auf derselben Netzwerkschnittstelle blockiert ist.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>Wsaabval</td>
<td>Verwenden Sie stattdessen IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="odd">
<td>IP_ADD_MEMBERSHIP</td>
<td>Wsaabval</td>
<td>Verwenden Sie stattdessen IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Gibt einen Fehler zurück, wenn versucht wird, ein Gruppen-/quellpaar aufzuheben, das sich nicht in der Liste der blockierten Netzwerke auf derselben Netzwerkschnittstelle befindet.</td>
</tr>
</tbody>
</table>



 

 

 



