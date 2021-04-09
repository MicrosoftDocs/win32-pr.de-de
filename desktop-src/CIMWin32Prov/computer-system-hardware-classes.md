---
description: Die Computer System-Hardware Kategorie gruppiert Klassen, die Hardware bezogene Objekte darstellen. Beispiele hierfür sind Eingabegeräte, Festplatten, Erweiterungskarten, Videogeräte, Netzwerkgeräte und die Systemleistung.
ms.assetid: 0b6cb410-166e-45cd-8dca-77a111b3cf62
ms.tgt_platform: multiple
title: Computer System-Hardware Klassen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3681f78d882a3e977b9721bd70f0b852114c257
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958398"
---
# <a name="computer-system-hardware-classes"></a>Computer System-Hardware Klassen

Die Computer System-Hardware Kategorie gruppiert Klassen, die Hardware bezogene Objekte darstellen. Beispiele hierfür sind Eingabegeräte, Festplatten, Erweiterungskarten, Videogeräte, Netzwerkgeräte und die Systemleistung.

-   [Geräteklassen Kühlung](#cooling-device-classes)
-   [Eingabegeräte Klassen](#input-device-classes)
-   [Massenspeicher Klassen](#mass-storage-classes)
-   [Motherboard-, Controller-und Port Klassen](#motherboard-controller-and-port-classes)
-   [Netzwerkgeräte Klassen](#networking-device-classes)
-   [Energieklassen](#power-classes)
-   [Druckklassen](#printing-classes)
-   [Telefonieklassen](#telephony-classes)
-   [Video-und Überwachungs Klassen](#video-and-monitor-classes)
-   [Zugehörige Themen](#related-topics)

## <a name="cooling-device-classes"></a>Geräteklassen Kühlung

Die Unterkategorie Kühlungs Geräte gruppiert Klassen, die instrumentierbare Fans, Temperaturtests und Kühlgeräte darstellen.



| Klasse                                                     | BESCHREIBUNG                                                                 |
|-----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Win32- \_ Lüfter**](win32-fan.md)                           | Stellt die Eigenschaften eines Lüfter-Geräts im Computersystem dar.           |
| [**Win32- \_ Heatpipe**](win32-heatpipe.md)                 | Stellt die Eigenschaften eines wärmepipe-kühl Geräts dar.                    |
| [**Win32- \_ Kühlung**](win32-refrigeration.md)       | Stellt die Eigenschaften eines kühl Geräts dar.                        |
| [**Win32- \_ Temperatur Überprüfung**](win32-temperatureprobe.md) | Stellt die Eigenschaften eines Temperatursensors (elektronisches Thermometer) dar. |



 

## <a name="input-device-classes"></a>Eingabegeräte Klassen

Die Unterkategorie Eingabegeräte gruppiert Klassen, die Tastaturen und Zeigegeräte darstellen.



| Klasse                                                 | BESCHREIBUNG                                                                                                         |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ Tastatur**](win32-keyboard.md)             | Stellt eine Tastatur dar, die auf einem Computersystem mit Windows installiert ist.                                               |
| [**Win32- \_ pointingdevice**](win32-pointingdevice.md) | Stellt ein Eingabegerät dar, das verwendet wird, um auf die Anzeige eines Computer Systems, auf dem Windows ausgeführt wird, zu zeigen. |



 

## <a name="mass-storage-classes"></a>Massenspeicher Klassen

Klassen in der Unterkategorie Massenspeicher stellen Speichergeräte wie Festplattenlaufwerke, CD-ROM-Laufwerke und Bandlaufwerke dar.



| Klasse                                                     | BESCHREIBUNG                                                                                  |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**Win32 \_ autochksetting**](win32-autochksetting.md)     | Stellt die Einstellungen für den AutoCheck-Vorgang eines Datenträgers dar.                               |
| [**Win32- \_ cdromdrive**](win32-cdromdrive.md)             | Stellt ein CD-ROM-Laufwerk auf einem Computersystem dar, auf dem Windows ausgeführt wird.                              |
| [**Win32- \_ diskdrive**](win32-diskdrive.md)               | Stellt ein physisches Laufwerk dar, das auf einem Computer mit dem Windows-Betriebssystem angezeigt wird. |
| [**Win32 \_ floppydrive**](win32-floppydrive.md)           | Verwaltet die Funktionen eines Disketten Laufwerks.                                             |
| [**Win32- \_ physicalmedia**](/previous-versions/windows/desktop/cimwin32a/win32-physicalmedia) | Stellt eine beliebige Art von Dokumentation oder Speichermedium dar.                                      |
| [**Win32- \_ TapeDrive**](win32-tapedrive.md)               | Stellt ein Bandlaufwerk auf einem Computersystem dar, auf dem Windows ausgeführt wird.                                |



 

## <a name="motherboard-controller-and-port-classes"></a>Motherboard-, Controller-und Port Klassen

In den Unterkategorien von Motherboard, Controllern und Ports werden Klassen gruppiert, die Systemgeräte darstellen. Beispiele hierfür sind System Arbeitsspeicher, Cache Speicher und Controller.



| Klasse                                                                       | BESCHREIBUNG                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32-Test \_ Controller**](win32-1394controller.md)                       | Stellt die Funktionen und die Verwaltung eines 1394-Controllers dar.<br/>                                                                                                                                               |
| [**Win32-" \_ 1394controllerdevice"**](win32-1394controllerdevice.md)           | Verknüpft den Hochleistungs-und den High-Speed-seriellem Buscontroller (IEEE 1394 FireWire) und die Verbindung mit der [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Instanz.<br/>                                                            |
| [**Win32- \_ Verteilungs Quelle**](win32-allocatedresource.md)                 | Ordnet ein logisches Gerät mit einer System Ressource in Beziehung.<br/>                                                                                                                                                                 |
| [**Win32 \_ associatedprocessormemory**](win32-associatedprocessormemory.md) | Verknüpft einen Prozessor und den zugehörigen Cache Speicher.<br/>                                                                                                                                                                      |
| [**Win32- \_ Baseboard**](win32-baseboard.md)                                 | Stellt ein Baseboard dar (auch als "Motherboard" oder "System Board" bezeichnet).<br/>                                                                                                                                          |
| [**Win32- \_ BIOS**](win32-bios.md)                                           | Stellt die Attribute der grundlegenden Eingabe-oder Ausgabe Dienste (BIOS) des Computer Systems dar, die auf dem Computer installiert sind.<br/>                                                                                   |
| [**Win32- \_ Bus**](win32-bus.md)                                             | Stellt einen physischen Bus dar, der in einem Windows-Betriebssystem angezeigt wird.<br/>                                                                                                                                               |
| [**Win32- \_ CacheMemory**](win32-cachememory.md)                             | Stellt den Cache Speicher (intern und extern) auf einem Computersystem dar.<br/>                                                                                                                                          |
| [**Win32- \_ controllerhashub**](/previous-versions/windows/desktop/cimwin32a/win32-controllerhashub)             | Stellt die nachgelagerten Hubs vom USB-Controller (Universal Serial Bus) dar.<br/>                                                                                                                                 |
| [**Win32- \_ devicebus**](win32-devicebus.md)                                 | Verknüpft einen Systembus und ein logisches Gerät mithilfe des Busses.<br/>                                                                                                                                                       |
| [**Win32 \_ devicememoryaddress**](win32-devicememoryaddress.md)             | Stellt eine Gerätespeicher Adresse in einem Windows-System dar.<br/>                                                                                                                                                        |
| [**Win32-Geräte-Manager \_**](win32-devicesettings.md)                       | Verknüpft ein logisches Gerät und eine Einstellung, die darauf angewendet werden können.<br/>                                                                                                                                              |
| [**Win32- \_ dmachannel**](win32-dmachannel.md)                               | Stellt einen DMA-Kanal (Direct Memory Access) auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                          |
| [**Win32- \_ Floppycontroller**](win32-floppycontroller.md)                   | Stellt die Funktionen und die Verwaltungskapazität eines Disketten Laufwerks Controllers dar.<br/>                                                                                                                         |
| [**Win32- \_ idecontroller**](win32-idecontroller.md)                         | Stellt die Funktionen eines IDE-Controller Geräts (Integrated Drive Electronics) dar.<br/>                                                                                                                        |
| [**Win32- \_ idecontrollerdevice**](win32-idecontrollerdevice.md)             | Association-Klasse, die einen IDE-Controller und das logische Gerät verknüpft.<br/>                                                                                                                                       |
| [**Win32-" \_ infrareddevice"**](win32-infrareddevice.md)                       | Stellt die Funktionen und die Verwaltung eines Infrarot Geräts dar.<br/>                                                                                                                                              |
| [**Win32-Webressource \_**](win32-irqresource.md)                             | Stellt eine Anzahl von Interrupt-Anforderungs Zeilen (UNQ) auf einem Windows-Computersystem dar.<br/>                                                                                                                                |
| [**Win32- \_ memoryarray**](win32-memoryarray.md)                             | Stellt die Eigenschaften des Computersystem-Speicherarrays und der zugeordneten Adressen dar.<br/>                                                                                                                            |
| [**Win32 \_ memoryarraylocation**](win32-memoryarraylocation.md)             | Verknüpft ein logisches Speicher Array und das physische Speicher Array, auf dem es vorhanden ist.<br/>                                                                                                                             |
| [**Win32- \_ memorydevice**](win32-memorydevice.md)                           | Stellt die Eigenschaften des Speichergeräts eines Computer Systems zusammen mit den zugeordneten zugeordneten Adressen dar.<br/>                                                                                                     |
| [**Win32 \_ memorydevicearray**](win32-memorydevicearray.md)                 | Verknüpft ein Speichergerät und das Speicher Array, in dem es sich befindet.<br/>                                                                                                                                              |
| [**Win32 \_ memorydevicelokation**](win32-memorydevicelocation.md)           | Zuordnungs Klasse, die ein Speichergerät und den physischen Speicher, in dem es vorhanden ist, verknüpft.<br/>                                                                                                                     |
| [**Win32- \_ motherboardgerät**](win32-motherboarddevice.md)                 | Stellt ein Gerät dar, das die zentralen Komponenten des Computer Systems enthält, auf dem Windows ausgeführt wird.<br/>                                                                                                               |
| [**Win32- \_ onboarddevice**](win32-onboarddevice.md)                         | Stellt allgemeine Adapter Geräte dar, die in die Hauptplatine (System Platine) integriert sind.<br/>                                                                                                                                   |
| [**Win32- \_ Parallelport**](win32-parallelport.md)                           | Stellt die Eigenschaften eines parallelen Ports auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                             |
| [**Win32- \_ PCMCIAController**](win32-pcmciacontroller.md)                   | Dient zum Verwalten der Funktionen eines Geräteschnittstellen Adapters (PCMCIA)-Controller Geräts für PCs.<br/>                                                                                                      |
| [**Win32- \_ PhysicalMemory**](win32-physicalmemory.md)                       | Stellt ein physisches Speichergerät dar, das sich auf einem Computer befindet, der für das Betriebssystem verfügbar ist.<br/>                                                                                                                |
| [**Win32 \_ physicalmemoryarray**](win32-physicalmemoryarray.md)             | Stellt Details zum physischen Arbeitsspeicher des Computer Systems dar.<br/>                                                                                                                                                |
| [**Win32 \_ physicalmemorylocation**](win32-physicalmemorylocation.md)       | Ordnet ein Array von physischem Speicher und dessen physischem Arbeitsspeicher in Beziehung.<br/>                                                                                                                                                   |
| [**Win32- \_ pnpallocatedresource**](win32-pnpallocatedresource.md)           | Stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar.<br/>                                                                                                                                        |
| [**Win32- \_ pnpdevice**](win32-pnpdevice.md)                                 | Verknüpft ein Gerät (Configuration Manager bekannt als pnptity) und die Funktion, die es ausführt.<br/>                                                                                                                |
| [**Win32- \_ pnptity**](win32-pnpentity.md)                                 | Stellt die Eigenschaften eines Plug & Play Geräts dar.<br/>                                                                                                                                                           |
| [**Win32- \_ portconnector**](win32-portconnector.md)                         | Stellt physische Verbindungsports dar, z. b. DB-25 Pin männlich, Centronics und PS/2.<br/>                                                                                                                            |
| [**Win32- \_ portresource**](win32-portresource.md)                           | Stellt einen I/O-Port auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                                                   |
| [**Win32- \_ Prozessor**](win32-processor.md)                                 | Stellt ein Gerät dar, das eine Sequenz von Computeranweisungen auf einem Computersystem interpretieren können, auf dem Windows ausgeführt wird.<br/>                                                                                           |
| [**Win32- \_ SCSIController**](win32-scsicontroller.md)                       | Stellt einen SCSI-Controller (Small Computersystem Interface) auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                           |
| [**Win32- \_ scsicontrollerdevice**](win32-scsicontrollerdevice.md)           | Verknüpft einen SCSI-Controller und das logische Gerät (Laufwerk), das mit ihm verbunden ist.<br/>                                                                                                                                 |
| [**Win32- \_ SerialPort**](win32-serialport.md)                               | Stellt einen seriellen Anschluss auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                                                 |
| [**Win32- \_ serialportconfiguration**](win32-serialportconfiguration.md)     | Stellt die Einstellungen für die Datenübertragung an einem seriellen Windows-Port dar.<br/>                                                                                                                                        |
| [**Win32- \_ serialportsetting**](win32-serialportsetting.md)                 | Ordnet einen seriellen Anschluss und seine Konfigurationseinstellungen in Beziehung.<br/>                                                                                                                                                          |
| [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)                           | Stellt die Funktionen und die Verwaltung von speicherbezogenen logischen Geräten dar.<br/>                                                                                                                                  |
| [**Win32- \_ Soundgerät**](win32-sounddevice.md)                             | Stellt die Eigenschaften eines Audiogeräts auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                              |
| [**Win32- \_ Systembios**](win32-systembios.md)                               | Bezieht ein Computersystem (einschließlich Daten wie Starteigenschaften, Zeitzonen, Start Konfigurationen oder Administrator Kennwörter) und ein System-BIOS (Dienste, Sprachen und System Verwaltungs Eigenschaften) in Beziehung.<br/> |
| [**Win32 \_ systemdriverpnptity**](win32-systemdriverpnpentity.md)         | In wird ein Plug & Play Gerät im Windows-Computersystem und der Treiber, der das Plug & Play Gerät unterstützt, in Beziehung gesetzt.<br/>                                                                                           |
| [**Win32- \_ Systemgehäuse**](win32-systemenclosure.md)                     | Stellt die einem physischen Systemgehäuse zugeordneten Eigenschaften dar.<br/>                                                                                                                                         |
| [**Win32 \_ systemmemoryresource**](win32-systemmemoryresource.md)           | Stellt eine Systemspeicher Ressource auf einem Windows-System dar.<br/>                                                                                                                                                       |
| [**Win32- \_ Systemslot**](win32-systemslot.md)                               | Stellt physische Verbindungspunkte einschließlich Ports, Motherboard-Slots und Peripheriegeräte sowie proprietäre Verbindungspunkte dar.<br/>                                                                                  |
| [**Win32-Start \_ Controller**](win32-usbcontroller.md)                         | Verwaltet die Funktionen eines USB-Controllers (Universal Serial Bus).<br/>                                                                                                                                           |
| [**Win32-Start \_ Controller Device**](win32-usbcontrollerdevice.md)             | Ordnet einen USB-Controller und die mit ihm verbundenen [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Instanzen in Beziehung.<br/>                                                                                                    |
| [**Win32-Startseite \_**](/previous-versions/windows/desktop/cimwin32a/win32-usbhub)                                 | Stellt die Verwaltungsmerkmale eines USB-Hubs dar.<br/>                                                                                                                                                        |



 

## <a name="networking-device-classes"></a>Netzwerkgeräte Klassen

Die Unterkategorie Netzwerkgeräte gruppiert Klassen, die den Netzwerkschnittstellen Controller, seine Konfigurationen und seine Einstellungen darstellen.



| Klasse                                                                           | BESCHREIBUNG                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ NetworkAdapter**](win32-networkadapter.md)                           | Stellt einen Netzwerkadapter auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                                          |
| [**Win32 \_ networkadapterconfiguration**](win32-networkadapterconfiguration.md) | Stellt die Attribute und Verhalten eines Netzwerkadapters dar. Es ist nicht garantiert, dass die-Klasse nach der Ratifizierung der DMTF (DMTF) CIM-Netzwerk Spezifikation unterstützt wird.<br/> |
| [**Win32- \_ networkadaptersetting**](win32-networkadaptersetting.md)             | Bezieht einen Netzwerkadapter und seine Konfigurationseinstellungen in Beziehung.<br/>                                                                                                                                                   |



 

## <a name="power-classes"></a>Energieklassen

Die Power SubCategory gruppiert Klassen, die Stromversorgung, Batterien und Ereignisse in Bezug auf diese Geräte darstellen.



| Klasse                                                             | BESCHREIBUNG                                                                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Win32- \_ Akku**](win32-battery.md)                           | Stellt einen Akku dar, der mit dem Computersystem verbunden ist.<br/>                                     |
| [**Win32 \_ currentprobe**](win32-currentprobe.md)                 | Stellt die Eigenschaften eines aktuellen Überwachungs Sensors (Ammeter) dar.<br/>                        |
| [**Win32 \_ portableakku**](win32-portablebattery.md)           | Stellt die Eigenschaften einer portablen Batterie dar, z. b. eine, die für einen Notebook-Computer verwendet wird.<br/> |
| [**Win32- \_ powermanagementevent**](win32-powermanagementevent.md) | Stellt Energie Verwaltungs Ereignisse dar, die sich aus Energie Zustandsänderungen ergeben.<br/>                     |
| [**Win32- \_ voltageprobe**](win32-voltageprobe.md)                 | Stellt die Eigenschaften eines Spannungs Sensors (Electronic Voltmeter) dar.<br/>                      |



 

## <a name="printing-classes"></a>Druckklassen

Die drucksubcategory gruppiert Klassen, die Drucker, Drucker Konfigurationen und Druckaufträge darstellen.



| Klasse                                                             | BESCHREIBUNG                                                                                                                              |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ driverfordevice**](win32-driverfordevice.md)           | Ordnet einen Drucker mit einem Druckertreiber in Beziehung.<br/>                                                                                        |
| [**Win32- \_ Drucker**](win32-printer.md)                           | Stellt ein Gerät dar, das mit einem Computersystem verbunden ist, auf dem Windows ausgeführt wird und das ein visuelles Bild auf einem Medium reproduzieren kann.<br/> |
| [**Win32- \_ printerconfiguration**](win32-printerconfiguration.md) | Definiert die Konfiguration für ein Druckergerät.<br/>                                                                               |
| [**Win32- \_ printercontroller**](win32-printercontroller.md)       | Bezieht einen Drucker und das lokale Gerät, mit dem der Drucker verbunden ist, in Beziehung.<br/>                                                     |
| [**Win32- \_ PrinterDriver**](win32-printerdriver.md)               | Stellt die Treiber für eine [**Win32- \_ Drucker**](win32-printer.md) Instanz dar.<br/>                                                |
| [**Win32 \_ printerdriverdll**](win32-printerdriverdll.md)         | Verknüpft einen lokalen Drucker und seine Treiberdatei (nicht der Treiber selbst).<br/>                                                          |
| [**Win32- \_ Einstellung**](win32-printersetting.md)             | Bezieht einen Drucker und seine Konfigurationseinstellungen in Beziehung.<br/>                                                                             |
| [**Win32- \_ PrintJob**](win32-printjob.md)                         | Stellt einen Druckauftrag dar, der von einer Windows-basierten Anwendung generiert wurde.<br/>                                                              |
| [**Win32- \_ tcpipprinterport**](win32-tcpipprinterport.md)         | Stellt einen TCP/IP-Dienst Zugriffspunkt dar.<br/>                                                                                     |



 

## <a name="telephony-classes"></a>Telefonieklassen

Die telefonieunterkategorie gruppiert Klassen, die "Plain Old Telefon"-Modem Geräte und die zugehörigen seriellen Verbindungen darstellen.



| Klasse                                                               | BESCHREIBUNG                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ potsmodem**](win32-potsmodem.md)                         | Stellt die Dienste und Merkmale eines Modem-Modem (Plain Old Telefon Service) auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/> |
| [**Win32-" \_ potsmudemtoserialport"**](win32-potsmodemtoserialport.md) | Verknüpft ein Modem und den seriellen Anschluss, den das Modem verwendet.<br/>                                                                             |



 

## <a name="video-and-monitor-classes"></a>Video-und Überwachungs Klassen

Die Unterkategorie Video und Monitors gruppiert Klassen, die Monitore, Grafikkarten und die zugehörigen Einstellungen darstellen.



| Klasse                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ Desktop Monitor**](win32-desktopmonitor.md)                                 | Stellt den Typ des Monitors oder des Anzeige Geräts dar, das mit dem Computersystem verbunden ist.<br/>                                                                                                                                                                                                                                                                                       |
| [**Win32 \_ displaycontrollerconfiguration**](win32-displaycontrollerconfiguration.md) | Stellt die Grafikkarten-Konfigurationsinformationen eines Computer Systems dar, auf dem Windows ausgeführt wird. Diese Klasse ist veraltet. Verwenden Sie anstelle dieser Klasse die Eigenschaften in den Klassen [**Win32 \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md)und [CIM \_ videocontrollerresolution](cim-videocontrollerresolution.md) .<br/> |
| [**Win32- \_ Videocontroller**](win32-videocontroller.md)                               | Stellt die Funktionen und die Verwaltungskapazität des Video Controllers auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                                                                                                                                                       |
| [**Win32- \_ Videoeinstellungen**](win32-videosettings.md)                                   | Verknüpft einen Videocontroller und Videoeinstellungen, die darauf angewendet werden können.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Win32-Klassen](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

