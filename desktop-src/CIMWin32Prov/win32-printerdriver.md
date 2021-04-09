---
description: Die \_ WMI-Klasse von Win32 PrinterDriver stellt die Treiber für eine Win32- \_ Drucker Instanz dar.
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
ms.openlocfilehash: 615d6561e12f67edee34e0de84dade12f250e0f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861172"
---
# <a name="win32_printerdriver-class"></a>Win32 \_ PrinterDriver-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) von **Win32 \_ PrinterDriver** stellt die Treiber für eine [**Win32- \_ Drucker**](win32-printer.md) Instanz dar.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften, schließt jedoch Methoden aus. Referenzinformationen zu Methoden finden Sie in der Tabelle mit den Methoden in diesem Thema.

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

Die **Win32 \_ PrinterDriver** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ PrinterDriver** -Klasse verfügt über diese Methoden.



| Methode                                                                           | BESCHREIBUNG                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| [**Addprinterdriver**](addprinterdriver-method-in-class-win32-printerdriver.md) | Erstellt einen neuen Druckertreiber.<br/> |
| [**Start Service**](startservice-method-in-class-win32-printerdriver.md)         | Startet den Druckdienst.<br/>         |
| [**Stop Service**](stopservice-method-in-class-win32-printerdriver.md)           | Beendet den Druckdienst.<br/>          |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ PrinterDriver** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**ConfigFile**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Konfigurationsdatei für diesen Druckertreiber.

Beispiel: "pscrptui.dll"

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Class Name")
</dt> </dl>

Der Name der Klasse oder der Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften dieser Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.

</dd> <dt>

**Datendatei**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) (CIM \_ datafile. filename)
</dt> </dl>

Die Datendatei für diesen Druckertreiber.

Beispiel: "qms810. PPD"

</dd> <dt>

**Defaultdatatype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Standard Datentyp für diesen Druckertreiber.

Beispiel: "EMF"

</dd> <dt>

**Dependentfiles**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array abhängiger Dateien für diesen Druckertreiber.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Kommentar, der den Link beschreibt.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**DriverPath "**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) (CIM \_ datafile. Path)
</dt> </dl>

Der Pfad für diesen Druckertreiber.

Beispiel: "C: \\ \\ Drivers \\ \\pscript.dll"

</dd> <dt>

**FilePath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Pfad zur verwendeten INF-Datei.

Beispiel: "c: \\ \\ Temp \\ \\ Driver"

</dd> <dt>

**HelpFile**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Hilfedatei für diesen Druckertreiber.

Beispiel: "PSCRPTUI. hlp"

</dd> <dt>

**InfName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Name der verwendeten INF-Datei. Standardmäßig wird eine vom Betriebssystem bereitgestellte Drucker-INF-Datei verwendet. Ein anderer Dateiname wird verwendet, wenn der Treiber direkt vom Hersteller des Druckers und nicht vom Betriebssystem bereitgestellt wird.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")
</dt> </dl>

Datum und Uhrzeit der Installation des-Objekts. Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**MonitorName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Monitors für diesen Druckertreiber.

Beispiel: "PJL-Monitor"

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](../wmisdk/key-qualifier.md)
</dt> </dl>

Treiber Name für diesen Drucker. Dabei handelt es sich um einen zusammengesetzten Schlüssel, der aus den Werten **Name**, **Version** und **SupportedPlatform** besteht.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) geerbt und überschreibt die **namens** Definition in dieser Klasse.

</dd> <dt>

**Oemurl**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

World Wide Web (www) Link zur Website des Druckerherstellers. Beachten Sie, dass diese Eigenschaft nicht aufgefüllt wird, wenn die Win32. inf-Datei verwendet wird, und gilt nur für Treiber, die direkt vom Hersteller bereitgestellt werden.

</dd> <dt>

**Gestartet**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Started")
</dt> </dl>

**True** gibt an, dass der Dienst gestartet wird. Wenn der Wert **false** ist, wird der Dienst beendet.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Start Modus")
</dt> </dl>

Der Start Modus des Dienstanbieter wird automatisch von einem Betriebssystem gestartet oder nur bei Anforderung gestartet.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.

Folgende Werte sind möglich:

<dl> <dd>Schem</dd> <dd>Manual</dd> </dl>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

**Automatisch** ("automatisch")


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

**Manuell** ("manuell")


</dt> <dd></dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen). Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der letztere Dienst kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

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

Herunter **gestuft ("** heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred-** Fehler ("pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

Wird **gestartet** ("wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

Wird **beendet ("wird angehalten** ")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Betont** ("gestresst")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Nicht wiederherstellen** ("nicht wiederherstellen")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorene** Kommunikations ("verlorene Kommunikations-")


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportedPlatform**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Betriebsumgebungen, für die der Treiber vorgesehen ist.

Beispiel: "Windows NT x86".

</dd> <dt>

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("System Klassenname")
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs Systems.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) (" System Name ")
</dt> </dl>

Der Name des Systems, das den Dienst hostet.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Betriebssystemversion für den Druckertreiber.

<dt>

<span id="3"></span>

<span id="3"></span>**€**


</dt> <dd>

Win2k

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32-Klasse \_ PrinterDriver** wird vom [**CIM- \_ Dienst**](cim-service.md) abgeleitet, der von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet wird.

Benutzer können einen Druckertreiber deinstallieren, indem Sie eine entsprechende Instanz dieser Klasse löschen. Zu diesem Zweck muss für den aufrufenden Prozess die **SeLoadDriverPrivilege** -Berechtigung festgelegt sein, um eine Instanz dieser Klasse löschen zu können.

## <a name="examples"></a>Beispiele

Im VBScript-Beispiel zum [Verwalten von Drucker-und Druckertreibern](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) werden Druckertreiber und Drucker Anschlüsse verwaltet.

In den [TechNet-Foren](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) wird beschrieben, wie ein Drucker erstellt und Treiber von einem Server hochgeladen werden.

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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Dienst**](./cim-service.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
