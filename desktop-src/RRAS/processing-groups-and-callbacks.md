---
title: Verarbeiten von Gruppen und Rückrufen
description: In der folgenden Tabelle sind eine Reihe von Schritten in einer betrieblichen Interaktion zwischen einem Routingprotokoll und dem Multicastgruppen-Manager zusammengefasst.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3315f0a5db0dbcef9ac13e07ff9b9a2bb0b476be
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479686"
---
# <a name="processing-groups-and-callbacks"></a>Verarbeiten von Gruppen und Rückrufen

In der folgenden Tabelle sind eine Reihe von Schritten in einer betrieblichen Interaktion zwischen einem Routingprotokoll und dem Multicastgruppen-Manager zusammengefasst. Die erste Spalte beschreibt die Aktionen, die das Routingprotokoll ausführt, und die Antworten des Routingprotokolls an den Multicastgruppen-Manager. Die zweite Spalte beschreibt die Antworten des Multicastgruppen-Managers auf das Routingprotokoll und alle Aktionen, die der Multicastgruppen-Manager ausführt, z. B. Rückrufe. Die dritte Spalte enthält alle zusätzlichen Informationen.

Jede Zeile der Tabelle stellt einen Schritt dar.

Die in dieser Tabelle aufgeführten Aufgaben werden in keiner bestimmten Reihenfolge ausgeführt. stattdessen treten sie basierend auf dem Status von Multicastgruppenmitgliedschaften auf. Die folgende Tabelle zeigt eine Beispielreihenfolge.




| Routingprotokollaktion | Multicast-Gruppen-Manager-Aktion | Hinweise | 
|-------------------------|--------------------------------|-------|
| Verwalten Sie Gruppenmitgliedschaften basierend auf Protokollinformationen, die für die Schnittstellen empfangen werden, die das Protokoll besitzt. Die Verwaltung erfolgt mithilfe der folgenden Funktionen:<ul><li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></li><li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></li></ul> | Fügen Sie der Ausgehenden Schnittstellenliste für die angegebenen Einträge (s, g), (*, g) und (*, *) hinzu, und löschen Sie sie. Diese Liste stellt den Satz von Schnittstellen dar, an die Daten für diese Gruppe weitergeleitet werden. Die Daten für diese Gruppe stammen aus der angegebenen Quelle. | 
| Senden sie Warnungen in Form von Rückrufen an Routingprotokolle. Die folgenden Ereignisse lösen den Multicastgruppen-Manager aus, um einen Rückruf aufzurufen:<ul><li>Beitreten zu oder Verlassen von Gruppen ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</li><li>Gruppenmitgliedschaft durch IGMP geändert ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</li><li>Auf der falschen Schnittstelle empfangene Daten ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</li><li>Daten, die aus neuen Quellen oder in einer neuen Gruppe <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>(PMGM_CREATION_ALERT_CALLBACK</strong></a> und <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>) empfangen werden.</li></ul> | Mithilfe dieser Rückrufe kann der Multicastgruppen-Manager die Paketweiterleitung koordinieren, wenn mehrere Multicastroutingprotokolle auf einem Router vorhanden sind. | 
| Auflisten der Multicastweiterleitungseinträge (MFEs) mithilfe der Funktionen <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe,</strong></a> <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>und <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe.</strong></a> Treffen Sie Entscheidungen zu Multicastdaten basierend auf den Ergebnissen der Enumeration. | Gibt die angeforderten MFEs zurück. Gibt ERROR_NO_MORE ITEMS zurück, wenn keine MFEs mehr zurückgegeben werden sollen.<br /> | Verwenden Sie die Funktionen <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats,</strong></a> <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>und <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats,</strong></a> um MFE-Statistiken aufzulisten. Ein vollständiges Beispiel für die Verwendung dieser Funktionen finden Sie unter Szenario für <a href="administrative-application-scenario.md">administrative</a> Anwendungen.<br /> | 
| Ändern Sie den Upstreamnachbarn in einem MFE mithilfe der <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe-Funktion.</strong></a> | Clients verwenden diese Funktion, um die Informationen zur eingehenden Schnittstelle zu ändern. | 




 

 

