---
description: Die Kategorie Computersystemhardware gruppiert Klassen, die hardwarebezogene Objekte darstellen. Beispiele hierfür sind Eingabegeräte, Festplatten, Erweiterungskarten, Videogeräte, Netzwerkgeräte und Systemleistung.
ms.assetid: 0b6cb410-166e-45cd-8dca-77a111b3cf62
ms.tgt_platform: multiple
title: Computersystemhardwareklassen
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
# <a name="computer-system-hardware-classes"></a>Computersystemhardwareklassen

Die Kategorie Computersystemhardware gruppiert Klassen, die hardwarebezogene Objekte darstellen. Beispiele hierfür sind Eingabegeräte, Festplatten, Erweiterungskarten, Videogeräte, Netzwerkgeräte und Systemleistung.

-   [Kühlgeräteklassen](#cooling-device-classes)
-   [Eingabegeräteklassen](#input-device-classes)
-   [Massen-Storage-Klassen](#mass-storage-classes)
-   [Hauptplatinen-, Controller- und Portklassen](#motherboard-controller-and-port-classes)
-   [Netzwerkgeräteklassen](#networking-device-classes)
-   [Energieklassen](#power-classes)
-   [Druckklassen](#printing-classes)
-   [Telefonieklassen](#telephony-classes)
-   [Video- und Monitorklassen](#video-and-monitor-classes)
-   [Zugehörige Themen](#related-topics)

## <a name="cooling-device-classes"></a>Kühlgeräteklassen

Die Unterkategorie Kühlgeräte gruppiert Klassen, die instrumentierbare Lüfter, Temperatursonden und Kühlgeräte darstellen.



| Klasse                                                     | BESCHREIBUNG                                                                 |
|-----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**\_Win32-Lüfter**](win32-fan.md)                           | Stellt die Eigenschaften eines Lüftergeräts im Computersystem dar.           |
| [**Win32 \_ HeatPipe**](win32-heatpipe.md)                 | Stellt die Eigenschaften eines Wärmeleitungskühlungsgeräts dar.                    |
| [**Win32 \_ Refrigeration**](win32-refrigeration.md)       | Stellt die Eigenschaften eines Kühlgeräts dar.                        |
| [**Win32 \_ TemperatureProbe**](win32-temperatureprobe.md) | Stellt die Eigenschaften eines Temperatursensors (elektronisches Thermometer) dar. |



 

## <a name="input-device-classes"></a>Eingabegeräteklassen

Die Unterkategorie Eingabegeräte gruppiert Klassen, die Tastaturen und zeigende Geräte darstellen.



| Klasse                                                 | BESCHREIBUNG                                                                                                         |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**\_Win32-Tastatur**](win32-keyboard.md)             | Stellt eine Tastatur dar, die auf einem Computersystem installiert ist, auf dem Windows ausgeführt wird.                                               |
| [**Win32 \_ PointingDevice**](win32-pointingdevice.md) | Stellt ein Eingabegerät dar, das verwendet wird, um auf die Bereiche auf der Anzeige eines Computersystems zu zeigen und diese auszuwählen, auf dem Windows ausgeführt wird. |



 

## <a name="mass-storage-classes"></a>Massen-Storage-Klassen

Klassen in der Unterkategorie "Mass Storage" stellen Speichergeräte wie Festplattenlaufwerke, CD-ROM-Laufwerke und Bandlaufwerke dar.



| Klasse                                                     | BESCHREIBUNG                                                                                  |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**Win32 \_ AutochkSetting**](win32-autochksetting.md)     | Stellt die Einstellungen für den automatischen Überprüfungsvorgang eines Datenträgers dar.                               |
| [**Win32 \_ CORPORADrive**](win32-cdromdrive.md)             | Stellt ein CD-ROM-Laufwerk auf einem Computersystem dar, auf dem Windows ausgeführt wird.                              |
| [**Win32 \_ DiskDrive**](win32-diskdrive.md)               | Stellt ein physisches Laufwerk dar, das von einem Computer angezeigt wird, auf dem das Windows Betriebssystem ausgeführt wird. |
| [**Win32 \_ FloppyDrive**](win32-floppydrive.md)           | Verwaltet die Funktionen eines Diskettenlaufwerks.                                             |
| [**Win32 \_ PhysicalMedia**](/previous-versions/windows/desktop/cimwin32a/win32-physicalmedia) | Stellt einen beliebigen Typ von Dokumentation oder Speichermedium dar.                                      |
| [**Win32 \_ TapeDrive**](win32-tapedrive.md)               | Stellt ein Bandlaufwerk auf einem Computersystem dar, auf dem Windows ausgeführt wird.                                |



 

## <a name="motherboard-controller-and-port-classes"></a>Hauptplatinen-, Controller- und Portklassen

Die Unterkategorie "Hauptplatine", "Controller" und "Ports" gruppiert Klassen, die Systemgeräte darstellen. Beispiele hierfür sind Systemspeicher, Cachespeicher und Controller.



| Klasse                                                                       | BESCHREIBUNG                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 1394Controller**](win32-1394controller.md)                       | Stellt die Funktionen und die Verwaltung eines 1394-Controllers dar.<br/>                                                                                                                                               |
| [**Win32 \_ 1394ControllerDevice**](win32-1394controllerdevice.md)           | Verknüpft den High-Speed-Controller für seriellen Bus (IEEE 1394 Firewire) und die damit verbundene [**CIM \_ LogicalDevice-Instanz.**](cim-logicaldevice.md)<br/>                                                            |
| [**Win32 \_ AllocatedResource**](win32-allocatedresource.md)                 | Verknüpft ein logisches Gerät mit einer Systemressource.<br/>                                                                                                                                                                 |
| [**Win32 \_ AssociatedProcessorMemory**](win32-associatedprocessormemory.md) | Verknüpft einen Prozessor und seinen Cachespeicher.<br/>                                                                                                                                                                      |
| [**Win32 \_ BaseBoard**](win32-baseboard.md)                                 | Stellt ein Baseboard (auch als Hauptplatine oder Systemboard bezeichnet) dar.<br/>                                                                                                                                          |
| [**\_Win32-BIOS**](win32-bios.md)                                           | Stellt die Attribute der grundlegenden Eingabe- oder Ausgabedienste (BIOS) des Computersystems dar, die auf dem Computer installiert sind.<br/>                                                                                   |
| [**\_Win32-Bus**](win32-bus.md)                                             | Stellt einen physischen Bus dar, wie er von einem Windows Betriebssystem erkannt wird.<br/>                                                                                                                                               |
| [**Win32 \_ CacheMemory**](win32-cachememory.md)                             | Stellt Cachespeicher (intern und extern) auf einem Computersystem dar.<br/>                                                                                                                                          |
| [**Win32 \_ ControllerHasHub**](/previous-versions/windows/desktop/cimwin32a/win32-controllerhashub)             | Stellt die Hubs dar, die vom USB-Controller (Universal Serial Bus) nachgeschaltet werden.<br/>                                                                                                                                 |
| [**Win32 \_ DeviceBus**](win32-devicebus.md)                                 | Verknüpft einen Systembus und ein logisches Gerät mithilfe des -Buss.<br/>                                                                                                                                                       |
| [**Win32 \_ DeviceMemoryAddress**](win32-devicememoryaddress.md)             | Stellt eine Gerätespeicheradresse auf einem Windows System dar.<br/>                                                                                                                                                        |
| [**Win32 \_ DeviceSettings**](win32-devicesettings.md)                       | Verknüpft ein logisches Gerät mit einer Einstellung, die darauf angewendet werden kann.<br/>                                                                                                                                              |
| [**Win32 \_ DMAChannel**](win32-dmachannel.md)                               | Stellt einen DMA-Kanal (Direct Memory Access) auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                          |
| [**Win32 \_ FloppyController**](win32-floppycontroller.md)                   | Stellt die Funktionen und die Verwaltungskapazität eines Diskettenlaufwerkcontrollers dar.<br/>                                                                                                                         |
| [**\_Win32-IDEController**](win32-idecontroller.md)                         | Stellt die Funktionen eines IDE-Controllergeräts (Integrated Drive Electronics) dar.<br/>                                                                                                                        |
| [**Win32 \_ IDEControllerDevice**](win32-idecontrollerdevice.md)             | Zuordnungsklasse, die einen IDE-Controller und das logische Gerät verknüpft.<br/>                                                                                                                                       |
| [**Win32- \_ Und-Vice-2016-2016-2**](win32-infrareddevice.md)                       | Stellt die Funktionen und die Verwaltung eines Geräts dar.<br/>                                                                                                                                              |
| [**Win32 \_ IRQResource**](win32-irqresource.md)                             | Stellt eine IRQ-Nummer (Interrupt Request Line) auf einem Windows-Computersystem dar.<br/>                                                                                                                                |
| [**Win32 \_ MemoryArray**](win32-memoryarray.md)                             | Stellt die Eigenschaften des Arbeitsspeicherarrays des Computersystems und der zugeordneten Adressen dar.<br/>                                                                                                                            |
| [**Win32 \_ MemoryArrayLocation**](win32-memoryarraylocation.md)             | Verknüpft ein logisches Speicherarray mit dem physischen Speicherarray, auf dem es vorhanden ist.<br/>                                                                                                                             |
| [**Win32 \_ MemoryDevice**](win32-memorydevice.md)                           | Stellt die Eigenschaften des Arbeitsspeichergeräts eines Computersystems zusammen mit den zugeordneten Adressen dar.<br/>                                                                                                     |
| [**Win32 \_ MemoryDeviceArray**](win32-memorydevicearray.md)                 | Verknüpft ein Speichergerät mit dem Speicherarray, in dem es sich befindet.<br/>                                                                                                                                              |
| [**Win32 \_ MemoryDeviceLocation**](win32-memorydevicelocation.md)           | Zuordnungsklasse, die ein Speichergerät mit dem physischen Speicher verknüpft, auf dem es vorhanden ist.<br/>                                                                                                                     |
| [**\_Win32-HauptplatineGeräte**](win32-motherboarddevice.md)                 | Stellt ein Gerät dar, das die zentralen Komponenten des Computersystems enthält, auf dem Windows ausgeführt wird.<br/>                                                                                                               |
| [**Win32 \_ OnBoardDevice**](win32-onboarddevice.md)                         | Stellt allgemeine Adaptergeräte dar, die in die Hauptplatine (Systemboard) integriert sind.<br/>                                                                                                                                   |
| [**Win32 \_ ParallelPort**](win32-parallelport.md)                           | Stellt die Eigenschaften eines parallelen Ports auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                             |
| [**Win32 \_ PCMCIAController**](win32-pcmciacontroller.md)                   | Verwaltet die Funktionen eines PCMCIA-Controllergeräts (Personal Computer Memory Card Interface Adapter).<br/>                                                                                                      |
| [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md)                       | Stellt ein physisches Speichergerät auf einem Computer dar, das für das Betriebssystem verfügbar ist.<br/>                                                                                                                |
| [**Win32 \_ PhysicalMemoryArray**](win32-physicalmemoryarray.md)             | Stellt Details zum physischen Arbeitsspeicher des Computersystems dar.<br/>                                                                                                                                                |
| [**Win32 \_ PhysicalMemoryLocation**](win32-physicalmemorylocation.md)       | Verknüpft ein Array von physischem Speicher und dessen physischem Speicher.<br/>                                                                                                                                                   |
| [**Win32 \_ PNPAllocatedResource**](win32-pnpallocatedresource.md)           | Stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar.<br/>                                                                                                                                        |
| [**Win32 \_ PNPDevice**](win32-pnpdevice.md)                                 | Verknüpft ein Gerät (Konfigurations-Manager als PNPEntity bezeichnet) und die funktion, die es ausführt.<br/>                                                                                                                |
| [**Win32 \_ PNPEntity**](win32-pnpentity.md)                                 | Stellt die Eigenschaften eines Plug & Play Geräts dar.<br/>                                                                                                                                                           |
| [**Win32 \_ PortConnector**](win32-portconnector.md)                         | Stellt physische Verbindungsports dar, z. B. DB-25 pin male, Cen csvs und PS/2.<br/>                                                                                                                            |
| [**Win32 \_ PortResource**](win32-portresource.md)                           | Stellt einen E/A-Port auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                                                   |
| [**\_Win32-Prozessor**](win32-processor.md)                                 | Stellt ein Gerät dar, das eine Sequenz von Computeranweisungen auf einem Computersystem interpretieren kann, auf dem Windows ausgeführt wird.<br/>                                                                                           |
| [**Win32 \_ SCSIController**](win32-scsicontroller.md)                       | Stellt einen kleinen SCSI-Controller (Computer System Interface) auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                           |
| [**Win32 \_ SCSIControllerDevice**](win32-scsicontrollerdevice.md)           | Bezieht sich auf einen SCSI-Controller und das mit ihm verbundene logische Gerät (Laufwerk).<br/>                                                                                                                                 |
| [**Win32 \_ SerialPort**](win32-serialport.md)                               | Stellt einen seriellen Anschluss auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                                                 |
| [**Win32 \_ SerialPortConfiguration**](win32-serialportconfiguration.md)     | Stellt die Einstellungen für die Datenübertragung an einem Windows seriellen Anschluss dar.<br/>                                                                                                                                        |
| [**Win32 \_ SerialPortSetting**](win32-serialportsetting.md)                 | Verknüpft einen seriellen Anschluss und seine Konfigurationseinstellungen.<br/>                                                                                                                                                          |
| [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)                           | Stellt die Funktionen und die Verwaltung speicherbezogener logischer Geräte dar.<br/>                                                                                                                                  |
| [**Win32 \_ SoundDevice**](win32-sounddevice.md)                             | Stellt die Eigenschaften eines Soundgeräts auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                              |
| [**\_Win32-SystemBIOS**](win32-systembios.md)                               | Bezieht sich auf ein Computersystem (einschließlich Daten wie Starteigenschaften, Zeitzonen, Startkonfigurationen oder Administratorkennwörter) und ein System-BIOS (Dienste, Sprachen und Systemverwaltungseigenschaften).<br/> |
| [**Win32 \_ SystemDriverPNPEntity**](win32-systemdriverpnpentity.md)         | Verknüpft ein Plug & Play Gerät auf dem Windows-Computersystem und dem Treiber, der das Plug & Play Gerät unterstützt.<br/>                                                                                           |
| [**Win32 \_ SystemEnclosure**](win32-systemenclosure.md)                     | Stellt die einem physischen Systemgehäuse zugeordneten Eigenschaften dar.<br/>                                                                                                                                         |
| [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md)           | Stellt eine Systemspeicherressource auf einem Windows System dar.<br/>                                                                                                                                                       |
| [**Win32 \_ SystemSlot**](win32-systemslot.md)                               | Stellt physische Verbindungspunkte dar, einschließlich Ports, Hauptplatinenslots und Peripheriegeräte sowie proprietäre Verbindungspunkte.<br/>                                                                                  |
| [**Win32 \_ USBController**](win32-usbcontroller.md)                         | Verwaltet die Funktionen eines USB-Controllers (Universal Serial Bus).<br/>                                                                                                                                           |
| [**Win32 \_ USBControllerDevice**](win32-usbcontrollerdevice.md)             | Verknüpft einen USB-Controller und die damit verbundenen [**CIM \_ LogicalDevice-Instanzen.**](cim-logicaldevice.md)<br/>                                                                                                    |
| [**Win32 \_ USBHub**](/previous-versions/windows/desktop/cimwin32a/win32-usbhub)                                 | Stellt die Verwaltungsmerkmale eines USB-Hubs dar.<br/>                                                                                                                                                        |



 

## <a name="networking-device-classes"></a>Netzwerkgeräteklassen

Die Unterkategorie Netzwerkgeräte gruppiert Klassen, die den Netzwerkschnittstellencontroller, seine Konfigurationen und seine Einstellungen darstellen.



| Klasse                                                                           | BESCHREIBUNG                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ NetworkAdapter**](win32-networkadapter.md)                           | Stellt einen Netzwerkadapter auf einem Computersystem dar, auf dem Windows ausgeführt wird.<br/>                                                                                                                                          |
| [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) | Stellt die Attribute und Verhaltensweisen eines Netzwerkadapters dar. Es ist nicht garantiert, dass die -Klasse nach der DmTF-CIM-Netzwerkspezifikation (Distributed Management Task Force) unterstützt wird.<br/> |
| [**Win32 \_ NetworkAdapterSetting**](win32-networkadaptersetting.md)             | Verknüpft einen Netzwerkadapter und seine Konfigurationseinstellungen.<br/>                                                                                                                                                   |



 

## <a name="power-classes"></a>Energieklassen

Die Unterkategorie Energie gruppiert Klassen, die Stromversorgungen, Akkus und Ereignisse im Zusammenhang mit diesen Geräten darstellen.



| Klasse                                                             | BESCHREIBUNG                                                                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**\_Win32-Akku**](win32-battery.md)                           | Stellt einen Akku dar, der mit dem Computersystem verbunden ist.<br/>                                     |
| [**Win32 \_ CurrentProbe**](win32-currentprobe.md)                 | Stellt die Eigenschaften eines aktuellen Überwachungssensors (Ammeter) dar.<br/>                        |
| [**Win32 \_ PortableBattery**](win32-portablebattery.md)           | Stellt die Eigenschaften eines tragbaren Akkus dar, z. B. einen, der für einen Notebookcomputer verwendet wird.<br/> |
| [**Win32 \_ PowerManagementEvent**](win32-powermanagementevent.md) | Stellt Energieverwaltungsereignisse dar, die sich aus Änderungen des Energiezustands ergeben.<br/>                     |
| [**Win32 \_ VoltageProbe**](win32-voltageprobe.md)                 | Stellt die Eigenschaften eines Spannungssensors (elektronisches Mikrometer) dar.<br/>                      |



 

## <a name="printing-classes"></a>Druckklassen

Die Unterkategorie Drucken gruppiert Klassen, die Drucker, Druckerkonfigurationen und Druckaufträge darstellen.



| Klasse                                                             | BESCHREIBUNG                                                                                                                              |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DriverForDevice**](win32-driverfordevice.md)           | Verknüpft einen Drucker mit einem Druckertreiber.<br/>                                                                                        |
| [**\_Win32-Drucker**](win32-printer.md)                           | Stellt ein Gerät dar, das mit einem Computersystem verbunden ist, auf dem Windows ausgeführt wird, das ein visuelles Bild auf einem Medium reproduzieren kann.<br/> |
| [**Win32 \_ PrinterConfiguration**](win32-printerconfiguration.md) | Definiert die Konfiguration für ein Druckergerät.<br/>                                                                               |
| [**Win32 \_ PrinterController**](win32-printercontroller.md)       | Verknüpft einen Drucker und das lokale Gerät, mit dem der Drucker verbunden ist.<br/>                                                     |
| [**Win32 \_ PrinterDriver**](win32-printerdriver.md)               | Stellt die Treiber für eine [**\_ Win32-Druckerinstanz**](win32-printer.md) dar.<br/>                                                |
| [**Win32 \_ PrinterDriverDll**](win32-printerdriverdll.md)         | Verknüpft einen lokalen Drucker und seine Treiberdatei (nicht den Treiber selbst).<br/>                                                          |
| [**Win32 \_ PrinterSetting**](win32-printersetting.md)             | Bezieht einen Drucker und seine Konfigurationseinstellungen.<br/>                                                                             |
| [**Win32 \_ PrintJob**](win32-printjob.md)                         | Stellt einen Druckauftrag dar, der von einer Windows-basierten Anwendung generiert wird.<br/>                                                              |
| [**Win32 \_ TCPIPPrinterPort**](win32-tcpipprinterport.md)         | Stellt einen TCP/IP-Dienstzugriffspunkt dar.<br/>                                                                                     |



 

## <a name="telephony-classes"></a>Telefonieklassen

Die Unterkategorie Telefonie gruppen Klassen, die "einfache alte Telefonmodemgeräte" und die zugehörigen seriellen Verbindungen darstellen.



| Klasse                                                               | BESCHREIBUNG                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Win32–10012 –10002222222**](win32-potsmodem.md)                         | Stellt die Dienste und Merkmale eines PLAIN OLD TELEPHONES-Modems (Plain Old Telephone Service) auf einem Computersystem dar, auf dem Windows.<br/> |
| [**\_Win32–MODISModemToSerialPort**](win32-potsmodemtoserialport.md) | Bezieht sich auf ein Modem und den seriellen Anschluss, den das Modem verwendet.<br/>                                                                             |



 

## <a name="video-and-monitor-classes"></a>Video- und Monitorklassen

Die Unterkategorie Video und Monitore gruppen Klassen, die Monitore, Grafikkarten und die zugehörigen Einstellungen darstellen.



| Klasse                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)                                 | Stellt den Typ des an das Computersystem angeschlossenen Monitors oder Anzeigegeräts dar.<br/>                                                                                                                                                                                                                                                                                       |
| [**Win32 \_ DisplayControllerConfiguration**](win32-displaycontrollerconfiguration.md) | Stellt die Konfigurationsinformationen der Grafikkarte eines Computersystems dar, auf dem Windows. Diese Klasse ist veraltet. Verwenden Sie statt dieser Klasse die Eigenschaften in den [**Klassen Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)und [CIM \_ VideoControllerResolution.](cim-videocontrollerresolution.md)<br/> |
| [**Win32 \_ VideoController**](win32-videocontroller.md)                               | Stellt die Funktionen und die Verwaltungskapazität des Videocontrollers auf einem Computersystem dar, auf dem Windows.<br/>                                                                                                                                                                                                                                                       |
| [**Win32 \_ VideoSettings**](win32-videosettings.md)                                   | Bezieht einen Videocontroller und Videoeinstellungen, die darauf angewendet werden können.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Win32-Klassen](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

