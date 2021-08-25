---
title: Informationen Windows Remoteverwaltung
description: Windows Die Remoteverwaltung ist eine Komponente der Windows Hardwareverwaltungsfeatures, die Serverhardware lokal und remote verwalten.
ms.assetid: f58add53-0746-4423-9ab8-02ba05f82fa7
ms.tgt_platform: multiple
keywords:
- Informationen Windows Remoteverwaltung
- Windows Remoteverwaltung, Informationen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a83df38de4af354f826b9bbba59ddab76e1b656c72e1c3dc74301da883f875cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858910"
---
# <a name="about-windows-remote-management"></a>Informationen Windows Remoteverwaltung

Windows Die Remoteverwaltung ist [](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) eine Komponente der Windows Hardwareverwaltungsfeatures, die Serverhardware lokal und remote verwalten. Zu diesen Features gehören ein Dienst, der das [*WS-Management-Protokoll*](windows-remote-management-glossary.md) implementiert, Hardwarediagnose und -steuerung [](winrm-scripting-api.md) über Baseboard-Verwaltungscontroller [*(BMCs)*](windows-remote-management-glossary.md)sowie eine COM-API und Skriptobjekte, mit denen Sie Anwendungen schreiben können, die remote über das WS-Management-Protokoll kommunizieren. Weitere Informationen zur öffentlichen Spezifikation für das WS-Management-Protokoll finden Sie unter Webdienste für die Verwaltung [(WS-Management).](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf)

## <a name="components-of-winrm-and-hardware-management"></a>Komponenten der WinRM- und Hardwareverwaltung

Im Folgenden finden Sie eine Liste der Komponenten und Features, die von WinRM und der Hardwareüberwachung bereitgestellt werden:

-   [WinRM-Skripterstellungs-API](winrm-scripting-api.md)

    Mit dieser Skripterstellungs-API können Sie Daten von Remotecomputern mithilfe von Skripts abrufen, WS-Management Protokollvorgänge ausführen.

-   **Winrm.cmd**

    Dieses Befehlszeilentool für die Systemverwaltung wird in einer Visual Basic Scripting Edition-Datei (Winrm.vbs) implementiert, die mit der WinRM-Skripterstellungs-API geschrieben wurde. Mit diesem Tool kann ein Administrator WinRM konfigurieren und Daten erhalten oder Ressourcen verwalten. Weitere Informationen finden Sie in der Onlinehilfe, die über die Befehlszeile **Winrm** **/? bereitgestellt wird.**

-   **Winrs.exe**

    Mit diesem Befehlszeilentool können Administratoren die meisten Cmd.exe Remotebefehle mithilfe des WS-Management ausführen. Weitere Informationen finden Sie in der Onlinehilfe, die von der Befehlszeile **Winrs** **/? bereitgestellt wird.**

-   Intelligent Platform Management Interface-Treiber (IPMI) und WMI-Anbieter

    Mit der Hardwareverwaltung über den Anbieter und Treiber von [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md) können Sie Remoteserverhardware über BMCs steuern und diagnostizieren, wenn das Betriebssystem nicht ausgeführt oder bereitgestellt wird.

    Weitere Informationen finden Sie unter [IPMI-Anbieter.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)

-   WMI-Dienst

    Der WMI-Dienst wird weiterhin zusammen mit WinRM ausgeführt und stellt über das [*WMI-Plug-In*](windows-remote-management-glossary.md)angeforderte Daten oder Steuerungen zur Verfügung. Sie können weiterhin Daten aus WMI-Standardklassen wie [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process)sowie von IPMI bereitgestellten Daten abrufen. Weitere Informationen zur Konfiguration und Installation, die für WinRM erforderlich sind, finden Sie unter [Einführung in die Hardwareverwaltung.](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10))

