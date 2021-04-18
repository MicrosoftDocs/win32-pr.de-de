---
description: Die Betriebssystem Kategorie gruppiert Klassen, die Objekte im Zusammenhang mit dem Betriebssystem darstellen.
ms.assetid: D0756D8C-A3D3-4C75-96A3-8C7F05300B39
ms.tgt_platform: multiple
title: Betriebssystemklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f47df8a949e3ac07bf2099ea708d496bed87298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344228"
---
# <a name="operating-system-classes"></a>Betriebssystemklassen

Die Betriebssystem Kategorie gruppiert Klassen, die Objekte im Zusammenhang mit dem Betriebssystem darstellen. Sie kennzeichnen die verschiedenen Konfigurationen und Einstellungen, die eine Computerumgebung definieren. Beispiele hierfür sind: Startkonfiguration, Component Object Model (com), Einstellungen für die Desktopumgebung, Treiber, Sicherheitseinstellungen, Benutzereinstellungen und Registrierungs Einstellungen.

Die Betriebs System Kategorie ist in die folgenden Unterkategorien eingeteilt:

-   [COM](#com)
-   [Desktop](#desktop)
-   [Treiber](#drivers)
-   [Ereignisprotokoll](#windows-event-log)
-   [Dateisystem](#file-system)
-   [Auftrags Objekte](#job-objects)
-   [Speicher-und Seiten Dateien](#memory-and-page-files)
-   [Multimedia-Audiodaten oder Visualisierungen](#multimedia-audio-or-visual)
-   [Netzwerk](#networking)
-   [Betriebssystem Ereignisse](#operating-system-events)
-   [Betriebs Systemeinstellungen](#operating-system-settings)
-   [Prozesse](#processes)
-   [Registrierung](#registry)
-   [Scheduler-Aufträge](#scheduler-jobs)
-   [Security](#security)
-   [Dienste](#services)
-   [Freigaben](#shares)
-   [Startmenü](#start-menu)
-   [Storage](#storage)
-   [Benutzer](#users)
-   [Windows-Produktaktivierung](#windows-product-activation)

## <a name="com"></a>COM

Die com-Unterkategorie gruppiert Klassen, die com-und DCOM-Einstellungen, Klassen und Client Anwendungseinstellungen darstellen.



| Klasse                                                                                           | BESCHREIBUNG                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ classicationclasses**](win32-classiccomapplicationclasses.md)               | Association-Klasse<br/> Verknüpft eine DCOM-Anwendung und eine gruppierte COM-Komponente.<br/>                                                                             |
| [**Win32 \_ classiccomclass**](win32-classiccomclass.md)                                         | Instanzklasse<br/> Stellt die Eigenschaften einer COM-Komponente dar.<br/>                                                                                                   |
| [**Win32 \_ classiccomclasssettings**](win32-classiccomclasssettings.md)                         | Association-Klasse<br/> Verknüpft eine COM-Klasse mit den Einstellungen, die zum Konfigurieren von Instanzen der com-Klasse verwendet werden.<br/>                                                           |
| [**Win32 \_ clientapplicationsetting**](win32-clientapplicationsetting.md)                       | Association-Klasse<br/> Verknüpft eine ausführbare Datei und eine DCOM-Anwendung, die die DCOM-Konfigurationsoptionen für die ausführbare Datei enthält.<br/>                           |
| [**Win32- \_ comapplication**](win32-comapplication.md)                                           | Instanzklasse<br/> Stellt eine COM-Anwendung dar.<br/>                                                                                                                   |
| [**Win32- \_ comapplicationclasses**](win32-comapplicationclasses.md)                             | Association-Klasse<br/> Verknüpft eine COM-Komponente und die COM-Anwendung, in der Sie sich befindet.<br/>                                                                            |
| [**Win32- \_ comapplicationsettings**](win32-comapplicationsettings.md)                           | Association-Klasse<br/> Bezieht eine DCOM-Anwendung und Ihre Konfigurationseinstellungen in Beziehung.<br/>                                                                                   |
| [**Win32- \_ ComClass**](win32-comclass.md)                                                       | Instanzklasse<br/> Stellt die Eigenschaften einer COM-Komponente dar.<br/>                                                                                                   |
| [**Win32 \_ comclassautoemulator**](win32-comclassautoemulator.md)                               | Association-Klasse<br/> Bezieht eine COM-Klasse und eine andere com-Klasse, die Sie automatisch emuliert.<br/>                                                                    |
| [**Win32- \_ comclassemulator**](win32-comclassemulator.md)                                       | Association-Klasse<br/> Verknüpft zwei Versionen einer com-Klasse.<br/>                                                                                                         |
| [**Win32- \_ Komponenten Kategorie**](win32-componentcategory.md)                                     | Instanzklasse<br/> Stellt eine Komponenten Kategorie dar.<br/>                                                                                                                |
| [**Win32- \_ comsetting**](win32-comsetting.md)                                                   | Instanzklasse<br/> Stellt die Einstellungen dar, die einer COM-Komponente oder einer COM-Anwendung zugeordnet sind.<br/>                                                                     |
| [**Win32- \_ dcomapplication**](win32-dcomapplication.md)                                         | Instanzklasse<br/> Stellt die Eigenschaften einer DCOM-Anwendung dar.<br/>                                                                                                |
| [**Win32 \_ dcomapplicationaccesszusetting**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationaccessallowedsetting) | Association-Klasse<br/> Bezieht die [**Win32- \_ dcomapplication**](win32-dcomapplication.md) -Instanz und die Benutzer Sicherheits-IDs (SID), die darauf zugreifen können.<br/> |
| [**Win32 \_ dcomapplicationlaunchzuweisung-Setting**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationlaunchallowedsetting) | Association-Klasse<br/> Ordnet die [**Win32- \_ dcomapplication**](win32-dcomapplication.md) -Instanz und die Benutzer-SIDs, die Sie starten können, in Beziehung.<br/>                           |
| [**Win32- \_ dcomapplicationsetting**](win32-dcomapplicationsetting.md)                           | Instanzklasse<br/> Stellt die Einstellungen einer DCOM-Anwendung dar.<br/>                                                                                                  |
| [**Win32 \_ implementedcategory**](win32-implementedcategory.md)                                 | Association-Klasse<br/> Verknüpft eine Komponenten Kategorie und die com-Klasse mithilfe ihrer-Schnittstellen.<br/>                                                                         |



 

## <a name="desktop"></a>Desktop

Die Desktop Unterkategorie gruppiert Klassen, die Objekte darstellen, die eine bestimmte Desktop Konfiguration definieren.



| Klasse                                           | BESCHREIBUNG                                                                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ -Desktop**](win32-desktop.md)         | Instanzklasse<br/> Stellt die allgemeinen Merkmale des Desktops eines Benutzers dar.<br/>                                    |
| [**Win32- \_ Umgebung**](win32-environment.md) | Instanzklasse<br/> Stellt eine Umgebung oder eine System Umgebungs Einstellung auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/> |
| [**Win32- \_ Zeitzone**](win32-timezone.md)       | Instanzklasse<br/> Stellt die Zeitzoneninformationen für ein Computersystem dar, auf dem Windows ausgeführt wird.<br/>                   |
| [**Win32 \_ -userdesktop**](win32-userdesktop.md) | Association-Klasse<br/> Verknüpft ein Benutzerkonto und die spezifischen Desktop Einstellungen.<br/>                   |



 

## <a name="drivers"></a>Treiber

Die Unterkategorie "Treiber" gruppiert Klassen, die virtuelle Gerätetreiber und System Treiber für Basisdienste darstellen.



| Klasse                                             | BESCHREIBUNG                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [**Win32- \_ System Treiber**](win32-systemdriver.md) | Instanzklasse<br/> Stellt den System Treiber für einen Basis Dienst dar.<br/> |



 

## <a name="file-system"></a>Dateisystem

Die Datei System-SubCategory gruppiert Klassen, die die logische Anordnung einer Festplatte darstellen. Dies schließt den Typ des verwendeten Dateisystems, die Verzeichnisstruktur und die Art der Partitionierung des Datenträgers ein.



| Klasse                                                                               | BESCHREIBUNG                                                                                                                                                                          |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ cimlogicaldevicecimdatafile**](win32-cimlogicaldevicecimdatafile.md)     | Association-Klasse<br/> Bezieht logische Geräte und Datendateien, die die vom Gerät verwendeten Treiberdateien angeben.<br/>                                                      |
| [**Win32- \_ Verzeichnis**](win32-directory.md)                                         | Instanzklasse<br/> Stellt einen Verzeichniseintrag auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                              |
| [**Win32- \_ directspecification**](/previous-versions/windows/desktop/msiprov/win32-directoryspecification)               | Instanzklasse<br/> Stellt das Verzeichnis Layout für das Produkt dar.<br/>                                                                                                |
| [**Win32 \_ diskdrive| Diskpartition**](win32-diskdrivetodiskpartition.md)           | Association-Klasse<br/> Verknüpft ein Laufwerks und eine vorhandene Partition.<br/>                                                                                         |
| [**Win32- \_ Diskpartition**](win32-diskpartition.md)                                 | Instanzklasse<br/> Stellt die Funktionen und die Verwaltungskapazität eines partitionierten Bereichs eines physischen Datenträgers auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>              |
| [**Win32 \_ Diskquota**](/previous-versions/windows/desktop/wmipdskq/win32-diskquota)                                    | Association-Klasse<br/> Verfolgt die Speicherplatz Auslastung für NTFS-Dateisystemvolumes.<br/>                                                                                        |
| [**Win32 \_ LogicalDisk**](win32-logicaldisk.md)                                     | Stellt eine Datenquelle dar, die in ein tatsächliches lokales Speichergerät auf einem Computersystem aufgelöst wird, auf dem Windows ausgeführt wird.<br/>                                                            |
| [**Win32 \_ logicaldiskrootdirectory**](win32-logicaldiskrootdirectory.md)           | Association-Klasse<br/> Ordnet einen logischen Datenträger und seine Verzeichnisstruktur in Beziehung.<br/>                                                                                          |
| [**Win32 \_ logicaldisktopartition**](win32-logicaldisktopartition.md)               | Association-Klasse<br/> Verknüpft ein logisches Laufwerk und die Datenträger Partition, auf der es sich befindet.<br/>                                                                           |
| [**Win32 \_ mappedlogicaldisk**](win32-mappedlogicaldisk.md)                         | Stellt Netzwerkspeicher Geräte dar, die auf dem Computersystem unter Windows als logische Datenträger zugeordnet sind.<br/>                                                               |
| [**Win32- \_ operatingsystemautochksetting**](/previous-versions//aa394240(v=vs.85)) | Association-Klasse<br/> Stellt die Zuordnung zwischen einer [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Instanz und den Einstellungen dar, die für diese Instanz definiert sind.<br/> |
| [**Win32 \_ quotaseup**](/previous-versions/windows/desktop/wmipdskq/win32-quotasetting)                              | Instanzklasse<br/> Enthält Einstellungs Informationen für Datenträger Kontingente auf einem Volume.<br/>                                                                                       |
| [**Win32- \_ shortcutfile**](win32-shortcutfile.md)                                   | Instanzklasse<br/> Stellt Dateien dar, bei denen es sich um Verknüpfungen zu anderen Dateien, Verzeichnissen und Befehlen handelt.<br/>                                                                  |
| [**Win32- \_ Unterverzeichnis**](win32-subdirectory.md)                                   | Association-Klasse<br/> Verknüpft ein Verzeichnis (Ordner) und eines seiner Unterverzeichnisse (Unterordner).<br/>                                                                     |
| [**Win32- \_ Systempartitionen**](win32-systempartitions.md)                           | Association-Klasse<br/> Bezieht ein Computersystem und eine Datenträger Partition auf diesem System.<br/>                                                                               |
| [**Win32- \_ Volume**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                               | Instanzklasse<br/> Stellt einen Speicherbereich auf einer Festplatte dar.<br/>                                                                                                   |
| [**Win32- \_ volumequota**](/previous-versions/windows/desktop/vdswmi/win32-volumequota)                                     | Association-Klasse<br/> Verknüpft ein Volume mit den Kontingent Einstellungen pro Volume.<br/>                                                                                           |
| [**Win32 \_ volumequotasetts**](/previous-versions/windows/desktop/wmipdskq/win32-volumequotasetting)                  | Association-Klasse<br/> Bezieht Einstellungen für Datenträger Kontingente mit einem bestimmten Datenträger Volume.<br/>                                                                                     |
| [**Win32- \_ volumeuserquota**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                             | Association-Klasse<br/> Bezieht sich auf Benutzerkontingente mit Kontingent aktivierten Volumes.<br/>                                                                                            |



 

## <a name="job-objects"></a>Auftrags Objekte

Die Auftrags Objekte Unterkategorie gruppiert Klassen, die Klassen darstellen, die die Mittel zum Instrumentieren von benannten Auftrags Objekten bereitstellen. Ein unbenanntes Auftrags Objekt kann nicht instrumentiert werden.



| Klasse                                                                               | BESCHREIBUNG                                                                                                                                                                                |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ collectionstatistics**](/previous-versions/windows/desktop/cimwin32a/win32-collectionstatistics)                   | Association-Klasse<br/> Verknüpft eine verwaltete System Element Auflistung und die-Klasse, die statistische Informationen über die-Auflistung darstellt.<br/>                               |
| [**Win32- \_ LUID**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luid)                                                   | Instanzklasse<br/> Stellt einen lokal eindeutigen Bezeichner (LUID) dar.<br/>                                                                                                         |
| [**Win32- \_ luidandattribute**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luidandattributes)                         | Instanzklasse<br/> Stellt eine LUID und deren Attribute dar.<br/>                                                                                                                 |
| [**Win32- \_ namedjobobject**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobject)                               | Instanzklasse<br/> Stellt ein Kernel Objekt dar, das zum Gruppieren von Prozessen verwendet wird, um die Lebensdauer und Ressourcen der Prozesse innerhalb des Auftrags Objekts zu steuern.<br/> |
| [**Win32- \_ namedjobobjectactginfo**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectactginfo)               | Instanzklasse<br/> Stellt die e/a-Buchhaltungsinformationen für ein Auftrags Objekt dar.<br/>                                                                                           |
| [**Win32 \_ namedjobobjectlimit**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimit)                     | Instanzklasse<br/> Stellt eine Zuordnung zwischen einem Auftrags Objekt und den Grenz Einstellungen für das Auftrags Objekt dar.<br/>                                                                     |
| [**Win32 \_ namedjobobjectlimitsetting**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimitsetting)       | Instanzklasse<br/> Stellt die Limit-Einstellungen für ein Auftrags Objekt dar.<br/>                                                                                                       |
| [**Win32 \_ namedjobobjectprocess**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectprocess)                 | Instanzklasse<br/> Verknüpft ein Auftrags Objekt und den Prozess, der im Auftrags Objekt enthalten ist.<br/>                                                                                     |
| [**Win32 \_ namedjobobjectserver climit**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimit)               | Instanzklasse<br/> Verknüpft ein Auftrags Objekt und die Sicherheits Limit-Einstellungen für das Auftrags Objekt.<br/>                                                                                      |
| [**Win32 \_ namedjobobjectabclimitsetting**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimitsetting) | Instanzklasse<br/> Stellt die Sicherheitseinstellungen für ein Auftrags Objekt dar.<br/>                                                                                              |
| [**Win32 \_ namedjobobjectstatistics**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectstatistics)           | Instanzklasse<br/> Stellt eine Zuordnung zwischen einem Auftrags Objekt und der e/a-Buchhaltungs Informations Klasse des Auftrags Objekts dar.<br/>                                                   |
| [**Win32- \_ sidandattribute**](/previous-versions/windows/desktop/wmipjobobjprov/win32-sidandattributes)                           | Instanzklasse<br/> Stellt eine Sicherheits-ID (SID) und ihre Attribute dar.<br/>                                                                                            |
| [**Win32- \_ Gruppen Gruppen**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokengroups)                                     | Ereignisklasse<br/> Stellt Informationen über die Gruppen-SIDs in einem Zugriffs Token dar.<br/>                                                                                          |
| [**Win32- \_ Tokenberechtigungen**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokenprivileges)                             | Ereignisklasse<br/> Stellt Informationen über einen Berechtigungs Satz für ein Zugriffs Token dar.<br/>                                                                                    |



 

## <a name="memory-and-page-files"></a>Speicher-und Seiten Dateien

Die Unterkategorie Speicher und Seiten Dateien gruppiert Klassen, die die Konfigurationseinstellungen für die Auslagerungs Datei darstellen.



| Klasse                                                                 | BESCHREIBUNG                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ Pagefile**](win32-pagefile.md)                             | Instanzklasse<br/> Stellt die Datei dar, die zum Verarbeiten des Austauschs virtueller Speicherdateien in einem Windows-System verwendet wird.<br/>                  |
| [**Win32 \_ pagefileelementsetting**](win32-pagefileelementsetting.md) | Association-Klasse<br/> Verknüpft die anfänglichen Einstellungen einer Auslagerungs Datei und den Zustand dieser Einstellungen während der normalen Verwendung.<br/>        |
| [**Win32- \_ pagefilesetting**](win32-pagefilesetting.md)               | Instanzklasse<br/> Stellt die Einstellungen einer Auslagerungs Datei dar.<br/>                                                                  |
| [**Win32 \_ Page File Usage**](win32-pagefileusage.md)                   | Instanzklasse<br/> Stellt die Datei dar, mit der das austauschen virtueller Speicher auf einem Computersystem mit Windows ausgeführt wird.<br/> |



 

## <a name="multimedia-audio-or-visual"></a>Multimedia-Audiodaten oder Visualisierungen

Die-Klasse in der Multimedia-oder Visual SubCategory stellt die Eigenschaften des auf dem Computersystem installierten Audiostreams oder Videocodecs dar.



| Klasse                                       | BESCHREIBUNG                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ codecfile**](win32-codecfile.md) | Instanzklasse<br/> Stellt den auf dem Computersystem installierten Audiostream oder Videocodec dar.<br/> |



 

## <a name="networking"></a>Netzwerk

Die Netzwerk SubCategory gruppiert Klassen, die Netzwerkverbindungen, Netzwerk Clients und Netzwerk Verbindungseinstellungen darstellen, wie z. b. das verwendete Protokoll.



| Klasse                                                                            | BESCHREIBUNG                                                                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ activeroute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)                       | Association-Klasse<br/> Verknüpft die aktuelle IP4 Route mit der beibehaltenen IP-Routing Tabelle.<br/>                           |
| [**Win32- \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable) | Instanzklasse<br/> Stellt persistente IP-Routen dar.<br/>                                                             |
| [**Win32- \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)                   | Instanzklasse<br/> Stellt Informationen dar, die das Routing von Netzwerkdaten Paketen steuern.<br/>                    |
| [**Win32- \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)         | Ereignisklasse<br/> Stellt IP-Routen Änderungs Ereignisse dar.<br/>                                                             |
| [**Win32- \_ networkclient**](win32-networkclient.md)                              | Instanzklasse<br/> Stellt einen Netzwerkclient auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                           |
| [**Win32- \_ NetworkConnection**](win32-networkconnection.md)                      | Instanzklasse<br/> Stellt eine aktive Netzwerkverbindung in einer Windows-Umgebung dar.<br/>                           |
| [**Win32- \_ networkprotocol**](win32-networkprotocol.md)                          | Instanzklasse<br/> Stellt ein Protokoll und seine Netzwerk Eigenschaften auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/> |
| [**Win32- \_ NTDomäne**](/previous-versions/windows/desktop/cimwin32a/win32-ntdomain)                                        | Instanzklasse<br/> Stellt eine Windows NT-Domäne dar.<br/>                                                             |
| [**Win32 \_ Pingstatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)                               | Instanzklasse<br/> Stellt die Werte dar, die vom **Standardpingbefehl** zurückgegeben werden.<br/>                            |
| [**Win32- \_ protocolbinding**](win32-protocolbinding.md)                          | Association-Klasse<br/> Verknüpft einen Treiber, ein Netzwerkprotokoll und einen Netzwerkadapter auf Systemebene.<br/>                    |



 

## <a name="operating-system-events"></a>Betriebssystemereignisse

Die Unterkategorie Betriebssystem Ereignisse gruppiert Klassen, die Ereignisse im Betriebssystem darstellen, die sich auf Prozesse, Threads und das Herunterfahren des Systems beziehen.



| Klasse                                                                                 | BESCHREIBUNG                                                                                                                                                              |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ computershutdownetzvent**](/previous-versions/windows/desktop/cimwin32a/win32-computershutdownevent)                   | Ereignisklasse<br/> Stellt das Herunterfahren von Computern dar.<br/>                                                                                                   |
| [**Win32 \_ computersystemevent**](/previous-versions/windows/desktop/cimwin32a/win32-computersystemevent)                       | Ereignisklasse<br/> Stellt Ereignisse im Zusammenhang mit einem Computersystem dar.<br/>                                                                                        |
| [**Win32 \_ devicechangeevent**](win32-devicechangeevent.md)                           | Ereignisklasse<br/> Stellt Geräte Änderungs Ereignisse dar, die sich aus dem Hinzufügen, entfernen oder Ändern von Geräten im Computersystem ergeben.<br/>               |
| [**Win32 \_ ModuleLoadTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduleloadtrace)                               | Ereignisklasse<br/> Gibt an, dass ein Prozess ein neues Modul geladen hat.<br/>                                                                                      |
| [**Win32- \_ ModuleTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduletrace)                                       | Ereignisklasse<br/> Basisereignis für Modul Ereignisse.<br/>                                                                                                          |
| [**Win32- \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace)                           | Ereignisklasse<br/> Gibt an, dass ein neuer Prozess gestartet wurde.<br/>                                                                                              |
| [**Win32- \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace)                             | Ereignisklasse<br/> Gibt an, dass ein Prozess beendet wurde.<br/>                                                                                               |
| [**Win32- \_ processtrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace)                                     | Ereignisklasse<br/> Basisereignis für Prozess Ereignisse.<br/>                                                                                                         |
| [**Win32 \_ systemconfigurationchangeevent**](win32-systemconfigurationchangeevent.md) | Ereignisklasse<br/> Gibt an, dass die Geräteliste im System aktualisiert wurde (ein Gerät wurde hinzugefügt oder entfernt, oder die Konfiguration wurde geändert).<br/>    |
| [**Win32- \_ systemtrace**](/previous-versions/windows/desktop/krnlprov/win32-systemtrace)                                       | Ereignisklasse<br/> Basisklasse für alle System Ablauf Verfolgungs Ereignisse, einschließlich Modul-, Prozess-und Thread Ablauf Verfolgungen.<br/>                                                  |
| [**Win32 \_ threadstarttrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstarttrace)                             | Ereignisklasse<br/> Gibt an, dass ein neuer Thread gestartet wurde.<br/>                                                                                                    |
| [**Win32 \_ ThreadStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstoptrace)                               | Ereignisklasse<br/> Gibt an, dass ein Thread beendet wurde.<br/>                                                                                                   |
| [**Win32- \_ ThreadTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadtrace)                                       | Ereignisklasse<br/> Basisereignis Klasse für Thread Ereignisse.<br/>                                                                                                    |
| [**Win32 \_ volumechangeevent**](win32-volumechangeevent.md)                           | Ereignisklasse<br/> Stellt ein Netzwerk Abbild eines Laufwerks dar, das sich aus dem Hinzufügen eines Netzwerklaufwerk Buchstabens oder eines eingebundenen Laufwerks auf dem Computersystem ergibt.<br/> |



 

## <a name="operating-system-settings"></a>Betriebssystemeinstellungen

Die Unterkategorie Betriebssystem Einstellungen gruppiert Klassen, die das Betriebssystem und seine Einstellungen darstellen.



| Klasse                                                                                       | BESCHREIBUNG                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ bootconfiguration**](win32-bootconfiguration.md)                                 | Instanzklasse<br/> Stellt die Startkonfiguration eines Computer Systems dar, auf dem Windows ausgeführt wird.<br/>                                                                       |
| [**Win32- \_ Computersystem**](win32-computersystem.md)                                       | Instanzklasse<br/> Stellt ein Computersystem dar, das in einer Windows-Umgebung ausgeführt wird.<br/>                                                                              |
| [**Win32 \_ computersystemprocessor**](win32-computersystemprocessor.md)                     | Association-Klasse<br/> Verknüpft ein Computersystem und einen Prozessor, der auf dem System ausgeführt wird.<br/>                                                                          |
| [**Win32 \_ computersystemproduct**](win32-computersystemproduct.md)                         | Instanzklasse<br/> Stellt ein Produkt dar.<br/>                                                                                                                         |
| [**Win32 \_ dependentservice**](win32-dependentservice.md)                                   | Association-Klasse<br/> Bezieht zwei voneinander abhängige Basisdienste in Beziehung.<br/>                                                                                                  |
| [**Win32- \_ LoadOrderGroup**](win32-loadordergroup.md)                                       | Instanzklasse<br/> Stellt eine Gruppe von System Diensten dar, die Ausführungs Abhängigkeiten definieren.<br/>                                                                     |
| [**Win32 \_ loadordergroupserviceabhängigkeiten**](win32-loadordergroupservicedependencies.md) | Instanzklasse<br/> Stellt eine Zuordnung zwischen einem Basis Dienst und einer Gruppe der Lade Reihenfolge dar, von der der Dienst zum Starten der Ausführung abhängig ist.<br/>                         |
| [**Win32 \_ loadordergroupservicemembers**](win32-loadordergroupservicemembers.md)           | Association-Klasse<br/> Bezieht eine Gruppe der Lade Reihenfolge und einen Basis Dienst.<br/>                                                                                             |
| [**Win32- \_ OperatingSystem**](win32-operatingsystem.md)                                     | Instanzklasse<br/> Stellt ein Betriebssystem dar, das auf einem Computersystem mit Windows installiert ist.<br/>                                                                |
| [**Win32- \_ operatingsystemqfe**](win32-operatingsystemqfe.md)                               | Association-Klasse<br/> Verknüpft ein Betriebssystem und Produktupdates, die in der [**Win32- \_ quickfixengineering**](win32-quickfixengineering.md)-Version angewendet wurden.<br/> |
| [**Win32 \_ osherstellyconfiguration**](win32-osrecoveryconfiguration.md)                     | Instanzklasse<br/> Stellt die Arten von Informationen dar, die beim Ausfall des Betriebssystems aus dem Arbeitsspeicher gesammelt werden.<br/>                                        |
| [**Win32- \_ quickfixengineering**](win32-quickfixengineering.md)                             | Instanzklasse<br/> Stellt systemweite Quick Fix Engineering (QFE) oder Updates dar, die auf das aktuelle Betriebssystem angewendet wurden.<br/>                         |
| [**Win32- \_ startupcommand**](win32-startupcommand.md)                                       | Instanzklasse<br/> Stellt einen Befehl dar, der automatisch ausgeführt wird, wenn sich ein Benutzer auf dem Computersystem anmeldet.<br/>                                                       |
| [**Win32 \_ systembootconfiguration**](win32-systembootconfiguration.md)                     | Association-Klasse<br/> Bezieht ein Computersystem und dessen Startkonfiguration in Beziehung.<br/>                                                                                      |
| [**Win32 \_ -System Desktop**](win32-systemdesktop.md)                                         | Association-Klasse<br/> Bezieht ein Computersystem und dessen Desktop Konfiguration in Beziehung.<br/>                                                                                   |
| [**Win32- \_ Systemgeräte**](win32-systemdevices.md)                                         | Association-Klasse<br/> Verknüpft ein Computersystem und ein logisches Gerät, das auf diesem System installiert ist.<br/>                                                                   |
| [**Win32- \_ systemloadordergroups**](win32-systemloadordergroups.md)                         | Association-Klasse<br/> Bezieht sich auf ein Computersystem und eine Gruppe der Lade Reihenfolge.<br/>                                                                                          |
| [**Win32- \_ systemnetworkconnections**](win32-systemnetworkconnections.md)                   | Association-Klasse<br/> Bezieht eine Netzwerkverbindung und das Computersystem, auf dem es sich befindet, in Beziehung.<br/>                                                                  |
| [**Win32 \_ systemoperatingsystem**](win32-systemoperatingsystem.md)                         | Association-Klasse<br/> Bezieht sich auf ein Computersystem und dessen Betriebssystem.<br/>                                                                                        |
| [**Win32- \_ System Prozesse**](win32-systemprocesses.md)                                     | Association-Klasse <br/> Beziehung zwischen einem Computersystem und einem Prozess, der auf dem System ausgeführt wird.<br/>                                                                           |
| [**Win32- \_ System programmgroups**](win32-systemprogramgroups.md)                             | Association-Klasse<br/> Bezieht ein Computersystem und eine logische Programmgruppe in Beziehung.<br/>                                                                                     |
| [**Win32- \_ systemresources**](win32-systemresources.md)                                     | Association-Klasse<br/> Bezieht sich auf eine System Ressource und das Computersystem, auf dem Sie sich befindet.<br/>                                                                           |
| [**Win32- \_ Systemdienste**](win32-systemservices.md)                                       | Association-Klasse<br/> Verknüpft ein Computersystem und ein Dienstprogramm, das im System vorhanden ist.<br/>                                                                 |
| [**Win32- \_ systemsetting**](win32-systemsetting.md)                                         | Association-Klasse<br/> Bezieht sich auf ein Computersystem und eine allgemeine Einstellung auf diesem System.<br/>                                                                            |
| [**Win32 \_ systemsystemdriver**](win32-systemsystemdriver.md)                               | Association-Klasse<br/> Beziehung zwischen einem Computersystem und einem System Treiber, der auf diesem Computersystem ausgeführt wird.<br/>                                                             |
| [**Win32- \_ systemtimezone**](win32-systemtimezone.md)                                       | Association-Klasse<br/> Bezieht ein Computersystem und eine Zeitzone in Beziehung.<br/>                                                                                                 |
| [**Win32-System \_ Parser**](win32-systemusers.md)                                             | Association-Klasse<br/> Verknüpft ein Computersystem und ein Benutzerkonto in diesem System.<br/>                                                                               |



 

## <a name="processes"></a>Prozesse

Die unterkategorieprozesse gruppiert Klassen, die System Prozesse und Threads darstellen.



| Klasse                                                 | BESCHREIBUNG                                                                                                     |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ Prozess**](win32-process.md)               | Instanzklasse<br/> Stellt eine Abfolge von Ereignissen auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>      |
| [**Win32- \_ processstartup**](win32-processstartup.md) | Instanzklasse<br/> Stellt die Startkonfiguration eines Computer Systems dar, auf dem Windows ausgeführt wird.<br/> |
| [**Win32- \_ Thread**](win32-thread.md)                 | Instanzklasse<br/> Stellt einen Ausführungs Thread dar.<br/>                                          |



 

## <a name="registry"></a>Registrierung

Die-Klasse in der Registrierungs Unterkategorie stellt den Inhalt der Windows-Registrierung dar.



| Klasse                                     | BESCHREIBUNG                                                                                               |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**Win32- \_ Registrierung**](win32-registry.md) | Instanzklasse<br/> Stellt die Systemregistrierung auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/> |



 

## <a name="scheduler-jobs"></a>Scheduler-Aufträge

Die Unterkategorie "Scheduler Jobs" gruppiert Klassen, die Einstellungen für geplante Aufträge darstellen.



| Klasse                                                | BESCHREIBUNG                                                                                                                                                                                                                                                           |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) | Abstrakte Klasse<br/> Stellt eine Instanz in der Zeit als Komponenten Sekunden, Minuten, Wochentag usw. dar.<br/>                                                                                                                                        |
| [**Win32 \_ ScheduledJob**](win32-scheduledjob.md)    | Instanzklasse<br/> Stellt einen mit dem Windows-Zeit Plan Dienst geplanten Auftrag dar.<br/>                                                                                                                                                                   |
| [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)     | Instanzklasse<br/> Stellt einen Zeitpunkt dar, der als [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) -Objekte zurückgegeben wird, die sich aus einer Abfrage ergeben. Die **Hour** -Eigenschaft wird als Ortszeit in einem 24-Stunden-Format zurückgegeben.<br/>                                |
| [**Win32- \_ utcTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)         | Instanzklasse<br/> Stellt einen Zeitpunkt dar, der als Win32- [**\_ utcTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) -Objekte zurückgegeben wird, die sich aus einer Abfrage ergeben. Die **Hour** -Eigenschaft wird in einem 24-Stunden-Takt als koordinierte Weltzeit (UTC) zurückgegeben.<br/> |



 

## <a name="security"></a>Sicherheit

Die sicherheitssubcategory gruppiert Klassen, die System Sicherheitseinstellungen darstellen.



| Klasse                                                                               | BESCHREIBUNG                                                                                                                                                  |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ AccountSid**](/previous-versions/windows/desktop/secrcw32prov/win32-accountsid)                                       | Association-Klasse<br/> Verknüpft eine Sicherheits Konto Instanz mit einer Sicherheits Deskriptorinstanz.<br/>                                             |
| [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)                                                     | Instanzklasse<br/> Stellt einen Zugriffssteuerungseintrag (ACE) dar.<br/>                                                                               |
| [**Win32 \_ logicalfileaccess**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileaccess)                         | Association-Klasse<br/> Verknüpft die Sicherheitseinstellungen einer Datei oder eines Verzeichnisses und eines Mitglieds seiner freigegebenen Zugriffs Steuerungs Liste (DACL).<br/> |
| [**Win32 \_ logicalfileauditing**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileauditing)                     | Association-Klasse<br/> Verknüpft die Sicherheitseinstellungen einer Datei oder eines Verzeichnisses mit einem Mitglied der System Zugriffs Steuerungs Liste (SACL).<br/>            |
| [**Win32 \_ logicalfilegroup**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilegroup)                           | Association-Klasse<br/> Bezieht die Sicherheitseinstellungen einer Datei oder eines Verzeichnisses und seiner Gruppe in Beziehung.<br/>                                                  |
| [**Win32 \_ logicalfileowner**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileowner)                           | Association-Klasse<br/> Verknüpft die Sicherheitseinstellungen einer Datei oder eines Verzeichnisses und seines Besitzers.<br/>                                                  |
| [**Win32 \_ logicalfilesecuritysetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)       | Instanzklasse<br/> Stellt Sicherheitseinstellungen für eine logische Datei dar.<br/>                                                                        |
| [**Win32 \_ logicalshareaccess**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareaccess)                       | Association-Klasse<br/> Verknüpft die Sicherheitseinstellungen einer Freigabe und eines Mitglieds der DACL.<br/>                                                 |
| [**Win32 \_ logicalshareauditing**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareauditing)                   | Association-Klasse<br/> Verknüpft die Sicherheitseinstellungen einer Freigabe und eines Mitglieds der SACL.<br/>                                                 |
| [**Win32 \_ logicalsharesecuritysetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting)     | Instanzklasse<br/> Stellt Sicherheitseinstellungen für eine logische Datei dar.<br/>                                                                        |
| [**Win32 \_ privilegesstatus**](win32-privilegesstatus.md)                           | Instanzklasse<br/> Stellt Informationen zu den Berechtigungen dar, die erforderlich sind, um einen Vorgang abzuschließen.<br/>                                          |
| [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)                       | Instanzklasse<br/> Stellt eine strukturelle Darstellung einer [**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)dar.<br/>                   |
| [**Win32- \_ securitysetting**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysetting)                             | Instanzklasse<br/> Stellt Sicherheitseinstellungen für ein verwaltetes Element dar.<br/>                                                                     |
| [**Win32 \_ securitysettingaccess**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingaccess)                 | Instanzklasse<br/> Stellt die Rechte dar, die einem Vertrauens nehmer für ein bestimmtes Objekt gewährt und verweigert werden.<br/>                                               |
| [**Win32 \_ securitysettingauditing**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingauditing)             | Instanzklasse<br/> Stellt die Überwachung für einen angegebenen Vertrauens nehmer für ein bestimmtes Objekt dar.<br/>                                                          |
| [**Win32 \_ securitysettinggroup**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettinggroup)                   | Association-Klasse<br/> Ordnet die Sicherheit eines Objekts und seiner Gruppe in Beziehung.<br/>                                                                     |
| [**Win32 \_ securitysettingoflogicalfile**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalfile)   | Instanzklasse<br/> Stellt die Sicherheitseinstellungen eines Datei-oder Verzeichnis Objekts dar.<br/>                                                             |
| [**Win32 \_ securitysettingoflogicalshare**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalshare) | Instanzklasse<br/> Stellt die Sicherheitseinstellungen eines freigegebenen-Objekts dar.<br/>                                                                        |
| [**Win32 \_ securitysettingofobject**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingofobject)             | Association-Klasse<br/> Verknüpft ein Objekt mit seinen Sicherheitseinstellungen.<br/>                                                                          |
| [**Win32 \_ securitysettingowner**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingowner)                   | Association-Klasse<br/> Verknüpft die Sicherheitseinstellungen eines Objekts und seines Besitzers.<br/>                                                            |
| [**Win32- \_ sid**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)                                                     | Instanzklasse<br/> Stellt eine beliebige sid dar.<br/>                                                                                            |
| [**Win32- \_ Treuhänder**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)                                             | Instanzklasse<br/> Stellt einen Vertrauens nehmer dar.<br/>                                                                                                   |



 

## <a name="services"></a>Dienste

Die Unterkategorie Dienste gruppiert Klassen, die Dienste und Basisdienste darstellen.



| Klasse                                           | BESCHREIBUNG                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ baseservice**](win32-baseservice.md) | Instanzklasse<br/> Stellt ausführbare Objekte dar, die in einer Registrierungsdatenbank installiert werden, die vom Dienststeuerungs-Manager verwaltet wird.<br/> |
| [**Win32- \_ Dienst**](win32-service.md)         | Instanzklasse<br/> Stellt einen Dienst auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                         |



 

## <a name="shares"></a>Freigaben

Die Unterkategorie Freigaben gruppiert Klassen, die Details zu freigegebenen Ressourcen, z. b. Drucker und Ordner, darstellen.



| Klasse                                                       | BESCHREIBUNG                                                                                                                                                                                          |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ dfsnode**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnode)                     | Association-Klasse<br/> Stellt einen Stamm Knoten oder einen Verbindungsknoten eines domänenbasierten oder eigenständigen verteilten Dateisystems (DFS) dar.<br/>                                                           |
| [**Win32 \_ dfsnodetarget**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnodetarget)         | Association-Klasse<br/> Stellt die Beziehung zwischen einem DFS-Knoten und einem seiner Ziele dar.<br/>                                                                                             |
| [**Win32- \_ dfstarget**](/previous-versions/windows/desktop/wmipdfs/win32-dfstarget)                 | Association-Klasse<br/> Stellt das Ziel eines DFS-Knotens dar.<br/>                                                                                                                         |
| [**Win32- \_ Server Verbindung**](/previous-versions/windows/desktop/wmipsess/win32-serverconnection)   | Instanzklasse<br/> Stellt die Verbindungen dar, die von einem Remote Computer zu einer freigegebenen Ressource auf dem lokalen Computer hergestellt werden.<br/>                                                              |
| [**Win32- \_ Serversession**](/previous-versions/windows/desktop/wmipsess/win32-serversession)         | Instanzklasse<br/> Stellt die Sitzungen dar, die von Benutzern auf einem Remote Computer mit dem lokalen Computer eingerichtet werden.<br/>                                                             |
| [**Win32- \_ connectionshare**](/previous-versions/windows/desktop/wmipsess/win32-connectionshare)     | Association-Klasse<br/> Verknüpft eine freigegebene Ressource auf dem Computer und die Verbindung, die mit der freigegebenen Ressource hergestellt wird.<br/>                                                                    |
| [**Win32- \_ Freigabe**](win32-printershare.md)           | Association-Klasse<br/> Bezieht einen lokalen Drucker und die Freigabe, die ihn darstellt, so ein, wie er über ein Netzwerk angezeigt wird.<br/>                                                                     |
| [**Win32 \_ sessionconnection**](/previous-versions/windows/desktop/wmipsess/win32-sessionconnection) | Association-Klasse<br/> Stellt eine Zuordnung zwischen einer Sitzung dar, die von einem Benutzer auf einem Remote Computer mit dem lokalen Server hergestellt wurde, und den Verbindungen, die von der Sitzung abhängen.<br/> |
| [**Win32 \_ sessionprocess**](win32-sessionprocess.md)       | Association-Klasse<br/> Stellt eine Zuordnung zwischen einer Anmelde Sitzung und den Prozessen dar, die dieser Sitzung zugeordnet sind.<br/>                                                            |
| [**Win32 \_ shareverzeichnis**](win32-sharetodirectory.md)   | Association-Klasse<br/> Bezieht eine freigegebene Ressource auf dem Computersystem und dem Verzeichnis, dem Sie zugeordnet ist.<br/>                                                                    |
| [**Win32- \_ Freigabe**](win32-share.md)                         | Instanzklasse<br/> Repräsentiert eine freigegebene Ressource auf einem Computersystem, auf dem Windows ausgeführt wird.<br/>                                                                                              |



 

## <a name="start-menu"></a>Startmenü

Die Unterkategorie Startmenü gruppiert Klassen, die Programm Gruppen darstellen.



| Klasse                                                                                   | BESCHREIBUNG                                                                                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ logicalprogramgroup**](win32-logicalprogramgroup.md)                         | Instanzklasse<br/> Stellt eine Programmgruppe in einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                    |
| [**Win32 \_ logicalprogramgroupdirectory**](win32-logicalprogramgroupdirectory.md)       | Association-Klasse<br/> Ordnet logische Programm Gruppen (Gruppierungen im Startmenü) und die Datei Verzeichnisse, in denen Sie gespeichert sind, in Beziehung.<br/>                 |
| [**Win32 \_ logicalprogramgroupitem**](win32-logicalprogramgroupitem.md)                 | Instanzklasse<br/> Stellt ein Element dar, das in einer **Win32- \_ Programm Gruppen** Instanz enthalten ist, das keine andere **Win32- \_ Programm Gruppen** Instanz ist.<br/> |
| [**Win32 \_ logicalprogramgroupitemdatafile**](win32-logicalprogramgroupitemdatafile.md) | Association-Klasse<br/> Verknüpft die Programm Gruppenelemente im Startmenü und die Dateien, in denen Sie gespeichert sind.<br/>                                       |
| [**Win32- \_ programmgroupcontent**](win32-programgroupcontents.md)                       | Association-Klasse<br/> Verknüpft eine Programm Gruppen Reihenfolge und eine einzelne Programmgruppe oder ein Element, das darin enthalten ist.<br/>                                           |
| [**Win32- \_ programmgrouporitem**](win32-programgrouporitem.md)                           | Instanzklasse<br/> Stellt eine logische Gruppierung von Programmen im Menü **Start** \| **Programme** des Benutzers dar.<br/>                                               |



 

## <a name="storage"></a>Storage

Die Unterkategorie Benutzer gruppiert Klassen, die Speicherinformationen darstellen.



| Klasse                                                                   | BESCHREIBUNG                                                                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ shadoby**](/previous-versions/windows/desktop/vsswmi/win32-shadowby)                               | Association-Klasse<br/> Stellt die Zuordnung zwischen einer Schatten Kopie und dem Anbieter dar, der die Schatten Kopie erstellt.<br/>      |
| [**Win32- \_ shadocontext**](/previous-versions/windows/desktop/vsswmi/win32-shadowcontext)                     | Association-Klasse<br/> Gibt an, wie eine Schatten Kopie erstellt, abgefragt oder gelöscht werden soll.<br/>                                   |
| [**Win32- \_ Schatten Kopie**](/previous-versions/windows/desktop/legacy/aa394428(v=vs.85))                           | Instanzklasse<br/> Stellt eine doppelte Kopie des ursprünglichen Volumes zu einem früheren Zeitpunkt dar.<br/>                                  |
| [**Win32- \_ shadodiffvolumesupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowdiffvolumesupport) | Association-Klasse<br/> Stellt eine Zuordnung zwischen einem Schattenkopieanbieter und einem Speicher Volume dar.<br/>                       |
| [**Win32 \_ shadowfor**](/previous-versions/windows/desktop/vsswmi/win32-shadowfor)                             | Association-Klasse<br/> Stellt eine Zuordnung zwischen einer Schatten Kopie und dem Volume dar, für das die Schatten Kopie erstellt wird.<br/> |
| [**Win32- \_ shadoon**](/previous-versions/windows/desktop/vsswmi/win32-shadowon)                               | Association-Klasse<br/> Stellt eine Zuordnung zwischen einer Schatten Kopie und dem Speicherort der differenziellen Daten dar.<br/>          |
| [**Win32- \_ Schatten Anbieter**](/previous-versions/windows/desktop/vsswmi/win32-shadowprovider)                   | Association-Klasse<br/> Stellt eine Komponente dar, die Volumeschattenkopien erstellt und darstellt.<br/>                             |
| [**Win32- \_ ShadowStorage**](/previous-versions/windows/desktop/legacy/aa394433(v=vs.85))                     | Association-Klasse<br/> Stellt eine Zuordnung zwischen einer Schatten Kopie und dem Speicherort der differenziellen Daten dar.<br/>          |
| [**Win32 \_ shadowvolumesupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowvolumesupport)         | Association-Klasse<br/> Stellt eine Zuordnung zwischen einem Schattenkopieanbieter und einem unterstützten Volume dar.<br/>                    |
| [**Win32- \_ Volume**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                   | Instanzklasse<br/> Stellt einen Speicherbereich auf einer Festplatte dar.<br/>                                                           |
| [**Win32- \_ volumeuserquota**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                 | Association-Klasse<br/> Stellt ein Volume für die Kontingent Einstellungen pro Volume dar.<br/>                                                |



 

## <a name="users"></a>Benutzer

Die Unterkategorie Benutzer gruppiert Klassen, die Benutzerkontoinformationen darstellen, z. b. Details zu Gruppenmitgliedschaften.



| Klasse                                                                 | BESCHREIBUNG                                                                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ Konto**](win32-account.md)                               | Instanzklasse<br/> Stellt Informationen zu Benutzerkonten und Gruppenkonten dar, die dem Computersystem bekannt sind, auf dem Windows ausgeführt wird.<br/> |
| [**Win32- \_ Gruppe**](win32-group.md)                                   | Instanzklasse<br/> Stellt Daten zu einem Gruppenkonto dar.<br/>                                                                      |
| [**Win32- \_ groupindomäne**](/previous-versions/windows/desktop/cimwin32a/win32-groupindomain)                   | Association-Klasse<br/> Identifiziert die einer Windows NT-Domäne zugeordneten Gruppenkonten.<br/>                                       |
| [**Win32- \_ groupuser**](win32-groupuser.md)                           | Association-Klasse<br/> Beziehung zwischen einer Gruppe und einem Konto, das Mitglied dieser Gruppe ist.<br/>                                           |
| [**Win32-Anmelde \_ Sitzung**](win32-logonsession.md)                     | Instanzklasse<br/> Beschreibt die Anmelde Sitzung oder Sitzungen, die einem Benutzer zugeordnet sind, der bei Windows angemeldet ist.<br/>                        |
| [**Win32 \_ logonsessionmappeddisk**](/windows/desktop/CIMWin32Prov/win32-logonsessionmappeddisk) | Instanzklasse<br/> Stellt die zugeordneten logischen Datenträger dar, die der Sitzung zugeordnet sind.<br/>                                            |
| [**Win32- \_ networkloginprofile**](win32-networkloginprofile.md)       | Instanzklasse<br/> Stellt die Netzwerk Anmelde Informationen eines bestimmten Benutzers auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>           |
| [**Win32- \_ Systemkonto**](win32-systemaccount.md)                   | Instanzklasse<br/> Stellt ein Systemkonto dar.<br/>                                                                                |
| [**Win32- \_ Benutzerkonto**](win32-useraccount.md)                       | Instanzklasse<br/> Stellt Informationen zu einem Benutzerkonto auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                           |
| [**Win32 \_ userindomain**](/previous-versions/windows/desktop/cimwin32a/win32-userindomain)                     | Association-Klasse<br/> Bezieht ein Benutzerkonto und eine Windows NT-Domäne in Beziehung.<br/>                                                          |



 

## <a name="windows-event-log"></a>Windows-Ereignisprotokoll

Die Unterkategorie des Windows-Ereignis Protokolls gruppiert Klassen, die Ereignisse, Ereignisprotokoll Einträge, Konfigurationseinstellungen für das Ereignisprotokoll usw. darstellen.



| Klasse                                                         | BESCHREIBUNG                                                                                                                                                                   |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ nteventlogfile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))         | Instanzklasse<br/> Stellt Daten dar, die in einer Windows-Ereignisprotokoll Datei gespeichert sind.<br/>                                                                                      |
| [**Win32- \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)                 | Instanzklasse<br/> Stellt Windows-Ereignisse dar.<br/>                                                                                                               |
| [**Win32- \_ ntlogeventcomputer**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventcomputer) | Association-Klasse<br/> Bezieht Instanzen von [**Win32 \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) und [**Win32 \_ Computersystem**](win32-computersystem.md).<br/>         |
| [**Win32- \_ ntlogeventlog**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventlog)           | Association-Klasse<br/> Bezieht Instanzen der [**Win32-Klassen \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) und [**Win32 \_ nteventlogfile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) .<br/> |
| [**Win32- \_ ntlogeventuser**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventuser)         | Association-Klasse<br/> Bezieht Instanzen von [**Win32 \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) und [**Win32 \_ User Account**](win32-useraccount.md).<br/>               |



 

## <a name="windows-product-activation"></a>Windows-Produktaktivierung

Die Windows-Produktaktivierung (WPA) ist eine Antipiraterie-Technologie, um das gelegentliche Kopieren von Software zu reduzieren.



| Klasse                                                                                                               | BESCHREIBUNG                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ computersystemwindowsproductactivationsetting**](/previous-versions/windows/desktop/licwmiprov/win32-computersystemwindowsproductactivationsetting) | Association-Klasse<br/> Bezieht Instanzen von [**Win32 \_ Computersystem**](win32-computersystem.md) und [**Win32 \_ windowsproductactivations**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)).<br/> |
| [**Win32- \_ Proxy**](/previous-versions/windows/desktop/legacy/aa394389(v=vs.85))                                                                                 | Instanzklasse<br/> Enthält Eigenschaften und Methoden zum Abfragen und Konfigurieren einer Internet Verbindung, die mit WPA verknüpft ist.<br/>                                                                |
| [**Win32- \_ windowsproductactivations**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85))                                           | Instanzklasse<br/> Enthält Eigenschaften und Methoden, die sich auf WPA beziehen.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Win32-Klassen](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

