---
description: Hier wird beschrieben, wie Sie die richtige WMI-Klasse und die richtigen Prozeduren für Skripts und Anwendungen finden, die allgemeine Computer-und Netzwerk Verwaltungsaufgaben ausführen.
ms.assetid: fe15b67c-8ae6-4360-a2ee-1eda292dd05a
ms.tgt_platform: multiple
title: WMI-Tasks für Skripts und Anwendungen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e2a18791f5055a7574b9e130cf10c0cd1246f6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528598"
---
# <a name="wmi-tasks-for-scripts-and-applications"></a>WMI-Tasks für Skripts und Anwendungen

In den folgenden Abschnitten werden verschiedene Computer-und Netzwerk Verwaltungsaufgaben beschrieben und Links zu den WMI-Klassen oder-Klassen bereitgestellt, die zum Ausführen dieser Aufgaben verwendet werden. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md). Weitere Informationen zur Verwendung von WMI finden Sie unter [Weitere Informationen](further-information.md). Weitere Informationen zur Verwendung von WMI finden Sie unter [technet scriptcenter](https://www.microsoft.com/technet/scriptcenter/default.mspx). (Diese Ressourcen sind möglicherweise nicht in allen Sprachen, Ländern oder Regionen verfügbar.)

Weitere Informationen zum Bereitstellen von Daten für WMI finden Sie unter [Verwenden von WMI](using-wmi.md), das auf Themen zum Schreiben eines WMI- [*Anbieters*](gloss-p.md)verweist.

Die in Skript Beispielen gezeigten Vorgänge können von Anwendungen in C++ oder Visual Basic ausgeführt werden. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung mithilfe von C++](creating-a-wmi-application-using-c-.md) und [WMI C++ Anwendungsbeispiele](wmi-c---application-examples.md).

In der folgenden Tabelle sind die Aufgaben Kategorien aufgeführt.



| Aufgabenkategorien                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Konten und Domänen](wmi-tasks--accounts-and-domains.md)                   | Abrufen von Informationen wie der Computer Domäne oder dem aktuell angemeldeten Benutzer. Viele Domänen-oder kontobezogene Aufgaben werden am besten mit [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) -Skripts ausgeführt. Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . |
| [Computerhardware](wmi-tasks--computer-hardware.md)                         | Informieren Sie sich über das vorhanden sein, den Status oder die Eigenschaften von Hardwarekomponenten. Beispielsweise können Sie bestimmen, ob ein Computer ein Desktop oder Laptop ist.                                                                                                                                                                                             |
| [Computer Software](wmi-tasks--computer-software.md)                         | Abrufen von Informationen, wie z. b. welche Software von der Windows Installer (MSI) und den Softwareversionen installiert wird.                                                                                                                                                                                                                                              |
| [Herstellen einer Verbindung mit dem WMI-Dienst](wmi-tasks--connecting-to-the-wmi-service.md) | Um Daten aus WMI auf dem lokalen Computer oder einem Remote Computer zu erhalten, müssen Sie eine Verbindung mit dem WMI-Dienst herstellen, indem Sie eine Verbindung mit einem bestimmten [*Namespace*](gloss-n.md)herstellen. Verwenden Sie in den meisten Fällen entweder die [Kurznamen-monikerverbindung](creating-a-wmi-script.md) oder die [**Locator**](swbemlocator-connectserver.md) -Verbindung.    |
| [Datumsangaben und Uhrzeiten](wmi-tasks--dates-and-times.md)                             | Es gibt WMI-Klassen und ein Skript Objekt, um das CIM- [DateTime](date-and-time-format.md) -Format zu analysieren oder zu konvertieren.                                                                                                                                                                                                                                     |
| [Desktop Verwaltung](wmi-tasks--desktop-management.md)                       | Abrufen von Daten von oder Steuern von Remote Desktops. Beispielsweise können Sie bestimmen, ob für den Bildschirmschoner ein Kennwort erforderlich ist. WMI bietet Ihnen außerdem die Möglichkeit, einen Remote Computer herunterzufahren.                                                                                                                                                               |
| [Datenträger und Dateisysteme](wmi-tasks--disks-and-file-systems.md)               | Abrufen von Informationen über den Hardware Status des Laufwerks, logische Volumes                                                                                                                                                                                                                                                                                      |
| [Ereignisprotokolle](wmi-tasks--event-logs.md)                                       | Abrufen von Ereignisdaten aus NT-Ereignisprotokoll Dateien und Ausführen von Vorgängen wie sichern oder Löschen von Protokolldateien.                                                                                                                                                                                                                                                   |
| [Dateien und Ordner](wmi-tasks--files-and-folders.md)                         | Ändern Sie die Datei-oder Ordnereigenschaften über WMI, einschließlich der Erstellung einer Freigabe oder dem Umbenennen einer Datei.                                                                                                                                                                                                                                                              |
| [Netzwerk](wmi-tasks--networking.md)                                       | Verwalten und Abrufen von Informationen zu Verbindungen und IP-oder Mac-Adressen.                                                                                                                                                                                                                                                                                  |
| [Betriebssysteme](wmi-tasks--operating-systems.md)                         | Abrufen von Informationen über das Betriebssystem, z. b. die Version, ob diese aktiviert ist oder welche Hotfixes installiert sind.                                                                                                                                                                                                                                  |
| [Leistungsüberwachung](wmi-tasks--performance-monitoring.md)               | Verwenden Sie die WMI-Klassen, die Daten aus Leistungsindikatoren abrufen, um auf Daten über die Computerleistung zuzugreifen und diese zu aktualisieren.                                                                                                                                                                                                                                     |
| [Prozesse](wmi-tasks--processes.md)                                         | Abrufen von Informationen wie dem Konto, unter dem ein Prozess ausgeführt wird. Sie können Aktionen wie das Erstellen von Prozessen ausführen.                                                                                                                                                                                                                                 |
| [Drucker und Druck](wmi-tasks--printers-and-printing.md)                 | Verwalten und Abrufen von Daten zu Druckern, z. b. Suchen oder Festlegen des Standard Druckers                                                                                                                                                                                                                                                                    |
| [Registrierung](wmi-tasks--registry.md)                                           | Erstellen und Ändern von Registrierungs Schlüsseln und-Werten.                                                                                                                                                                                                                                                                                                               |
| [Geplante Aufgaben](wmi-tasks--scheduled-tasks.md)                             | Erstellen und erhalten Sie Informationen zu geplanten Tasks.                                                                                                                                                                                                                                                                                                         |
| [Dienste](wmi-tasks--services.md)                                           | Abrufen von Informationen zu Diensten, einschließlich abhängiger oder Vorgänger Dienste                                                                                                                                                                                                                                                                            |



 

 

 
