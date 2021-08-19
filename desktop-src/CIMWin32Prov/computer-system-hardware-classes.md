---
description: Die Kategorie Hardware des Computersystems unterteilt Klassen, die hardwarebezogene Objekte darstellen. Beispiele hierfür sind Eingabegeräte, Festplatten, Erweiterungskarten, Videogeräte, Netzwerkgeräte und Systemleistung.
ms.assetid: 0b6cb410-166e-45cd-8dca-77a111b3cf62
ms.tgt_platform: multiple
title: Hardwareklassen des Computersystems
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d541071698c08510452faaf6bef0cd706dab66e5eaa77b5db121e522785c5c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420095"
---
# <a name="computer-system-hardware-classes"></a>Hardwareklassen des Computersystems

Die Kategorie Hardware des Computersystems unterteilt Klassen, die hardwarebezogene Objekte darstellen. Beispiele hierfür sind Eingabegeräte, Festplatten, Erweiterungskarten, Videogeräte, Netzwerkgeräte und Systemleistung.

-   [Klassen für Kühlgeräte](#cooling-device-classes)
-   [Eingabegeräteklassen](#input-device-classes)
-   [Massenklassen Storage Massenklassen](#mass-storage-classes)
-   [Hauptplatinen-, Controller- und Portklassen](#motherboard-controller-and-port-classes)
-   [Netzwerkgeräteklassen](#networking-device-classes)
-   [Energieklassen](#power-classes)
-   [Druckklassen](#printing-classes)
-   [Telefonieklassen](#telephony-classes)
-   [Video- und Monitorklassen](#video-and-monitor-classes)
-   [Zugehörige Themen](#related-topics)

## <a name="cooling-device-classes"></a>Klassen für Kühlgeräte

Die Unterkategorie Cooling Devices (Kühlgeräte) gruppen Klassen, die instrumentierbare Lüfter, Temperatursonden und Geräte darstellen.



| Klasse                                                     | Beschreibung                                                                 |
|-----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Win32-Lüfter \_**](win32-fan.md)                           | Stellt die Eigenschaften eines Lüftergeräts im Computersystem dar.           |
| [**Win32 \_ HeatPipe**](win32-heatpipe.md)                 | Stellt die Eigenschaften eines Wärmeleitungs-Kühlgeräts dar.                    |
| [**\_Win32-Aggregat**](win32-refrigeration.md)       | Stellt die Eigenschaften eines Nicht-Gerätes dar.                        |
| [**Win32 \_ TemperatureProbe**](win32-temperatureprobe.md) | Stellt die Eigenschaften eines Temperatursensors (elektronisches Thermometer) dar. |



 

## <a name="input-device-classes"></a>Eingabegeräteklassen

Die Unterkategorie Eingabegeräte gruppen Klassen, die Tastaturen und zeigende Geräte darstellen.



| Klasse                                                 | Beschreibung                                                                                                         |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**Win32-Tastatur \_**](win32-keyboard.md)             | Stellt eine Tastatur dar, die auf einem Computersystem installiert ist, auf dem Windows.                                               |
| [**Win32 \_ PointingDevice**](win32-pointingdevice.md) | Stellt ein Eingabegerät dar, das verwendet wird, um auf die Anzeige eines Computersystems zu zeigen und Bereiche auszuwählen, auf denen Windows. |



 

## <a name="mass-storage-classes"></a>Massenklassen Storage Massenklasse

Klassen in der Storage-Kategorie stellen Speichergeräte wie Festplattenlaufwerke, CD-ROM-Laufwerke und Bandlaufwerke dar.



| Klasse                                                     | Beschreibung                                                                                  |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**Win32 \_ AutochkSetting**](win32-autochksetting.md)     | Stellt die Einstellungen für den Vorgang der automatischen Überprüfung eines Datenträgers dar.                               |
| [**Win32 \_ C LAUFWERK**](win32-cdromdrive.md)             | Stellt ein CD-ROM-Laufwerk auf einem Computersystem dar, auf dem Windows.                              |
| [**Win32 \_ DiskDrive**](win32-diskdrive.md)               | Stellt ein physisches Laufwerk dar, das von einem Computer mit dem Windows wird. |
| [**Win32 \_ FloppyDrive**](win32-floppydrive.md)           | Verwaltet die Funktionen eines Diskettenlaufwerks.                                             |
| [**Win32 \_ PhysicalMedia**](/previous-versions/windows/desktop/cimwin32a/win32-physicalmedia) | Stellt einen beliebigen Dokumentations- oder Speichermediumtyp dar.                                      |
| [**Win32 \_ TapeDrive**](win32-tapedrive.md)               | Stellt ein Bandlaufwerk auf einem Computersystem dar, auf dem Windows.                                |



 

## <a name="motherboard-controller-and-port-classes"></a>Hauptplatinen-, Controller- und Portklassen

Die Unterkategorie Hauptplatine, Controller und Ports gruppen Klassen, die Systemgeräte darstellen. Beispiele hierfür sind Systemspeicher, Cachespeicher und Controller.



| Klasse                                                                       | Beschreibung                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 1394Controller**](win32-1394controller.md)                       | Stellt die Funktionen und die Verwaltung eines 1394-Controllers dar.<br/>                                                                                                                                               |
| [**Win32 \_ 1394ControllerDevice**](win32-1394controllerdevice.md)           | Verknüpft den hochgeschwindigkeitsbasierten seriellen Buscontroller (IEEE 1394 Firewire) und die damit verbundene [**CIM \_ LogicalDevice-Instanz.**](cim-logicaldevice.md)<br/>                                                            |
| [**Win32 \_ AllocatedResource**](win32-allocatedresource.md)                 | Verbindet ein logisches Gerät mit einer Systemressource.<br/>                                                                                                                                                                 |
| [**Win32 \_ AssociatedProcessorMemory**](win32-associatedprocessormemory.md) | Bezieht einen Prozessor und seinen Cachespeicher.<br/>                                                                                                                                                                      |
| [**Win32 \_ BaseBoard**](win32-baseboard.md)                                 | Stellt ein Baseboard dar (auch als Hauptplatine oder Systemboard bekannt).<br/>                                                                                                                                          |
| [**Win32 \_ BIOS**](win32-bios.md)                                           | Stellt die Attribute der grundlegenden Eingabe- oder Ausgabedienste (BIOS) des Computersystems dar, die auf dem Computer installiert sind.<br/>                                                                                   |
| [**Win32 \_ Bus**](win32-bus.md)                                             | Stellt einen physischen Bus dar, der von einem Windows wird.<br/>                                                                                                                                               |
| [**Win32 \_ CacheMemory**](win32-cachememory.md)                             | Stellt Cachespeicher (intern und extern) auf einem Computersystem dar.<br/>                                                                                                                                          |
| [**\_Win32-ControllerHasHub**](/previous-versions/windows/desktop/cimwin32a/win32-controllerhashub)             | Stellt die Hubs dar, die nach dem USB-Controller (Universal Serial Bus) nachgeschaltet sind.<br/>                                                                                                                                 |
| [**Win32 \_ DeviceBus**](win32-devicebus.md)                                 | Verbindet einen Systembus und ein logisches Gerät mithilfe des Bus.<br/>                                                                                                                                                       |
| [**Win32 \_ DeviceMemoryAddress**](win32-devicememoryaddress.md)             | Stellt eine Gerätespeicheradresse auf einem Windows dar.<br/>                                                                                                                                                        |
| [**Win32 \_ DeviceSettings**](win32-devicesettings.md)                       | Bezieht ein logisches Gerät und eine Einstellung, die darauf angewendet werden können.<br/>                                                                                                                                              |
| [**Win32 \_ DMAChannel**](win32-dmachannel.md)                               | Stellt einen DMA-Kanal (Direct Memory Access) auf einem Computersystem dar, auf dem Windows.<br/>                                                                                                                          |
| [**Win32 \_ FloppyController**](win32-floppycontroller.md)                   | Stellt die Funktionen und die Verwaltungskapazität eines Diskettenlaufwerkcontrollers dar.<br/>                                                                                                                         |
| [**Win32 \_ IDEController**](win32-idecontroller.md)                         | Stellt die Funktionen eines IDE-Controllergeräts (Integrated Drive Electronics) dar.<br/>                                                                                                                        |
| [**Win32 \_ IDEControllerDevice**](win32-idecontrollerdevice.md)             | Zuordnungsklasse, die einen IDE-Controller und das logische Gerät verbindet.<br/>                                                                                                                                       |
| [**\_Win32-12-2016**](win32-infrareddevice.md)                       | Stellt die Funktionen und die Verwaltung eines Nicht-Gerätes dar.<br/>                                                                                                                                              |
| [**Win32 \_ IRQResource**](win32-irqresource.md)                             | Stellt eine Nummer der Interruptanforderungszeile (INTERRUPT Request Line, IRQ) auf einem Windows dar.<br/>                                                                                                                                |
| [**Win32 \_ MemoryArray**](win32-memoryarray.md)                             | Stellt die Eigenschaften des Computersystem-Speicherarrays und der zugeordneten Adressen dar.<br/>                                                                                                                            |
| [**Win32 \_ MemoryArrayLocation**](win32-memoryarraylocation.md)             | Bezieht ein logisches Speicherarray und das physische Speicherarray, auf dem es vorhanden ist.<br/>                                                                                                                             |
| [**Win32 \_ MemoryDevice**](win32-memorydevice.md)                           | Stellt die Eigenschaften des Speichergeräts eines Computersystems zusammen mit den zugeordneten zugeordneten Adressen dar.<br/>                                                                                                     |
| [**Win32 \_ MemoryDeviceArray**](win32-memorydevicearray.md)                 | Bezieht ein Speichergerät und das Speicherarray, in dem es sich befindet.<br/>                                                                                                                                              |
| [**Win32 \_ MemoryDeviceLocation**](win32-memorydevicelocation.md)           | Zuordnungsklasse, die ein Speichergerät mit dem physischen Speicher verbindet, auf dem es vorhanden ist.<br/>                                                                                                                     |
| [**\_Win32-HauptplatineGeräte**](win32-motherboarddevice.md)                 | Stellt ein Gerät dar, das die zentralen Komponenten des Computersystems enthält, auf dem Windows.<br/>                                                                                                               |
| [**Win32 \_ OnBoardDevice**](win32-onboarddevice.md)                         | Stellt allgemeine Adaptergeräte dar, die in die Hauptplatine (Systemboard) integriert sind.<br/>                                                                                                                                   |
| [**Win32 \_ ParallelPort**](win32-parallelport.md)                           | Stellt die Eigenschaften eines parallelen Ports auf einem Computersystem dar, auf dem Windows.<br/>                                                                                                                             |
| [**Win32 \_ PCMCIAController**](win32-pcmciacontroller.md)                   | Verwaltet die Funktionen eines PCMCIA-Controllergeräts (Personal Computer Memory Card Interface Adapter).<br/>                                                                                                      |
| [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md)                       | Stellt ein physisches Speichergerät dar, das sich auf einem Computer befindet und für das Betriebssystem verfügbar ist.<br/>                                                                                                                |
| [**Win32 \_ PhysicalMemoryArray**](win32-physicalmemoryarray.md)             | Stellt Details zum physischen Speicher des Computersystems dar.<br/>                                                                                                                                                |
| [**Win32 \_ PhysicalMemoryLocation**](win32-physicalmemorylocation.md)       | Bezieht ein Array von physischem Speicher und dessen physischem Speicher.<br/>                                                                                                                                                   |
| [**Win32 \_ PNPAllocatedResource**](win32-pnpallocatedresource.md)           | Stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar.<br/>                                                                                                                                        |
| [**Win32 \_ PNPDevice**](win32-pnpdevice.md)                                 | Bezieht ein Gerät (bekannt Konfigurations-Manager als PNPEntity) und die funktion, die es ausführt.<br/>                                                                                                                |
| [**Win32 \_ PNPEntity**](win32-pnpentity.md)                                 | Stellt die Eigenschaften eines Plug & Play dar.<br/>                                                                                                                                                           |
| [**Win32 \_ PortConnector**](win32-portconnector.md)                         | Stellt physische Verbindungsports dar, z. B. DB-25 pin male, Centronics und PS/2.<br/>                                                                                                                            |
| [**Win32 \_ PortResource**](win32-portresource.md)                           | Stellt einen E/A-Port auf einem Computersystem dar, auf dem Windows.<br/>                                                                                                                                                   |
| [**Win32-Prozessor \_**](win32-processor.md)                                 | Stellt ein Gerät dar, das eine Sequenz von Computeranweisungen auf einem Computersystem interpretieren kann, auf dem Windows.<br/>                                                                                           |
| [**Win32 \_ SCSIController**](win32-scsicontroller.md)                       | Stellt einen kleinen SCSI-Controller (Computer System Interface) auf einem Computersystem dar, auf dem Windows.<br/>                                                                                                           |
| [**Win32 \_ SCSIControllerDevice**](win32-scsicontrollerdevice.md)           | Verknüpft einen SCSI-Controller und das damit verbundene logische Gerät (Laufwerk).<br/>                                                                                                                                 |
| [**Win32 \_ SerialPort**](win32-serialport.md)                               | Stellt einen seriellen Anschluss auf einem Computersystem dar, auf dem Windows.<br/>                                                                                                                                                 |
| [**Win32 \_ SerialPortConfiguration**](win32-serialportconfiguration.md)     | Stellt die Einstellungen für die Datenübertragung an einem seriellen Windows dar.<br/>                                                                                                                                        |
| [**Win32 \_ SerialPortSetting**](win32-serialportsetting.md)                 | Bezieht einen seriellen Anschluss und seine Konfigurationseinstellungen.<br/>                                                                                                                                                          |
| [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)                           | Stellt die Funktionen und die Verwaltung von speicherbezogenen logischen Geräten dar.<br/>                                                                                                                                  |
| [**Win32 \_ SoundDevice**](win32-sounddevice.md)                             | Stellt die Eigenschaften eines Soundgeräts auf einem Computersystem dar, auf dem Windows.<br/>                                                                                                                              |
| [**Win32 \_ SystemBIOS**](win32-systembios.md)                               | Bezieht sich auf ein Computersystem (einschließlich Daten wie Starteigenschaften, Zeitzonen, Startkonfigurationen oder Administratorkennwörter) und ein System-BIOS (Dienste, Sprachen und Systemverwaltungseigenschaften).<br/> |
| [**Win32 \_ SystemDriverPNPEntity**](win32-systemdriverpnpentity.md)         | Bezieht ein Plug & Play-Gerät auf Windows Computersystem und den Treiber, der das Plug & Play unterstützt.<br/>                                                                                           |
| [**Win32 \_ SystemEnclosure**](win32-systemenclosure.md)                     | Stellt die Eigenschaften dar, die einem physischen Systemgehäuse zugeordnet sind.<br/>                                                                                                                                         |
| [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md)           | Stellt eine Systemspeicherressource auf einem Windows dar.<br/>                                                                                                                                                       |
| [**Win32 \_ SystemSlot**](win32-systemslot.md)                               | Stellt physische Verbindungspunkte wie Ports, Hauptplatinenslots und Peripheriegeräte sowie proprietäre Verbindungspunkte dar.<br/>                                                                                  |
| [**Win32 \_ USBController**](win32-usbcontroller.md)                         | Verwaltet die Funktionen eines USB-Controllers (Universal Serial Bus).<br/>                                                                                                                                           |
| [**Win32 \_ USBControllerDevice**](win32-usbcontrollerdevice.md)             | Verknüpft einen USB-Controller und die [**damit verbundenen CIM \_ LogicalDevice-Instanzen.**](cim-logicaldevice.md)<br/>                                                                                                    |
| [**Win32 \_ USBHub**](/previous-versions/windows/desktop/cimwin32a/win32-usbhub)                                 | Stellt die Verwaltungsmerkmale eines USB-Hubs dar.<br/>                                                                                                                                                        |



 

## <a name="networking-device-classes"></a>Netzwerkgeräteklassen

Die Unterkategorie Netzwerkgeräte gruppen Klassen, die den Netzwerkschnittstellencontroller, seine Konfigurationen und seine Einstellungen darstellen.



| Klasse                                                                           | Beschreibung                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ NetworkAdapter**](win32-networkadapter.md)                           | Stellt einen Netzwerkadapter auf einem Computersystem dar, auf dem Windows.<br/>                                                                                                                                          |
| [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) | Stellt die Attribute und Verhaltensweisen eines Netzwerkadapters dar. Es ist nicht garantiert, dass die Klasse nach der Cim-Netzwerkspezifikation distributed Management Task Force (DMTF) unterstützt wird.<br/> |
| [**Win32 \_ NetworkAdapterSetting**](win32-networkadaptersetting.md)             | Bezieht einen Netzwerkadapter und seine Konfigurationseinstellungen.<br/>                                                                                                                                                   |



 

## <a name="power-classes"></a>Energieklassen

Die Unterkategorie Energie gruppen Klassen, die Stromversorgungen, Akkus und Ereignisse im Zusammenhang mit diesen Geräten darstellen.



| Klasse                                                             | Beschreibung                                                                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Win32-Akku \_**](win32-battery.md)                           | Stellt einen Akku dar, der mit dem Computersystem verbunden ist.<br/>                                     |
| [**Win32 \_ CurrentProbe**](win32-currentprobe.md)                 | Stellt die Eigenschaften eines aktuellen Überwachungssensors (Ammeter) dar.<br/>                        |
| [**Win32 \_ PortableBattery**](win32-portablebattery.md)           | Stellt die Eigenschaften eines tragbaren Akkus dar, z. B. eines für einen Notebookcomputer verwendeten Akkus.<br/> |
| [**Win32 \_ PowerManagementEvent**](win32-powermanagementevent.md) | Stellt Energieverwaltungsereignisse dar, die sich aus Energiezustandsänderungen ergeben.<br/>                     |
| [**Win32 \_ VoltageProbe**](win32-voltageprobe.md)                 | Stellt die Eigenschaften eines Spannungssensors (elektronisches Meter) dar.<br/>                      |



 

## <a name="printing-classes"></a>Druckklassen

Die Unterkategorie Drucken gruppen Klassen, die Drucker, Druckerkonfigurationen und Druckaufträge darstellen.



| Klasse                                                             | Beschreibung                                                                                                                              |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DriverForDevice**](win32-driverfordevice.md)           | Verbindet einen Drucker mit einem Druckertreiber.<br/>                                                                                        |
| [**Win32-Drucker \_**](win32-printer.md)                           | Stellt ein Gerät dar, das mit einem Computersystem verbunden ist Windows das ein visuelles Bild auf einem Medium reproduzieren kann.<br/> |
| [**Win32 \_ PrinterConfiguration**](win32-printerconfiguration.md) | Definiert die Konfiguration für ein Druckergerät.<br/>                                                                               |
| [**Win32 \_ PrinterController**](win32-printercontroller.md)       | Verknüpft einen Drucker und das lokale Gerät, mit dem der Drucker verbunden ist.<br/>                                                     |
| [**Win32 \_ PrinterDriver**](win32-printerdriver.md)               | Stellt die Treiber für eine [**\_ Win32-Druckerinstanz**](win32-printer.md) dar.<br/>                                                |
| [**Win32 \_ PrinterDriverDll**](win32-printerdriverdll.md)         | Bezieht einen lokalen Drucker und seine Treiberdatei (nicht den Treiber selbst).<br/>                                                          |
| [**Win32 \_ PrinterSetting**](win32-printersetting.md)             | Verknüpft einen Drucker und seine Konfigurationseinstellungen.<br/>                                                                             |
| [**Win32 \_ PrintJob**](win32-printjob.md)                         | Stellt einen Druckauftrag dar, der von einer Windows-basierten Anwendung generiert wird.<br/>                                                              |
| [**Win32 \_ TCPIPPrinterPort**](win32-tcpipprinterport.md)         | Stellt einen TCP/IP-Dienstzugriffspunkt dar.<br/>                                                                                     |



 

## <a name="telephony-classes"></a>Telefonieklassen

Die Unterkategorie Telefonie gruppiert Klassen, die "einfache alte Telefongeräte" und die zugehörigen seriellen Verbindungen darstellen.



| Klasse                                                               | Beschreibung                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32- \_ UND-MODUS**](win32-potsmodem.md)                         | Stellt die Dienste und Merkmale eines PLAIN OLD Phone Service-Modems (TIES) auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/> |
| [**Win32- \_ UND-MODUSMTOSerialPort**](win32-potsmodemtoserialport.md) | Verknüpft ein Modem und den seriellen Anschluss, den das Modem verwendet.<br/>                                                                             |



 

## <a name="video-and-monitor-classes"></a>Video- und Monitorklassen

Die Unterkategorie Video und Monitore gruppiert Klassen, die Monitore, Grafikkarten und die zugehörigen Einstellungen darstellen.



| Klasse                                                                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)                                 | Stellt den Typ des an das Computersystem angeschlossenen Überwachungs- oder Anzeigegeräts dar.<br/>                                                                                                                                                                                                                                                                                       |
| [**Win32 \_ DisplayControllerConfiguration**](win32-displaycontrollerconfiguration.md) | Stellt die Konfigurationsinformationen der Grafikkarte eines Computersystems dar, auf dem Windows ausgeführt wird. Diese Klasse ist veraltet. Verwenden Sie anstelle dieser Klasse die Eigenschaften in den Klassen [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)und [CIM \_ VideoControllerResolution.](cim-videocontrollerresolution.md)<br/> |
| [**Win32 \_ VideoController**](win32-videocontroller.md)                               | Stellt die Funktionen und die Verwaltungskapazität des Videocontrollers auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                                                                                                                                                       |
| [**Win32 \_ VideoSettings**](win32-videosettings.md)                                   | Verknüpft einen Videocontroller und Videoeinstellungen, die darauf angewendet werden können.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Win32-Klassen](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

