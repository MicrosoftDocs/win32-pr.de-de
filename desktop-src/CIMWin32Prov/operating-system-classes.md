---
description: Die Kategorie Betriebssystemgruppenklassen, die betriebssystembezogene Objekte darstellen.
ms.assetid: D0756D8C-A3D3-4C75-96A3-8C7F05300B39
ms.tgt_platform: multiple
title: Betriebssystemklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5cbb168b2a322b5ceae8a2bd73985d14a74b4f1df227fd3e6cce384c554742
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588290"
---
# <a name="operating-system-classes"></a>Betriebssystemklassen

Die Kategorie Betriebssystemgruppenklassen, die betriebssystembezogene Objekte darstellen. Sie bezeichnen die verschiedenen Konfigurationen und Einstellungen, die eine Computingumgebung definieren. Beispiele hierfür sind die Startkonfiguration, Component Object Model (COM)-Einstellungen, Desktopumgebungseinstellungen, Treiber, Sicherheitseinstellungen, Benutzereinstellungen und Registrierungseinstellungen.

Die Kategorie Betriebssystem ist in die folgenden Unterkategorien eingereiht:

-   [COM](#com)
-   [Desktop](#desktop)
-   [Treiber](#drivers)
-   [Ereignisprotokoll](#windows-event-log)
-   [Dateisystem](#file-system)
-   [Auftragsobjekte](#job-objects)
-   [Speicher- und Seitendateien](#memory-and-page-files)
-   [Multimediaaudio oder -visual](#multimedia-audio-or-visual)
-   [Netzwerk](#networking)
-   [Betriebssystemereignisse](#operating-system-events)
-   [Betriebssystemeinstellungen](#operating-system-settings)
-   [Prozesse](#processes)
-   [Registrierung](#registry)
-   [Scheduler-Aufträge](#scheduler-jobs)
-   [Sicherheit](#security)
-   [Dienste](#services)
-   [Freigaben](#shares)
-   [Startmenü](#start-menu)
-   [Storage](#storage)
-   [Benutzer](#users)
-   [Windows Produktaktivierung](#windows-product-activation)

## <a name="com"></a>COM

Die COM-Unterkategorie gruppen Klassen, die COM- und DCOM-Einstellungen, -Klassen und Clientanwendungseinstellungen darstellen.



| Klasse                                                                                           | Beschreibung                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ClassicCOMApplicationClasses**](win32-classiccomapplicationclasses.md)               | Association-Klasse<br/> Bezieht eine DCOM-Anwendung und eine darunter gruppierte COM-Komponente.<br/>                                                                             |
| [**Win32 \_ ClassicCOMClass**](win32-classiccomclass.md)                                         | Instanzklasse<br/> Stellt die Eigenschaften einer COM-Komponente dar.<br/>                                                                                                   |
| [**Win32 \_ ClassicCOMClassSettings**](win32-classiccomclasssettings.md)                         | Association-Klasse<br/> Bezieht sich auf eine COM-Klasse und die Einstellungen, die zum Konfigurieren von Instanzen der COM-Klasse verwendet werden.<br/>                                                           |
| [**Win32 \_ ClientApplicationSetting**](win32-clientapplicationsetting.md)                       | Association-Klasse<br/> Bezieht eine ausführbare Datei und eine DCOM-Anwendung, die die DCOM-Konfigurationsoptionen für die ausführbare Datei enthält.<br/>                           |
| [**Win32 \_ COMApplication**](win32-comapplication.md)                                           | Instanzklasse<br/> Stellt eine COM-Anwendung dar.<br/>                                                                                                                   |
| [**Win32 \_ COMApplicationClasses**](win32-comapplicationclasses.md)                             | Association-Klasse<br/> Bezieht eine COM-Komponente mit der COM-Anwendung, in der sie sich befindet.<br/>                                                                            |
| [**Win32 \_ COMApplicationSettings**](win32-comapplicationsettings.md)                           | Association-Klasse<br/> Bezieht eine DCOM-Anwendung und ihre Konfigurationseinstellungen.<br/>                                                                                   |
| [**Win32 \_ COMClass**](win32-comclass.md)                                                       | Instanzklasse<br/> Stellt die Eigenschaften einer COM-Komponente dar.<br/>                                                                                                   |
| [**Win32 \_ ComClassAutoEmulator**](win32-comclassautoemulator.md)                               | Association-Klasse<br/> Bezieht eine COM-Klasse und eine andere COM-Klasse, die automatisch emuliert wird.<br/>                                                                    |
| [**Win32 \_ ComClassEmulator**](win32-comclassemulator.md)                                       | Association-Klasse<br/> Bezieht sich auf zwei Versionen einer COM-Klasse.<br/>                                                                                                         |
| [**Win32 \_ ComponentCategory**](win32-componentcategory.md)                                     | Instanzklasse<br/> Stellt eine Komponentenkategorie dar.<br/>                                                                                                                |
| [**Win32 \_ COMSetting**](win32-comsetting.md)                                                   | Instanzklasse<br/> Stellt die Einer COM-Komponente oder COM-Anwendung zugeordneten Einstellungen dar.<br/>                                                                     |
| [**Win32 \_ DCOMApplication**](win32-dcomapplication.md)                                         | Instanzklasse<br/> Stellt die Eigenschaften einer DCOM-Anwendung dar.<br/>                                                                                                |
| [**Win32 \_ DCOMApplicationAccessAllowedSetting**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationaccessallowedsetting) | Association-Klasse<br/> Bezieht die [**Win32 \_ DCOMApplication-Instanz**](win32-dcomapplication.md) und die Benutzersicherheits-ID (SID), die darauf zugreifen können.<br/> |
| [**Win32 \_ DCOMApplicationLaunchAllowedSetting**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationlaunchallowedsetting) | Association-Klasse<br/> Bezieht die [**Win32 \_ DCOMApplication-Instanz**](win32-dcomapplication.md) und die Benutzer-SIDs, die sie starten können.<br/>                           |
| [**Win32 \_ DCOMApplicationSetting**](win32-dcomapplicationsetting.md)                           | Instanzklasse<br/> Stellt die Einstellungen einer DCOM-Anwendung dar.<br/>                                                                                                  |
| [**Win32 \_ ImplementedCategory**](win32-implementedcategory.md)                                 | Association-Klasse<br/> Bezieht eine Komponentenkategorie und die COM-Klasse unter Verwendung ihrer Schnittstellen.<br/>                                                                         |



 

## <a name="desktop"></a>Desktop

Die Desktop-Unterkategorie gruppen Klassen, die Objekte darstellen, die eine bestimmte Desktopkonfiguration definieren.



| Klasse                                           | Beschreibung                                                                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ Desktop**](win32-desktop.md)         | Instanzklasse<br/> Stellt die allgemeinen Merkmale des Desktops eines Benutzers dar.<br/>                                    |
| [**Win32-Umgebung \_**](win32-environment.md) | Instanzklasse<br/> Stellt eine Umgebungs- oder Systemumgebungseinstellung auf einem Computersystem dar, auf dem Windows.<br/> |
| [**\_Win32-Zeitzone**](win32-timezone.md)       | Instanzklasse<br/> Stellt die Zeitzoneninformationen für ein Computersystem dar, auf dem Windows.<br/>                   |
| [**Win32 \_ UserDesktop**](win32-userdesktop.md) | Association-Klasse<br/> Bezieht sich auf ein Benutzerkonto und die spezifischen Desktopeinstellungen.<br/>                   |



 

## <a name="drivers"></a>Treiber

Die Unterkategorie Drivers (Treiber) gruppen Klassen, die virtuelle Gerätetreiber und Systemtreiber für Basisdienste darstellen.



| Klasse                                             | Beschreibung                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [**Win32 \_ SystemDriver**](win32-systemdriver.md) | Instanzklasse<br/> Stellt den Systemtreiber für einen Basisdienst dar.<br/> |



 

## <a name="file-system"></a>Dateisystem

Die Unterkategorie Dateisystem gruppen Klassen, die die logisch angeordnete Festplatte darstellen. Dies schließt den Typ des verwendeten Dateisystems, die Verzeichnisstruktur und die Partitionierung des Datenträgers ein.



| Klasse                                                                               | Beschreibung                                                                                                                                                                          |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CIMLogicalDeviceCIMDataFile**](win32-cimlogicaldevicecimdatafile.md)     | Association-Klasse<br/> Bezieht sich auf logische Geräte und Datendateien, die die vom Gerät verwendeten Treiberdateien angeben.<br/>                                                      |
| [**Win32-Verzeichnis \_**](win32-directory.md)                                         | Instanzklasse<br/> Stellt einen Verzeichniseintrag auf einem Computersystem dar, auf dem Windows.<br/>                                                                              |
| [**Win32 \_ DirectorySpecification**](/previous-versions/windows/desktop/msiprov/win32-directoryspecification)               | Instanzklasse<br/> Stellt das Verzeichnislayout für das Produkt dar.<br/>                                                                                                |
| [**Win32 \_ DiskDriveToDiskPartition**](win32-diskdrivetodiskpartition.md)           | Association-Klasse<br/> Bezieht ein Laufwerk und eine darauf vorhandene Partition.<br/>                                                                                         |
| [**Win32 \_ DiskPartition**](win32-diskpartition.md)                                 | Instanzklasse<br/> Stellt die Funktionen und die Verwaltungskapazität eines partitionierten Bereichs eines physischen Datenträgers auf einem Computersystem dar, auf dem Windows.<br/>              |
| [**Win32 \_ DiskQuota**](/previous-versions/windows/desktop/wmipdskq/win32-diskquota)                                    | Association-Klasse<br/> Verfolgt die Speicherplatznutzung für NTFS-Dateisystemvolumes nach.<br/>                                                                                        |
| [**Win32 \_ LogicalDisk**](win32-logicaldisk.md)                                     | Stellt eine Datenquelle dar, die in ein tatsächliches lokales Speichergerät auf einem Computersystem mit Windows.<br/>                                                            |
| [**Win32 \_ LogicalDiskRootDirectory**](win32-logicaldiskrootdirectory.md)           | Association-Klasse<br/> Bezieht einen logischen Datenträger und seine Verzeichnisstruktur.<br/>                                                                                          |
| [**Win32 \_ LogicalDiskToPartition**](win32-logicaldisktopartition.md)               | Association-Klasse<br/> Bezieht ein logisches Laufwerk und die Datenträgerpartition, auf der es sich befindet.<br/>                                                                           |
| [**Win32 \_ MappedLogicalDisk**](win32-mappedlogicaldisk.md)                         | Stellt Netzwerkspeichergeräte dar, die als logische Datenträger auf dem Computersystem zugeordnet sind, auf dem Windows.<br/>                                                               |
| [**Win32 \_ OperatingSystemAutochkSetting**](/previous-versions//aa394240(v=vs.85)) | Association-Klasse<br/> Stellt die Zuordnung zwischen einer [**CIM \_ ManagedSystemElement-Instanz**](cim-managedsystemelement.md) und den dafür definierten Einstellungen dar.<br/> |
| [**Win32 \_ QuotaSetting**](/previous-versions/windows/desktop/wmipdskq/win32-quotasetting)                              | Instanzklasse<br/> Enthält Einstellungsinformationen für Datenträgerkontingente auf einem Volume.<br/>                                                                                       |
| [**Win32 \_ ShortcutFile**](win32-shortcutfile.md)                                   | Instanzklasse<br/> Stellt Dateien dar, die Verknüpfungen zu anderen Dateien, Verzeichnissen und Befehlen sind.<br/>                                                                  |
| [**\_Win32-Unterverzeichnis**](win32-subdirectory.md)                                   | Association-Klasse<br/> Bezieht sich auf ein Verzeichnis (Ordner) und eines seiner Unterverzeichnisse (Unterordner).<br/>                                                                     |
| [**Win32 \_ SystemPartitions**](win32-systempartitions.md)                           | Association-Klasse<br/> Bezieht sich auf ein Computersystem und eine Datenträgerpartition auf diesem System.<br/>                                                                               |
| [**Win32-Volume \_**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                               | Instanzklasse<br/> Stellt einen Speicherbereich auf einer Festplatte dar.<br/>                                                                                                   |
| [**Win32 \_ VolumeQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumequota)                                     | Association-Klasse<br/> Bezieht ein Volume auf die Kontingenteinstellungen pro Volume.<br/>                                                                                           |
| [**Win32 \_ VolumeQuotaSetting**](/previous-versions/windows/desktop/wmipdskq/win32-volumequotasetting)                  | Association-Klasse<br/> Bezieht Datenträgerkontingenteinstellungen mit einem bestimmten Datenträgervolumen in Zusammenhang.<br/>                                                                                     |
| [**Win32 \_ VolumeUserQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                             | Association-Klasse<br/> Bezieht sich pro Benutzer auf kontingentfähige Volumes.<br/>                                                                                            |



 

## <a name="job-objects"></a>Auftragsobjekte

Die Unterkategorie Auftragsobjekte gruppen Klassen, die Klassen darstellen, die die Instrumentierung von benannten Auftragsobjekten ermöglichen. Ein unbenanntes Auftragsobjekt kann nicht instrumentiert werden.



| Klasse                                                                               | Beschreibung                                                                                                                                                                                |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CollectionStatistics**](/previous-versions/windows/desktop/cimwin32a/win32-collectionstatistics)                   | Association-Klasse<br/> Bezieht eine verwaltete Systemelementsammlung und die -Klasse, die statistische Informationen über die Auflistung darstellt.<br/>                               |
| [**\_Win32-LUID**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luid)                                                   | Instanzklasse<br/> Stellt einen lokal eindeutigen Bezeichner (LUID) dar.<br/>                                                                                                         |
| [**Win32 \_ LUIDandAttributes**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luidandattributes)                         | Instanzklasse<br/> Stellt eine LUID und ihre Attribute dar.<br/>                                                                                                                 |
| [**Win32 \_ NamedJobObject**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobject)                               | Instanzklasse<br/> Stellt ein Kernelobjekt dar, das zum Gruppieren von Prozessen verwendet wird, um die Lebensdauer und Ressourcen der Prozesse innerhalb des Auftragsobjekts zu steuern.<br/> |
| [**Win32 \_ NamedJobObjectActgInfo**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectactginfo)               | Instanzklasse<br/> Stellt die E/A-Kontoführungsinformationen für ein Auftragsobjekt dar.<br/>                                                                                           |
| [**Win32 \_ NamedJobObjectLimit**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimit)                     | Instanzklasse<br/> Stellt eine Zuordnung zwischen einem Auftragsobjekt und den Grenzwerteinstellungen des Auftragsobjekts dar.<br/>                                                                     |
| [**Win32 \_ NamedJobObjectLimitSetting**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimitsetting)       | Instanzklasse<br/> Stellt die Begrenzungseinstellungen für ein Auftragsobjekt dar.<br/>                                                                                                       |
| [**Win32 \_ NamedJobObjectProcess**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectprocess)                 | Instanzklasse<br/> Bezieht ein Auftragsobjekt und den prozess, der im Auftragsobjekt enthalten ist.<br/>                                                                                     |
| [**Win32 \_ NamedJobObjectSecLimit**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimit)               | Instanzklasse<br/> Bezieht sich auf ein Auftragsobjekt und die Sicherheitslimiteinstellungen des Auftragsobjekts.<br/>                                                                                      |
| [**Win32 \_ NamedJobObjectSecLimitSetting**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimitsetting) | Instanzklasse<br/> Stellt die Sicherheitslimiteinstellungen für ein Auftragsobjekt dar.<br/>                                                                                              |
| [**Win32 \_ NamedJobObjectStatistics**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectstatistics)           | Instanzklasse<br/> Stellt eine Zuordnung zwischen einem Auftragsobjekt und der Auftragsobjekt-E/A-Buchhaltungsinformationsklasse dar.<br/>                                                   |
| [**Win32 \_ SIDandAttributes**](/previous-versions/windows/desktop/wmipjobobjprov/win32-sidandattributes)                           | Instanzklasse<br/> Stellt eine Sicherheits-ID (SID) und deren Attribute dar.<br/>                                                                                            |
| [**Win32 \_ TokenGroups**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokengroups)                                     | Ereignisklasse<br/> Stellt Informationen zu den Gruppen-SIDs in einem Zugriffstoken dar.<br/>                                                                                          |
| [**Win32 \_ TokenPrivileges**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokenprivileges)                             | Ereignisklasse<br/> Stellt Informationen zu einem Satz von Berechtigungen für ein Zugriffstoken dar.<br/>                                                                                    |



 

## <a name="memory-and-page-files"></a>Speicher- und Seitendateien

In der Unterkategorie Speicher- und Seitendateien werden Klassen gruppen, die Konfigurationseinstellungen für Seitendateien darstellen.



| Klasse                                                                 | Beschreibung                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ PageFile**](win32-pagefile.md)                             | Instanzklasse<br/> Stellt die Datei dar, die zum Verarbeiten des Dateitauschs virtueller Speicher auf einem Windows wird.<br/>                  |
| [**Win32 \_ PageFileElementSetting**](win32-pagefileelementsetting.md) | Association-Klasse<br/> Bezieht die anfänglichen Einstellungen einer Seitendatei und den Status dieser Einstellungen während der normalen Verwendung.<br/>        |
| [**Win32 \_ PageFileSetting**](win32-pagefilesetting.md)               | Instanzklasse<br/> Stellt die Einstellungen einer Seitendatei dar.<br/>                                                                  |
| [**Win32 \_ PageFileUsage**](win32-pagefileusage.md)                   | Instanzklasse<br/> Stellt die Datei dar, die zum Verarbeiten des Dateitauschs des virtuellen Arbeitsspeichers auf einem Computersystem verwendet wird, auf dem Windows.<br/> |



 

## <a name="multimedia-audio-or-visual"></a>Multimediaaudio oder Visuelles Audio

Die -Klasse in der Unterkategorie Multimedia Audio oder Visual stellt Eigenschaften des Audio- oder Videocodecs dar, der auf dem Computersystem installiert ist.



| Klasse                                       | Beschreibung                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CodecFile**](win32-codecfile.md) | Instanzklasse<br/> Stellt den auf dem Computersystem installierten Audio- oder Videocodec dar.<br/> |



 

## <a name="networking"></a>Netzwerk

Die Unterkategorie Netzwerk gruppen Klassen, die Netzwerkverbindungen, Netzwerkclients und Netzwerkverbindungseinstellungen wie das verwendete Protokoll darstellen.



| Klasse                                                                            | Beschreibung                                                                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ActiveRoute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)                       | Association-Klasse<br/> Bezieht die aktuelle IP4-Route auf die persistente IP-Routentabelle.<br/>                           |
| [**Win32 \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable) | Instanzklasse<br/> Stellt persistente IP-Routen dar.<br/>                                                             |
| [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)                   | Instanzklasse<br/> Stellt Informationen dar, die das Routing von Netzwerkdatenpaketen steuern.<br/>                    |
| [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)         | Ereignisklasse<br/> Stellt IP-Routenänderungsereignisse dar.<br/>                                                             |
| [**Win32 \_ NetworkClient**](win32-networkclient.md)                              | Instanzklasse<br/> Stellt einen Netzwerkclient auf einem Computersystem dar, auf dem Windows.<br/>                           |
| [**Win32 \_ NetworkConnection**](win32-networkconnection.md)                      | Instanzklasse<br/> Stellt eine aktive Netzwerkverbindung in einer Windows dar.<br/>                           |
| [**Win32 \_ NetworkProtocol**](win32-networkprotocol.md)                          | Instanzklasse<br/> Stellt ein Protokoll und seine Netzwerkmerkmale auf einem Computersystem dar, auf dem Windows.<br/> |
| [**Win32 \_ NTDomain**](/previous-versions/windows/desktop/cimwin32a/win32-ntdomain)                                        | Instanzklasse<br/> Stellt eine Windows NT-Domäne dar.<br/>                                                             |
| [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)                               | Instanzklasse<br/> Stellt die Vom **Standard-Pingbefehl zurückgegebenen Werte** dar.<br/>                            |
| [**\_Win32-Protokollbindung**](win32-protocolbinding.md)                          | Association-Klasse<br/> Bezieht einen Treiber, ein Netzwerkprotokoll und einen Netzwerkadapter auf Systemebene.<br/>                    |



 

## <a name="operating-system-events"></a>Betriebssystemereignisse

Die Unterkategorie Betriebssystemereignisse gruppen Klassen, die Ereignisse im Betriebssystem darstellen, die sich auf Prozesse, Threads und das Herunterfahren des Systems bezieht.



| Klasse                                                                                 | Beschreibung                                                                                                                                                              |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ComputerShutdownEvent**](/previous-versions/windows/desktop/cimwin32a/win32-computershutdownevent)                   | Ereignisklasse<br/> Stellt Ereignisse zum Herunterfahren von Computern dar.<br/>                                                                                                   |
| [**Win32 \_ ComputerSystemEvent**](/previous-versions/windows/desktop/cimwin32a/win32-computersystemevent)                       | Ereignisklasse<br/> Stellt Ereignisse dar, die mit einem Computersystem verknüpft sind.<br/>                                                                                        |
| [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)                           | Ereignisklasse<br/> Stellt Geräteänderungsereignisse dar, die sich aus dem Additions-, Entfernungs- oder Änderungswechsel von Geräten auf dem Computersystem ergeben.<br/>               |
| [**Win32 \_ ModuleLoadTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduleloadtrace)                               | Ereignisklasse<br/> Gibt an, dass ein Prozess ein neues Modul geladen hat.<br/>                                                                                      |
| [**Win32 \_ ModuleTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduletrace)                                       | Ereignisklasse<br/> Basisereignis für Modulereignisse.<br/>                                                                                                          |
| [**Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace)                           | Ereignisklasse<br/> Gibt an, dass ein neuer Prozess gestartet wurde.<br/>                                                                                              |
| [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace)                             | Ereignisklasse<br/> Gibt an, dass ein Prozess beendet wurde.<br/>                                                                                               |
| [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace)                                     | Ereignisklasse<br/> Basisereignis für Prozessereignisse.<br/>                                                                                                         |
| [**Win32 \_ SystemConfigurationChangeEvent**](win32-systemconfigurationchangeevent.md) | Ereignisklasse<br/> Gibt an, dass die Geräteliste auf dem System aktualisiert wurde (ein Gerät wurde hinzugefügt oder entfernt oder die Konfiguration geändert).<br/>    |
| [**Win32 \_ SystemTrace**](/previous-versions/windows/desktop/krnlprov/win32-systemtrace)                                       | Ereignisklasse<br/> Basisklasse für alle Systemablaufverfolgungsereignisse, einschließlich Modul-, Prozess- und Threadablaufverfolgungen.<br/>                                                  |
| [**Win32 \_ ThreadStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstarttrace)                             | Ereignisklasse<br/> Gibt an, dass ein neuer Thread gestartet wurde.<br/>                                                                                                    |
| [**Win32 \_ ThreadStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstoptrace)                               | Ereignisklasse<br/> Gibt an, dass ein Thread beendet wurde.<br/>                                                                                                   |
| [**Win32 \_ ThreadTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadtrace)                                       | Ereignisklasse<br/> Basisereignisklasse für Threadereignisse.<br/>                                                                                                    |
| [**Win32 \_ VolumeChangeEvent**](win32-volumechangeevent.md)                           | Ereignisklasse<br/> Stellt ein ereignisbasiertes Netzwerklaufwerk dar, das sich aus dem Hinzufügen eines Netzlaufwerkbuchstabens oder bereitgestellten Laufwerks auf dem Computersystem ergibt.<br/> |



 

## <a name="operating-system-settings"></a>Betriebssystemeinstellungen

Das Betriebssystem Einstellungen Unterkategorie gruppiert Klassen, die das Betriebssystem und seine Einstellungen darstellen.



| Klasse                                                                                       | Beschreibung                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ BootConfiguration**](win32-bootconfiguration.md)                                 | Instanzklasse<br/> Stellt die Startkonfiguration eines Computersystems dar, auf dem Windows ausgeführt wird.<br/>                                                                       |
| [**Win32 \_ ComputerSystem**](win32-computersystem.md)                                       | Instanzklasse<br/> Stellt ein Computersystem dar, das in einer Windows-Umgebung betrieben wird.<br/>                                                                              |
| [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md)                     | Association-Klasse<br/> Bezieht sich auf ein Computersystem und einen Prozessor, der auf diesem System ausgeführt wird.<br/>                                                                          |
| [**Win32 \_ ComputerSystemProduct**](win32-computersystemproduct.md)                         | Instanzklasse<br/> Stellt ein Produkt dar.<br/>                                                                                                                         |
| [**Win32 \_ DependentService**](win32-dependentservice.md)                                   | Association-Klasse<br/> Verknüpft zwei voneinander abhängige Basisdienste.<br/>                                                                                                  |
| [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md)                                       | Instanzklasse<br/> Stellt eine Gruppe von Systemdiensten dar, die Ausführungsabhängigkeiten definieren.<br/>                                                                     |
| [**Win32 \_ LoadOrderGroupServiceDependencies**](win32-loadordergroupservicedependencies.md) | Instanzklasse<br/> Stellt eine Zuordnung zwischen einem Basisdienst und einer Lastreihenfolgegruppe dar, von der der Dienst abhängt, um mit der Ausführung zu beginnen.<br/>                         |
| [**Win32 \_ LoadOrderGroupServiceMembers**](win32-loadordergroupservicemembers.md)           | Association-Klasse<br/> Verknüpft eine Lastreihenfolgegruppe und einen Basisdienst.<br/>                                                                                             |
| [**Win32 \_ OperatingSystem**](win32-operatingsystem.md)                                     | Instanzklasse<br/> Stellt ein Betriebssystem dar, das auf einem Computersystem installiert ist, auf dem Windows ausgeführt wird.<br/>                                                                |
| [**Win32 \_ OperatingSystem RADIALE**](win32-operatingsystemqfe.md)                               | Association-Klasse<br/> Verknüpft ein Betriebssystem und Produktupdates, die wie in [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md)dargestellt angewendet werden.<br/> |
| [**Win32 \_ OSRecoveryConfiguration**](win32-osrecoveryconfiguration.md)                     | Instanzklasse<br/> Stellt die Informationstypen dar, die aus dem Arbeitsspeicher gesammelt werden, wenn das Betriebssystem ausfällt.<br/>                                        |
| [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md)                             | Instanzklasse<br/> Stellt systemweite schnelle Problembehebung Engineering (QFE) oder Updates dar, die auf das aktuelle Betriebssystem angewendet wurden.<br/>                         |
| [**Win32 \_ StartupCommand**](win32-startupcommand.md)                                       | Instanzklasse<br/> Stellt einen Befehl dar, der automatisch ausgeführt wird, wenn sich ein Benutzer beim Computersystem anmeldet.<br/>                                                       |
| [**Win32 \_ SystemBootConfiguration**](win32-systembootconfiguration.md)                     | Association-Klasse<br/> Verknüpft ein Computersystem mit seiner Startkonfiguration.<br/>                                                                                      |
| [**Win32 \_ SystemDesktop**](win32-systemdesktop.md)                                         | Association-Klasse<br/> Verknüpft ein Computersystem mit seiner Desktopkonfiguration.<br/>                                                                                   |
| [**Win32 \_ SystemDevices**](win32-systemdevices.md)                                         | Association-Klasse<br/> Verknüpft ein Computersystem und ein auf diesem System installiertes logisches Gerät.<br/>                                                                   |
| [**Win32 \_ SystemLoadOrderGroups**](win32-systemloadordergroups.md)                         | Association-Klasse<br/> Verknüpft ein Computersystem und eine Lastreihenfolgegruppe.<br/>                                                                                          |
| [**Win32 \_ SystemNetworkConnections**](win32-systemnetworkconnections.md)                   | Association-Klasse<br/> Bezieht sich auf eine Netzwerkverbindung und das Computersystem, auf dem sie sich befindet.<br/>                                                                  |
| [**Win32 \_ SystemOperatingSystem**](win32-systemoperatingsystem.md)                         | Association-Klasse<br/> Bezieht sich auf ein Computersystem und sein Betriebssystem.<br/>                                                                                        |
| [**Win32 \_ SystemProcesses**](win32-systemprocesses.md)                                     | Association-Klasse <br/> Verknüpft ein Computersystem und einen Prozess, der auf diesem System ausgeführt wird.<br/>                                                                           |
| [**Win32 \_ SystemProgramGroups**](win32-systemprogramgroups.md)                             | Association-Klasse<br/> Verknüpft ein Computersystem und eine logische Programmgruppe.<br/>                                                                                     |
| [**Win32 \_ SystemResources**](win32-systemresources.md)                                     | Association-Klasse<br/> Verknüpft eine Systemressource mit dem Computersystem, auf dem sie sich befindet.<br/>                                                                           |
| [**Win32 \_ SystemServices**](win32-systemservices.md)                                       | Association-Klasse<br/> Verknüpft ein Computersystem und ein Dienstprogramm, das auf dem System vorhanden ist.<br/>                                                                 |
| [**Win32 \_ SystemSetting**](win32-systemsetting.md)                                         | Association-Klasse<br/> Bezieht sich auf ein Computersystem und eine allgemeine Einstellung auf diesem System.<br/>                                                                            |
| [**Win32 \_ SystemSystemDriver**](win32-systemsystemdriver.md)                               | Association-Klasse<br/> Bezieht sich auf ein Computersystem und einen auf diesem Computersystem ausgeführten Systemtreiber.<br/>                                                             |
| [**Win32 \_ SystemTimeZone**](win32-systemtimezone.md)                                       | Association-Klasse<br/> Verknüpft ein Computersystem und eine Zeitzone.<br/>                                                                                                 |
| [**Win32 \_ SystemUsers**](win32-systemusers.md)                                             | Association-Klasse<br/> Bezieht sich auf ein Computersystem und ein Benutzerkonto auf diesem System.<br/>                                                                               |



 

## <a name="processes"></a>Prozesse

Die Unterkategorie Prozesse gruppiert Klassen, die Systemprozesse und Threads darstellen.



| Klasse                                                 | Beschreibung                                                                                                     |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**\_Win32-Prozess**](win32-process.md)               | Instanzklasse<br/> Stellt eine Sequenz von Ereignissen auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>      |
| [**\_Win32-ProzessStartup**](win32-processstartup.md) | Instanzklasse<br/> Stellt die Startkonfiguration eines Computersystems dar, auf dem Windows ausgeführt wird.<br/> |
| [**\_Win32-Thread**](win32-thread.md)                 | Instanzklasse<br/> Stellt einen Ausführungsthread dar.<br/>                                          |



 

## <a name="registry"></a>Registrierung

Die -Klasse in der Registrierungsunterkategorie stellt den Inhalt der Windows Registrierung dar.



| Klasse                                     | Beschreibung                                                                                               |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**\_Win32-Registrierung**](win32-registry.md) | Instanzklasse<br/> Stellt die Systemregistrierung auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/> |



 

## <a name="scheduler-jobs"></a>Scheduler-Aufträge

Die Unterkategorie Scheduleraufträge gruppiert Klassen, die einstellungen für geplante Aufträge darstellen.



| Klasse                                                | Beschreibung                                                                                                                                                                                                                                                           |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) | Abstrakte Klasse<br/> Stellt eine -Instanz in Zeit als Komponentensekunden, Minuten, Wochentag usw. dar.<br/>                                                                                                                                        |
| [**Win32 \_ ScheduledJob**](win32-scheduledjob.md)    | Instanzklasse<br/> Stellt einen Auftrag dar, der mithilfe des Windows Zeitplandiensts geplant wurde.<br/>                                                                                                                                                                   |
| [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)     | Instanzklasse<br/> Stellt einen Zeitpunkt dar, der als [**Win32 \_ LocalTime-Objekte**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) zurückgegeben wird, die sich aus einer Abfrage ergeben. Die **Hour-Eigenschaft** wird als Ortszeit in einer 24-Stunden-Zeit zurückgegeben.<br/>                                |
| [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)         | Instanzklasse<br/> Stellt einen Zeitpunkt dar, der als [**Win32 \_ UTCTime-Objekte**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) zurückgegeben wird, die sich aus einer Abfrage ergeben. Die **Hour-Eigenschaft** wird als UTC-Zeit (Coordinated Universal Time) in einer Uhrzeit von 24 Stunden zurückgegeben.<br/> |



 

## <a name="security"></a>Sicherheit

Die Unterkategorie Sicherheit gruppiert Klassen, die Systemsicherheitseinstellungen darstellen.



| Klasse                                                                               | Beschreibung                                                                                                                                                  |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ AccountSID**](/previous-versions/windows/desktop/secrcw32prov/win32-accountsid)                                       | Association-Klasse<br/> Verknüpft eine Sicherheitskontoinstanz mit einer Sicherheitsdeskriptorinstanz.<br/>                                             |
| [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)                                                     | Instanzklasse<br/> Stellt einen Zugriffssteuerungseintrag (ACE) dar.<br/>                                                                               |
| [**Win32 \_ LogicalFileAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileaccess)                         | Association-Klasse<br/> Verknüpft die Sicherheitseinstellungen einer Datei oder eines Verzeichnisses mit einem Mitglied der dacl (Discretionary Access Control List).<br/> |
| [**Win32 \_ LogicalFileAuditing**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileauditing)                     | Association-Klasse<br/> Verknüpft die Sicherheitseinstellungen einer Datei oder eines Verzeichnisses mit einem Mitglied der Systemzugriffssteuerungsliste (SACL).<br/>            |
| [**Win32 \_ LogicalFileGroup**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilegroup)                           | Association-Klasse<br/> Verknüpft die Sicherheitseinstellungen einer Datei oder eines Verzeichnisses mit ihrer Gruppe.<br/>                                                  |
| [**Win32 \_ LogicalFileOwner**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileowner)                           | Association-Klasse<br/> Verknüpft die Sicherheitseinstellungen einer Datei oder eines Verzeichnisses mit ihrem Besitzer.<br/>                                                  |
| [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)       | Instanzklasse<br/> Stellt Sicherheitseinstellungen für eine logische Datei dar.<br/>                                                                        |
| [**Win32 \_ LogicalShareAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareaccess)                       | Association-Klasse<br/> Verknüpft die Sicherheitseinstellungen einer Freigabe und eines Mitglieds ihrer DACL.<br/>                                                 |
| [**Win32 \_ LogicalShareAuditing**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareauditing)                   | Association-Klasse<br/> Verknüpft die Sicherheitseinstellungen einer Freigabe und eines Mitglieds der SACL.<br/>                                                 |
| [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting)     | Instanzklasse<br/> Stellt Sicherheitseinstellungen für eine logische Datei dar.<br/>                                                                        |
| [**Win32 \_ PrivilegesStatus**](win32-privilegesstatus.md)                           | Instanzklasse<br/> Stellt Informationen zu den Berechtigungen dar, die zum Abschließen eines Vorgangs erforderlich sind.<br/>                                          |
| [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)                       | Instanzklasse<br/> Stellt eine strukturelle Darstellung eines [**SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)dar.<br/>                   |
| [**Win32 \_ SecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysetting)                             | Instanzklasse<br/> Stellt Sicherheitseinstellungen für ein verwaltetes Element dar.<br/>                                                                     |
| [**Win32 \_ SecuritySettingAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingaccess)                 | Instanzklasse<br/> Stellt die Rechte dar, die einem Vertrauensnehmer für ein bestimmtes Objekt gewährt und verweigert werden.<br/>                                               |
| [**Win32 \_ SecuritySettingAuditing**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingauditing)             | Instanzklasse<br/> Stellt die Überwachung für einen angegebenen Vertrauensnehmer für ein angegebenes -Objekt dar.<br/>                                                          |
| [**Win32 \_ SecuritySettingGroup**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettinggroup)                   | Association-Klasse<br/> Verknüpft die Sicherheit eines Objekts und seiner Gruppe.<br/>                                                                     |
| [**Win32 \_ SecuritySettingOfLogicalFile**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalfile)   | Instanzklasse<br/> Stellt Sicherheitseinstellungen eines Datei- oder Verzeichnisobjekts dar.<br/>                                                             |
| [**Win32 \_ SecuritySettingOfLogicalShare**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalshare) | Instanzklasse<br/> Stellt Sicherheitseinstellungen eines freigegebenen -Objekts dar.<br/>                                                                        |
| [**Win32 \_ SecuritySettingOfObject**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingofobject)             | Association-Klasse<br/> Verknüpft ein Objekt mit seinen Sicherheitseinstellungen.<br/>                                                                          |
| [**Win32 \_ SecuritySettingOwner**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingowner)                   | Association-Klasse<br/> Bezieht die Sicherheitseinstellungen eines Objekts und seines Besitzers.<br/>                                                            |
| [**Win32-SID \_**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)                                                     | Instanzklasse<br/> Stellt eine beliebige SID dar.<br/>                                                                                            |
| [**Win32-Vertrauenshänder \_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)                                             | Instanzklasse<br/> Stellt einen Vertrauenshänder dar.<br/>                                                                                                   |



 

## <a name="services"></a>Dienste

Die Unterkategorie Dienste gruppen Klassen, die Dienste und Basisdienste darstellen.



| Klasse                                           | Beschreibung                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ BaseService**](win32-baseservice.md) | Instanzklasse<br/> Stellt ausführbare Objekte dar, die in einer vom Dienststeuerungs-Manager verwalteten Registrierungsdatenbank installiert werden.<br/> |
| [**Win32-Dienst \_**](win32-service.md)         | Instanzklasse<br/> Stellt einen Dienst auf einem Computersystem dar, auf dem Windows.<br/>                                                         |



 

## <a name="shares"></a>Freigaben

Die Unterkategorie Freigaben gruppen Klassen, die Details zu freigegebenen Ressourcen wie Druckern und Ordnern darstellen.



| Klasse                                                       | Beschreibung                                                                                                                                                                                          |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DFSNode**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnode)                     | Association-Klasse<br/> Stellt einen Stamm- oder Verbindungsknoten eines domänenbasierten oder eigenständigen verteilten Dateisystems (DFS) dar.<br/>                                                           |
| [**Win32 \_ DFSNodeTarget**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnodetarget)         | Association-Klasse<br/> Stellt die Beziehung eines DFS-Knotens zu einem seiner Ziele dar.<br/>                                                                                             |
| [**Win32 \_ DFSTarget**](/previous-versions/windows/desktop/wmipdfs/win32-dfstarget)                 | Association-Klasse<br/> Stellt das Ziel eines DFS-Knotens dar.<br/>                                                                                                                         |
| [**Win32 \_ ServerConnection**](/previous-versions/windows/desktop/wmipsess/win32-serverconnection)   | Instanzklasse<br/> Stellt die Verbindungen dar, die von einem Remotecomputer mit einer freigegebenen Ressource auf dem lokalen Computer hergestellt werden.<br/>                                                              |
| [**Win32 \_ ServerSession**](/previous-versions/windows/desktop/wmipsess/win32-serversession)         | Instanzklasse<br/> Stellt die Sitzungen dar, die von Benutzern auf einem Remotecomputer mit dem lokalen Computer eingerichtet werden.<br/>                                                             |
| [**Win32 \_ ConnectionShare**](/previous-versions/windows/desktop/wmipsess/win32-connectionshare)     | Association-Klasse<br/> Bezieht eine freigegebene Ressource auf dem Computer und die Verbindung mit der freigegebenen Ressource.<br/>                                                                    |
| [**Win32 \_ PrinterShare**](win32-printershare.md)           | Association-Klasse<br/> Bezieht einen lokalen Drucker und die Freigabe, die ihn darstellt, während er über ein Netzwerk angezeigt wird.<br/>                                                                     |
| [**Win32 \_ SessionConnection**](/previous-versions/windows/desktop/wmipsess/win32-sessionconnection) | Association-Klasse<br/> Stellt eine Zuordnung zwischen einer Sitzung, die von einem Benutzer auf einem Remotecomputer mit dem lokalen Server eingerichtet wurde, und den Verbindungen dar, die von der Sitzung abhängen.<br/> |
| [**Win32 \_ SessionProcess**](win32-sessionprocess.md)       | Association-Klasse<br/> Stellt eine Zuordnung zwischen einer Anmeldesitzung und den Prozessen dar, die dieser Sitzung zugeordnet sind.<br/>                                                            |
| [**Win32 \_ ShareToDirectory**](win32-sharetodirectory.md)   | Association-Klasse<br/> Bezieht eine freigegebene Ressource auf dem Computersystem und das Verzeichnis, dem sie zugeordnet ist.<br/>                                                                    |
| [**Win32-Freigabe \_**](win32-share.md)                         | Instanzklasse<br/> Stellt eine freigegebene Ressource auf einem Computersystem dar, auf dem Windows.<br/>                                                                                              |



 

## <a name="start-menu"></a>Startmenü

Die Unterkategorie Startmenü gruppen Klassen, die Programmgruppen darstellen.



| Klasse                                                                                   | Beschreibung                                                                                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ LogicalProgramGroup**](win32-logicalprogramgroup.md)                         | Instanzklasse<br/> Stellt eine Programmgruppe in einem Computersystem dar, auf dem Windows.<br/>                                                                    |
| [**Win32 \_ LogicalProgramGroupDirectory**](win32-logicalprogramgroupdirectory.md)       | Association-Klasse<br/> Bezieht logische Programmgruppen (Gruppierungen im Startmenü) und die Dateiverzeichnisse, in denen sie gespeichert sind.<br/>                 |
| [**Win32 \_ LogicalProgramGroupItem**](win32-logicalprogramgroupitem.md)                 | Instanzklasse<br/> Stellt ein Element dar, das in einer **Win32 \_ ProgramGroup-Instanz** enthalten ist, die selbst keine **andere Win32 \_ ProgramGroup-Instanz** ist.<br/> |
| [**Win32 \_ LogicalProgramGroupItemDataFile**](win32-logicalprogramgroupitemdatafile.md) | Association-Klasse<br/> Bezieht die Programmgruppenelemente der Startmenü und die Dateien, in denen sie gespeichert sind.<br/>                                       |
| [**Win32 \_ ProgramGroupContents**](win32-programgroupcontents.md)                       | Association-Klasse<br/> Bezieht eine Programmgruppenbestellung und eine einzelne darin enthaltene Programmgruppe oder ein element.<br/>                                           |
| [**Win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md)                           | Instanzklasse<br/> Stellt eine logische Gruppierung von Programmen im Menü **Startprogramme** \| **des Benutzers** dar.<br/>                                               |



 

## <a name="storage"></a>Storage

Die Unterkategorie Users (Benutzer) gruppen Klassen, die Speicherinformationen darstellen.



| Klasse                                                                   | Beschreibung                                                                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ShadowBy**](/previous-versions/windows/desktop/vsswmi/win32-shadowby)                               | Association-Klasse<br/> Stellt die Zuordnung zwischen einer Schattenkopie und dem Anbieter dar, der die Schattenkopie erstellt.<br/>      |
| [**Win32 \_ ShadowContext**](/previous-versions/windows/desktop/vsswmi/win32-shadowcontext)                     | Association-Klasse<br/> Gibt an, wie eine Schattenkopie erstellt, abgefragt oder gelöscht werden soll.<br/>                                   |
| [**Win32 \_ ShadowCopy**](/previous-versions/windows/desktop/legacy/aa394428(v=vs.85))                           | Instanzklasse<br/> Stellt eine doppelte Kopie des ursprünglichen Volumes zu einem früheren Zeitpunkt dar.<br/>                                  |
| [**Win32 \_ ShadowDiffVolumeSupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowdiffvolumesupport) | Association-Klasse<br/> Stellt eine Zuordnung zwischen einem Schattenkopieanbieter und einem Speichervolumen dar.<br/>                       |
| [**Win32 \_ ShadowFor**](/previous-versions/windows/desktop/vsswmi/win32-shadowfor)                             | Association-Klasse<br/> Stellt eine Zuordnung zwischen einer Schattenkopie und dem Volume dar, für das die Schattenkopie erstellt wird.<br/> |
| [**Win32 \_ ShadowOn**](/previous-versions/windows/desktop/vsswmi/win32-shadowon)                               | Association-Klasse<br/> Stellt eine Zuordnung zwischen einer Schattenkopie und dem Ort dar, an dem die differenziellen Daten geschrieben werden.<br/>          |
| [**Win32 \_ ShadowProvider**](/previous-versions/windows/desktop/vsswmi/win32-shadowprovider)                   | Association-Klasse<br/> Stellt eine Komponente dar, die Volumeschattenkopien erstellt und darstellt.<br/>                             |
| [**Win32 \_ ShadowStorage**](/previous-versions/windows/desktop/legacy/aa394433(v=vs.85))                     | Association-Klasse<br/> Stellt eine Zuordnung zwischen einer Schattenkopie und dem Ort dar, an dem die differenziellen Daten geschrieben werden.<br/>          |
| [**Win32 \_ ShadowVolumeSupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowvolumesupport)         | Association-Klasse<br/> Stellt eine Zuordnung zwischen einem Schattenkopieanbieter und einem unterstützten Volume dar.<br/>                    |
| [**Win32-Volume \_**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                   | Instanzklasse<br/> Stellt einen Speicherbereich auf einer Festplatte dar.<br/>                                                           |
| [**Win32 \_ VolumeUserQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                 | Association-Klasse<br/> Stellt ein Volume für die Kontingenteinstellungen pro Volume dar.<br/>                                                |



 

## <a name="users"></a>Benutzer

Die Unterkategorie Benutzer gruppen Klassen, die Benutzerkontoinformationen darstellen, z. B. Gruppenmitgliedschaftsdetails.



| Klasse                                                                 | Beschreibung                                                                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32-Konto \_**](win32-account.md)                               | Instanzklasse<br/> Stellt Informationen zu Benutzerkonten und Gruppenkonten dar, die dem Computersystem bekannt sind, auf dem Windows.<br/> |
| [**Win32-Gruppe \_**](win32-group.md)                                   | Instanzklasse<br/> Stellt Daten zu einem Gruppenkonto dar.<br/>                                                                      |
| [**Win32 \_ GroupInDomain**](/previous-versions/windows/desktop/cimwin32a/win32-groupindomain)                   | Association-Klasse<br/> Identifiziert die Gruppenkonten, die einer Windows NT-Domäne zugeordnet sind.<br/>                                       |
| [**Win32 \_ GroupUser**](win32-groupuser.md)                           | Association-Klasse<br/> Bezieht eine Gruppe und ein Konto, das Mitglied dieser Gruppe ist.<br/>                                           |
| [**Win32 \_ LogonSession**](win32-logonsession.md)                     | Instanzklasse<br/> Beschreibt die Anmeldesitzung oder -sitzungen, die einem Benutzer zugeordnet sind, der bei der Anmeldung Windows.<br/>                        |
| [**Win32 \_ LogonSessionMappedDisk**](/windows/desktop/CIMWin32Prov/win32-logonsessionmappeddisk) | Instanzklasse<br/> Stellt die zugeordneten logischen Datenträger dar, die der Sitzung zugeordnet sind.<br/>                                            |
| [**Win32 \_ NetworkLoginProfile**](win32-networkloginprofile.md)       | Instanzklasse<br/> Stellt die Netzwerkanmeldungsinformationen eines bestimmten Benutzers auf einem Computersystem dar, auf dem Windows.<br/>           |
| [**Win32 \_ SystemAccount**](win32-systemaccount.md)                   | Instanzklasse<br/> Stellt ein Systemkonto dar.<br/>                                                                                |
| [**Win32 \_ UserAccount**](win32-useraccount.md)                       | Instanzklasse<br/> Stellt Informationen zu einem Benutzerkonto auf einem Computersystem dar, auf dem Windows.<br/>                           |
| [**Win32 \_ UserInDomain**](/previous-versions/windows/desktop/cimwin32a/win32-userindomain)                     | Association-Klasse<br/> Bezieht ein Benutzerkonto und eine Windows NT-Domäne.<br/>                                                          |



 

## <a name="windows-event-log"></a>Windows-Ereignisprotokoll

Die Windows Ereignisprotokoll-Unterkategoriegruppenklassen, die Ereignisse, Ereignisprotokolleinträge, Einstellungen für die Ereignisprotokollkonfiguration und so weiter darstellen.



| Klasse                                                         | Beschreibung                                                                                                                                                                   |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))         | Instanzklasse<br/> Stellt Daten dar, die in einer Windows Ereignisprotokolldatei gespeichert sind.<br/>                                                                                      |
| [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)                 | Instanzklasse<br/> Stellt Windows Ereignisse dar.<br/>                                                                                                               |
| [**Win32 \_ NTLogEventComputer**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventcomputer) | Association-Klasse<br/> Bezieht Instanzen von [**Win32 \_ NTLogEvent und**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) [**Win32 \_ ComputerSystem.**](win32-computersystem.md)<br/>         |
| [**Win32 \_ NTLogEventLog**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventlog)           | Association-Klasse<br/> Bezieht Instanzen der [**Win32 \_ NTLogEvent- und**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) [**Win32 \_ NTEventlogFile-Klassen.**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))<br/> |
| [**Win32 \_ NTLogEventUser**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventuser)         | Association-Klasse<br/> Bezieht Instanzen von [**Win32 \_ NTLogEvent und**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) [**Win32 \_ UserAccount.**](win32-useraccount.md)<br/>               |



 

## <a name="windows-product-activation"></a>Windows Produktaktivierung

Windows Die Produktaktivierung (Product Activation, WPA) ist eine antigrafische Technologie, um das gelegentliche Kopieren von Software zu reduzieren.



| Klasse                                                                                                               | Beschreibung                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ComputerSystemWindowsProductActivationSetting**](/previous-versions/windows/desktop/licwmiprov/win32-computersystemwindowsproductactivationsetting) | Association-Klasse<br/> Bezieht Instanzen von [**Win32 \_ ComputerSystem und**](win32-computersystem.md) [**Win32 \_ WindowsProductActivation auf.**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85))<br/> |
| [**Win32-Proxy \_**](/previous-versions/windows/desktop/legacy/aa394389(v=vs.85))                                                                                 | Instanzklasse<br/> Enthält Eigenschaften und Methoden zum Abfragen und Konfigurieren einer Internetverbindung im Zusammenhang mit WPA.<br/>                                                                |
| [**Win32 \_ WindowsProductActivation**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85))                                           | Instanzklasse<br/> Enthält Eigenschaften und Methoden im Zusammenhang mit WPA.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Win32-Klassen](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