-   WS-Management-Protokoll

    WS-Management Protokoll, ein SOAP-basiertes, firewallfreundliches Protokoll, wurde für Systeme entwickelt, um Verwaltungsinformationen zu suchen und austauschen. Das Ziel der WS-Management-Protokollspezifikation besteht in der Bereitstellung von Interoperabilität und Konsistenz für Unternehmenssysteme mit Computern, die auf einer Vielzahl von Betriebssystemen verschiedener Anbieter ausgeführt werden.

    WS-Management-Protokoll basiert auf den folgenden Standardspezifikationen für Webdienste: HTTPS, SOAP über HTTP (WS-I-Profil), SOAP 1.2, WS-Adressierung, WS-Übertragung, WS-Enumeration und WS-Eventing. Weitere Informationen zum aktuellen Entwurf der Spezifikation finden Sie auf der [Indexseite für Verwaltungsspezifikationen.](/previous-versions/dotnet/articles/ms951267(v=msdn.10))

## <a name="working-with-winrm"></a>Arbeiten mit WinRM

Weitere Informationen zum Schreiben von WinRM-Skripts finden Sie unter [Using Windows Remote Management](using-windows-remote-management.md).

Die folgende Tabelle enthält Themen, die Informationen zum WS-Management-Protokoll, WinRM und WMI sowie zum Angeben von Verwaltungsressourcen wie Laufwerken oder Prozessen bereitstellen.



| Thema                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Installation und Konfiguration für Windows Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md) | Der [*WinRM-Listener*](windows-remote-management-glossary.md) erfordert eine Konfiguration auf Client- und Servercomputern.                                                                                                                                                                                                                               |
| [Windows Architektur der Remoteverwaltung](windows-remote-management-architecture.md)                                             | Diagramm, das die Komponenten von WinRM und die Komponenten auf Client- und Servercomputern veranschaulicht.                                                                                                                                                                                                                                                               |
| [WS-Verwaltungsprotokoll](ws-management-protocol.md)                                                                             | Beschreibung des öffentlichen Standardprotokolls WS-Management Remotesenden und Empfangen von Verwaltungsdaten an jedes Computergerät, das das Protokoll implementiert.                                                                                                                                                                                                             |
| [Skripterstellung in Windows Remoteverwaltung](scripting-in-windows-remote-management.md)                                             | Die WinRM-Skripterstellungs-API ähnelt den Aktionen des WS-Management Protokolls. Von Skripts abgerufene Daten werden in XML formatiert, nicht in -Objekten.                                                                                                                                                                                                                                  |
| [Authentifizierung für Remoteverbindungen](authentication-for-remote-connections.md)                                               | WS-Management-Protokoll behält die Sicherheit für die Datenübertragung zwischen Computern bei, indem mehrere Standardmethoden für die Authentifizierung und Nachrichtenverschlüsselung unterstützt werden.                                                                                                                                                                                                                |
| [Windows Remoteverwaltung und WMI](windows-remote-management-and-wmi.md)                                                       | Da WinRM in die Windows [Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page)integriert ist, können Sie WMI-Daten mit Skripts oder Anwendungen abrufen, die die WinRM-Skripterstellungs-API oder das Winrm-Befehlszeilentool [verwenden.](winrm-scripting-api.md)                                                                                                                     |
| [Ressourcen-URIs](resource-uris.md)                                                                                               | Ein [*Ressourcen-URI*](windows-remote-management-glossary.md) ist ein Bezeichner für einen Verwaltungsvorgang oder -wert. Datenträger stellen z. B. einen Ressourcentyp dar.                                                                                                                                                                              |
| [Remotehardwareverwaltung](remote-hardware-management.md)                                                                     | Der [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) stellt Klassen und Daten zur Verfügung, die die Hardwareverwaltungsdomäne des Baseboard-Verwaltungscontrollers (Baseboard Management Controller, BMC), die BMC-Computersysteme in der Domäne und die BMC-Sensoren beschreiben. [](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) Andere Objekte stellen das BMC-Systemereignisprotokoll (SEL) und die Meldungen im Protokoll dar. |
| [Ereignisse](events.md)                                                                                                             | Sie können keine Ereignisse über WinRM-Skripts abrufen, aber Sie können das Befehlszeilentool Wevtutil.exe, um [Ereignissammlerereignisse](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) anzeigen zu können.                                                                                                                                                                                        |



 

 

 