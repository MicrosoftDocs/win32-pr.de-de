---
title: Windows-Bereitstellungsdienste
description: Stellen Sie Windows Betriebssystem bereit. Richten Sie neue Clients mit einer netzwerkbasierten Installation ein, ohne dass Administratoren jeden Computer besuchen oder direkt von CD- oder DVD-Medien installieren müssen.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Windows Bereitstellungsdienste Windows Bereitstellungsdienste
- Windows Bereitstellungsdienste Windows Bereitstellungsdienste, Startseite
- Bereitstellungsdienste Windows Bereitstellungsdienste
- WDS Windows Deployment Services Siehe Windows Deployment Services
- Remoteinstallationsdienste Windows Bereitstellungsdienste Siehe Windows Deployment Services
- RIS Windows Deployment Services Siehe Windows Deployment Services
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

Windows Bereitstellungsdienste (Deployment Services, WDS) ist die überarbeitete Version der Remoteinstallationsdienste (REMOTE Installation Services, RIS). WDS ermöglicht die Bereitstellung von Windows Betriebssystemen. Sie können WDS verwenden, um neue Clients mit einer netzwerkbasierten Installation einzurichten, ohne dass Administratoren jeden Computer besuchen oder direkt von CD- oder DVD-Medien installieren müssen.

## <a name="developer-audience"></a>Entwicklergruppe

Die primäre Entwicklergruppe der WDS-API ist für Gruppen, die benutzerdefinierte Tools und Prozesse für DIE IT und andere Computerverwaltungsgruppen entwickeln. In Umgebungen, in denen die Standardlösung Windows Deployment Services (WDS) nicht verwendet werden kann, ermöglicht die WDS-API den programmgesteuerten Zugriff auf einige WDS-Komponenten.

Originalgerätehersteller (OEMs), Systementwickler und IT-Experten des Unternehmens, die Informationen zum Bereitstellen von Windows auf neuen Computern suchen, sollten die Informationen zur Standardlösung für Windows Deployment Services (WDS) in der [Schritt-für-Schritt-Anleitung](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) Windows Deployment Services Update und im [Windows Automated Installation Kit (OEMK)](https://www.microsoft.com/download/details.aspx?id=10333)anzeigen.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

WDS ist als Add-On für Windows Server 2003 mit Service Pack 1 (SP1) verfügbar und ab Windows Server 2003 mit Service Pack 2 (SP2) und Windows Server 2008 im Betriebssystem enthalten. Die WDS-PXE-Server-API erfordert die WDS-Serverrolle auf dem Server, um benutzerdefinierte PXE-Anbieter zu implementieren. Die WDS-Client-API erfordert die Phase der Einrichtung der Microsoft Windows Preinstallation Environment (Windows PE 2.0). Ein startbares RAMDISK-Image von Windows PE 2.0 in der . Das WIM-Format muss im Rahmen des Netzwerkstartprozesses heruntergeladen werden, um benutzerdefinierte WDS-Clients zu implementieren.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                 | BESCHREIBUNG                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Informationen zur Windows Deployment Services-API](about-the-windows-deployment-services-api.md)<br/> | Allgemeine Informationen zur WDS-Server-API und WDS-Client-API.<br/>    |
| [Windows Referenz zu Bereitstellungsdiensten](windows-deployment-services-reference.md)<br/>         | Beschreibt die Windows Deployment Services-Funktionen und -Strukturen.<br/> |



 

 

