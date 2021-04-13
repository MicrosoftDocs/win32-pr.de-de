---
title: Routing Table Manager Version 2-Funktionen
description: Die folgenden Funktionen werden für die Interaktion mit dem Routing Tabellen-Manager verwendet.
ms.assetid: ac5c6ada-c38e-476a-9896-cdd8c51cc0be
keywords:
- RRAS für den Routing-und RAS-Dienst, Routing-Tabellen-Manager Version 2, Funktionen
- Routing Table Manager Version 2 RRAS, Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f59e4a1ad2bf091d8a74672f1f473589c5fa1d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388448"
---
# <a name="routing-table-manager-version-2-functions"></a>Routing Table Manager Version 2-Funktionen

Die folgenden Funktionen werden für die Interaktion mit dem Routing Tabellen-Manager verwendet.

## <a name="registration-functions"></a>Registrierungsfunktionen

[**Rtmregisterentity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)

[**Rtmderegisterentity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity)

[**Rtmgetregisteredentities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities)

[**Rtmreleaseentities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities)

## <a name="opaque-pointer-functions"></a>Nicht transparente Zeiger Funktionen

[**Rtmlockdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination)

[**Rtmgetopaqueingeformationpointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer)

## <a name="export-method-functions"></a>Methoden Funktionen exportieren

[**Rtmgetentitymethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods)

[**Rtminvokemethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod)

[**Rtmblockmethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods)

## <a name="handle-to-information-structure-functions"></a>Handle für Informationsstruktur Funktionen

[**Rtmgetentityinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo)

[**Rtmgetdestinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo)

[**Rtmgetrouteingefo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)

[**Rtmgetnexthopinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo)

[**Rtmreleaseentityinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo)

[**Rtmreleasedestinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo)

[**Rtmreleaserouteingefo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo)

[**Rtmreleasenexthopinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)

## <a name="routing-table-insertion-and-deletion-functions"></a>Funktionen zum Einfügen und Löschen von Routing Tabellen

[**Rtmaddroutededest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest)

[**Rtmdeleteroutededest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutetodest)

[**Rtmholddestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination)

[**Rtmgetroutepointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetroutepointer)

[**Rtmlockroute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute)

[**Rtmupdateandunlockroute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute)

## <a name="routing-table-query-functions"></a>Routing Tabellen-Abfragefunktionen

[**Rtmgetexactmatchdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination)

[**Rtmgetmuspecificdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)

[**Rtmgetlessspecificdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination)

[**Rtmgetexactmatchroute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute)

[**Rtmisbestroute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute)

## <a name="next-hop-insertion-and-deletion-functions"></a>Funktionen zum Einfügen und löschen im nächsten Hop

[**Rtmaddnexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)

[**Rtmfindnexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop)

[**Rtmdeletenexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop)

[**Rtmgetnexthoppointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthoppointer)

[**Rtmlocknexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop)

## <a name="routing-table-enumeration-functions"></a>Routing Tabellen-Enumerationsfunktionen

[**Rtmkreatedesterum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum)

[**Rtmgetenumschlag**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests)

[**Rtmreleasedests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests)

[**Rtmkreaterouteenum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum)

[**Rtmgetenumroutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes)

[**Rtmreleaseroutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes)

[**Rtmkreatenexthopenum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum)

[**Rtmgetenrenexthops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops)

[**Rtmreleasenexthops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops)

[**Rtmdeleteenumschlag handle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle)

## <a name="change-notification-functions"></a>Änderungs Benachrichtigungsfunktionen

[**Rtmregisterforchangenotifizierung**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)

[**Rtmgetchangeddebug**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)

[**Rtmreleasechangeddebug**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests)

[**Rtmignorechangedentsts**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)

[**Rtmgetchangestatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus)

[**Rtmmarkdestforchangenotifizierung**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification)

[**Rtmismarkedforchangenotifizierung**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmismarkedforchangenotification)

[**Rtmderegisterfromchangenotifizierung**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)

## <a name="route-list-function"></a>Routenlisten Funktion

[**Rtmkreateroutelist**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist)

[**Rtminsertinroutelist**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist)

[**Rtmkreateroutelistenum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum)

[**Rtmgetlistenumroutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes)

[**Rtmdeleteroutelist**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist)

## <a name="handle-management-functions"></a>Verwalten von Verwaltungsfunktionen

[**Rtmreferencehandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles)

 

 




