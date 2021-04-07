---
title: Windows-Remoteverwaltung-Architektur
description: Die Windows-Remoteverwaltung-Architektur besteht aus Komponenten auf den Client-und Server Computern.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729185"
---
# <a name="windows-remote-management-architecture"></a>Windows-Remoteverwaltung-Architektur

Die Windows-Remoteverwaltung-Architektur besteht aus Komponenten auf den Client-und Server Computern. Die folgende Abbildung zeigt die Komponenten auf beiden Computern, die Interaktion der Komponenten mit anderen Komponenten und das Protokoll, das für die Kommunikation zwischen den Computern verwendet wird.

![WinRM-Architektur](images/winrm-architecture.png)

## <a name="requesting-client"></a>Anfordernder Client

Die folgenden WinRM-Komponenten befinden sich auf dem Computer, auf dem das Skript ausgeführt wird, das Daten anfordert.

-   WinRM-Anwendung

    Dies ist das Skript oder **WinRM** -Befehlszeilen Tool, das die WinRM-Skript-API verwendet, um Aufrufe zum Anfordern von Daten oder zum Ausführen von Methoden auszuführen. Weitere Informationen finden Sie in der [WinRM-Skript-API](winrm-scripting-api.md).

-   WSMAuto.dll

    Die Automatisierungs Schicht, die Skriptunterstützung bereitstellt.

-   WsmCL.dll

    C-API-Ebene innerhalb des Betriebssystems.

-   HTTP-API

    WinRM erfordert Unterstützung für http-und HTTPS-Transport.

## <a name="responding-server"></a>Reaktions Ende Server

Die folgenden WinRM-Komponenten befinden sich auf dem Reaktions enden Computer.

-   HTTP-API

    WinRM erfordert Unterstützung für http-und HTTPS-Transport.

-   WSMAuto.dll

    Die Automatisierungs Schicht, die Skriptunterstützung bereitstellt.

-   WsmCL.dll

    C-API-Ebene innerhalb des Betriebssystems.

-   WsmSvc.dll

    WinRM- [*Listenerdienst*](windows-remote-management-glossary.md) .

-   WsmProv.dll

    Anbieter Subsystem.

-   WsmRes.dll

    Ressourcendatei

-   WsmWmiPl.dll

    [*WMI-Plug-in*](windows-remote-management-glossary.md). Dies ermöglicht Ihnen das Abrufen von WMI-Daten über WinRM.

-   Intelligent Platform Management Interface (IPMI)-Treiber und WMI-IPMI-Anbieter

    Diese Komponenten stellen alle Hardware Daten bereit, die mithilfe der IPMI-Klassen angefordert werden. Weitere Informationen finden Sie unter [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider). BMC-Hardware muss von dem SMBIOS oder vom Gerät, das manuell erstellt wurde, durch Laden des Treibers erkannt werden. Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> </dl>

 

 