---
title: Informationen zu Windows-Remoteverwaltung
description: Windows-Remoteverwaltung ist eine Komponente der Windows-Hardware Verwaltungsfunktionen, mit denen die Server Hardware lokal und Remote verwaltet wird.
ms.assetid: f58add53-0746-4423-9ab8-02ba05f82fa7
ms.tgt_platform: multiple
keywords:
- Informationen zu Windows-Remoteverwaltung
- Windows-Remoteverwaltung, Informationen zu
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9221676d3a9864e4fc88fc57c5bb6691512c220a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338292"
---
# <a name="about-windows-remote-management"></a>Informationen zu Windows-Remoteverwaltung

Windows-Remoteverwaltung ist eine Komponente der [Windows-Hardware Verwaltungs](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) Funktionen, mit denen die Server Hardware lokal und Remote verwaltet wird. Zu diesen Features gehören ein Dienst, der das [*WS-Verwaltungs*](windows-remote-management-glossary.md) Protokoll, die Hardware Diagnose und-Steuerung über Baseboard-Verwaltungs Controller ([*BMCs*](windows-remote-management-glossary.md)) sowie eine com-API und [Skript Objekte](winrm-scripting-api.md) implementiert, mit denen Sie Anwendungen schreiben können, die Remote über das WS-Management Protokoll kommunizieren. Weitere Informationen zur öffentlichen Spezifikation WS-Management Protokolls finden Sie unter [Web Services for Management (WS – Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).

## <a name="components-of-winrm-and-hardware-management"></a>Komponenten von WinRM und Hardware Verwaltung

Im folgenden finden Sie eine Liste der Komponenten und Features, die von WinRM und der Hardware Überwachung bereitgestellt werden:

-   [WinRM-Skript-API](winrm-scripting-api.md)

    Diese Skript-API ermöglicht das Abrufen von Daten von Remote Computern mithilfe von Skripts, die WS-Management Protokoll Vorgänge ausführen.

-   **WinRM. cmd**

    Dieses Befehlszeilen Tool für die Systemverwaltung ist in einer Visual Basic Scripting Edition Datei (Winrm.vbs) implementiert, die mithilfe der WinRM-Skript-API geschrieben wurde. Dieses Tool ermöglicht es einem Administrator, WinRM zu konfigurieren und Daten zu erhalten oder Ressourcen zu verwalten. Weitere Informationen finden Sie in der Online Hilfe von der Befehlszeile **WinRM** **/?**.

-   **Winrs.exe**

    Mithilfe dieses Befehlszeilen Tools können Administratoren die meisten Cmd.exe Befehle mithilfe des WS-Management Protokolls Remote ausführen. Weitere Informationen finden Sie in der Online Hilfe von der Befehlszeile **Winrs** **/?**.

-   Intelligent Platform Management Interface (IPMI)-Treiber und WMI-Anbieter

    Mithilfe der Hardware Verwaltung über den Anbieter und Treiber der [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md) können Sie Remote Server Hardware über BMCs Steuern und diagnostizieren, wenn das Betriebssystem nicht ausgeführt wird oder bereitgestellt wird.

    Weitere Informationen finden Sie unter der [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

-   WMI-Dienst

    Der WMI-Dienst wird weiterhin nebeneinander mit WinRM ausgeführt und stellt über das [*WMI-Plug-in*](windows-remote-management-glossary.md)angeforderte Daten bereit. Sie können weiterhin Daten aus standardmäßigen WMI-Klassen abrufen, wie z. b. [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process), sowie von IPMI bereitgestellte Daten. Weitere Informationen zur Konfiguration und Installation, die für WinRM erforderlich ist, finden Sie unter Einführung in die [Hardware Verwaltung](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).

-   WS-Management-Protokoll

    WS-Management-Protokoll, ein SOAP-basiertes, firewallfreundliches Protokoll, wurde für Systeme entworfen, um Verwaltungsinformationen zu finden und auszutauschen. Die Spezifikation des WS-Management Protokolls besteht darin, Interoperabilität und Konsistenz für Unternehmenssysteme bereitzustellen, deren Computer auf einer Vielzahl von Betriebssystemen von unterschiedlichen Anbietern ausgeführt werden.

    WS-Management Protokoll basiert auf den folgenden Standardweb Dienst Spezifikationen: https, SOAP über HTTP (WS-I Profile), SOAP 1,2, WS-Adressierung, WS-Transfer, WS-Enumeration und WS-Eventing. Weitere Informationen zum aktuellen Entwurf der Spezifikation finden Sie auf der Seite mit den [Verwaltungs Spezifikationen Index](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

## <a name="working-with-winrm"></a>Arbeiten mit WinRM

Weitere Informationen zum Schreiben von WinRM-Skripts finden [Sie unter Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md).

In der folgenden Tabelle sind Themen aufgeführt, die Informationen über das WS-Management Protokoll, WinRM und WMI bereitstellen, die angeben, wie Verwaltungsressourcen wie Laufwerke oder Prozesse angegeben werden.



| Thema                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md) | Der WinRM- [*Listener*](windows-remote-management-glossary.md) muss sowohl auf Client-als auch auf Server Computern konfiguriert werden.                                                                                                                                                                                                                               |
| [Windows-Remoteverwaltung-Architektur](windows-remote-management-architecture.md)                                             | Das Diagramm veranschaulicht die Komponenten von WinRM und welche Komponenten auf Client-und Server Computern gefunden werden.                                                                                                                                                                                                                                                               |
| [WS-Verwaltungsprotokoll](ws-management-protocol.md)                                                                             | Die Beschreibung des öffentlichen Standard WS-Management Protokolls für das Remote senden und empfangen von Verwaltungsdaten an ein beliebiges Computer Gerät, das das Protokoll implementiert.                                                                                                                                                                                                             |
| [Skripterstellung in Windows-Remoteverwaltung](scripting-in-windows-remote-management.md)                                             | Die WinRM-Skript-API ähnelt den Aktionen des WS-Management Protokolls. Die von Skripts abgerufenen Daten werden in XML und nicht in-Objekten formatiert.                                                                                                                                                                                                                                  |
| [Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md)                                               | WS-Management Protokoll verwaltet die Sicherheit für die Datenübertragung zwischen Computern, indem mehrere Standard Authentifizierungsmethoden und Nachrichten Verschlüsselung unterstützt werden.                                                                                                                                                                                                                |
| [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md)                                                       | Da WinRM in [Windows-Verwaltungsinstrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page)integriert ist, können Sie WMI-Daten mit Skripts oder Anwendungen abrufen, die die [WinRM-Skript-API](winrm-scripting-api.md) oder das WinRM-Befehlszeilen Tool verwenden.                                                                                                                     |
| [Ressourcen-URIs](resource-uris.md)                                                                                               | Ein [*Ressourcen-URI*](windows-remote-management-glossary.md) ist ein Bezeichner für einen Verwaltungsvorgang oder-Wert. Beispielsweise stellen Laufwerke einen Ressourcentyp dar.                                                                                                                                                                              |
| [Remote Hardware Verwaltung](remote-hardware-management.md)                                                                     | Der [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) stellt [Klassen](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) und Daten bereit, mit denen die BMC-Hardware Verwaltungs Domäne (Baseboard Management Controller), die BMC-Computersysteme in der Domäne und die BMC-Sensoren beschrieben werden. Andere Objekte stellen das BMC-System Ereignisprotokoll (SEL) und die Nachrichten im Protokoll dar. |
| [Ereignisse](events.md)                                                                                                             | Ereignisse können nicht über die WinRM-Skripterstellung abgerufen werden, aber Sie können das Befehlszeilen Tool Wevtutil.exe verwenden, um [Ereignis Sammler](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) Ereignisse anzuzeigen.                                                                                                                                                                                        |



 

 

 