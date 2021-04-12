---
title: Remote Datendienst entfernt
description: Remote Data Service-Serverkomponenten werden in Windows 8 entfernt
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- RDS-Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103949183"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a>Remote Data Service-Serverkomponenten werden in Windows 8 entfernt

## <a name="platforms"></a>Plattformen

 **Clients** -Windows 8  
**Server** -Windows Server 2012  



## <a name="description"></a>BESCHREIBUNG

Der Remote Data Service (RDS)-Server ist in Windows 8 nicht verfügbar:

-   Die Datei msadcf.dll, die das standardmäßige "Geschäftsobjekt" RDSServer. DataFactory hostet, wird entfernt, und die zugehörigen Dateien (msadcfr.dll, msadcfr.dll. MUI, Handler. reg und handsafe. reg) werden entfernt.
-   Die Datei msdfmap.dll, die der Standard Handler ist, wird entfernt, und die Datei msdfmap.ini wird entfernt.
-   Die Datei msadcs.dll, die ISAPI, wurde entfernt.

## <a name="manifestation"></a>Ausstrahlung

Kunden können keinen RDS-Server unter Windows 8 hosten.

## <a name="mitigation"></a>Minderung

Kunden können Ihren RDS-Server auf einem Computer mit Windows 7 oder anderen untergeordneten Betriebssystemen aufbewahren.

## <a name="solution"></a>Lösung

Kunden können Ihren RDS-Server auf einem Computer mit Windows 7 oder anderen untergeordneten Betriebssystemen aufbewahren.

## <a name="resources"></a>Ressourcen

[Roadmap für Datenzugriffs Technologien](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 