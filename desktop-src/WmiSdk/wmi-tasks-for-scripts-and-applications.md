---
description: Beschreibt, wie sie die richtige WMI-Klasse und -Prozeduren finden, die in Skripts und Anwendungen verwendet werden, die allgemeine Computer- und Netzwerkverwaltungsaufgaben ausführen.
ms.assetid: fe15b67c-8ae6-4360-a2ee-1eda292dd05a
ms.tgt_platform: multiple
title: WMI-Aufgaben für Skripts und Anwendungen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d273db41b832b8141fe13bdf0538b51fb221688949792e214c9f81c1e7b96e69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553124"
---
# <a name="wmi-tasks-for-scripts-and-applications"></a>WMI-Aufgaben für Skripts und Anwendungen

In den folgenden Abschnitten werden verschiedene Computer- und Netzwerkverwaltungsaufgaben beschrieben und Links zu den WMI-Klassen zur Ausführung dieser Aufgaben enthalten. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder Skript.](creating-a-wmi-application-or-script.md) Weitere Informationen zur Verwendung von WMI finden Sie unter [Weitere Informationen.](further-information.md) Weitere Informationen zur Verwendung von WMI finden Sie unter [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx). (Diese Ressourcen sind möglicherweise nicht in jeder Sprache oder in jedem Land/jeder Region verfügbar.)

Weitere Informationen zum Bereitstellen von Daten für WMI finden Sie unter Verwenden von [WMI,](using-wmi.md)das auf Themen zum Schreiben eines WMI-Anbieters [*verweist.*](gloss-p.md)

Die in Skriptbeispielen gezeigten Vorgänge können von Anwendungen in C++ oder Visual Basic. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung mit C++](creating-a-wmi-application-using-c-.md) und [WMI C++-Anwendungsbeispiele.](wmi-c---application-examples.md)

In der folgenden Tabelle sind die Kategorien von Aufgaben aufgeführt.



| Aufgabenkategorien                                                               | Beschreibung                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Konten und Domänen](wmi-tasks--accounts-and-domains.md)                   | Abrufen von Informationen wie der Computerdomäne oder dem derzeit angemeldeten Benutzer. Viele domänen- oder kontobezogene Aufgaben werden am besten mit [ADSI-Skripts](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) ausgeführt. Beispiele finden Sie im TechNet ScriptCenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . |
| [Computerhardware](wmi-tasks--computer-hardware.md)                         | Abrufen von Informationen über das Vorhandensein, den Zustand oder die Eigenschaften von Hardwarekomponenten. Beispielsweise können Sie bestimmen, ob es sich bei einem Computer um einen Desktop oder Laptop handelt.                                                                                                                                                                                             |
| [Computersoftware](wmi-tasks--computer-software.md)                         | Abrufen von Informationen, z. B. welche Software vom Windows Installer (MSI) und Softwareversionen installiert wird.                                                                                                                                                                                                                                              |
| [Herstellen einer Verbindung mit dem WMI-Dienst](wmi-tasks--connecting-to-the-wmi-service.md) | Um Daten aus WMI entweder auf dem lokalen Computer oder von einem Remotecomputer zu erhalten, müssen Sie eine Verbindung mit dem WMI-Dienst herstellen, indem Sie eine Verbindung mit einem bestimmten [*Namespace herstellen.*](gloss-n.md) Verwenden Sie in den meisten Fällen entweder die [Kurzzeitmonikerverbindung](creating-a-wmi-script.md) oder die [**Locator-Verbindung.**](swbemlocator-connectserver.md)    |
| [Datums- und Zeitangaben](wmi-tasks--dates-and-times.md)                             | Es gibt WMI-Klassen und ein Skriptobjekt zum Analysieren oder Konvertieren des [CIM-DateTime-Formats.](date-and-time-format.md)                                                                                                                                                                                                                                     |
| [Desktopverwaltung](wmi-tasks--desktop-management.md)                       | Abrufen von Daten von Remotedesktops oder Steuern von Remotedesktops Beispielsweise können Sie bestimmen, ob der Bildschirmschoner ein Kennwort erfordert. WMI bietet Ihnen auch die Möglichkeit, einen Remotecomputer herunterfahren.                                                                                                                                                               |
| [Datenträger und Dateisysteme](wmi-tasks--disks-and-file-systems.md)               | Abrufen von Informationen zum Hardwarestatus des Datenträgerlaufwerks und zu logischen Volumes.                                                                                                                                                                                                                                                                                      |
| [Ereignisprotokolle](wmi-tasks--event-logs.md)                                       | Abrufen von Ereignisdaten aus NT-Ereignisprotokolldateien und Ausführen von Vorgängen wie dem Sichern oder Löschen von Protokolldateien.                                                                                                                                                                                                                                                   |
| [Dateien und Ordner](wmi-tasks--files-and-folders.md)                         | Ändern der Datei- oder Ordnereigenschaften über WMI, einschließlich erstellen einer Freigabe oder Umbenennen einer Datei.                                                                                                                                                                                                                                                              |
| [Netzwerk](wmi-tasks--networking.md)                                       | Verwalten und Abrufen von Informationen zu Verbindungen und IP- oder MAC-Adressen.                                                                                                                                                                                                                                                                                  |
| [Betriebssysteme](wmi-tasks--operating-systems.md)                         | Abrufen von Informationen zum Betriebssystem, z. B. version, ob es aktiviert ist oder welche Hotfixes installiert sind.                                                                                                                                                                                                                                  |
| [Leistungsüberwachung](wmi-tasks--performance-monitoring.md)               | Verwenden Sie die WMI-Klassen, die Daten aus Leistungsindikatoren abrufen, um auf Daten zur Computerleistung zu zugreifen und diese zu aktualisieren.                                                                                                                                                                                                                                     |
| [Prozesse](wmi-tasks--processes.md)                                         | Abrufen von Informationen wie dem Konto, unter dem ein Prozess ausgeführt wird. Sie können Aktionen wie das Erstellen von Prozessen ausführen.                                                                                                                                                                                                                                 |
| [Drucker und Drucken](wmi-tasks--printers-and-printing.md)                 | Verwalten und Abrufen von Daten zu Druckern, z. B. Suchen oder Festlegen des Standarddruckers.                                                                                                                                                                                                                                                                    |
| [Registrierung](wmi-tasks--registry.md)                                           | Erstellen und Ändern von Registrierungsschlüsseln und -werten.                                                                                                                                                                                                                                                                                                               |
| [Geplante Aufgaben](wmi-tasks--scheduled-tasks.md)                             | Erstellen und Erhalten von Informationen zu geplanten Aufgaben.                                                                                                                                                                                                                                                                                                         |
| [Dienste](wmi-tasks--services.md)                                           | Abrufen von Informationen zu Diensten, einschließlich abhängiger oder vorerkannter Dienste.                                                                                                                                                                                                                                                                            |



 

 

 
