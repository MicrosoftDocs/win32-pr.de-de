---
title: Windows Architektur der Remoteverwaltung
description: Die Windows-Remoteverwaltungsarchitektur besteht aus Komponenten auf den Client- und Servercomputern.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 889a823c4c67bed29f9ce695d84c893654b541aed76e0c79860e31f24c543662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121594"
---
# <a name="windows-remote-management-architecture"></a>Windows Architektur der Remoteverwaltung

Die Windows-Remoteverwaltungsarchitektur besteht aus Komponenten auf den Client- und Servercomputern. Die folgende Abbildung zeigt die Komponenten auf beiden Computern, die Interaktion der Komponenten mit anderen Komponenten und das Protokoll, das für die Kommunikation zwischen den Computern verwendet wird.

![winrm-Architektur](images/winrm-architecture.png)

## <a name="requesting-client"></a>Anfordern des Clients

Die folgenden WinRM-Komponenten befinden sich auf dem Computer, auf dem das Skript zum Anfordern von Daten ausgeführt wird.

-   WinRM-Anwendung

    Dies ist  das Skript oder Winrm-Befehlszeilentool, das die WinRM-Skripterstellungs-API verwendet, um Aufrufe zum Anfordern von Daten oder zum Ausführen von Methoden auszuführen. Weitere Informationen finden Sie in der [WinRM-Skripterstellungs-API.](winrm-scripting-api.md)

-   WSMAuto.dll

    Die Automatisierungsebene, die Skriptunterstützung bietet.

-   WsmCL.dll

    C-API-Ebene innerhalb des Betriebssystems.

-   HTTP-API

    WinRM erfordert Unterstützung für HTTP- und HTTPS-Transport.

## <a name="responding-server"></a>Antwortserver

Die folgenden WinRM-Komponenten befinden sich auf dem reagierenden Computer.

-   HTTP-API

    WinRM erfordert Unterstützung für HTTP- und HTTPS-Transport.

-   WSMAuto.dll

    Die Automatisierungsebene, die Skriptunterstützung bietet.

-   WsmCL.dll

    C-API-Ebene innerhalb des Betriebssystems.

-   WsmSvc.dll

    [*WinRM-Listenerdienst.*](windows-remote-management-glossary.md)

-   WsmProv.dll

    Anbietersubsystem.

-   WsmRes.dll

    Ressourcendatei

-   WsmWmiPl.dll

    [*WMI-Plug-In*](windows-remote-management-glossary.md). Dadurch können Sie WMI-Daten über WinRM abrufen.

-   IPMI-Treiber (Intelligent Platform Management Interface) und WMI-IPMI-Anbieter

    Diese Komponenten stellen alle Hardwaredaten zur Verfügung, die mithilfe der IPMI-Klassen angefordert werden. Weitere Informationen finden Sie unter [IPMI-Anbieter.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) BMC-Hardware muss vom SMBIOS oder dem gerät erkannt worden sein, das manuell durch Laden des Treibers erstellt wurde. Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows Remoteverwaltung.](installation-and-configuration-for-windows-remote-management.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> </dl>

 

 