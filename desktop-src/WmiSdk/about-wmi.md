---
description: Die Windows-Verwaltungsinstrumentation (Windows Management Instrumentation, WMI) ist die Microsoft-Implementierung von WBEM (Web-Based Enterprise Management). Hierbei handelt es sich um eine Brancheninitiative zum Entwickeln einer Standardtechnologie für den Zugriff auf Verwaltungsinformationen in einer Unternehmensumgebung.
ms.assetid: d745cf25-a139-439d-9ac5-e7720b640516
ms.tgt_platform: multiple
title: Informationen zu WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cf42ead6c3ae1b364ab8f83c83a744afa28734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348418"
---
# <a name="about-wmi"></a>Informationen zu WMI

Die Windows-Verwaltungsinstrumentation (Windows Management Instrumentation, WMI) ist die Microsoft-Implementierung von WBEM (Web-Based Enterprise Management). Hierbei handelt es sich um eine Brancheninitiative zum Entwickeln einer Standardtechnologie für den Zugriff auf Verwaltungsinformationen in einer Unternehmensumgebung. WMI verwendet den Branchenstandard %%amp;quot;Common Information Model (CIM)%%amp;quot; zum Darstellen von Systemen, Anwendungen, Netzwerken, Geräten und anderen verwalteten Komponenten. CIM wird von der verteilten Verwaltungs Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) entwickelt und verwaltet.

> [!Note]  
> Die nächste Generation von WMI, die als Windows-Verwaltungsinfrastruktur (Mi) bezeichnet wird, ist zurzeit verfügbar. Mi ist vollständig kompatibel mit früheren Versionen von WMI und bietet eine Reihe von Features und Vorteilen, mit denen das Entwerfen und entwickeln von Anbietern und Clients einfacher als je zuvor ist. Beispielsweise werden viele neuere Anbieter mit dem Mi-Framework geschrieben, aber Sie können mit WMI-Skripts und-Anwendungen darauf zugreifen. Weitere Informationen zu den Unterschieden zwischen den beiden Technologien finden Sie Untergründe für die [Verwendung von Mi](/previous-versions/windows/desktop/wmi_v2/why-use-mi-) .

 

## <a name="managing-remote-computer-systems-with-wmi"></a>Verwalten von Remote Computer Systemen mit WMI

WMI ermöglicht das Abrufen von Verwaltungsdaten von Remotecomputern. WMI-Remoteverbindungen werden per DCOM hergestellt. Eine Alternative ist die Verwendung von Windows-Remoteverwaltung ([WinRM](/windows/desktop/WinRM/portal)), die WMI-Remote Verwaltungsdaten mithilfe des WS-Management SOAP-basierten Protokolls abruft.

## <a name="programming-with-wmi"></a>Programmieren mit WMI

Verwaltungs Anwendungen oder Skripts können Daten über WMI in einer Vielzahl von Sprachen erhalten. Weitere Informationen finden Sie im Abschnitt Developer Audience unter [Windows-Verwaltungsinstrumentation](wmi-start-page.md).

Vielen Windows-Features sind WMI-Anbieter zugeordnet, wie z. b. der [Startkonfigurationsdaten (BCD)-Anbieter](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) oder der [Speichervolumeanbieter](/previous-versions/windows/desktop/vdswmi/storage-volume-provider). WMI-Anbieter implementieren die von WMI-Klassen Methoden und-Eigenschaften beschriebenen Funktionen zum Verwalten zugehöriger Windows-Features. Weitere Informationen finden Sie unter [WMI-Anbieter](wmi-providers.md) und [WMI-Klassen](wmi-classes.md).

Weitere Informationen zum Schreiben eines Anbieters zur Bereitstellung von Daten aus neuen Hardware oder Anwendungen finden Sie unter [Bereitstellen von Daten für WMI](providing-data-to-wmi.md).

Weitere Informationen zur Implementierung dieser Technologie finden Sie unter Verwenden von [WMI](using-wmi.md).

In der folgenden Tabelle sind die in diesem Abschnitt enthaltenen Themen aufgeführt.



| `Section`                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Neues in WMI](what-s-new-in-wmi.md)                                                             | Neue Features in WMI.                                                                                                                                                                                                                              |
| [Betriebs System Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md) | Einige Komponenten sind nicht mehr verfügbar oder sind als optionale Installation verfügbar.                                                                                                                                                             |
| [WMI-Architektur](wmi-architecture.md)                                                               | Eine Verwaltungs Anwendung kommuniziert mit WMI über eine Vielzahl von Schnittstellen, wie z. b. Visual Basic, C++, ODBC und ActiveX. Alle WMI-Schnittstellen basieren auf dem Component Object Model (com).                                              |
| [Common Information Model](common-information-model.md)                                               | Ein sprachunabhängiges Programmiermodell, das objektorientierte Techniken verwendet, um ein Unternehmen zu beschreiben.                                                                                                                                          |
| [Managed Object Format](managed-object-format--mof-.md)                                               | Ein Format, das es Ihnen ermöglicht, lesbaren Code zu erstellen, der vom Betriebssystem in einen Satz von CIM-Klassen übersetzt werden kann. Mithilfe der neuen Klassen können Sie neue Technologien für ein Unternehmen modellieren und steuern.                                 |
| [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md)                                       | Die Benutzerkontensteuerung (User Account Control, UAC) wirkt sich auf die zurückgegebenen WMI-Daten, den Remote Zugriff und die Ausführung von Skripts aus. Weitere Informationen finden Sie unter [Getting Started with User Account Control on Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista). |
| [Zugriff auf Sicherungs fähige WMI-Objekte](access-to-wmi-securable-objects.md)                                 | WMI verwendet standardmäßige Windows-Sicherheits Objekte und-Prozeduren, um den Zugriff auf Sicherungs fähige Objekte wie WMI-Namespaces, Drucker, Dienste und DCOM-Anwendungen zu steuern und zu schützen.                                                                      |
| [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md)                                     | Daten aus den Systemleistungs Indikatoren sind in WMI-Klassen verfügbar.                                                                                                                                                                            |
| [IPv6-und IPv4-Unterstützung in WMI](ipv6-and-ipv4-support-in-wmi.md)                                       | WMI [-IP-Routen Anbieter](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) und Netzwerk Klassen stellen Daten für IPv4-Adressen bereit. Ab Windows Vista bietet WMI auch eingeschränkte Unterstützung für IPv6-Netzwerkfunktionen.                                       |
| [Datums-und Uhrzeit Format](date-and-time-format.md)                                                       | WMI verwendet die Datums-und Uhrzeit Formate, die von der CIM-Spezifikation für die verteilte Verwaltung definiert werden. Weitere Informationen finden Sie unter [DMTF](https://www.dmtf.org/).                                                          |
| [Skripterstellung für den WMI-Zugriff](scripting-access-to-wmi.md)                                                 | Schreiben Sie WMI-Skripts, um Verwaltungsaufgaben auszuführen.                                                                                                                                                                                                    |
| [WMI-Problembehandlung](wmi-troubleshooting.md)                                                         | Wenn Sie in einer Anwendung oder einem Skript auf lokale WMI-oder Remote Daten zugreifen, erhalten Sie möglicherweise Fehler im Bereich fehlender Klassen für den Zugriff verweigert. Außerdem verfügen Anbieter über Debugoptionen und Fehler Behebungs Klassen.                           |
| [Weitere Informationen](further-information.md)                                                         | Websites, Bücher und Artikel zu WMI.                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> <dt>

[WMI-Referenz](wmi-reference.md)
</dt> </dl>

 

 
