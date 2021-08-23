---
description: Remotedesktopdienste (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Remotedesktopdienste (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10af070d54dceebe51f9872b3b58c42467040d5ad8f24f593774576b159cbbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645740"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Remotedesktopdienste (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)

## <a name="affected-platforms"></a>Betroffene Plattformen

**Server** – Windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>Beschreibung

Remotedesktopdienste (früher als Terminaldienste bezeichnet) ermöglicht es mehreren gleichzeitigen Benutzern, auf Windows Server zuzugreifen, um Anwendungs- und Datenhostingdienste mithilfe der Microsoft-Technologie "Presentation Virtualization" bereitzustellen.

Während die meisten 32-Bit- und 64-Bit-Anwendungen auf Windows Remotedesktopdienste ausgeführt werden, werden einige andere aufgrund der Unterschiede in der Plattform (Umgebung mit mehreren Benutzern, gleichzeitiger Zugriff durch mehrere Benutzer usw.) nicht wie erwartet ausgeführt.

Weitere Informationen zur Anwendungsqualität finden Sie im Whitepaper *Anwendungsbereitschaft für Terminaldienste.* Besuchen Sie die Produktseite Remotedesktopdienste, und auf den TS TechNet-Websites erfahren Sie mehr über Remotedesktopdienste. Weitere Informationen zum Entwickeln von Anwendungen für Remotedesktopdienste finden Sie in den Programmierrichtlinien für *Terminaldienste.* (Diese Ressourcen sind in einigen Sprachen und Ländern/Regionen möglicherweise nicht verfügbar.)

## <a name="manifestation-of-impacts-and-their-mitigations"></a>Auswirkungen und ihre Entschärfungen

Drei Änderungen in Windows 7 wirken sich auf Anwendungen auf Remotedesktopdienste aus:

-   Windows Server 2008 R2 ist nur 64-Bit
-   IP-Virtualisierung pro Sitzung
-   MSI-basierte Bereitstellungen : Benutzerspezifische Schlüssel

**Nur 64-Bit-Windows Server 2008 R2**

Anwendungen, die für einen 32-Bit-Server geschrieben wurden, werden im WoW-Modus und nicht nativ auf dem Windows Server 2008 R2 oder somit auf Remotedesktopdienste ausgeführt. Weitere Informationen finden Sie im Thema Windows 7 64-Bit Only.

*Entschärfungen nur für 64-Bit-Windows Server 2008 R2*

Die meisten Anwendungen, die für 32-Bit geschrieben wurden, funktionieren im WoW-Modus weiterhin wie gewohnt. Alle neuen Anwendungen, die für Windows 7 Remotedesktopdienste geschrieben wurden, sollten für die Bereitstellung auf 64-Bit-Plattformen entwickelt und getestet werden.

**IP-Virtualisierung**

Remotedesktop-IP-Virtualisierung ermöglicht es dem Benutzer, Remotedesktopverbindungen pro Sitzung oder pro Programm IP-Adressen zuzuweisen:

-   Wenn Sie IP-Adressen pro Sitzung zuweisen, verwenden alle Anwendungen die Sitzungs-IP-Adresse.
-   Wenn Sie ip-Adressen pro Programm zuweisen, verwenden nur die angegebenen Anwendungen die Sitzungs-IP-Adresse, und die verbleibenden Anwendungen in der Sitzung sind nicht betroffen.
-   Wenn Sie IP-Adressen für mehrere Programme zuweisen, wird eine Sitzungs-IP-Adresse gemeinsam verwendet.
-   Wenn auf dem Computer mehrere Netzwerkadapter installiert sind, müssen Sie auch einen netzwerkadapter für Remotedesktop-IP-Virtualisierung auswählen.

*Entschärfungen für die IP-Virtualisierung*

Einige Programme erfordern eine eindeutige IP-Adresse für jede Instanz der Anwendung. Vor Windows Server 2008 R2 hat jede Sitzung auf einem Remotedesktopserver dieselbe IP-Adresse freigegeben, was zu Kompatibilitätsproblemen für diese Anwendungen führt. Remotedesktop-IP-Virtualisierung ermöglicht die Ausführung dieser Anwendungen auf einem Remotedesktop Server.

**MSI-basierte Bereitstellungen**

Die RDS-Kompatibilität von Microsoft Installer ist ein neues Feature, das in Remotedesktopdienste in Windows Server 2008 R2 enthalten ist. Mit Remotedesktopdienste in Windows Server 2008 R2 werden Anwendungsinstallationen pro Benutzer vom Remotedesktop Server in die Warteschlange eingereiht und dann vom Microsoft Installer verarbeitet.

In Windows Server 2008 R2 können Sie ein Programm auf dem Remotedesktop Server genauso installieren wie auf einem lokalen Desktop. Stellen Sie jedoch sicher, dass Sie das Programm für alle Benutzer installieren und alle Komponenten des Programms lokal auf dem Remotedesktop Server installieren.

*Entschärfungen für MSI-basierte Bereitstellungen*

Vor der Windows Server 2008 R2-Version von Remotedesktopdienste unterstützte Windows jeweils nur eine installation Windows Installers. Für Anwendungen, die benutzerspezifische Konfigurationen erforderten, z. B. Microsoft Office Word, musste ein Administrator die Anwendung vorab installieren, und Anwendungsentwickler mussten diese Anwendungen sowohl auf dem Remotedesktopclient als auch auf dem Remotedesktop-Sitzungshost testen. Windows Das RdS-Kompatibilitätsfeature des Installationsprogramms ermöglicht das gleichzeitige Identifizieren und Installieren fehlender Konfigurationen pro Benutzer für mehrere Benutzer und macht die Anwendungsinstallation auf Remotedesktop Server ähnlich wie auf einem lokalen Desktop.

**Windows Server 2008 R2 mit aktivierter [Remotedesktopdienste-Rolle:](../termserv/terminal-services-portal.md)** Wird nicht unterstützt. Bei einer Installation mehrerer Pakete mithilfe der [MsiEmbeddedChainer-Tabelle](../msi/msiembeddedchainer-table.md) tritt ein Fehler auf, wenn die [Remotedesktopdienste-Rolle](../termserv/terminal-services-portal.md) aktiviert ist.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Programmierrichtlinien für Terminaldienste](../termserv/terminal-services-programming-guidelines.md)
-   [Startseite des Terminaldienste-Produkts](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [Whitepaper zur Anwendungsbereitschaft für Terminaldienste](/collaborate/connect-redirect)

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern/Regionen möglicherweise nicht verfügbar.

 

 

 
