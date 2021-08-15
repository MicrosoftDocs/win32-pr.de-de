---
title: Windows-Bereitstellungsdienste
description: Bereitstellen Windows Betriebssystemen. Richten Sie neue Clients mit einer netzwerkbasierten Installation ein, ohne dass Administratoren jeden Computer besuchen oder direkt über CD- oder DVD-Medien installieren müssen.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Windows Bereitstellungsdienste Windows Bereitstellungsdiensten
- Windows Deployment Services Windows Deployment Services , Startseite
- Bereitstellungsdienste Windows Bereitstellungsdiensten
- WDS Windows Deployment Services siehe Windows Deployment Services
- Remoteinstallationsdienste Windows Bereitstellungsdienste siehe Windows Bereitstellungsdienste
- RIS Windows Deployment Services siehe Windows Deployment Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100483541420015ed84a95543f2f94bafb2d509d44e6b321b53729caa94588cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999510"
---
# <a name="windows-deployment-services"></a>Windows-Bereitstellungsdienste

## <a name="purpose"></a>Zweck

Windows Deployment Services (WDS) ist die überarbeitete Version der Remoteinstallationsdienste (Remote Installation Services, RIS). WDS ermöglicht die Bereitstellung Windows Betriebssystemen. Mit WDS können Sie neue Clients mit einer netzwerkbasierten Installation einrichten, ohne dass Administratoren jeden Computer besuchen oder direkt über CD- oder DVD-Medien installieren müssen.

## <a name="developer-audience"></a>Entwicklergruppe

Die primäre Entwicklergruppe der WDS-API ist für Gruppen, die benutzerdefinierte Tools und Prozesse für IT- und andere Computerverwaltungsgruppen entwickeln. In Umgebungen, in denen die standard Windows Deployment Services (WDS)-Lösung nicht verwendet werden kann, ermöglicht die WDS-API programmgesteuerten Zugriff auf einige WDS-Komponenten.

Originalgerätehersteller (Original Equipment Manufacturers, OEMs), Systemgeneratoren und IT-Experten im Unternehmen, die Informationen zum Bereitstellen von Windows auf neuen Computern suchen, sollten die Informationen zur standardmäßigen WDS-Lösung (Windows Deployment Services) in der [Schritt-für-Schritt-Anleitung](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) zum Update von Windows Deployment Services und im [Windows Automated Installation Kit (CSK)](https://www.microsoft.com/download/details.aspx?id=10333)finden.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

WDS ist als Add-On für Windows Server 2003 mit Service Pack 1 (SP1) verfügbar und ab Windows Server 2003 mit Service Pack 2 (SP2) und Windows Server 2008 im Betriebssystem enthalten. Die WDS-PXE-Server-API erfordert die WDS-Serverrolle auf dem Server, um benutzerdefinierte PXE-Anbieter zu implementieren. Die WDS-Client-API erfordert die Microsoft Windows-Vorinstallationsumgebung (Windows PE 2.0) der Setupverarbeitung. Ein startbares RAMDISK-Image Windows PE 2.0 im . Das WIM-Format muss im Rahmen des Netzwerkstartprozesses heruntergeladen werden, um benutzerdefinierte WDS-Clients zu implementieren.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                 | BESCHREIBUNG                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Informationen zur Windows Deployment Services-API](about-the-windows-deployment-services-api.md)<br/> | Allgemeine Informationen zur WDS-Server-API und WDS-Client-API.<br/>    |
| [Windows Referenz zu Bereitstellungsdiensten](windows-deployment-services-reference.md)<br/>         | Beschreibt die Windows Und-Strukturen der Bereitstellungsdienste.<br/> |



 

 

