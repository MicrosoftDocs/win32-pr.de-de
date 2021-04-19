---
description: .
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Remotedesktopdienste (Windows 7 und Windows Server 2008 R2 Anwendungsqualität Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46bd39785526b11ac2e4c0ede26bbb9971aadc9a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106357178"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Remotedesktopdienste (Windows 7 und Windows Server 2008 R2 Anwendungsqualität Cookbook)

## <a name="affected-platforms"></a>Betroffene Plattformen

**Server** – Windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>BESCHREIBUNG

Remotedesktopdienste (früher als "Terminal Services" bezeichnet) ermöglicht mehreren gleichzeitigen Benutzern den Zugriff auf Windows Server, um Anwendungs-und datenhostingdienste mithilfe von Microsoft "Presentation Virtualization"-Technologie bereitzustellen.

Während die meisten 32-Bit-und 64-Bit-Anwendungen unter Windows Remotedesktopdienste ausgeführt werden, unterscheiden sich einige andere nicht erwartungsgemäß durch den Unterschied in der Plattform (mehr Benutzerumgebung, gleichzeitiger Zugriff durch mehrere Benutzer usw.).

Weitere Informationen zur Anwendungsqualität finden Sie im Whitepaper " *Anwendungs Bereitschaft für Terminal Dienste* ". Besuchen Sie die Produktseite Remotedesktopdienste und die TS TechNet-Websites Weitere Informationen zu Remotedesktopdienste. Weitere Informationen zum Entwickeln von Anwendungen für Remotedesktopdienste finden Sie in den *Programmier Richtlinien für Terminal Dienste*. (Diese Ressourcen sind in einigen Sprachen und Ländern bzw. Regionen möglicherweise nicht verfügbar.)

## <a name="manifestation-of-impacts-and-their-mitigations"></a>Demonstration von Auswirkungen und deren entschärfungen

Drei Änderungen in Windows 7 wirken sich auf Anwendungen auf Remotedesktopdienste aus:

-   Windows Server 2008 R2 ist nur 64 Bit
-   Pro Sitzung-IP-Virtualisierung
-   MSI-basierte bereit Stellungen – benutzerspezifische Schlüssel

**64-Bit nur Windows Server 2008 R2**

Anwendungen, die für den 32-Bit-Server geschrieben wurden, werden im WOW-Modus ausgeführt, nicht nativ auf Windows Server 2008 R2 oder, daher auf Remotedesktopdienste. Ausführliche Informationen finden Sie im Thema nur Windows 7 64-Bit.

*Entschärfungen für nur 64-Bit-Windows Server 2008 R2*

Die meisten Anwendungen, die für 32-Bit geschrieben wurden, funktionieren im WOW-Modus weiterhin wie gewohnt. Alle neuen Anwendungen für Windows 7-Remotedesktopdienste sollten für die Bereitstellung auf 64-Bit-Plattformen entwickelt und getestet werden.

**IP-Virtualisierung**

Remotedesktop-IP-Virtualisierung ermöglicht dem Benutzer das Zuweisen von IP-Adressen zu Remote Desktop Verbindungen pro Sitzung oder pro Programm:

-   Wenn Sie IP-Adressen pro Sitzung zuweisen, verwenden alle Anwendungen die Sitzungs-IP-Adresse.
-   Wenn Sie IP-Adressen pro Programm zuweisen, werden nur die angegebenen Anwendungen die Sitzungs-IP-Adresse verwenden, und die übrigen Anwendungen in der Sitzung werden nicht beeinträchtigt.
-   Wenn Sie IP-Adressen für mehrere Programme zuweisen, wird die IP-Adresse der Sitzung gemeinsam genutzt.
-   Wenn Sie über mehr als einen Netzwerkadapter auf dem Computer verfügen, müssen Sie auch einen davon für Remotedesktop-IP-Virtualisierung auswählen.

*Entschärfungen bei der IP-Virtualisierung*

Einige Programme erfordern eine eindeutige IP-Adresse für jede Instanz der Anwendung. Vor Windows Server 2008 R2 teilte jede Sitzung auf einem Remote Desktop Server die gleiche IP-Adresse, was zu Kompatibilitätsproblemen für diese Anwendungen führte. Remotedesktop-IP-Virtualisierung können diese Anwendungen auf einem Remotedesktop Server ausgeführt werden.

**MSI-basierte bereit Stellungen**

Die Microsoft Installer RDS-Kompatibilität ist ein neues Feature, das in Remotedesktopdienste in Windows Server 2008 R2 enthalten ist. Mit Remotedesktopdienste in Windows Server 2008 R2 werden Anwendungen für anwendungsspezifische Anwendungen vom Remotedesktop Server in die Warteschlange eingereiht und dann vom Microsoft Installer verarbeitet.

In Windows Server 2008 R2 können Sie ein Programm auf dem Remotedesktop Server genau so installieren, wie Sie es auf einem lokalen Desktop installieren. Stellen Sie jedoch sicher, dass Sie das Programm für alle Benutzer installieren und alle Komponenten des Programms lokal auf dem Remotedesktop Server installieren.

*Entschärfungen für MSI-basierte bereit Stellungen*

Vor der Windows Server 2008 R2-Version von Remotedesktopdienste unterstützte Windows jeweils nur eine Windows Installer Installation. Für Anwendungen, die benutzerspezifische Konfigurationen erfordern (z. b. Microsoft Office Word), musste ein Administrator die Anwendung vorab installieren, und Anwendungsentwickler mussten diese Anwendungen sowohl auf dem Remote Desktop Client als auch auf dem Remotedesktop-Sitzungshost testen. Mit Windows Installer RDS-Kompatibilitäts Funktion können fehlende benutzerspezifische Konfigurationen für mehrere Benutzer gleichzeitig identifiziert und installiert werden. so wird die Anwendungs Installation auf Remotedesktop Server ähnlich wie auf einem lokalen Desktop ermöglicht.

**Windows Server 2008 R2 mit aktivierter [Remotedesktopdienste](../termserv/terminal-services-portal.md) Rolle:** Nicht unterstützt. Eine mehrfach Paketinstallation mithilfe der [msiembeddedchainer-Tabelle](../msi/msiembeddedchainer-table.md) schlägt fehl, wenn die [Remotedesktopdienste](../termserv/terminal-services-portal.md) Rolle aktiviert ist.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Programmier Richtlinien für Terminal Dienste](../termserv/terminal-services-programming-guidelines.md)
-   [Startseite für das Terminal Dienste-Produkt](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [Whitepaper zur Anwendungs Bereitschaft für Terminal Dienste](/collaborate/connect-redirect)

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern bzw. Regionen möglicherweise nicht verfügbar.

 

 

 
