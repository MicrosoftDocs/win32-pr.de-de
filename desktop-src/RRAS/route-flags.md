---
title: Weiterleitungs Flags
description: Weiterleitungs Flags
ms.assetid: 17deae88-573f-48ec-887e-521549b39c32
keywords:
- Route
- Weiterleitungs Flags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1711ef4ed621d55cc00302cca181676a3892c030
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947447"
---
# <a name="route-flags"></a>Weiterleitungs Flags

## <a name="state-of-the-route-constants"></a>Status der Routen Konstanten



| Konstante                    | Wert | BESCHREIBUNG             |
|-----------------------------|-------|-------------------------|
| RTM- \_ Routen \_ Status \_ erstellt  | 0     | Die Route wurde erstellt. |
| RTM-Weiterleitungs \_ \_ Status wird \_ gelöscht | 1     | Die Route wird gelöscht. |
| RTM- \_ Routen \_ Status \_ gelöscht  | 2     | Die Route wurde gelöscht. |



 

## <a name="route-update-flags"></a>Weiterleitungs Update-Flags



| Konstante                  | Wert      | BESCHREIBUNG                                                                                                                                                                                |
|---------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RTM- \_ Routen \_ Änderung \_ zuerst | 0x01       | Gibt an, dass der Routing Tabellen-Manager das **Nachbar** Mitglied der RTM-Weiterleitungs [**\_ \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur nicht überprüfen soll, wenn bestimmt wird, wann zwei Routen gleich sind. |
| RTM- \_ Routen \_ Änderung \_ neu   | 0x02       | Wird vom Routing Tabellen-Manager zurückgegeben, um anzugeben, dass eine neue Route erstellt wurde.                                                                                                                 |
| RTM- \_ Routen \_ Änderung \_ am besten  | 0x00010000 | Wird vom Routing Tabellen-Manager zurückgegeben, um anzugeben, dass die Route, die hinzugefügt oder aktualisiert wurde, die beste Route war, oder dass aufgrund der Änderung eine neue Route zum besten Weg wurde.           |



 

## <a name="unicast-flags"></a>Unicastflags



| Konstante                  | Wert  | BESCHREIBUNG                                                            |
|---------------------------|--------|------------------------------------------------------------------------|
| RTM-Weiterleitungs \_ \_ Flags \_ lokal  | 0x0010 | Gibt an, dass sich ein Ziel in einem direkt erreichbaren Netzwerk befindet.            |
| RTM-Weiterleitungs \_ \_ Flags \_ Remote | 0x0020 | Gibt an, dass das Ziel nicht in einem direkt erreichbaren Netzwerk ist. |
| RTM-Weiterleitungs \_ \_ Flags \_ selbst | 0x0040 | Gibt an, dass das Ziel eine der Adressen des Routers ist.            |



 

## <a name="broadcast-and-multicast-flags"></a>Broadcast-und Multicast-Flags



| Konstante                           | Wert  | BESCHREIBUNG                                                                                                                                                                                                |
|------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RTM-Weiterleitungs \_ \_ Flags ( \_ mcast)           | 0x0100 | Gibt an, dass diese Route eine Route zu einer Multicast Adresse ist.                                                                                                                                               |
| RTM-Weiterleitungs \_ \_ Flags \_ lokale \_ mcast    | 0x0200 | Gibt an, dass diese Route eine Route zu einer lokalen Multicast Adresse ist.                                                                                                                                         |
| RTM-Weiterleitungs \_ \_ Flags \_ beschränkt auf \_ BC     | 0x0400 | Gibt an, dass diese Route eine eingeschränkte Broadcast Adresse ist. Pakete an dieses Ziel sollten nicht weitergeleitet werden.                                                                                             |
| RTM \_ - \_ Weitergabeflags \_ Nullen \_ netbc    | 0x1000 | Gibt an, dass das Ziel mit der vollständig Nullen-Broadcast Adresse einer Schnittstelle übereinstimmt. Wenn Broadcast Weiterleitung aktiviert ist, sollten Pakete empfangen und erneut gesendet werden.               |
| RTM \_ - \_ Weitergabeflags \_ Nullen \_ subnetbc | 0x2000 | Gibt an, dass das Ziel mit der Subnetz-Broadcast Adresse einer Schnittstelle mit allen Nullen übereinstimmt. Wenn die Weiterleitung von Subnetzbroadcast aktiviert ist, sollten Pakete empfangen und erneut übermittelt werden. |
| RTM \_ - \_ Weitergabeflags \_ \_ netbc     | 0x4000 | Gibt an, dass das Ziel mit der gesamten Broadcast Adresse einer Schnittstelle übereinstimmt. Wenn Broadcast Weiterleitung aktiviert ist, sollten Pakete empfangen und erneut gesendet werden.                |
| RTM \_ - \_ Weitergabeflags \_ \_ subnetbc  | 0x8000 | Gibt an, dass das Ziel mit der Subnetzbroadcast-Adresse einer Schnittstelle übereinstimmt. Wenn die Weiterleitung von Subnetzbroadcast aktiviert ist, sollten Pakete empfangen und erneut übermittelt werden.  |



 

## <a name="grouping-of-flags"></a>Gruppierung von Flags



| Gruppieren                            | Member                                                                                                                                                                  | BESCHREIBUNG                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| \_ \_ Weiterleitungs-Flags für RTM \_    | RTM-Weiterleitungs \_ \_ Flags \_ Martian, RTM-Weiterleitungs \_ \_ Flags \_ Blackhole, RTM-Weitergabeflags \_ \_ \_ verwerfen, RTM-Weitergabeflags \_ \_ \_                                                        | Gibt alle Weiterleitungs Flags an.                          |
| RTM-Weiterleitungs \_ \_ Flags \_ alle \_ Unicasts  | RTM-Weiterleitungs \_ \_ Flags \_ lokal, RTM-Weiterleitungs \_ \_ Flags \_ Remote, RTM-Weiterleitungs \_ \_ Flags \_ selbst                                                                                           | Gibt alle unicastflags an.                             |
| RTM-Weiterleitungs \_ \_ Flags für \_ beliebige \_ mcast    | RTM-Weiterleitungs \_ \_ Flags \_ mcast, RTM-Weiterleitungs \_ \_ Flags \_ lokale \_ mcast                                                                                                                | Gibt alle unicastflags an.                             |
| BCAST für RTM-Weiterleitungs \_ \_ Flags- \_ Subnetz \_ | RTM \_ - \_ Weitergabeflags \_ \_ : Subnetz- \_ BC, RTM-Weitergabeflags \_ \_ \_ Nullen \_ subnetbc                                                                                                  | Gibt alle subnetzübertragungsflags an.                    |
| RTM-Weiterleitungs \_ \_ Flags \_ net \_ Bcast    | RTM \_ - \_ Weitergabeflags \_ \_ netbc, RTM-Weiterleitungs \_ \_ Flags \_ Nullen \_ netbc                                                                                                          | Gibt alle netzwerkweiten Broadcast-Flags an.                  |
| RTM-Weiterleitungs \_ \_ Flags \_ beliebiger \_ Bcast    | RTM-Weiterleitungs \_ \_ Flags \_ beschränkte \_ BC, RTM-Weitergabeflags \_ \_ \_ \_ netbc, RTM-Weitergabeflags für \_ \_ \_ \_ Subnetz- \_ BC, RTM-Weiterleitungs \_ \_ Flags \_ Nullen \_ netbc, RTM-Weiterleitungs \_ \_ Flags \_ Nullen \_ subnetbc | Gibt das Subnetz oder die Netzwerk weiten Broadcast-Flags an. |



 

 

 




