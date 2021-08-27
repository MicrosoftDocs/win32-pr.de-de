---
description: Stellt ein Gerät dar, das mit einem Computer verbunden ist, der auf einem Microsoft Windows Betriebssystem ausgeführt wird, das ein gedrucktes Bild oder Text auf Papier oder einem anderen Medium erzeugen kann.
ms.assetid: 58090e6a-8f13-4859-adb8-a7c6299d3efd
ms.tgt_platform: multiple
title: Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer
- Win32_Printer.Reset
- Win32_Printer.SetPowerState
- Win32_Printer.Attributes
- Win32_Printer.Availability
- Win32_Printer.AvailableJobSheets
- Win32_Printer.AveragePagesPerMinute
- Win32_Printer.Capabilities
- Win32_Printer.CapabilityDescriptions
- Win32_Printer.Caption
- Win32_Printer.CharSetsSupported
- Win32_Printer.Comment
- Win32_Printer.ConfigManagerErrorCode
- Win32_Printer.ConfigManagerUserConfig
- Win32_Printer.CreationClassName
- Win32_Printer.CurrentCapabilities
- Win32_Printer.CurrentCharSet
- Win32_Printer.CurrentLanguage
- Win32_Printer.CurrentMimeType
- Win32_Printer.CurrentNaturalLanguage
- Win32_Printer.CurrentPaperType
- Win32_Printer.Default
- Win32_Printer.DefaultCapabilities
- Win32_Printer.DefaultCopies
- Win32_Printer.DefaultLanguage
- Win32_Printer.DefaultMimeType
- Win32_Printer.DefaultNumberUp
- Win32_Printer.DefaultPaperType
- Win32_Printer.DefaultPriority
- Win32_Printer.Description
- Win32_Printer.DetectedErrorState
- Win32_Printer.DeviceID
- Win32_Printer.Direct
- Win32_Printer.DoCompleteFirst
- Win32_Printer.DriverName
- Win32_Printer.EnableBIDI
- Win32_Printer.EnableDevQueryPrint
- Win32_Printer.ErrorCleared
- Win32_Printer.ErrorDescription
- Win32_Printer.ErrorInformation
- Win32_Printer.ExtendedDetectedErrorState
- Win32_Printer.ExtendedPrinterStatus
- Win32_Printer.Hidden
- Win32_Printer.HorizontalResolution
- Win32_Printer.InstallDate
- Win32_Printer.JobCountSinceLastReset
- Win32_Printer.KeepPrintedJobs
- Win32_Printer.LanguagesSupported
- Win32_Printer.LastErrorCode
- Win32_Printer.Local
- Win32_Printer.Location
- Win32_Printer.MarkingTechnology
- Win32_Printer.MaxCopies
- Win32_Printer.MaxNumberUp
- Win32_Printer.MaxSizeSupported
- Win32_Printer.MimeTypesSupported
- Win32_Printer.Name
- Win32_Printer.NaturalLanguagesSupported
- Win32_Printer.Network
- Win32_Printer.PaperSizesSupported
- Win32_Printer.PaperTypesAvailable
- Win32_Printer.Parameters
- Win32_Printer.PNPDeviceID
- Win32_Printer.PortName
- Win32_Printer.PowerManagementCapabilities
- Win32_Printer.PowerManagementSupported
- Win32_Printer.PrinterPaperNames
- Win32_Printer.PrinterState
- Win32_Printer.PrinterStatus
- Win32_Printer.PrintJobDataType
- Win32_Printer.PrintProcessor
- Win32_Printer.Priority
- Win32_Printer.Published
- Win32_Printer.Queued
- Win32_Printer.RawOnly
- Win32_Printer.SeparatorFile
- Win32_Printer.ServerName
- Win32_Printer.Shared
- Win32_Printer.ShareName
- Win32_Printer.SpoolEnabled
- Win32_Printer.StartTime
- Win32_Printer.Status
- Win32_Printer.StatusInfo
- Win32_Printer.SystemCreationClassName
- Win32_Printer.SystemName
- Win32_Printer.TimeOfLastReset
- Win32_Printer.UntilTime
- Win32_Printer.VerticalResolution
- Win32_Printer.WorkOffline
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f1a91ac90560343a38e546590005e8b984d13843eba8195381daa204e2d22cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077310"
---
# <a name="win32_printer-class"></a>\_Win32-Druckerklasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) **"Win32-Drucker" \_** stellt ein Gerät dar, das mit einem Computer verbunden ist, der auf einem Microsoft Windows Betriebssystem ausgeführt wird und ein gedrucktes Bild oder Text auf Papier oder einem anderen Medium erzeugen kann.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_Printer : CIM_Printer
{
  uint32   Attributes;
  uint16   Availability;
  string   AvailableJobSheets[];
  uint32   AveragePagesPerMinute;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  string   Comment;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  boolean  Default;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  uint32   DefaultPriority;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  Direct;
  boolean  DoCompleteFirst;
  string   DriverName;
  boolean  EnableBIDI;
  boolean  EnableDevQueryPrint;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint16   ExtendedDetectedErrorState;
  uint16   ExtendedPrinterStatus;
  boolean  Hidden;
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  boolean  KeepPrintedJobs;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  boolean  Local;
  string   Location;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  boolean  Network;
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   Parameters;
  string   PNPDeviceID;
  string   PortName;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrinterPaperNames[];
  uint32   PrinterState;
  uint16   PrinterStatus;
  string   PrintJobDataType;
  string   PrintProcessor;
  uint32   Priority;
  boolean  Published;
  boolean  Queued;
  boolean  RawOnly;
  string   SeparatorFile;
  string   ServerName;
  boolean  Shared;
  string   ShareName;
  boolean  SpoolEnabled;
  datetime StartTime;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  datetime UntilTime;
  uint32   VerticalResolution;
  boolean  WorkOffline;
};
```

## <a name="members"></a>Member

Die **\_ Win32-Druckerklasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **\_ Win32-Druckerklasse** verfügt über diese Methoden.



| Methode                                                                               | BESCHREIBUNG                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddPrinterConnection**](addprinterconnection-method-in-class-win32-printer.md)   | Fügt dem Drucker eine Verbindung hinzu.<br/>                                                                                                                                                                      |
| [**CancelAllJobs**](cancelalljobs-method-in-class-win32-printer.md)                 | Bricht alle Aufträge ab.<br/>                                                                                                                                                                                      |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-printer.md) | Gibt die Sicherheitsbeschreibung zurück, die den Zugriff auf den Drucker steuert.<br/>                                                                                                                                   |
| [**Anhalten**](pause-method-in-class-win32-printer.md)                                 | Hält die Druckwarteschlange an.<br/>                                                                                                                                                                                |
| [**PrintTestPage**](printtestpage-method-in-class-win32-printer.md)                 | Druckt eine Testseite.<br/>                                                                                                                                                                                    |
| [**RenamePrinter**](renameprinter-method-in-class-win32-printer.md)                 | Benennt einen Drucker um.<br/>                                                                                                                                                                                     |
| **Zurücksetzen**                                                                            | Nicht implementiert. Weitere Informationen zum Implementieren dieser Methode [](reset-method-in-class-cim-controller.md) finden Sie unter Reset-Methode in [**CIM \_ Printer**](cim-printer.md).<br/>                 |
| [**Fortsetzen**](resume-method-in-class-win32-printer.md)                               | Setzt angehaltene Druckwarteschlange fort.<br/>                                                                                                                                                                            |
| [**SetDefaultPrinter**](setdefaultprinter-method-in-class-win32-printer.md)         | Legt den Standarddrucker fest.<br/>                                                                                                                                                                              |
| **SetPowerState**                                                                    | Nicht implementiert. Weitere Informationen zum Implementieren dieser Methode finden Sie unter [**SetPowerState-Methode**](setpowerstate-method-in-class-cim-controller.md) in [**\_ CIM-Drucker.**](cim-printer.md)<br/> |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-printer.md) | Schreibt eine aktualisierte Version des Sicherheitsdeskriptors, der den Zugriff auf den Drucker steuert.<br/>                                                                                                              |



 

### <a name="properties"></a>Eigenschaften

Die **\_ Win32-Druckerklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Attribute**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bitmap von Attributen für ein Windows-basiertes Druckgerät.

<dt>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**DRUCKER \_ ATTRIBUTE \_ QUEUED** (1 (0x1))


</dt> <dd>

In Warteschlange

Druckaufträge werden gepuffert und in die Warteschlange eingereiht.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**DRUCKER \_ ATTRIBUTE \_ DIRECT** (2 (0x2))


</dt> <dd>

Direkt

Dokument, das direkt an den Drucker gesendet werden soll. Dieser Wert wird verwendet, wenn Druckaufträge nicht ordnungsgemäß in die Warteschlange eingereiht werden.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**DRUCKER \_ ATTRIBUTE \_ DEFAULT** (4 (0x4))


</dt> <dd>

Standard

Standarddrucker auf einem Computer.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**DRUCKER \_ ATTRIBUTE \_ SHARED** (8 (0x8))


</dt> <dd>

Shared

Verfügbar als freigegebene Netzwerkressource.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**DRUCKER \_ ATTRIBUTE \_ NETWORK** (16 (0x10))


</dt> <dd>

Netzwerk

An ein Netzwerk angefügt. Wenn sowohl lokale als auch Netzwerkbits festgelegt sind, gibt dies einen Netzwerkdrucker an.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**DRUCKER \_ ATTRIBUTE \_ HIDDEN** (32 (0x20))


</dt> <dd>

Ausgeblendet

Für einige Benutzer im Netzwerk ausgeblendet.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**DRUCKER \_ ATTRIBUTE \_ LOCAL** (64 (0x40))


</dt> <dd>

Lokales Gerät

Direkt mit einem Computer verbunden. Wenn sowohl lokale als auch Netzwerkbits festgelegt sind, gibt dies einen Netzwerkdrucker an.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**DRUCKER \_ ATTRIBUTE \_ ENABLEDEVQ** (128 (0x80))


</dt> <dd>

EnableDevQ

Aktivieren Sie ggf. die Warteschlange auf dem Drucker.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**DRUCKER \_ ATTRIBUTE \_ KEEPPRINTEDJOBS** (256 (0x100))


</dt> <dd>

KeepPrintedJobs

Spooler sollte Dokumente nicht löschen, nachdem sie gedruckt wurden.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**DRUCKER \_ ATTRIBUTE \_ DO \_ COMPLETE \_ FIRST** (512 (0x200))


</dt> <dd>

DoCompleteFirst

Starten Sie Aufträge, deren Spooling abgeschlossen ist.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**DRUCKER \_ ATTRIBUTE \_ WORK \_ OFFLINE** (1024 (0x400))


</dt> <dd>

WorkOffline

Warteschlangendruckaufträge, wenn kein Drucker verfügbar ist.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**DRUCKER \_ ATTRIBUTE \_ ENABLE \_ BIDI** (2048 (0x800))


</dt> <dd>

EnableBIDI

Aktivieren Sie bidirektionalen Druck.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**DRUCKER \_ \_ \_ NUR ATTRIBUT RAW** (4096 (0x1000))


</dt> <dd>

Nur Rohdatentypaufträge dürfen gespoolt werden.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**DRUCKER \_ \_VERÖFFENTLICHTES ATTRIBUT** (8192 (0x2000))


</dt> <dd>

Veröffentlicht

Veröffentlicht im Netzwerkverzeichnisdienst.

</dd> </dl>

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Operational State \| 003.5", "MIB. IETF \| HOST-RESOURCES-MIB.hrDeviceStatus")
</dt> </dl>

Verfügbarkeit und Status des Geräts.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>Running/Full Power (3) **(Ausführen/Vollbetrieb** (3))


</dt> <dd>

Running or Full Power

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Heruntergestuft** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiesparen – Unbekannt** (13)


</dt> <dd>

Das Gerät befindet sich bekanntermaßen im Energiesparmodus, aber sein genauer Status ist unbekannt.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus – Energiesparmodus** (14)


</dt> <dd>

Das Gerät befindet sich im Energiesparzustand, ist aber weiterhin funktionsfähig und kann eine beeinträchtigte Leistung aufweisen.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus – Standby** (15)


</dt> <dd>

Das Gerät funktioniert nicht, kann aber schnell voll ausgepowert werden.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Stromzyklus** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiesparen – Warnung** (17)


</dt> <dd>

Das Gerät befindet sich in einem Warnungszustand, aber auch im Energiesparmodus.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angehalten** (18)


</dt> <dd>

Das Gerät wird angehalten.

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)


</dt> <dd>

Das Gerät ist nicht bereit.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)


</dt> <dd>

Das Gerät ist nicht konfiguriert.

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Still** (21)


</dt> <dd>

Das Gerät ist still.

</dd> </dl>

</dd> <dt>

**AvailableJobSheets**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.RequiredJobSheets")
</dt> </dl>

Array aller auf einem Drucker verfügbaren Auftragsblätter. Kann auch verwendet werden, um das Banner zu beschreiben, das ein Drucker zu Beginn jedes Auftrags bereitstellen kann, oder andere vom Benutzer angegebene Optionen.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**AveragePagesPerMinute**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Druckrate in der durchschnittlichen Anzahl von Seiten pro Minute, die ein Drucker ausgeben kann.

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indiziert"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md). CapabilityDescriptions", "CIM \_ PrintJob.Finish", "CIM \_ PrintService.Capabilities")
</dt> </dl>

Array von Druckerfunktionen.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Farbdruck** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplexdruck** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Kopien** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Sortierung** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparenzdruck** (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Ausser** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binden** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Schwarz-Weiß-Druck** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Einseitig** (12)


</dt> <dd>

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Zweiseitiger langer Rand** (13)


</dt> <dd>

Two-Sided Long Edge

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Zweiseitiger kurzer Rand** (14)


</dt> <dd>

Two-Sided Short Edge

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Hochformat** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Querformat** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Umgekehrtes Hochformat** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Umgekehrte Querformat** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualität niedrig** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indiziert"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md).**Funktionen**")
</dt> </dl>

Array von Freiformzeichenfolgen, die ausführliche Erläuterungen zu den im **Capabilities-Array** angegebenen Druckerfunktionen bereitstellen. Jeder Eintrag dieses Arrays bezieht sich auf einen Eintrag im **Capabilities-Array,** der sich im gleichen Index befindet.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Kurze Beschreibung eines Objekts– eine einzeilige Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**CharSetsSupported**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.CharSet"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.prtLocalizationCharacterSet")
</dt> </dl>

Array verfügbarer Zeichensätze für die Ausgabe. Zeichenfolgen, die in dieser Eigenschaft bereitgestellt werden, müssen der Semantik und Syntax entsprechen, die in Abschnitt 4.1.2 ("Charset-Parameter") in RFC 2046 (MIME Part 2) angegeben sind und in der IANA-Zeichensatzregistrierung enthalten sind. Beispiele hierfür sind "UTF-8", "us-ASCII" und "iso-8859-1".

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**Comment**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Kommentar für eine Druckwarteschlange.

Beispiel: Farbdrucker

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Win32 Konfigurations-Manager Fehlercode.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**  (0)


</dt> <dd>

Das Gerät funktioniert ordnungsgemäß.

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.** (1)


</dt> <dd>

Das Gerät ist nicht ordnungsgemäß konfiguriert.

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows kann den Treiber für dieses Gerät nicht laden.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder ihr System hat möglicherweise nicht genügend Arbeitsspeicher oder andere Ressourcen.** (3)


</dt> <dd>

Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System hat möglicherweise wenig Arbeitsspeicher oder andere Ressourcen.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder Ihre Registrierung ist möglicherweise beschädigt.** (4)


</dt> <dd>

Das Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die Windows verwaltet werden kann.** (5)


</dt> <dd>

Der Treiber für das Gerät erfordert eine Ressource, die Windows verwaltet werden kann.

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**  (6)


</dt> <dd>

Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiberlader für das Gerät fehlt.** (8)


</dt> <dd>

Das Treiberladegerät für das Gerät fehlt.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die steuernde Firmware die Ressourcen für das Gerät falsch berichtet.** (9)


</dt> <dd>

Das Gerät funktioniert nicht ordnungsgemäß. Die steuernde Firmware berichtet falsch über die Ressourcen für das Gerät.

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.** (10)


</dt> <dd>

Das Gerät kann nicht gestartet werden.

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Fehler bei diesem Gerät.** (11)


</dt> <dd>

Fehler beim Gerät.

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Dieses Gerät kann nicht genügend freie Ressourcen finden, die es verwenden kann.** (12)


</dt> <dd>

Das Gerät kann nicht genügend freie Ressourcen für die Verwendung finden.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows können die Ressourcen dieses Geräts nicht überprüfen.** (13)


</dt> <dd>

Windows können die Ressourcen des Geräts nicht überprüfen.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst dann ordnungsgemäß, wenn Sie Ihren Computer neu starten.** (14)


</dt> <dd>

Das Gerät funktioniert erst dann ordnungsgemäß, wenn der Computer neu gestartet wird.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Enumeration vor liegt.** (15)


</dt> <dd>

Das Gerät funktioniert aufgrund eines möglichen Problems mit der erneuten Enumeration nicht ordnungsgemäß.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows können nicht alle Ressourcen identifizieren, die dieses Gerät verwendet.** (16)


</dt> <dd>

Windows können nicht alle Ressourcen identifizieren, die das Gerät verwendet.

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.** (17)


</dt> <dd>

Das Gerät fordert einen unbekannten Ressourcentyp an.

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.** (18)


</dt> <dd>

Gerätetreiber müssen neu installiert werden.

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler beim Verwenden des VxD-Ladeers.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Ihre Registrierung ist möglicherweise beschädigt.** (20)


</dt> <dd>

Die Registrierung ist möglicherweise beschädigt.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Systemfehler: Versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, lesen Sie ihre Hardwaredokumentation. Windows entfernt dieses Gerät.** (21)


</dt> <dd>

Systemfehler. Wenn das Ändern des Gerätetreibers ineffektiv ist, lesen Sie die Hardwaredokumentation. Windows entfernt das Gerät.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.** (22)


</dt> <dd>

Das Gerät ist deaktiviert.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Systemfehler: Versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, lesen Sie Ihre Hardwaredokumentation.** (23)


</dt> <dd>

Systemfehler. Wenn das Ändern des Gerätetreibers ineffektiv ist, lesen Sie die Hardwaredokumentation.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß oder verfügt nicht über alle installierten Treiber.** (24)


</dt> <dd>

Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß oder verfügt nicht über alle installierten Treiber.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows wird dieses Gerät weiterhin eingerichtet.** (25)


</dt> <dd>

Windows wird das Gerät weiterhin eingerichtet.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows wird dieses Gerät weiterhin eingerichtet.** (26)


</dt> <dd>

Windows wird das Gerät weiterhin eingerichtet.

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokollkonfiguration.** (27)


</dt> <dd>

Das Gerät verfügt nicht über eine gültige Protokollkonfiguration.

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.** (28)


</dt> <dd>

Gerätetreiber sind nicht installiert.

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen zur Verfügung hat.** (29)


</dt> <dd>

Das Gerät ist deaktiviert. Die Gerätefirmware hat nicht die erforderlichen Ressourcen zur Verfügung stellt.

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine IrQ-Ressource (Interrupt Request), die von einem anderen Gerät verwendet wird.** (30)


</dt> <dd>

Das Gerät verwendet eine IRQ-Ressource, die ein anderes Gerät verwendet.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden können.** (31)


</dt> <dd>

Das Gerät funktioniert nicht ordnungsgemäß. Windows die erforderlichen Gerätetreiber können nicht geladen werden.

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **\_ CIM-Schlüssel**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Name der ersten konkreten Klasse, die in der Vererbungskette angezeigt wird, die zum Erstellen einer Instanz verwendet wird. Bei Verwendung mit anderen Schlüsseleigenschaften der -Klasse ermöglicht die -Eigenschaft die eindeutige Identifizierung aller Instanzen dieser Klasse und ihrer Unterklassen.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**CurrentCapabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md).**Funktionen**")
</dt> </dl>

Array von Druckerfunktionen, die derzeit verwendet werden. Ein Eintrag in dieser Eigenschaft muss auch im **Capabilities-Array** aufgeführt werden.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Farbdruck** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplexdruck** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Kopien** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Sortierung** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparenzdruck** (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Ausser** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binden** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Schwarz-Weiß-Druck** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Einseitig** (12)


</dt> <dd>

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Zweiseitiger langer Rand** (13)


</dt> <dd>

Two-Sided Long Edge

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Zweiseitiger kurzer Rand** (14)


</dt> <dd>

Two-Sided Short Edge

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Hochformat** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Querformat** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Umgekehrtes Hochformat** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Umgekehrte Querformat** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualität niedrig** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**CurrentCharSet**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md).**CharSetsSupported**")
</dt> </dl>

Der zeichensatz, der derzeit für die Ausgabe verwendet wird. Zeichenfolgen, die in dieser Eigenschaft bereitgestellt werden, müssen der Semantik und Syntax entsprechen, die in Abschnitt 4.1.2 ("Charset-Parameter") in RFC 2046 (MIME Part 2) angegeben sind und in der IANA-Zeichensatzregistrierung enthalten sind. Beispiele hierfür sind "utf-8", "us-ASCII" und iso-8859-1.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md). LanguagesSupported", "**CIM \_ Printer**.**CurrentMimeType**")
</dt> </dl>

Derzeit verwendete Druckersprache. Die verwendete Sprache muss in der **LanguagesSupported-Eigenschaft** aufgeführt werden.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Libyn** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Zeilendaten** (15)


</dt> <dd>

Linedata

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16)


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**REGIS** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SOLLL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Einfacher Text** (31)


</dt> <dd>

SimpleText

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**DOC** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**LIPS** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnose** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**EXCL** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**LCS** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**XES** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47)


</dt> <dd></dd> <dt>

48
</dt> <dd>

XPS

</dd> <dt>

49
</dt> <dd>

HPGL2

</dd> <dt>

50
</dt> <dd>

PCLXL

</dd> </dl>

</dd> <dt>

**CurrentMimeType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md).**CurrentLanguage**")
</dt> </dl>

Mime-Typ, der derzeit verwendet wird, wenn **CurrentLanguage** ein MIME-Typ ist (Wert = 47).

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**CurrentNaturalLanguage**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md).**NaturalLanguagesSupported**")
</dt> </dl>

Sprache, die der Drucker derzeit für die Verwaltung verwendet. Die hier aufgeführte Sprache muss auch in der **NaturalLanguagesSupported-Eigenschaft** aufgeführt werden.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**CurrentPaperType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md).**PaperTypesAvailable**")
</dt> </dl>

Papiertyp, der vom Drucker verwendet wird. Muss in der von der ISO/IEC 10175 Document Printing Application (DPA) angegebenen Form ausgedrückt werden, die in Anhang C von RFC 1759 (Printer MIB) zusammengefasst ist.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**Standard**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass der Drucker der Standarddrucker ist.

</dd> <dt>

**DefaultCapabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md).**Funktionen**")
</dt> </dl>

Array der standardmäßig verwendeten Druckerfunktionen. Jeder Eintrag im **DefaultCapabilities-Array** muss auch im **Capabilities-Array** aufgeführt werden.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Farbdruck** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplexdruck** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Kopien** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Sortierung** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparenzdruck** (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Ausser** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binden** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Schwarz-Weiß-Druck** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Einseitig** (12)


</dt> <dd>

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Zweiseitiger langer Rand** (13)


</dt> <dd>

Two-Sided Long Edge

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Zweiseitiger kurzer Rand** (14)


</dt> <dd>

Two-Sided Short Edge

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Hochformat** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Querformat** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Umgekehrtes Hochformat** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Umgekehrte Querformat** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualität niedrig** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**DefaultCopies**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl von Kopien, die für einen Auftrag erstellt wurden – sofern nicht anders angegeben.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**DefaultLanguage**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md). LanguagesSupported", "**CIM \_ Printer**.**DefaultMimeType**")
</dt> </dl>

Standarddruckersprache. Die hier aufgeführte Sprache muss auch in der **LanguagesSupported-Eigenschaft** aufgeführt werden.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Libyn** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Zeilendaten** (15)


</dt> <dd>

Linedata

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16)


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**REGIS** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SOLLL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Einfacher Text** (31)


</dt> <dd>

SimpleText

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**DOC** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**LIPS** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnose** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**EXCL** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**LCS** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**XES** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47)


</dt> <dd></dd> <dt>

48
</dt> <dd>

XPS

</dd> <dt>

49
</dt> <dd>

HPGL2

</dd> <dt>

50
</dt> <dd>

PCLXL

</dd> </dl>

</dd> <dt>

**DefaultMimeType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md).**DefaultLanguage**")
</dt> </dl>

Mime-Typ, der derzeit verwendet wird, wenn der **DefaultLanguage-Wert** ein MIME-Typ ist (Wert = 47).

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**DefaultNumberUp**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Druckstreamseiten, die der Drucker auf einem Medienblatt rendert– es sei denn, ein Auftrag gibt etwas anderes an.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**DefaultPaperType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md).**PaperTypesAvailable**")
</dt> </dl>

Vom Drucker verwendeter Papiertyp– es sei denn, ein Druckauftrag gibt einen anderen Papiertyp an. Die Zeichenfolge muss in der Form ausgedrückt werden, die von der ISO/IEC 1017 Document Printing Application (DPA) angegeben wird, die in Anhang C von [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB) zusammengefasst ist.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**DefaultPriority**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Standardprioritätswert, der jedem Druckauftrag zugewiesen ist.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Beschreibung")
</dt> </dl>

Beschreibung eines Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**DetectedErrorState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.hrPrinterDetectedErrorState")
</dt> </dl>

Druckerfehlerinformationen.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

**Kein Fehler** (2)


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

**Low Paper** (3)


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

**Kein Papier** (4)


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

**Niedriger Toner** (5)


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

**Kein Toner** (6)


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

**Door Open** (7)


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

**Jammed** (8)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (9)


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

**Angeforderter Dienst** (10)


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

**Ausgabecontainer voll** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **\_ CIM-Schlüssel**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Eindeutiger Bezeichner des Druckers auf einem System.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**Direkt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True gibt an, dass der Druckauftrag direkt an den Drucker gesendet wird. False gibt an, dass der Druckauftrag gespoolt wird.

</dd> <dt>

**DoCompleteFirst**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True gibt an, dass der Drucker Aufträge startet, deren Spooling abgeschlossen ist. **False** gibt an, dass der Drucker Aufträge in der Reihenfolge startet, in der die Aufträge empfangen werden.

</dd> <dt>

**DriverName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Name des Windows Druckertreibers.

Beispiel: Windows Faxtreiber

</dd> <dt>

**EnableBIDI**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True gibt an, dass der Drucker bidirektional drucken kann.

</dd> <dt>

**EnableDevQueryPrint**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True gibt an, dass der Drucker Dokumente in der Warteschlange enthält, wenn Dokument- und Druckersetups nicht übereinstimmen.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass der in **LastErrorCode** gemeldete Fehler gelöscht wurde.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Informationen zu dem in **LastErrorCode** aufgezeichneten Fehler und Informationen zu Korrekturmaßnahmen, die ausgeführt werden können.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**ErrorInformation**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md).**DetectedErrorState**")
</dt> </dl>

Array mit zusätzlichen Informationen für den aktuellen Fehlerzustand, der in **DetectedErrorState** angegeben ist.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**ExtendedDetectedErrorState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Meldet Standardfehlerinformationen. Zusätzliche Informationen sollten in **DetectedErrorState** aufgezeichnet werden.

Gültige Werte:

<dt>

0 (0x0)
</dt> <dd>

Unbekannt

</dd> <dt>

1 (0x1)
</dt> <dd>

Andere

</dd> <dt>

2 (0x2)
</dt> <dd>

Kein Fehler

</dd> <dt>

3 (0x3)
</dt> <dd>

Wenig Papier

</dd> <dt>

4 (0x4)
</dt> <dd>

Kein Papier

</dd> <dt>

5 (0x5)
</dt> <dd>

Wenig Toner

</dd> <dt>

6 (0x6)
</dt> <dd>

Kein Toner

</dd> <dt>

7 (0x7)
</dt> <dd>

Gerät geöffnet

</dd> <dt>

8 (0x8)
</dt> <dd>

Papierstau

</dd> <dt>

9 (0x9)
</dt> <dd>

Angeforderter Dienst

</dd> <dt>

10 (0xA)
</dt> <dd>

Ausgabeschacht voll

</dd> <dt>

11 (0xB)
</dt> <dd>

Papierproblem

</dd> <dt>

12 (0xC)
</dt> <dd>

Seite kann nicht gedruckt werden

</dd> <dt>

13 (0xD)
</dt> <dd>

Benutzereingriff erforderlich

</dd> <dt>

14 (0xE)
</dt> <dd>

Nicht genügend Arbeitsspeicher

</dd> <dt>

15 (0xF)
</dt> <dd>

Server unbekannt

</dd> </dl>

</dd> <dt>

**ExtendedPrinterStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Statusinformationen für einen Drucker, die sich von den in der **Availability-Eigenschaft** angegebenen Informationen unterscheiden.

<dt>

1 (0x1)
</dt> <dd>

Andere

</dd> <dt>

2 (0x2)
</dt> <dd>

Unbekannt

</dd> <dt>

3 (0x3)
</dt> <dd>

Idle

</dd> <dt>

4 (0x4)
</dt> <dd>

Drucken

</dd> <dt>

5 (0x5)
</dt> <dd>

Aufwärmung

</dd> <dt>

6 (0x6)
</dt> <dd>

Druck beendet

</dd> <dt>

7
</dt> <dd>

Offline

</dd> <dt>

8 (0x8)
</dt> <dd>

Angehalten

</dd> <dt>

9 (0x9)
</dt> <dd>

Fehler

</dd> <dt>

10 (0xA)
</dt> <dd>

Busy

</dd> <dt>

11 (0xB)
</dt> <dd>

Nicht verfügbar

</dd> <dt>

12 (0xC)
</dt> <dd>

Wartend

</dd> <dt>

13 (0xD)
</dt> <dd>

Verarbeitung

</dd> <dt>

14 (0xE)
</dt> <dd>

Initialisierung

</dd> <dt>

15
</dt> <dd>

Energiesparen

</dd> <dt>

16 (0x10)
</dt> <dd>

Löschen ausstehend

</dd> <dt>

17 (0x11)
</dt> <dd>

E/A aktiv

</dd> <dt>

18 (0x12)
</dt> <dd>

Manueller Feed

</dd> </dl>

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True gibt an, dass der Drucker für Netzwerkbenutzer ausgeblendet ist.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.HorizontalResolution"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Pixel pro Zoll")
</dt> </dl>

Horizontale Auflösung des Druckers – in Pixel pro Zoll.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Installationsdatum")
</dt> </dl>

Datum und Uhrzeit der Installation eines Objekts. Das -Objekt kann installiert werden, ohne dass ein Wert in diese Eigenschaft geschrieben wird. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**JobCountSinceLastReset**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Leistungsindikator**
</dt> </dl>

Anzahl der Druckaufträge seit dem letzten Zurücksetzen des Druckers.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**KeepPrintedJobs**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True gibt an, dass der Druckspooler die abgeschlossenen Aufträge nicht löscht.

</dd> <dt>

**LanguagesSupported**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md). MimeTypesSupported", "CIM \_ PrintJob.Language", "CIM \_ PrintService.LanguagesSupported")
</dt> </dl>

Array der nativ unterstützten Drucksprachen.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Libyn** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Zeilendaten** (15)


</dt> <dd>

Linedata

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16)


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**REGIS** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SOLLL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Einfacher Text** (31)


</dt> <dd>

SimpleText

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**DOC** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**LIPS** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnose** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**EXCL** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**LCS** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**XES** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47)


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span id="XPS"></span><span id="xps"></span>**XPS** (48)


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Letzter Fehlercode, der vom logischen Gerät gemeldet wird.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**Lokal**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True gibt an, dass der Drucker nicht an ein Netzwerk angefügt ist. Wenn sowohl die Eigenschaften **Lokal** als auch **Netzwerk** auf **TRUE** festgelegt sind, ist der Drucker ein Netzwerkdrucker.

</dd> <dt>

**Speicherort**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Physischer Speicherort des Druckers.

Beispiel: Bldg. 38, Raum 1164

</dd> <dt>

**MarkingTechnology**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.prtMarkerMarkTech")
</dt> </dl>

Markierungstechnologie, die der Drucker verwendet.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

**Photographische LED** (3)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

**Photographic Zoom** (4)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

**Photographic Other** (5)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

**Impact Moving Head Dot Matrix 9pin** (6)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

**Impact Moving Head Dot Matrix 24pin** (7)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

**Impact Moving Head Dot Matrix Other** (8)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

**Impact Moving Head Fully Formed** (9)


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

**Impact Band** (10)


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

**Impact Other** (11)


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

**Inkjet Aqueous** (12)


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

**Inkjet Solid** (13)


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

**Inkjet Other** (14)


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

**Stift** (15)


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

**Wärmeübertragung** (16)


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

**Temperaturempfindlich** (17)


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

**Therme** (18)


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

**Sonstiges** (19)


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

**Adulterosion** (20)


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

**Static (21)**


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

**Photonische Mikrofiche** (22)


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

**Fotobilderetter** (23)


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

**Foto: Sonstiges** (24)


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

**Ion Deposition** (25)


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

**eBeam** (26)


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

**Typesetter** (27)


</dt> <dd></dd> </dl>

</dd> <dt>

**MaxCopies**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.Copies")
</dt> </dl>

Maximale Anzahl von Kopien, die der Drucker für einen Auftrag erstellen kann.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**MaxNumberUp**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.NumberUp")
</dt> </dl>

Maximale Anzahl von Druckstreamseiten, die der Drucker auf einem Medienblatt rendern kann, z. B. Papier.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**MaxSizeSupported**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.JobSize"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")
</dt> </dl>

Größter Auftrag als Bytestream in Kilobyte, den der Drucker akzeptieren kann. Der Wert 0 (null) gibt an, dass kein Grenzwert festgelegt ist.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**MimeTypesSupported**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-Drucker**](cim-printer.md). LanguagesSupported", "CIM \_ PrintJob.MimeTypes", "CIM \_ PrintService.MimeTypesSupported")
</dt> </dl>

Array mit ausführlichen Erklärungen des MIME-Typs, die der Drucker unterstützt. Wenn Daten bereitgestellt werden, muss der Wert 47 ("MIME") in der **LanguagesSupported-Eigenschaft** enthalten sein.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Name des Druckers.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**NaturalLanguagesSupported**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.NaturalLanguage")
</dt> </dl>

Array von Sprachen, die für Zeichenfolgen unterstützt werden, die der Drucker für die Ausgabe von Verwaltungsinformationen verwendet. Muss [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt)entsprechen. Beispielsweise wird "en" für Englisch verwendet.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

</dd> <dt>

**Netzwerk**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True gibt an, dass der Drucker ein Netzwerkdrucker ist. Wenn sowohl die Eigenschaften **Lokal** als auch **Netzwerk** auf **TRUE** festgelegt sind, ist der Drucker ein Netzwerkdrucker.

</dd> <dt>

**PaperSizesSupported**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array der Papiertypen, die der Drucker unterstützt.

Diese Eigenschaft wird vom [**\_ CIM-Drucker**](cim-printer.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span id="A"></span><span id="a"></span>**A** (2)


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span id="B"></span><span id="b"></span>**B** (3)


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span id="C"></span><span id="c"></span>**C** (4)


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span id="D"></span><span id="d"></span>**D** (5)


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span id="E"></span><span id="e"></span>**E** (6)


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Buchstabe** (7)


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**NA-10x13-Envelope** (9)


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**NA-9x12-Envelope** (10)


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**NA-Number-10-Envelope** (11)


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**NA-7x9-Envelope** (12)


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**NA-9x11-Envelope** (13)


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**NA-10x14-Envelope** (14)


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**NA-Number-9-Envelope** (15)


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**NA-6x9-Envelope** (16)


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**NA-10x15-Envelope** (17)


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span id="A0"></span><span id="a0"></span>**A0** (18)


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span id="A1"></span><span id="a1"></span>**A1** (19)


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span id="A2"></span><span id="a2"></span>**A2** (20)


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span id="A3"></span><span id="a3"></span>**A3** (21)


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span id="A4"></span><span id="a4"></span>**A4** (22)


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span id="A5"></span><span id="a5"></span>**A5** (23)


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span id="A6"></span><span id="a6"></span>**A6** (24)


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span id="A7"></span><span id="a7"></span>**A7** (25)


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span id="A8"></span><span id="a8"></span>**A8** (26)


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span id="B0"></span><span id="b0"></span>**B0** (28)


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span id="B1"></span><span id="b1"></span>**B1** (29)


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span id="B2"></span><span id="b2"></span>**B2** (30)


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span id="B3"></span><span id="b3"></span>**B3** (31)


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span id="B4"></span><span id="b4"></span>**B4** (32)


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span id="B5"></span><span id="b5"></span>**B5** (33)


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span id="B6"></span><span id="b6"></span>**B6** (34)


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span id="B7"></span><span id="b7"></span>**B7** (35)


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span id="B8"></span><span id="b8"></span>**B8** (36)


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span id="B9"></span><span id="b9"></span>**B9** (37)


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span id="B10"></span><span id="b10"></span>**B10** (38)


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span id="C0"></span><span id="c0"></span>**C0** (39)


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span id="C1"></span><span id="c1"></span>**C1** (40)


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)


</dt> <dd>

C2

</dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span id="C4"></span><span id="c4"></span>**C4** (42)


</dt> <dd>

C3

</dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span id="C5"></span><span id="c5"></span>**C5** (43)


</dt> <dd>

C4

</dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span id="C6"></span><span id="c6"></span>**C6** (44)


</dt> <dd>

C5

</dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span id="C7"></span><span id="c7"></span>**C7** (45)


</dt> <dd>

C6

</dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span id="C8"></span><span id="c8"></span>**C8** (46)


</dt> <dd>

C7

</dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**ISO-designiert** (47)


</dt> <dd>

C8

</dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)


</dt> <dd>

ISO-Designated

</dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)


</dt> <dd>

JIS B0

</dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)


</dt> <dd>

JIS B1

</dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)


</dt> <dd>

JIS B2

</dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)


</dt> <dd>

JIS B3

</dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)


</dt> <dd>

JIS B4

</dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)


</dt> <dd>

JIS B5

</dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)


</dt> <dd>

JIS B6

</dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)


</dt> <dd>

JIS B7

</dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)


</dt> <dd>

JIS B8

</dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)


</dt> <dd>

JIS B9

</dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**NA-Letter** (59)


</dt> <dd>

JIS B10

</dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**NA-Legal** (60)


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-Envelope** (61)


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-Envelope** (62)


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-Envelope** (63)


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-Envelope** (64)


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-Envelope** (65)


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-Envelope** (66)


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designated-Long-Envelope** (67)


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Tenumschlag** (68)


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Blatt** (70)


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Rechnung** (71)


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Ledger** (72)


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73)


</dt> <dd></dd> </dl>

</dd> <dt>

**PaperTypesAvailable**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.RequiredPaperType", "CIM \_ PrintService.PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.prtInputMediaName")
</dt> </dl>

Array von Papiertypen, die derzeit auf dem Drucker verfügbar sind. Jede Zeichenfolge muss in dem Format ausgedrückt werden, das von ISO/IEC 10175 Document Printing Application (DPA) angegeben wird, das in Anhang C von [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Drucker-MIB) zusammengefasst ist. Jedes in dieser Eigenschaft identifizierte Papierformat muss auch in der **PaperSizesSupported-Eigenschaft angezeigt** werden.

Diese Eigenschaft wird vom [**CIM-Drucker \_ geerbt.**](cim-printer.md)

Beispiel: iso-a4-farbig

</dd> <dt>

**Parameter**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Optionale Parameter für den Druckprozessor.

Beispiel: "Copies=2"

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Windows Plug & Play Gerätebezeichner des logischen Geräts.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

Beispiel: \* PNP030b

</dd> <dt>

**Portname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Port, der zum Übertragen von Daten an einen Drucker verwendet wird. Wenn ein Drucker mit mehreren Ports verbunden ist, werden die Namen der einzelnen Ports durch Kommas getrennt.

Beispiel: LPT1:, LPT2:, LPT3:

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.

Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)


</dt> <dd>

Die Energieverwaltungsfunktionen sind derzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiesparmodi** (4)


</dt> <dd>

Das Gerät kann seinen Energiezustand basierend auf der Nutzung oder anderen Kriterien ändern.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)


</dt> <dd>

Die [**SetPowerState-Methode**](setpowerstate-method-in-class-cim-controller.md) wird unterstützt. Diese Methode befindet sich in der übergeordneten **CIM \_ LogicalDevice-Klasse** und kann implementiert werden. Weitere Informationen finden Sie unter [Entwerfen von MOF-Klassen (Managed Object Format).](../wmisdk/designing-managed-object-format--mof--classes.md)

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**PowerCycling unterstützt** (6)


</dt> <dd>

Die [**SetPowerState-Methode**](setpowerstate-method-in-class-cim-controller.md) kann aufgerufen werden, wobei der *PowerState-Parameter* auf 5 (Power Cycle) festgelegt ist.

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Timed Power On Supported (7) **(Zeitiertes Einschalten unterstützt** (7)


</dt> <dd>

Timed Power-On Supported

Die [**SetPowerState-Methode**](setpowerstate-method-in-class-cim-controller.md) kann aufgerufen werden, wobei der *PowerState-Parameter* für das Einschalten auf 5 (Power Cycle) und *Time* auf ein bestimmtes Datum und eine bestimmte Uhrzeit oder ein bestimmtes Intervall festgelegt ist.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass die Leistung des Geräts verwaltet werden kann, was bedeutet, dass es in den Unterbrechungsmodus versetzt werden kann. Die -Eigenschaft gibt nicht an, dass Energieverwaltungsfunktionen aktiviert sind, sondern nur, dass das logische Gerät energieverwaltungsfähig ist.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**PrinterPaperNames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von Papiergrößen, die vom Drucker unterstützt werden. Die vom Drucker angegebenen Namen werden verwendet, um unterstützte Papiergrößen darzustellen.

Beispiel: B5 (JIS)

</dd> <dt>

**PrinterState**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Veraltet**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Einer der möglichen Zustände im Zusammenhang mit diesem Drucker. Diese Eigenschaft ist veraltet. Verwenden Sie anstelle dieser Eigenschaft **PrinterStatus**.

<dt>

0
</dt> <dd>

Leerlauf: Weitere Informationen finden Sie weiter unten im Abschnitt "Hinweise".

</dd> <dt>

1
</dt> <dd>

Angehalten

</dd> <dt>

2
</dt> <dd>

Fehler

</dd> <dt>

3
</dt> <dd>

Löschen ausstehend

</dd> <dt>

4
</dt> <dd>

Papierstaus

</dd> <dt>

5
</dt> <dd>

Paper Out

</dd> <dt>

6
</dt> <dd>

Manueller Feed

</dd> <dt>

7
</dt> <dd>

Papierproblem

</dd> <dt>

8
</dt> <dd>

Offline

</dd> <dt>

9
</dt> <dd>

E/A aktiv

</dd> <dt>

10
</dt> <dd>

Busy

</dd> <dt>

11
</dt> <dd>

Drucken

</dd> <dt>

12
</dt> <dd>

Ausgabeschacht voll

</dd> <dt>

13
</dt> <dd>

Nicht verfügbar

</dd> <dt>

14
</dt> <dd>

Wartend

</dd> <dt>

15
</dt> <dd>

Verarbeitung

</dd> <dt>

16
</dt> <dd>

Initialisierung

</dd> <dt>

17
</dt> <dd>

Aufwärmung

</dd> <dt>

18
</dt> <dd>

Toner Low

</dd> <dt>

19
</dt> <dd>

Kein Toner

</dd> <dt>

20
</dt> <dd>

Seite Punt

</dd> <dt>

21
</dt> <dd>

Benutzereingriff erforderlich

</dd> <dt>

22
</dt> <dd>

Nicht genügend Arbeitsspeicher

</dd> <dt>

23
</dt> <dd>

Gerät geöffnet

</dd> <dt>

24
</dt> <dd>

Server \_ unbekannt

</dd> <dt>

25
</dt> <dd>

Stromsparen

</dd> </dl>

</dd> <dt>

**PrinterStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.hrPrinterStatus")
</dt> </dl>

Statusinformationen für einen Drucker, die sich von den in der Eigenschaft Verfügbarkeit des logischen Geräts **angegebenen Informationen** unterscheiden.

Diese Eigenschaft wird vom [**CIM-Drucker \_ geerbt.**](cim-printer.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Leerlauf** (3)


</dt> <dd>

Leerlauf: Weitere Informationen finden Sie weiter unten im Abschnitt "Hinweise".

</dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Drucken** (4)


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Aufwärmung** (5)


</dt> <dd>

Aufwärm

</dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Beendeter Druck** (6)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**PrintJobDataType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Datentyp eines Druckauftrags, der auf das Windows Druckgerät wartet.

</dd> <dt>

**Printprocessor**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Name des Druckspoolers, der Druckaufträge verarbeitet.

Beispiel: SPOOLSS.DLL

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Priorität des Druckers. Aufträge auf einem Drucker mit höherer Priorität werden zuerst geplant.

</dd> <dt>

**Veröffentlicht**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True **gibt an,** dass der Drucker im Netzwerkverzeichnisdienst veröffentlicht wird.

</dd> <dt>

**In Warteschlange**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True **gibt an,** dass der Drucker Druckaufträge puffert und in die Warteschlange einreiht.

</dd> <dt>

**RawOnly**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True **gibt an,** dass der Drucker nur rohe Daten akzeptiert, die in den Pool poolt werden sollen.

</dd> <dt>

**SeparatorFile**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Name der Datei, die zum Erstellen einer Trennzeichenseite verwendet wird. Diese Seite wird verwendet, um druckaufträge zu trennen, die an den Drucker gesendet werden.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name des Servers, der den Drucker steuert. Wenn diese Zeichenfolge **NULL ist,** wird der Drucker lokal gesteuert.

</dd> <dt>

**Freigegeben**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True **gibt an,** dass der Drucker als freigegebene Netzwerkressource verfügbar ist.

</dd> <dt>

**ShareName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Freigabename des Windows-basierten Druckgeräts.

Beispiel: \\ \\ "PRINTSERVER1 \\ PRINTER2"

</dd> <dt>

**SpoolEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Veraltet**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Diese Eigenschaft ist veraltet. nicht verwenden. True **gibt an,** dass das Spoolen für den Drucker aktiviert ist.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Datum und Uhrzeit, zu der ein Drucker mit dem Drucken eines Auftrags beginnen kann, wenn der Drucker auf den Druck zu bestimmten Zeiten beschränkt ist. Dieser Wert wird als die Zeit ausgedrückt, die seit 12:00 Uhr GMT (Greenwich Mean Time) verstrichen ist.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene betriebsbereite und nicht betriebsbereite Status definiert werden. Zu den Betriebsstatus  **zählen: OK,** Heruntergestuft und Fehler vor dem Ausfall **(ein** Element, z. B. ein SMART-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber es wird ein Fehler in naher Zukunft vorhergesagt). Zu den nicht operativen Status zählen: **Fehler**, **Starting**, **Stopping** und **Service**. Letzteres, **Der Dienst,** kann während der Spiegelung eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen administrativen Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder **OK** noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Heruntergestuft** ("Heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Wird** gestartet ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Wird beendet** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Striche** ("Strich")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Operational State \| 003.3")
</dt> </dl>

Status des logischen Geräts. Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (**Nicht** zutreffend ) verwendet werden.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (4)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Nicht zutreffend** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-System**](cim-system.md).**CreationClassName**"), [**\_ CIM-Schlüssel**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Der Wert der **CreationClassName-Eigenschaft** des Bereichscomputers.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-System**](cim-system.md).**Name**"), [**\_ CIM-Schlüssel**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Name des Bereichssystems.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der letzten Zurücksetzung des Druckers.

Diese Eigenschaft wird vom [**CIM-Drucker \_ geerbt.**](cim-printer.md)

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Datum und Uhrzeit, zu der ein Drucker den letzten Auftrag drucken kann, wenn der Drucker auf das Drucken zu bestimmten Zeiten beschränkt ist. Dieser Wert wird als die Zeit ausgedrückt, die seit 12:00 Uhr GMT (Greenwich Mean Time) verstrichen ist.

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.HorizontalResolution"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Pixel pro Zoll")
</dt> </dl>

Vertikale Auflösung des Druckers in Pixel pro Zoll.

Diese Eigenschaft wird vom [**CIM-Drucker \_ geerbt.**](cim-printer.md)

</dd> <dt>

**WorkOffline**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True **gibt an,** dass Druckaufträge auf dem Computer in die Warteschlange gestellt werden können, wenn der Drucker offline ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ Win32-Druckerklasse** wird vom [**CIM-Drucker \_ abgeleitet.**](cim-printer.md) Vor dem Aufrufen von [**SWbemObject.Put \_**](../wmisdk/swbemobject-put-.md) oder [**IWbemServices::P utInstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) für eine **Win32 \_ Printer-Instanz** muss die **Berechtigung SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** für Visual Basic und LoadDriver für Skriptmoniker) aktiviert werden. Weitere Informationen finden Sie unter [**Privilege Constants**](../wmisdk/privilege-constants.md) und [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md). Das folgende VBScript-Codebeispiel zeigt, wie sie die **Berechtigung SetLoadDriverPrivilege im** Skript aktivieren.

Verwenden Sie für die Arbeit mit MSCS-Druckerclustern die prnadmin.dll Assembly oder den .NET Framework [System.Printing-Namespace.](/dotnet/api/system.printing)


```VB
Set objPrinter = GetObject("winmgmts:{impersonationLevel=Impersonate,(LoadDriver)}!//./Root/CIMv2:Win32_Printer")
```



Windows verwendet die Anmeldeinformationen des Benutzers, der das Skript ausgeführt, um zu bestimmen, welche Drucker verfügbar sind. Wenn Sie ein Skript remote ausführen, können Sie daher möglicherweise nur auf jeden Drucker zugreifen, der für Ihr Benutzerkonto auf diesem Remotesystem verfügbar ist.

Sie können die **\_ Win32-Druckerklasse** nicht für Drucker in einem MSCS-Druckercluster verwenden. Stattdessen müssen Sie möglicherweise entweder das PrinterAdmin-Tool (PrnAdmin.dll) oder den .NET Framework [System.Printing-Namespace](/dotnet/api/system.printing) verwenden.

> [!Note]  
> Wenn Sie **PrinterStatus** = 3 oder **PrinterState** = 0 abrufen, überträgt der Druckertreiber möglicherweise keine genauen Informationen in WMI. WMI ruft die Druckerinformationen aus dem spoolsv.exe ab. Es ist möglich, dass der Druckertreiber seinen Status nicht an den Spooler berichtet. In diesem Fall meldet **der Win32-Drucker \_** den Drucker als **Leerlauf.**

 

## <a name="examples"></a>Beispiele

Das [Ps Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery verwendet **Win32 \_ Printer** für die Interaktion mit dem Visio-Automatisierungsmodell, um eine Visio zu erstellen.

Das [PowerShell-Remote-PC-Infoskript](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) verwendet eine Reihe von Klassen, einschließlich **Win32 \_ Printer,** um Informationen zu einem Remotecomputer abzurufen.

Das folgende PowerShell-Codebeispiel zeigt, wie Sie den Standarddrucker des lokalen Computers bestimmen.


```PowerShell
Get-WmiObject win32_printer | %{if ($_.default) {$_}}
```



Im folgenden VBScript-Codebeispiel wird beschrieben, wie Druckerstatistiken aus Instanzen von **Win32 Printer abgerufen \_ werden.**


```VB
Set PrinterSet = GetObject("winmgmts:").InstancesOf ("Win32_Printer")
If (PrinterSet.Count = 0 ) Then WScript.Echo "No Printers Installed!"
for each Printer in PrinterSet
   if Printer.PrinterStatus = 3 then WScript.Echo Printer.Name & Chr(13) & "Status:  Idle"
   if Printer.PrinterStatus = 4 then WScript.Echo Printer.Name & Chr(13) & "Status:  Printing"
   
