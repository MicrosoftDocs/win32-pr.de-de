---
description: Die \_ WMI-Klasse Win32 PrinterDriver stellt die Treiber für eine \_ Win32-Druckerinstanz dar.
ms.assetid: baf48bbf-60a3-4d9b-93b7-c1b22518a9c1
ms.tgt_platform: multiple
title: Win32_PrinterDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver
- Win32_PrinterDriver.Caption
- Win32_PrinterDriver.ConfigFile
- Win32_PrinterDriver.CreationClassName
- Win32_PrinterDriver.DataFile
- Win32_PrinterDriver.DefaultDataType
- Win32_PrinterDriver.DependentFiles
- Win32_PrinterDriver.Description
- Win32_PrinterDriver.DriverPath
- Win32_PrinterDriver.FilePath
- Win32_PrinterDriver.HelpFile
- Win32_PrinterDriver.InfName
- Win32_PrinterDriver.InstallDate
- Win32_PrinterDriver.MonitorName
- Win32_PrinterDriver.Name
- Win32_PrinterDriver.OEMUrl
- Win32_PrinterDriver.Started
- Win32_PrinterDriver.StartMode
- Win32_PrinterDriver.Status
- Win32_PrinterDriver.SupportedPlatform
- Win32_PrinterDriver.SystemCreationClassName
- Win32_PrinterDriver.SystemName
- Win32_PrinterDriver.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f28958436ba7ff87aed139bf58129f028c5c3e008f8cc0f291bc3b37091fc5d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971870"
---
# <a name="win32_printerdriver-class"></a>Win32 \_ PrinterDriver-Klasse

Die **WMI-Klasse \_ Win32 PrinterDriver** [stellt](../wmisdk/retrieving-a-class.md) die Treiber für eine [**Win32-Druckerinstanz \_**](win32-printer.md) dar.

