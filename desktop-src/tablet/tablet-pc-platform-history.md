---
description: In diesem Abschnitt wird der Versionsverlauf für die Tablet PC-Technologie beschrieben.
ms.assetid: 69eb161a-2330-456f-b7b8-234cf02c8b58
title: Verlauf der Tablet PC-Plattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78cbcecd8ee02f56a4d89b2ca9d14217da277525dd3548adec7282d6744d1d24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843050"
---
# <a name="tablet-pc-platform-history"></a>Verlauf der Tablet PC-Plattform

In diesem Abschnitt wird der Versionsverlauf für die Tablet PC-Technologie beschrieben.

## <a name="platform-description"></a>Plattformbeschreibung

Mit den Komponenten der Tablet PC-Technologie können Sie Anwendungen entwickeln, die für Tablet PC-Hardware entwickelt wurden.

Diese Komponenten können zum Erstellen von Anwendungen verwendet werden, die unter Windows XP Tablet PC Edition 2005, Windows Vista, Windows 7, Windows Server 2008 R2 und bestimmten anderen früheren Betriebssystemen ausgeführt werden.

Der Windows Presentation Foundation unterstützt auch die Entwicklung von Tablet PC-Anwendungen.

## <a name="version-history"></a>Versionsverlauf

### <a name="tablet-platform-in-windows-7-and-windows-server-2008-r2"></a>Tablet Platform in Windows 7 und Windows Server 2008 R2

Windows 7 führt zusätzliche Sprachunterstützung, das mathematische Eingabesteuerfeld und benutzerdefinierte Wörterbücher ein. [Windows Touch-Features](../wintouch/windows-touch-portal.md) wurden auch zu Windows hinzugefügt.

Windows Server 2008 R2 bietet Unterstützung für zusätzliche Sprachen, benutzerdefinierte Wörterbücher und serverseitige Erkennung.

Die folgenden Features verbessern die Tablet-Funktionalität und ermöglichen Entwicklern die Bereitstellung neuer Anwendungen, die praktische Szenarien für Endbenutzer unterstützen.

-   Das mathematische Eingabesteuerfeld ermöglicht die Eingabe von mathematischen Formeln und Funktionen aus handschriftlichem Text in Windows 7.
-   Um die Texterkennung zu verbessern, unterstützen Windows 7 und Windows Server 2008 R2 benutzerdefinierte Wörterbücher, sodass Administratoren die Unterstützung für Wortlisten direkt aktivieren können.
-   Windows Toucheingaben unterstützen Eingaben aus mehreren Berührungsquellen über neue Fenstermeldungen sowie eine Gestenerkennungs-API, die Schwenken, Zoomen und Drehen unterstützt.
-   Windows Server 2008 R2 unterstützt die serverseitige Erkennung von Formulareingaben sowie benutzerdefinierte Wörterbücher für die serverseitige Erkennung. Durch das Hinzufügen dieser Features können Entwickler und Administratoren leistungsstarke Anwendungen erstellen und anpassen, die die Handschrifterkennung auf Serverseite unterstützen.

### <a name="tablet-platform-in-windows-vista"></a>Tablet Platform in Windows Vista

Die Binärdateien der Tablet PC-Technologie wurden in Windows Vista aktualisiert. Die aktualisierte Tablet PC-Technologie enthält neue APIs für die Ink-Analyse und eine COM-Version der Eingabe-APIs für Tablettstift. Anwendungen, die für frühere Versionen der Tablet PC-Technologie geschrieben wurden, werden Windows Vista ausgeführt.

Die Komponenten der Tablet PC-Technologie sind nur als Teil des Windows SDK ab der Veröffentlichung von Windows Vista verfügbar. Weitere Informationen finden Sie unter [Neues bei der Entwicklung von Tablet-PCs.](what-s-new-in-tablet-pc-development.md)

### <a name="version-17"></a>Version 1.7

Das Tablet PC Development Kit 1.7 erweiterte die Entwicklungsfunktionalität über die in Version 1.5 verfügbare Funktionalität hinaus, indem die Eingabe-APIs für Tablettstifte und die Unterstützung für Freieingaben im Web hinzugefügt wurden.

In der Vergangenheit lag die Funktionalität von Version 1.5 in einer separaten Binärdatei vor, aber im Tablet PC Development Kit 1.7 wurden alle Funktionen in einer einzelnen Binärdatei platziert.

### <a name="version-15"></a>Version 1.5

Version 1.5 des Development Kit ersetzt Version 1.1. Es wurden Stifteingabebereich-APIs und das Divider-Objekt bereitgestellt.

> [!Note]  
> Wenn Sie das Tablet PC Development Kit Version 1.5 installieren, müssen Sie nach der Installation Verweise auf die Microsoft-Ink-Assembly in Anwendungen wiederherstellen, die für frühere Versionen des Tablet PC SDK geschrieben wurden, bevor Sie kompilieren und ausführen.

 

### <a name="version-11"></a>Version 1.1

Version 1.1 des Development Kit ersetzt Version 1.0. Die Version 1.1 bestand ausschließlich aus Updates der Dokumentation. Die Plattformbinärdateien wurden zwischen Version 1.1 des Development Kit und der ausgelieferten Version von Windows XP Tablet PC Edition nicht geändert. Daher müssen Anwendungen, die für version 1.1 Development Kit entwickelt wurden, keine Komponenten neu verteilen, um Plattformfeatures zu verwenden, wenn sie auf Tablet-PCs installiert sind.

> [!Note]  
> Anwendungen, die an Nicht-Tablet PC-Betriebssysteme verteilt werden, können eine Teilmenge der Features der Tablet PC-Plattform verwenden. Diese Anwendungen müssen das neu verteilte Mergemodul, das im Development Kit der Version 1.1 enthalten ist, mit ihrem Setup enthalten.

 

### <a name="version-10"></a>Version 1.0

Version 1.0 des Development Kit wurde durch Version 1.1 ersetzt.

 

 
