---
title: Verarbeiten von Gruppen und Rückrufen
description: In der folgenden Tabelle werden eine Reihe von Schritten für eine operative Interaktion zwischen einem Routing Protokoll und dem Multicast-Gruppen-Manager zusammengefasst.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2878ec15cfb663353f3dd0bc1dc5aeadbd2e1e7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316635"
---
# <a name="processing-groups-and-callbacks"></a>Verarbeiten von Gruppen und Rückrufen

In der folgenden Tabelle werden eine Reihe von Schritten für eine operative Interaktion zwischen einem Routing Protokoll und dem Multicast-Gruppen-Manager zusammengefasst. In der ersten Spalte werden die Aktionen beschrieben, die das Routing Protokoll ausführt, und die Antwort des Routing Protokolls an den Multicast-Gruppen-Manager. In der zweiten Spalte werden die Antworten des Multicast Gruppen-Managers auf das Routing Protokoll und alle Aktionen beschrieben, die der Multicast-Gruppen-Manager ausführt, z. b. Rückrufe. Die dritte Spalte enthält alle zusätzlichen Informationen.

Jede Zeile der Tabelle stellt einen Schritt dar.

Die in dieser Tabelle aufgeführten Tasks treten nicht in einer bestimmten Reihenfolge auf. Stattdessen erfolgen Sie basierend auf dem Status von Multicast Gruppenmitgliedschaften. Die folgende Tabelle zeigt eine Beispiel Reihenfolge.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Routing Protokoll Aktion</th>
<th>Multicast-Gruppen-Manager-Aktion</th>
<th>Notizen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Verwalten von Gruppenmitgliedschaften auf der Grundlage von Protokollinformationen, die über die Schnittstellen des Protokolls empfangen werden. Die Verwaltung erfolgt mithilfe der folgenden Funktionen:
<ul>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>Mgmaddgroupmembership shipentry</strong></a></li>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>Mgmdeletegroupmembership shipentry</strong></a></li>
</ul></td>
<td>Fügen Sie in der Liste der ausgehenden Schnittstellen zu und für die angegebenen Einträge (s, g), (*, g) und (*, *) hinzu, und löschen Sie Sie. Diese Liste stellt den Satz von Schnittstellen dar, an denen Daten für diese Gruppe weitergeleitet werden. Die Daten für diese Gruppe werden aus der angegebenen Quelle abgeleitet.</td>

</tr>
<tr class="even">

<td>Senden von Warnungen an Routing Protokolle in Form von Rückrufen Die folgenden Ereignisse lösen den Multicast-Gruppen-Manager aus, um einen Rückruf aufzurufen:
<ul>
<li>Beitreten oder verlassen Sie Gruppen <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong></strong></a>(PMGM_JOIN_ALERT_CALLBACK <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</li>
<li>Die Gruppenmitgliedschaft wurde von IGMP geändert ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a> <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</li>
<li>An falscher Schnittstelle empfangene Daten ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</li>
<li>Daten, die von neuen Quellen oder einer neuen Gruppe ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> und <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>) empfangen werden.</li>
</ul></td>
<td>Mithilfe dieser Rückrufe kann der Multicast-Gruppen-Manager die Paket Weiterleitung koordinieren, wenn mehrere Multicast-Routing Protokolle auf einem Router vorhanden sind.</td>
</tr>
<tr class="odd">
<td>Auflisten der Multicast Weiterleitungs Einträge (MFEs) mithilfe der <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>mgmgetfirstmfe</strong></a>-, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>mgmgetnextmfe</strong></a>-und <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>mgmgetmfe</strong></a> -Funktionen. Treffen Sie Entscheidungen über Multicast Daten basierend auf den Ergebnissen der-Enumeration.</td>
<td>Gibt die angeforderten MFEs zurück. Gibt ERROR_NO_MORE Elemente zurück, wenn keine weiteren MFEs zurückgegeben werden müssen.<br/></td>
<td>Verwenden Sie die <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>mgmgetfirstmfestats</strong></a>-, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>mgmgetnextmfestats</strong></a>-und <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>mgmgetmfestats</strong></a> -Funktionen, um MFE-Statistiken aufzuzählen. Ein umfassendes Beispiel für die Verwendung dieser Funktionen finden Sie unter <a href="administrative-application-scenario.md">Verwaltungs Anwendungsszenario</a> .<br/></td>
</tr>
<tr class="even">
<td>Ändern Sie den Upstream-Nachbar in einem MFE mithilfe der <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>mgmabtmfe</strong></a> -Funktion.</td>

<td>Clients verwenden diese Funktion, um die Informationen in Bezug auf die eingehende Schnittstelle zu ändern.</td>
</tr>
</tbody>
</table>



 

 

