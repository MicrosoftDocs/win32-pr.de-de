---
title: Windows-Remoteverwaltung
description: Windows-Remoteverwaltung (Windows-Remoteverwaltung) ist die Microsoft-Implementierung des WS-Management Protokolls, ein Standardmäßiges SOAP-basiertes, firewallfreundliches Protokoll, das die Interoperabilität von Hardware und Betriebssystemen von unterschiedlichen Anbietern ermöglicht.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Windows-Remoteverwaltung (WinRM), Start Seite
- WS-Verwaltung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27311699fe0321eddc1d3117b17acf3e49e9d518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948772"
---
# <a name="windows-remote-management"></a>Windows-Remoteverwaltung

## <a name="purpose"></a>Zweck

Bei der Windows-Remoteverwaltung (WinRM) handelt es sich um die Microsoft-Implementierung des [WS-Verwaltungsprotokolls](ws-management-protocol.md)– ein standardmäßiges, SOAP-basiertes und firewallfreundliches Protokoll, das die Zusammenarbeit von Hardware und Betriebssystemen unterschiedlicher Anbieter ermöglicht.

Die WS-Management-Protokollspezifikation bietet eine gängige Möglichkeit für Systeme, auf Verwaltungsinformationen in einer IT-Infrastruktur zuzugreifen und diese auszutauschen. WinRM und [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md)zusammen mit dem [Ereignis Sammler](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) sind Komponenten der Windows- [Hardware Verwaltungs](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) Funktionen.

## <a name="where-applicable"></a>Anwendungsbereich

Mit WinRM-Skript Objekten, dem WinRM-Befehlszeilen Tool oder dem Windows-Remoteshell-Befehlszeilen Tool Winrs können Sie Verwaltungsdaten von lokalen Computern und Remote Computern abrufen, die möglicherweise über [*Baseboard-Verwaltungs Controller (Baseboard Management Controllers, BMCs)*](windows-remote-management-glossary.md)verfügen. Wenn auf dem Computer eine Windows-basierte Betriebssystemversion mit WinRM ausgeführt wird, werden die Verwaltungsdaten von [Windows-Verwaltungsinstrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page)bereitgestellt.

Sie können in Ihrem Unternehmen auch Hardware- und Systemdaten aus Implementierungen des WS-Verwaltungsprotokolls abrufen, die nicht unter Windows ausgeführt werden. WinRM richtet eine Sitzung mit einem Remotecomputer über das SOAP-basierte WS-Verwaltungsprotokoll ein, anstatt wie WMI eine Verbindung über DCOM herzustellen. An das WS-Verwaltungsprotokoll zurückgegebene Daten werden nicht als Objekte, sondern als XML-Daten formatiert.

Der WMI-Anbieter für die [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) ist ein standardmäßiger WMI-Anbieter mit Klassen, die BMC-Sensordaten von Computern mit entsprechender Hardware abrufen. Auf IPMI-Daten kann über die WinRM-Skript-API, die WMI- [Skript](/windows/desktop/WmiSdk/scripting-api-for-wmi)Erstellung oder über [com](/windows/desktop/WmiSdk/com-api-for-wmi) -APIs zugegriffen werden.

## <a name="developer-audience"></a>Entwicklergruppe

Die Entwicklergruppe ist der IT-Spezialist, der Skripts zum Automatisieren der Verwaltung von Servern oder des ISV-Entwicklers schreibt, der Daten für Verwaltungs Anwendungen erhält.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

WinRM ist Teil des Betriebssystems. Zum Abrufen von Daten von Remote Computern müssen Sie jedoch einen WinRM- [*Listener*](windows-remote-management-glossary.md#l)konfigurieren. Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md). Wenn beim Systemstart ein BMC erkannt wird, wird der IPMI-Anbieter geladen. Andernfalls sind die WinRM-Skript Objekte und das WinRM-Befehlszeilen Tool weiterhin verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dd>

Verknüpfung mit der öffentlichen WS-Management-Protokollspezifikation, WinRM-Architektur, Beziehung zu WMI, Hardware Verwaltung mit IPMI-Anbieter, Konfiguration und Installation.

</dd> <dt>

[Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md)
</dt> <dd>

Beginnen Sie mit der Verwendung der WinRM-Skript-API und der Hardware Verwaltung.

</dd> <dt>

[Windows-Remoteverwaltung Referenz](windows-remote-management-reference.md)
</dt> <dd>

Liste der Skript Schnittstellen, die von Microsoft Web Services for Management (WS-Management)-Automatisierung und Klassendefinitionen der vom IPMI-Anbieter erstellten WMI-Klassen und Klassendefinitionen für die Kommunikation mit dem IPMI-Treiber zum Abrufen von [Baseboard-Verwaltungs Controller (BMC)](windows-remote-management-glossary.md) -Daten definiert werden.

</dd> </dl>

 

 