next
```



Im folgenden Perl-Codebeispiel wird beschrieben, wie Druckerstatistiken aus Instanzen des **Win32-Druckers abgerufen \_ werden.**


```
use strict;
use Win32::OLE;

my $PrinterSet;

eval { $PrinterSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf ("Win32_Printer"); };
unless($@)
{
   if ($PrinterSet->{Count} == 0) 
   {
      print "No Printers Installed!\n";
   }

   foreach my $PrinterInst (in $PrinterSet)
   {
      if ($PrinterInst->{PrinterStatus} == 3) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Idle\n";
      }
      if ($PrinterInst->{PrinterStatus} == 4) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Printing\n";
      }
   }
}
else
{
   print STDERR Win32::OLE->LastError, "\n";
}
```



Das folgende VBScript-Codebeispiel zeigt, wie Sie den Namen des Standarddruckers für einen Computer abrufen.


```VB
strComputer = "."
Set objWMIService = GetObject( "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colInstalledPrinters =  objWMIService.ExecQuery ("Select * from Win32_Printer")
For Each objPrinter in colInstalledPrinters

    If objPrinter.Default = "True" Then 
      Wscript.Echo "Name: " & objPrinter.Name
    End If
Next
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Drucker**](cim-printer.md)
</dt> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> <dt>

[WMI-Aufgaben: Drucker und Drucken](../wmisdk/wmi-tasks--printers-and-printing.md)
</dt> </dl>

 

 