Die folgende Syntax wird von MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften, schließt jedoch Methoden aus. Referenzinformationen zu Methoden finden Sie in der Tabelle der Methoden in diesem Thema.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_PrinterDriver : CIM_Service
{
  string   Caption;
  string   ConfigFile;
  string   CreationClassName;
  string   DataFile;
  string   DefaultDataType;
  string   DependentFiles[];
  string   Description;
  string   DriverPath;
  string   FilePath;
  string   HelpFile;
  string   InfName;
  datetime InstallDate;
  string   MonitorName;
  string   Name;
  string   OEMUrl;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SupportedPlatform;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Version;
};
```

## <a name="members"></a>Member

Die **Win32 \_ PrinterDriver-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ PrinterDriver-Klasse** verfügt über diese Methoden.



| Methode                                                                           | Beschreibung                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| [**AddPrinterDriver**](addprinterdriver-method-in-class-win32-printerdriver.md) | Erstellt einen neuen Druckertreiber.<br/> |
| [**Startservice**](startservice-method-in-class-win32-printerdriver.md)         | Startet den Druckdienst.<br/>         |
| [**StopService**](stopservice-method-in-class-win32-printerdriver.md)           | Beendet den Druckdienst.<br/>          |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ PrinterDriver-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Kurze Beschreibung des -Objekts– eine einzeilenbasierte Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Configfile**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Konfigurationsdatei für diesen Druckertreiber.

Beispiel: "pscrptui.dll"

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](../wmisdk/standard-wmi-qualifiers.md) [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Klassenname")
</dt> </dl>

Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit den anderen Schlüsseleigenschaften dieser Klasse ermöglicht diese Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird vom [**CIM-Dienst \_ geerbt.**](cim-service.md)

</dd> <dt>

**Datafile**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM \_ DataFile.FileName)
</dt> </dl>

Datendatei für diesen Druckertreiber.

Beispiel: "qms810.ppd"

</dd> <dt>

**DefaultDataType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Standarddatentyp für diesen Druckertreiber.

Beispiel: "EMF"

</dd> <dt>

**DependentFiles**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von abhängigen Dateien für diesen Druckertreiber.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Kommentar, der den Link beschreibt.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**DriverPath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM \_ DataFile.Path)
</dt> </dl>

Pfad für diesen Druckertreiber.

Beispiel: "C: \\ \\ Treiber \\ \\pscript.dll"

</dd> <dt>

**Filepath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Pfad zur verwendeten INF-Datei.

Beispiel: "c: \\ \\ temp \\ \\ driver"

</dd> <dt>

**Helpfile**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Hilfedatei für diesen Druckertreiber.

Beispiel: "pscrptui.hlp"

</dd> <dt>

**InfName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Name der verwendeten INF-Datei. Standardmäßig wird eine vom Betriebssystem bereitgestellte Drucker-INF-Datei verwendet. Ein anderer Dateiname wird verwendet, wenn der Treiber direkt vom Hersteller des Druckers und nicht vom Betriebssystem bereitgestellt wird.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Installation date")
</dt> </dl>

Datum und Uhrzeit der Installation des Objekts. Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**MonitorName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name des Monitors für diesen Druckertreiber.

Beispiel: "PJL-Monitor"

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](../wmisdk/key-qualifier.md)
</dt> </dl>

Treibername für diesen Drucker. Dies ist ein zusammengesetzter Schlüssel, der aus den Werten **Name,** **Version** und **SupportedPlatform** besteht.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) geerbt und überschreibt die **Name-Definition** in dieser Klasse.

</dd> <dt>

**OEMUrl**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

World Wide Web Link (WWW) zur Website des Druckerherstellers. Beachten Sie, dass diese Eigenschaft nicht aufgefüllt wird, wenn die Win32.inf-Datei verwendet wird. Sie gilt nur für Treiber, die direkt vom Hersteller bereitgestellt werden.

</dd> <dt>

**Begann**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")
</dt> </dl>

True gibt an, dass der Dienst gestartet wird. False gibt an, dass der Dienst beendet wird.

Diese Eigenschaft wird vom [**\_ CIM-Dienst**](cim-service.md)geerbt.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Startmodus")
</dt> </dl>

Der Startmodus des Diensts wird automatisch von einem Betriebssystem gestartet oder nur bei Anforderung gestartet.

Diese Eigenschaft wird vom [**\_ CIM-Dienst**](cim-service.md)geerbt.

Folgende Werte sind möglich:

<dl> <dd>"Automatisch"</dd> <dd>"Manuell"</dd> </dl>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

**Automatisch** ("Automatisch")


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

**Manuell** ("Manuell")


</dt> <dd></dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs- und Nichtoperationsstatus definiert werden. Betriebsstatus: "OK", "Heruntergestuft" und "Pred Fail" (ein Element, z. B. ein SMART-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, sagt aber einen Fehler in naher Zukunft vorher). Nichtoperationale Status: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann beim Spiegelungsresilvering eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Verwaltungsaufgaben angewendet werden. Nicht alle dieser Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

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

**Wird gestartet** ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Beenden** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Mannslast** ("1000")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorenes Komma** ("Verlorenes Komma")


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportedPlatform**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Betriebsumgebungen, für die der Treiber vorgesehen ist.

Beispiel: "Windows NT x86".

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-System**](cim-system.md).**CreationClassName**"), [**\_ CIM-Schlüssel,**](../wmisdk/standard-wmi-qualifiers.md) [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Systemklassenname")
</dt> </dl>

Der Name der Erstellungsklasse des Bereichssystems.

Diese Eigenschaft wird vom [**\_ CIM-Dienst**](cim-service.md)geerbt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-System**](cim-system.md).**Name**"), [**\_ CIM-Schlüssel,**](../wmisdk/standard-wmi-qualifiers.md) [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Systemname")
</dt> </dl>

Name des Systems, das diesen Dienst hostet.

Diese Eigenschaft wird vom [**\_ CIM-Dienst**](cim-service.md)geerbt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Betriebssystemversion für den Druckertreiber.

<dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Win2k

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ PrinterDriver-Klasse** wird vom [**\_ CIM-Dienst**](cim-service.md) abgeleitet, der von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet wird.

Benutzer können einen Druckertreiber deinstallieren, indem sie eine entsprechende Instanz dieser Klasse löschen. Hierzu muss für den aufrufenden Prozess die **SeLoadDriverPrivilege-Berechtigung** festgelegt sein, um eine Instanz dieser Klasse zu löschen.

## <a name="examples"></a>Beispiele

Im VBScript-Beispiel [Drucker- und Druckertreiber verwalten](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) werden Druckertreiber und Druckerports verwaltet.

In der folgenden [Diskussion in den TechNet-Foren](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) wird beschrieben, wie Sie einen Drucker erstellen und Treiber von einem Server hochladen.

Im folgenden VBScript-Beispiel werden alle Druckertreiber aufgelistet, die auf einem Computer installiert wurden.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrinterDriver") 
 
For each objPrinter in colInstalledPrinters 
    Wscript.Echo "Configuration File: " & objPrinter.ConfigFile 
    Wscript.Echo "Data File: " & objPrinter.DataFile 
    Wscript.Echo "Description: " & objPrinter.Description 
    Wscript.Echo "Driver Path: " & objPrinter.DriverPath 
    Wscript.Echo "File Path: " & objPrinter.FilePath 
    Wscript.Echo "Help File: " & objPrinter.HelpFile 
    Wscript.Echo "INF Name: " & objPrinter.InfName 
    Wscript.Echo "Monitor Name: " & objPrinter.MonitorName 
    Wscript.Echo "Name: " & objPrinter.Name 
    Wscript.Echo "OEM Url: " & objPrinter.OEMUrl 
    Wscript.Echo "Supported Platform: " & objPrinter.SupportedPlatform 
    Wscript.Echo "Version: " & objPrinter.Version 
Next 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Dienst**](./cim-service.md)
</dt> <dt>

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
