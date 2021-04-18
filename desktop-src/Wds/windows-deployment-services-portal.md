---
title: Windows-Bereitstellungsdienste
description: Bereitstellen von Windows-Betriebssystemen. Richten Sie neue Clients mit einer netzwerkbasierten Installation ein, ohne dass Administratoren jeden Computer besuchen oder direkt von CD-oder DVD-Medien installieren.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Windows-Bereitstellungs Dienste Windows-Bereitstellungs Dienste
- Windows-Bereitstellungs Dienste Windows-Bereitstellungs Dienste, Startseite
- Bereitstellungs Dienste Windows-Bereitstellungs Dienste
- WDS Windows-Bereitstellungs Dienste Siehe Windows-Bereitstellungs Dienste
- Remoteinstallations Dienste Windows-Bereitstellungs Dienste Weitere Informationen
- RIS Windows-Bereitstellungs Dienste Siehe Windows-Bereitstellungs Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341327"
---
# <a name="windows-deployment-services"></a>Windows-Bereitstellungsdienste

## <a name="purpose"></a>Zweck

Die Windows-Bereitstellungs Dienste (Windows Deployment Services, WDS) sind die überarbeitete Version der Remoteinstallations Dienste WDS ermöglicht die Bereitstellung von Windows-Betriebssystemen. Sie können WDS verwenden, um neue Clients mit einer netzwerkbasierten Installation einzurichten, ohne dass Administratoren jeden Computer besuchen oder direkt von CD-oder DVD-Medien installieren müssen.

## <a name="developer-audience"></a>Entwicklergruppe

Die primäre Entwicklergruppe der WDS-API ist für Gruppen vorgesehen, die benutzerdefinierte Tools und Prozesse für Sie und andere Computer Verwaltungs Gruppen entwickeln. In Umgebungen, in denen die Standardlösung für Windows-Bereitstellungs Dienste (WDS) nicht verwendet werden kann, ermöglicht die WDS-API den programmgesteuerten Zugriff auf einige WDS-Komponenten.

Original Gerätehersteller (OEMs), System-Generatoren und IT-Experten von Unternehmen, die Informationen zur Bereitstellung von Windows auf neuen Computern suchen, sollten die Informationen zur Standardlösung für Windows-Bereitstellungs Dienste (Windows Deployment Services, WDS) in den [Schritt-für-Schritt-Anleitungen für die Windows-Bereitstellungs Dienste](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) und das [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333)sehen.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

WDS ist als Add-on für Windows Server 2003 mit Service Pack 1 (SP1) verfügbar und im Betriebssystem ab Windows Server 2003 mit Service Pack 2 (SP2) und Windows Server 2008 enthalten. Die WDS-PXE-Server-API erfordert, dass die WDS-Server Rolle auf dem Server benutzerdefinierte PXE-Anbieter implementiert. Die WDS-Client-API erfordert die Microsoft Windows Preinstallation Environment-Phase (Windows PE 2,0) der Setup Verarbeitung. Ein RAMDisk-Start fähiges Image von Windows PE 2,0 in der. Das WIM-Format muss als Teil des Netzwerkstart Vorgangs heruntergeladen werden, um benutzerdefinierte WDS-Clients implementieren zu können.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                 | BESCHREIBUNG                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Informationen zur API für die Windows-Bereitstellungs Dienste](about-the-windows-deployment-services-api.md)<br/> | Allgemeine Informationen über die WDS-Server-API und die WDS-Client-API.<br/>    |
| [Referenz zu Windows-Bereitstellungs Diensten](windows-deployment-services-reference.md)<br/>         | Beschreibt die Funktionen und Strukturen der Windows-Bereitstellungs Dienste.<br/> |



 

 

