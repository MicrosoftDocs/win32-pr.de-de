---
title: Routenflags
description: Routenflags
ms.assetid: 17deae88-573f-48ec-887e-521549b39c32
keywords:
- Route
- Routenflags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1476742f1204eb14dd2bb96b289825d179a58e5bec01ff0aee18bcfbdb13a9b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081240"
---
# <a name="route-flags"></a>Routenflags

## <a name="state-of-the-route-constants"></a>Status der Routenkonst constants



| Konstante                    | Wert | BESCHREIBUNG             |
|-----------------------------|-------|-------------------------|
| \_RTM-ROUTENSTATUS \_ \_ ERSTELLT  | 0     | Route wurde erstellt. |
| \_ \_ RTM-ROUTENSTATUSLÖSCHUNG \_ | 1     | Die Route wird gelöscht. |
| \_RTM-ROUTENSTATUS \_ \_ GELÖSCHT  | 2     | Die Route wurde gelöscht. |



 

## <a name="route-update-flags"></a>Routenaktualisierungsflags



| Konstante                  | Wert      | BESCHREIBUNG                                                                                                                                                                                |
|---------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_RTM-ROUTENÄNDERUNG \_ \_ ZUERST | 0x01       | Gibt an, dass der Routingtabellen-Manager beim Bestimmen, ob zwei Routen gleich sind, nicht das Member **"1000"** der [**\_ \_ RTM-ROUTENINFORMATIONsstruktur**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) überprüfen soll. |
| \_RTM-ROUTENÄNDERUNG \_ \_ NEU   | 0x02       | Wird vom Routingtabellen-Manager zurückgegeben, um anzugeben, dass eine neue Route erstellt wurde.                                                                                                                 |
| \_RTM-ROUTENÄNDERUNG \_ \_ AM BESTEN  | 0x00010000 | Wird vom Routingtabellen-Manager zurückgegeben, um anzugeben, dass die hinzugefügte oder aktualisierte Route die beste Route war oder dass aufgrund der Änderung eine neue Route zur besten Route wurde.           |



 

## <a name="unicast-flags"></a>Unicastflags



| Konstante                  | Wert  | BESCHREIBUNG                                                            |
|---------------------------|--------|------------------------------------------------------------------------|
| \_RTM-ROUTENFLAGS \_ \_ LOKAL  | 0x0010 | Gibt an, dass sich ein Ziel in einem direkt erreichbaren Netzwerk befindet.            |
| \_RTM-ROUTENFLAGS \_ \_ REMOTE | 0x0020 | Gibt an, dass sich das Ziel nicht in einem direkt erreichbaren Netzwerk befindet. |
| \_ \_ RTM-ROUTENFLAGS \_ SELBST | 0x0040 | Gibt an, dass das Ziel eine der Adressen des Routers ist.            |



 

## <a name="broadcast-and-multicast-flags"></a>Broadcast- und Multicastflags



| Konstante                           | Wert  | BESCHREIBUNG                                                                                                                                                                                                |
|------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_RTM-ROUTENFLAGS \_ \_ MCAST           | 0x0100 | Gibt an, dass diese Route eine Route zu einer Multicastadresse ist.                                                                                                                                               |
| RTM \_ ROUTE \_ FLAGS \_ LOCAL \_ MCAST    | 0x0200 | Gibt an, dass diese Route eine Route zu einer lokalen Multicastadresse ist.                                                                                                                                         |
| RTM \_ ROUTE \_ FLAGS \_ LIMITED \_ BC     | 0x0400 | Gibt an, dass diese Route eine eingeschränkte Broadcastadresse ist. Pakete an dieses Ziel sollten nicht weitergeleitet werden.                                                                                             |
| \_RTM-ROUTENFLAGS \_ \_ NULLEN \_ NETBC    | 0x1000 | Gibt an, dass das Ziel mit der Broadcastadresse einer Schnittstelle mit nullen übereinstimmung. Wenn die Broadcastweiterleitung aktiviert ist, sollten Pakete empfangen und alle entsprechenden Schnittstellen erneut gesendet werden.               |
| RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ SUBNETBC | 0x2000 | Gibt an, dass das Ziel mit der Broadcastadresse des Subnetzes mit allen Nullen einer Schnittstelle entspricht. Wenn die Subnetzübertragungsweiterleitung aktiviert ist, sollten Pakete empfangen und alle entsprechenden Schnittstellen erneut gesendet werden. |
| RTM \_ ROUTE \_ FLAGS \_ ONES \_ NETBC     | 0x4000 | Gibt an, dass das Ziel der All-Ones-Broadcastadresse einer Schnittstelle entspricht. Wenn die Broadcastweiterleitung aktiviert ist, sollten Pakete empfangen und alle entsprechenden Schnittstellen erneut gesendet werden.                |
| RTM \_ ROUTE \_ FLAGS \_ ONES \_ SUBNETBC  | 0x8000 | Gibt an, dass das Ziel der Broadcastadresse eines All-Ones-Subnetzes einer Schnittstelle entspricht. Wenn die Subnetzübertragungsweiterleitung aktiviert ist, sollten Pakete empfangen und alle entsprechenden Schnittstellen erneut gesendet werden.  |



 

## <a name="grouping-of-flags"></a>Gruppieren von Flags



| Group                            | Members                                                                                                                                                                  | Beschreibung                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| WEITERLEITUNG VON \_ \_ RTM-ROUTENFLAGS \_    | RTM \_ ROUTE \_ FLAGS \_ MARTIAN, RTM \_ ROUTE \_ FLAGS \_ BLACKHOLE, RTM \_ ROUTE \_ FLAGS \_ DISCARD, RTM \_ ROUTE \_ FLAGS \_ INACTIVE                                                        | Gibt alle Weiterleitungsflags an.                          |
| RTM \_ ROUTE \_ FLAGS \_ ANY \_ UNICAST  | RTM \_ ROUTE \_ FLAGS \_ LOCAL, RTM \_ ROUTE \_ FLAGS \_ REMOTE, RTM \_ ROUTE \_ FLAGS \_ MYSELF                                                                                           | Gibt alle Unicastflags an.                             |
| RTM \_ ROUTE \_ FLAGS \_ ANY \_ MCAST    | RTM \_ ROUTE \_ FLAGS \_ MCAST, RTM \_ ROUTE \_ FLAGS \_ LOCAL \_ MCAST                                                                                                                | Gibt alle Unicastflags an.                             |
| \_RTM-ROUTENFLAGS \_ \_ SUBNETZ \_ BCAST | RTM \_ ROUTE \_ FLAGS \_ ONES \_ SUBNET \_ BC, RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ SUBNETBC                                                                                                  | Gibt alle Subnetz-Broadcastflags an.                    |
| \_RTM-ROUTENFLAGS \_ \_ NET \_ BCAST    | RTM \_ ROUTE \_ FLAGS \_ ONES \_ NETBC, RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ NETBC                                                                                                          | Gibt alle netzweiten Broadcastflags an.                  |
| RTM \_ ROUTE \_ FLAGS \_ ANY \_ BCAST    | RTM \_ ROUTE \_ FLAGS \_ LIMITED \_ BC, RTM \_ ROUTE \_ FLAGS \_ ONES \_ NETBC, RTM \_ ROUTE \_ FLAGS \_ ONES \_ SUBNET \_ BC, RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ NETBC, RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ SUBNETBC | Gibt eines der Subnetz- oder netzwerkweiten Broadcastflags an. |



 

 

 




