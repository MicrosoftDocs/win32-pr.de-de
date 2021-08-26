---
title: RAS-Verwaltungsfunktionen
description: In dieser Dokumentation werden RRAS-Funktionen beschrieben, die zum Entwickeln von Software zum Verwalten von RAS-DFÜ-Verbindungen verwendet werden.
ms.assetid: 27cf63e2-9dd3-4bc1-98af-e93055d89492
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2013305f1e37cdc90a1e331c93813520ff20aaafc6b32ffd2471f1f2cb7074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036280"
---
# <a name="ras-administration-functions"></a>RAS-Verwaltungsfunktionen

In dieser Dokumentation werden RRAS-Funktionen beschrieben, die zum Entwickeln von Software zum Verwalten von RAS-DFÜ-Verbindungen verwendet werden. Zu diesen Funktionen gehören:

-   [**MprAdminConnectionClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)
-   [**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)
-   [**MprAdminConnectionEnumEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenumex)
-   [**MprAdminConnectionGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)
-   [**MprAdminConnectionGetInfoEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfoex)
-   [**MprAdminConnectionRemoveQuarantine**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionremovequarantine)
-   [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)
-   [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)
-   [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)
-   [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)
-   [**MprAdminPortReset**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

Zusätzliche Funktionen werden sowohl für die RAS-Verwaltung als auch für die Routerverwaltung verwendet. Die folgenden Funktionen sind in der Referenz [zu Routerverwaltungsfunktionen](router-administration-functions.md) dokumentiert:

-   [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)
-   [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)
-   [**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)
-   [**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)
-   [**MprAdminServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

Verwenden Sie zum Implementieren einer RAS-Verwaltungs-DLL die im folgenden Thema beschriebenen Funktionen:

-   [RAS-Administrator-DLL-Funktionen](ras-admin-dll-functions.md)

Verwenden Sie zum Verwalten von Benutzern eines RAS-Servers die im folgenden Thema beschriebenen Funktionen:

-   [RAS-Benutzerverwaltungsfunktionen](ras-user-administration-functions.md)

 

 




