---
description: In diesem Abschnitt wird der Versionsverlauf von Tablet PC-Technologien beschrieben.
ms.assetid: 69eb161a-2330-456f-b7b8-234cf02c8b58
title: Verlauf der Tablet PC-Plattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f258876f79f8e701ed59242233dcccc292b15f52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050443"
---
# <a name="tablet-pc-platform-history"></a>Verlauf der Tablet PC-Plattform

In diesem Abschnitt wird der Versionsverlauf von Tablet PC-Technologien beschrieben.

## <a name="platform-description"></a>Platt Form Beschreibung

Mit den Komponenten der Tablet PC-Technologie können Sie Anwendungen entwickeln, die für Tablet PC-Hardware entwickelt wurden.

Diese Komponenten können zum Erstellen von Anwendungen verwendet werden, die unter Windows XP Tablet PC Edition 2005, Windows Vista, Windows 7, Windows Server 2008 R2 und bestimmten anderen älteren Betriebssystemen ausgeführt werden.

Der Windows Presentation Foundation unterstützt auch die Entwicklung von Tablet PC-Anwendungen.

## <a name="version-history"></a>Versionsverlauf

### <a name="tablet-platform-in-windows-7-and-windows-server-2008-r2"></a>Tablet Platform in Windows 7 und Windows Server 2008 R2

Mit Windows 7 werden zusätzliche Sprachunterstützung, das mathematische Eingabe Steuerelement und benutzerdefinierte Wörterbücher eingeführt. [Windows-Berührungs](../wintouch/windows-touch-portal.md) Features wurden auch Windows-Betriebssystemen hinzugefügt.

Windows Server 2008 R2 bietet Unterstützung für zusätzliche Sprachen, benutzerdefinierte Wörterbücher und Server seitige Erkennung.

Die folgenden Features verbessern die Tablet-Funktionalität und ermöglichen Entwicklern, neue Anwendungen bereitzustellen, die praktische Szenarios für Endbenutzer unterstützen.

-   Das mathematische Eingabe Steuerelement ermöglicht die Eingabe von mathematischen Formeln und Funktionen aus Hand schriftlichem Text in Windows 7.
-   Um die Texterkennung zu verbessern, unterstützen Windows 7 und Windows Server 2008 R2 benutzerdefinierte Wörterbücher, sodass Administratoren die Unterstützung für Word-Listen direkt aktivieren können.
-   Windows Toucheingabe unterstützt Eingaben aus mehreren touchquellen über neue Fenster Meldungen zusätzlich zu einer Gesten Erkennungs-API, die das Schwenken, Zoomen und drehen unterstützt.
-   Windows Server 2008 R2 unterstützt die serverseitige Erkennung von Formular Eingaben und unterstützt auch benutzerdefinierte Wörterbücher für die serverseitige Erkennung. Durch das Hinzufügen dieser Features können Entwickler und Administratoren leistungsstarke Anwendungen erstellen und anpassen, die die Handschrifterkennung von der Serverseite unterstützen.

### <a name="tablet-platform-in-windows-vista"></a>Tablet Platform in Windows Vista

Die Binärdateien der Tablet PC-Technologie wurden in Windows Vista aktualisiert. Die aktualisierte Tablet PC-Technologie umfasst neue frei Hand Analyse-APIs und eine com-Version der Tablettstifteingabe-APIs. Anwendungen, die für frühere Versionen der Tablet PC-Technologie geschrieben wurden, werden ohne Änderungen unter Windows Vista ausgeführt.

Die Tablet PC-Technologiekomponenten sind nur als Teil der Windows SDK verfügbar, beginnend mit der Veröffentlichung von Windows Vista. Weitere Informationen finden Sie unter [What es New in Tablet PC Development](what-s-new-in-tablet-pc-development.md).

### <a name="version-17"></a>Version 1,7

Das Tablet PC Development Kit 1,7 hat die in Version 1,5 verfügbare Entwicklungs Funktionalität erweitert und fügt die Tablettstifteingabe-APIs und die Unterstützung für frei Hand Eingaben im Web hinzu.

In der Vergangenheit war die Funktionalität von Version 1,5 in einer separaten Binärdatei, aber im Tablet PC Development Kit 1,7 wurde die gesamte Funktionalität in einer einzigen Binärdatei platziert.

### <a name="version-15"></a>Version 1.5

Version 1,5 des Development Kits hat Version 1,1 abgelöst. Es wurden Stift Eingabe Panel-APIs und das unter Teiler-Objekt bereitgestellt.

> [!Note]  
> Wenn Sie das Tablet PC Development Kit, Version 1,5, installieren, müssen Sie nach der Installation Verweise auf die Microsoft Ink-Assembly in Anwendungen, die für frühere Versionen des Tablet PC SDK geschrieben wurden, vor dem Kompilieren und ausführen erneut einrichten.

 

### <a name="version-11"></a>Version 1.1

Version 1,1 des Development Kits hat Version 1,0 abgelöst. Die Version 1,1 wurde ausschließlich aus Updates der Dokumentation herausgegeben. die Binärdateien der Plattform wurden zwischen Version 1,1 des Development Kit und der gelieferten Version von Windows XP Tablet PC Edition nicht geändert. Daher müssen Anwendungen, die für das Development Kit der Version 1,1 entwickelt wurden, keine Komponenten neu verteilen, um Platt Form Features zu verwenden, wenn Sie auf Tablet PCs installiert werden.

> [!Note]  
> Anwendungen, die an nicht – Tablet PC-Betriebssysteme verteilt werden, können eine Teilmenge der Features der Tablet PC-Plattform verwenden. Diese Anwendungen müssen das verteilbare Mergemodul enthalten, das im Development Kit der Version 1,1 mit dem Setup ausgeliefert wurde.

 

### <a name="version-10"></a>Version 1.0

Version 1,0 des Development Kit wurde durch Version 1,1 abgelöst.

 

 
