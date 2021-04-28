---
description: Remotedesktopdienste (Cookbook zur Anwendungsqualität unter Windows 7 und Windows Server 2008 R2)
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Remotedesktopdienste (Cookbook zur Anwendungsqualität unter Windows 7 und Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725844d49f465c3c79dbc19fd01ec0f18b09759e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116118"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Remotedesktopdienste (Cookbook zur Anwendungsqualität unter Windows 7 und Windows Server 2008 R2)

## <a name="affected-platforms"></a>Betroffene Plattformen

**Server** – Windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>BESCHREIBUNG

Remotedesktopdienste (früher als Terminaldienste bezeichnet) ermöglicht mehreren gleichzeitigen Benutzern den Zugriff auf Windows Server, um Anwendungs- und Datenhostingdienste mithilfe der Microsoft Presentation Virtualization-Technologie zur Verfügung zu stellen.

Während die meisten 32-Bit- und 64-Bit-Anwendungen wie unter Windows Remotedesktopdienste ausgeführt werden, werden einige andere aufgrund des Unterschieds in der Plattform (Umgebung mit mehreren Benutzern, gleichzeitiger Zugriff durch mehrere Benutzer und so weiter) nicht wie erwartet ausgeführt.

Weitere Informationen zur Anwendungsqualität finden Sie im Whitepaper *Anwendungsbereitschaft für Terminaldienste.* Besuchen Sie die Remotedesktopdienste-Produktseite, und auf den TS TechNet-Websites erfahren Sie mehr über Remotedesktopdienste. Weitere Informationen zum Entwickeln von Anwendungen für Remotedesktopdienste finden Sie in den Terminal Services Programming Guidelines (Richtlinien für die *Terminaldiensteprogrammierung).* (Diese Ressourcen sind in einigen Sprachen und Ländern/Regionen möglicherweise nicht verfügbar.)

## <a name="manifestation-of-impacts-and-their-mitigations"></a>Abwehr von Auswirkungen und deren Entschärfungen

Drei Änderungen in Windows 7 wirken sich auf Anwendungen auf Remotedesktopdienste:

-   Windows Server 2008 R2 ist nur 64-Bit
-   IP-Virtualisierung pro Sitzung
-   MSI-basierte Bereitstellungen – benutzerspezifische Schlüssel

**Nur 64-Bit-Version von Windows Server 2008 R2**

Anwendungen, die für 32-Bit-Server geschrieben wurden, werden im WoW-Modus und nicht nativ unter Windows Server 2008 R2 oder daher auf Remotedesktopdienste. Weitere Informationen finden Sie im Thema Nur 64-Bit-Windows 7.

*Risikominderungen nur für 64-Bit-Versionen von Windows Server 2008 R2*

Die meisten Anwendungen, die für 32-Bit geschrieben wurden, funktionieren im WoW-Modus weiterhin wie gewohnt. Alle neuen Anwendungen, die für Windows 7 Remotedesktopdienste geschrieben wurden, sollten für die Bereitstellung auf 64-Bit-Plattformen entwickelt und getestet werden.

**IP-Virtualisierung**

Remotedesktop-IP-Virtualisierung ermöglicht es dem Benutzer, Remotedesktopverbindungen pro Sitzung oder pro Programm IP-Adressen zuzuweisen:

-   Wenn Sie IP-Adressen pro Sitzung zuweisen, verwenden alle Anwendungen die Sitzungs-IP-Adresse.
-   Wenn Sie pro Programm IP-Adressen zuweisen, verwenden nur die angegebenen Anwendungen die Sitzungs-IP-Adresse, und die verbleibenden Anwendungen in der Sitzung sind nicht betroffen.
-   Wenn Sie IP-Adressen für mehrere Programme zuweisen, wird eine Sitzungs-IP-Adresse gemeinsam verwendet.
-   Wenn auf dem Computer mehrere Netzwerkadapter installiert sind, müssen Sie auch einen netzwerkadapter für Remotedesktop-IP-Virtualisierung auswählen.

*Entschärfungen für DIE IP-Virtualisierung*

Einige Programme erfordern eine eindeutige IP-Adresse für jede Instanz der Anwendung. Vor Windows Server 2008 R2 hat jede Sitzung auf einem Remotedesktopserver dieselbe IP-Adresse gemeinsam genutzt, was zu Kompatibilitätsproblemen für diese Anwendungen führt. Remotedesktop-IP-Virtualisierung ermöglicht die Ausführung dieser Anwendungen auf einem Remotedesktop Server.

**MSI-basierte Bereitstellungen**

Die RDS-Kompatibilität von Microsoft Installer ist ein neues Feature, das in Remotedesktopdienste in Windows Server 2008 R2 enthalten ist. Mit Remotedesktopdienste in Windows Server 2008 R2 werden Anwendungsinstallationen pro Benutzer vom Remotedesktop Server in die Warteschlange eingereiht und dann vom Microsoft Installer verarbeitet.

In Windows Server 2008 R2 können Sie ein Programm auf dem Remotedesktop Server genauso installieren wie auf einem lokalen Desktop. Stellen Sie jedoch sicher, dass Sie das Programm für alle Benutzer installieren und alle Komponenten des Programms lokal auf dem Remotedesktop Server installieren.

*Entschärfungen für MSI-basierte Bereitstellungen*

Vor der Windows Server 2008 R2-Version von Remotedesktopdienste unterstützte Windows nur eine installation Windows Installer gleichzeitig. Für Anwendungen, die benutzerspezifische Konfigurationen erforderten, z. B. Microsoft Office Word, musste ein Administrator die Anwendung vorab installieren, und Anwendungsentwickler mussten diese Anwendungen sowohl auf dem Remotedesktopclient als auch auf dem Remotedesktop-Sitzungshost. Windows Installer RDS-Kompatibilitätsfeature ermöglicht es, fehlende Konfigurationen pro Benutzer für mehrere Benutzer gleichzeitig zu identifizieren und zu installieren, und die Anwendungsinstallation auf Remotedesktop Server ähnelt der auf einem lokalen Desktop.

**Windows Server 2008 R2 mit [aktivierter Remotedesktopdienste](../termserv/terminal-services-portal.md) Rolle:** Nicht unterstützt. Eine Installation mehrerer Pakete mithilfe der [MsiEmbeddedChainer-Tabelle](../msi/msiembeddedchainer-table.md) schlägt fehl, wenn [die](../termserv/terminal-services-portal.md) Remotedesktopdienste aktiviert ist.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Programmierrichtlinien für Terminaldienste](../termserv/terminal-services-programming-guidelines.md)
-   [Terminal services product home page (Produkt-Homepage der Terminaldienste)](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [Whitepaper "Anwendungsbereitschaft für Terminaldienste"](/collaborate/connect-redirect)

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern/Regionen möglicherweise nicht verfügbar.

 

 

 
