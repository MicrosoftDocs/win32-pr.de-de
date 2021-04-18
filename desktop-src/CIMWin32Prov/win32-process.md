---
Description: Der Win32- \_ Prozess&\# 32; Die WMI-Klasse stellt einen Prozess in einem Betriebssystem dar.
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Win32_Process-Klasse
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371080"
---
# <a name="win32_process-class"></a>Win32- \_ Prozess Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32- \_ Prozess** stellt einen Prozess in einem Betriebssystem dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

> [!NOTE]
> Eine allgemeine Erörterung von Prozessen und Threads in Windows finden Sie im Thema [Prozesse und Threads](/ProcThread/processes-and-threads.md).

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a>Member

Die **Win32- \_ Prozess** Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32- \_ Prozess** Klasse verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachDebugger**](attachdebugger-method-in-class-win32-process.md)   | Startet den aktuell registrierten Debugger für einen Prozess.<br/>                                                                                                                                                                                                                      |
| [**Stelle**](create-method-in-class-win32-process.md)                   | Erstellt einen neuen Prozess.<br/>                                                                                                                                                                                                                                                         |
| [**Getavailablevirtualsize**](getavailablevirtualsize-win32-process.md) | Ruft die aktuelle Größe des freien virtuellen Adressraums in Bytes ab, der für den Prozess verfügbar ist.<br/> **Windows Server 2012, Windows 8, Windows 7, Windows Server 2008 und Windows Vista:** Diese Methode wird vor Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.<br/> |
| [**GetOwner**](getowner-method-in-class-win32-process.md)               | Ruft den Benutzernamen und den Domänen Namen ab, unter dem der Prozess ausgeführt wird.<br/>                                                                                                                                                                                                    |
| [**GetOwnerSID**](getownersid-method-in-class-win32-process.md)         | Ruft die Sicherheits-ID (SID) für den Besitzer eines Prozesses ab.<br/>                                                                                                                                                                                                            |
| [**SetPriority**](setpriority-method-in-class-win32-process.md)         | Ändert die Ausführungs Priorität eines Prozesses.<br/>                                                                                                                                                                                                                                   |
| [**Terminate**](terminate-method-in-class-win32-process.md)             | Beendet einen Prozess und alle zugehörigen Threads.<br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ Prozess** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Kurze Beschreibung eines Objekts – eine einzeilige Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**CommandLine**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Befehlszeile zum Starten des Prozesses")
</dt> </dl>

Die Befehlszeile, mit der ein bestimmter Prozess gestartet wird, falls zutreffend.

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Klassen Name")
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("up date")
</dt> </dl>

Datum, an dem die Ausführung beginnt.

Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Name der Computer System Klasse ")
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs Computer Systems.

Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Csname**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Computer System Name ")
</dt> </dl>

Name des Bereichs Computer Systems.

Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Die Beschreibung eines Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**ExecutablePath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Berechtigungen**](../wmisdk/standard-wmi-qualifiers.md) ("Einstellungs Verzeichnis"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tool Help Structures \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| szexepath"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Pfad der ausführbaren Datei")
</dt> </dl>

Pfad zur ausführbaren Datei des Prozesses.

Beispiel: "C: \\ Windows \\ System \\Explorer.Exe"

</dd> <dt>

**ExecutionState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Ausführungs Status")
</dt> </dl>

Aktueller Betriebszustand des Prozesses.

Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Unbekannt

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd>

Sonstiges

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Bereit** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blockiert** (4)


</dt> <dd>

Gesperrt

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Gesperrt** (5)


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>Angeh **alten (6** )


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Beendet** (7)


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (8)


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Wächst** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Display Name**](../wmisdk/standard-qualifiers.md) ("handle")
</dt> </dl>

Prozess Bezeichner.

Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.

</dd> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| Lenker"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("handle count")
</dt> </dl>

Die Gesamtanzahl der geöffneten Handles im Besitz des Prozesses. " **Lenker count** " ist die Summe der Handles, die zurzeit von jedem Thread in diesem Prozess geöffnet werden. Ein Handle wird verwendet, um die Systemressourcen zu überprüfen oder zu ändern. Jedes Handle verfügt über einen Eintrag in einer Tabelle, der intern verwaltet wird. Einträge enthalten die Adressen der Ressourcen und Daten zur Identifizierung des Ressourcentyps.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")
</dt> </dl>

Datum, an dem ein Objekt installiert ist. Das-Objekt kann installiert werden, ohne dass ein Wert in diese Eigenschaft geschrieben wird.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Kernelmodetime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("kernelmodetime"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")
</dt> </dl>

Zeit im Kernel Modus in Millisekunden. Wenn diese Informationen nicht verfügbar sind, verwenden Sie den Wert 0 (null).

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Maximumworkingsetsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Berechtigungen**](../wmisdk/standard-wmi-qualifiers.md) ("" * "," * "), [**mappingstrings**](../wmisdk/standard-qualifiers.md) (" Win32 \| Winnt ". H- \| Kontingent \_ Limits \| maximumworkingsetsize "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" maximale Workingsetgröße "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Kilobyte ")
</dt> </dl>

Maximale Workingsetgröße des Prozesses. Der Arbeits Satz eines Prozesses ist der Satz von Speicherseiten, die für den Prozess im physischen RAM sichtbar sind. Diese Seiten sind residente und können von einer Anwendung verwendet werden, ohne dass ein Seiten Fehler ausgelöst wird.

Beispiel: 1413120

</dd> <dt>

**MinimumWorkingSetSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Berechtigungen**](../wmisdk/standard-wmi-qualifiers.md) ("" * "," * "), [**mappingstrings**](../wmisdk/standard-qualifiers.md) (" Win32 \| Winnt ". H \| Kontingent \_ Limits \| MinimumWorkingSetSize "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" minimale Workingsetgröße "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Kilobyte ")
</dt> </dl>

Minimale Workingsetgröße des Prozesses. Der Arbeits Satz eines Prozesses ist der Satz von Speicherseiten, die für den Prozess im physischen RAM sichtbar sind. Diese Seiten sind residente und können für eine Anwendung verwendet werden, ohne dass ein Seiten Fehler ausgelöst wird.

Beispiel: 20480

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Der Name der für den Prozessverantwortlichen ausführbaren Datei, die der Eigenschaft Image Name im Task-Manager entspricht.

Wenn Sie von einer Unterklasse geerbt wird, kann die-Eigenschaft als Schlüsseleigenschaft überschrieben werden. Der Name ist in der Anwendung selbst hart codiert und wird durch Ändern des Datei namens nicht beeinträchtigt. Wenn Sie z. b. Calc.exe umbenennen, wird der Name Calc.exe weiterhin im Task-Manager und in WMI-Skripts angezeigt, die den Prozessnamen abrufen.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Oscreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Betriebs System-Klassenname")
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs bezogenen Betriebssystems.

Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.

</dd> <dt>

**OSName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Betriebs System Name ")
</dt> </dl>

Der Name des Bereichs bezogenen Betriebssystems.

Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.

</dd> <dt>

**Otheroperationcount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| System \_ Process \_ Information \| otheroperationcount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Other Operation count")
</dt> </dl>

Anzahl der durchgeführten e/a-Vorgänge, die keine Lese-oder Schreibvorgänge sind.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Othertransfercount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| System \_ Process \_ Information \| othertransfercount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Other Transfer count"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Datenmenge, die bei Vorgängen übertragen wird, die keine Lese-oder Schreibvorgänge sind.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**PageFaults**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| pagefehlercount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("number of Page Faults")
</dt> </dl>

Anzahl der Seiten Fehler, die von einem Prozess generiert werden.

Beispiel: 10

</dd> <dt>

**PageFileUsage**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PageFileUsage"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Auslagerungs Datei Verwendung"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")
</dt> </dl>

Der Umfang des Auslagerungs Datei-Speicherplatzes, den ein Prozess zurzeit verwendet. Dieser Wert entspricht dem **vmsize** -Wert in TaskMgr.exe.

Beispiel: 102435

</dd> <dt>

**"Parametriprocessid"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| vereritedfromuniqueprocessid"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Parent Process ID")
</dt> </dl>

Eindeutiger Bezeichner des Prozesses, von dem ein Prozess erstellt wird. Die prozesbezeichnernummern werden wieder verwendet, sodass Sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren. Es ist möglich, dass der durch " **parameterprocessid** " identifizierte Prozess beendet wird, sodass " **parameterprocessid** " möglicherweise nicht auf einen laufenden Prozess verweist. Es ist auch möglich, dass " **paramedprocessid** " fälschlicherweise auf einen Prozess verweist, der einen Prozess Bezeichner wieder verwendet. Sie können mit der Eigenschaft " **kreationdate** " bestimmen, ob das angegebene übergeordnete Element erstellt wurde, nachdem der von dieser **Win32- \_ Prozess** Instanz dargestellte Prozess erstellt wurde.

</dd> <dt>

**"Peer Page File Usage"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PeakPageFileUsage"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Top Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("Kilobytes")
</dt> </dl>

Maximale Menge an Auslagerungs Dateispeicher Platz, die während der Lebensdauer eines Prozesses verwendet wird.

Beispiel: 102367

</dd> <dt>

**Peakvirtualsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| peakvirtualsize"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("maximale Auslastung des virtuellen Adressraums"), [**Einheiten**](../wmisdk/standard-qualifiers.md) (Bytes)
</dt> </dl>

Maximaler virtueller Adressraum, der von einem Prozess zu einem beliebigen Zeitpunkt verwendet wird. Die Verwendung von virtuellem Adressraum impliziert nicht notwendigerweise die entsprechende Verwendung von Datenträger-oder Hauptspeicher Seiten. Der virtuelle Speicherplatz ist jedoch begrenzt, und der Prozess kann möglicherweise nicht in der Lage sein, Bibliotheken zu laden.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PeakWorkingSetSize"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("maximale Workingsetgröße"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")
</dt> </dl>

Maximale Workingsetgröße eines Prozesses.

Beispiel: 1413120

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Priorität"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| BasePriority"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Priority")
</dt> </dl>

Planen der Priorität eines Prozesses in einem Betriebssystem. Je höher der Wert ist, desto höher wird ein Prozess von einem Prozess empfangen. Prioritätswerte liegen im Bereich von 0 (null). Dies ist die niedrigste Priorität von 31 (höchste Priorität).

Beispiel: 7

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PrivatePageCount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("private Page count")
</dt> </dl>

Aktuelle Anzahl der zugeordneten Seiten, auf die nur für den von dieser **Win32- \_ Prozess** Instanz dargestellten Prozess zugegriffen werden kann.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**Process \_ Information**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| dwProcessId"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Process ID")
</dt> </dl>

Numerischer Bezeichner zum unterscheiden eines Prozesses von einem anderen. Processids sind ab dem Prozess Erstellungs Zeitpunkt für die Prozess Beendigung gültig. Bei Beendigung kann derselbe numerische Bezeichner auf einen neuen Prozess angewendet werden.

Dies bedeutet, dass Sie ProcessID nicht allein verwenden können, um einen bestimmten Prozess zu überwachen. Beispielsweise könnte eine Anwendung eine ProcessID von 7 aufweisen und dann fehlschlagen. Wenn ein neuer Prozess gestartet wird, kann der neue Prozess ProcessID 7 zugewiesen werden. Ein Skript, das nur auf eine angegebene ProcessID geprüft wurde, könnte daher "täuschen", wenn die ursprüngliche Anwendung noch ausgeführt wird.

</dd> <dt>

**Quotanonpgedpoolusage**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| quotanonpgedpoolusage"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("nicht auslageres Pool Nutzungs Kontingent")
</dt> </dl>

Kontingent Betrag der nicht auslagerungspoolverwendung für einen Prozess.

Beispiel: 15

</dd> <dt>

**Quotapgedpoolusage**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| quotapaargedpoolusage"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Kontingent für Auslagerungs Pool Nutzung")
</dt> </dl>

Kontingent Betrag der auslagerungspoolverwendung für einen Prozess.

Beispiel: 22

</dd> <dt>

**Quotapeaknonpgedpoolusage**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| quotapeaknonpfgedpoolusage"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Maximum Non-Auslagerungs Pool Usage Quota")
</dt> </dl>

Maximale Kontingent Kontingent Menge der nicht ausgelagerten Pool Nutzung für einen Prozess.

Beispiel: 31

</dd> <dt>

**Quotapeakpgedpoolusage**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| quotapeakpgedpoolusage"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Kontingent für Auslagerungs Pool-Nutzungs Kontingent")
</dt> </dl>

Maximale Kontingent Kontingent Menge der ausgelagerten Pool Nutzung für einen Prozess.

Beispiel: 31

</dd> <dt>

**"Read operationcount"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| System \_ Process \_ Information \| leseoperationcount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Anzahl der Lesevorgänge")
</dt> </dl>

Anzahl der ausgeführten Lesevorgänge.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Read Transfer count**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| System \_ Process \_ Information \| lesetransfercount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Read Transfer count"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Menge der gelesenen Daten.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| SessionID"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Sitzungs-ID")
</dt> </dl>

Eindeutiger Bezeichner, den ein Betriebssystem generiert, wenn eine Sitzung erstellt wird. Eine Sitzung erstreckt sich vor der Anmeldung von einem bestimmten System aus über eine bestimmte Zeitspanne.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Diese Eigenschaft ist nicht implementiert und wird für keine Instanz dieser Klasse aufgefüllt. Es ist immer **null**.

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

**TerminationDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Beendigungs Datum")
</dt> </dl>

Der Prozess wurde beendet oder beendet. Um die Beendigungs Zeit zu erhalten, muss ein Handle für den Prozess offen gehalten werden. Andernfalls gibt diese Eigenschaft **null** zurück.

Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.

</dd> <dt>

**Thread Anzahl**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| numofthreads"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Thread Anzahl")
</dt> </dl>

Anzahl der aktiven Threads in einem Prozess. Eine Anweisung ist die grundlegende Einheit der Ausführung in einem Prozessor, und ein Thread ist das Objekt, das eine Anweisung ausführt. Jeder laufende Prozess verfügt über mindestens einen Thread.

</dd> <dt>

**UserModeTime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("UserModeTime"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")
</dt> </dl>

Zeit im Benutzermodus in 100 Nanosekunden-Einheiten. Wenn diese Informationen nicht verfügbar sind, verwenden Sie den Wert 0 (null).

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| VirtualSize"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Virtual Address Space use"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Die aktuelle Größe des virtuellen Adressraums, der von einem Prozess verwendet wird, nicht der physische oder virtuelle Speicher, der tatsächlich vom Prozess verwendet wird. Die Verwendung von virtuellem Adressraum impliziert nicht notwendigerweise die entsprechende Verwendung von Datenträger-oder Hauptspeicher Seiten. Der virtuelle Speicherplatz ist begrenzt. Wenn Sie zu viel verwenden, ist der Prozess möglicherweise nicht in der Lage, Bibliotheken zu laden. Dieser Wert entspricht dem, was Sie in Perfmon.exe sehen.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**WindowsVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Functions \| getprocessversion"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Windows Version")
</dt> </dl>

Version von Windows, in der der Prozess ausgeführt wird.

Beispiel: 4,0

</dd> <dt>

**Workingsetsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Workingsetgröße"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Der Arbeitsspeicher in Bytes, der für die effiziente Ausführung eines Prozesses erforderlich ist – für ein Betriebssystem, das die Seiten basierte Speicherverwaltung verwendet. Wenn das System nicht über genügend Arbeitsspeicher verfügt (weniger als die Workingsetgröße), tritt ein Fehler auf. Wenn die Größe des Workingsets nicht bekannt ist, verwenden Sie **null** oder 0 (null). Wenn Workingsetdaten bereitgestellt werden, können Sie die Informationen überwachen, um die veränderlichen Arbeitsspeicher Anforderungen eines Prozesses zu verstehen.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.

</dd> <dt>

**Schreiboperationcount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| System \_ Process \_ Information \| Beschreib teoperationcount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Write Operation count")
</dt> </dl>

Anzahl der ausgeführten Schreibvorgänge.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Schreib Übertragungs Zähler**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| System \_ Process \_ Information \| Beschreib tetransfercount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Write Transfer count"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Menge der geschriebenen Daten.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ Prozess** Klasse wird vom [**CIM- \_ Prozess**](cim-process.md)abgeleitet. Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen. Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](../wmisdk/executing-privileged-operations.md).

### <a name="overview"></a>Übersicht

Prozesse sind fast alles, was auf einem Computer passiert. Tatsächlich kann die Ursache der meisten Computerprobleme auf Prozesse zurückzuführen sein. Beispielsweise kann es vorkommen, dass zu viele Prozesse auf einem Computer ausgeführt werden (und Konflikte für einen begrenzten Satz von Ressourcen haben), oder ein einzelner Prozess verwendet möglicherweise mehr als seinen Ressourcen Anteil. Diese Faktoren machen es wichtig, dass Sie die auf einem Computer laufenden Prozesse genau beobachten. Mit der Prozessüberwachung, der Hauptaktivität in der Prozess Verwaltung, können Sie bestimmen, was ein Computer tatsächlich tut, welche Anwendungen der Computer ausführt und wie diese Anwendungen von Änderungen in der Computerumgebung betroffen sind.

### <a name="monitoring-a-process"></a>Überwachen eines Prozesses

Durch die regelmäßige Überwachung von Prozessen können Sie sicherstellen, dass ein Computer mit hoher Effizienz ausgeführt wird und seine vorgesehenen Aufgaben erwartungsgemäß ausführt. Beispielsweise können Sie bei der Überwachung von Prozessen sofort eine beliebige Anwendung Benachrichtigen, die nicht mehr reagiert, und dann Maßnahmen ergreifen, um diesen Vorgang zu beenden. Außerdem können Sie mithilfe der Prozessüberwachung Probleme erkennen, bevor Sie auftreten. Beispielsweise können Sie durch wiederholtes Überprüfen der von einem Prozess genutzten Arbeitsspeicher Menge einen Speicherlecks erkennen. Sie können den Prozess beenden, bevor die fehlerhafte Anwendung den gesamten verfügbaren Arbeitsspeicher verwendet und den Computer angehalten wird.

Mit der Prozessüberwachung können auch die Unterbrechungen minimiert werden, die durch geplante Ausfälle bei Upgrades und Wartungsarbeiten verursacht werden. Wenn Sie z. b. den Status einer Datenbankanwendung überprüfen, die auf Client Computern ausgeführt wird, können Sie die Auswirkungen der Offline Schaltung der Datenbank ermitteln, um die Software zu aktualisieren.

Überwachen der Prozess Verfügbarkeit. Misst den Prozentsatz der Zeit, zu der ein Prozess verfügbar ist. Die Verfügbarkeit wird in der Regel durch die Verwendung eines einfachen Tests überwacht, der meldet, ob der Prozess noch ausgeführt wird. Durch die Nachverfolgung der Ergebnisse der einzelnen Tests können Sie die Verfügbarkeit des Prozesses berechnen. Beispielsweise hat ein Prozess, bei dem 100-mal geprüft werden und auf 95 dieser Vorkommen antwortet, eine Verfügbarkeit von 95 Prozent. Diese Art der Überwachung ist in der Regel für Datenbanken, e-Mail-Programme und andere Anwendungen reserviert, die zu jedem Zeitpunkt erwartungsgemäß ausgeführt werden. Sie eignet sich nicht für Textverarbeitungsprogramme, Kalkulations Tabellen oder andere Anwendungen, die routinemäßig mehrmals täglich gestartet und angehalten werden.

Sie können eine Instanz der Win32-Klasse " [**\_ processstartup**](win32-processstartup.md) " erstellen, um den Prozess zu konfigurieren.

Sie können die Prozessleistung mit der [**Win32 \_ perfformatteddata \_ perfproc \_ Process**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) -Klasse und einem WMI-Aktualisierungs Objekt (z. b. " [**Swap**](../wmisdk/swbemrefresher.md)-Aktualisierungs Programm") überwachen. Weitere Informationen finden Sie unter über [Wachen von Leistungsdaten](../wmisdk/monitoring-performance-data.md).

## <a name="examples"></a>Beispiele

In der [Liste der Eigenschaften von WMI-Klassen](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) PowerShell-Codebeispiel in TechNet Gallery wird die **Win32- \_ Prozess** Klasse beschrieben und die Ergebnisse im Excel-Format ausgegeben.

Der [Prozess zum Beenden der Ausführung auf mehreren Servern](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) beendet einen Prozess, der auf einem oder mehreren Computern ausgeführt wird.

Im [Beispiel: Aufrufen einer Anbieter Methode](../wmisdk/example--calling-a-provider-method.md) verwendet der Code C++, um den Win32- **\_ Prozess** zum Erstellen eines Prozesses aufzurufen.

Verfügbarkeit ist die einfachste Form der Prozessüberwachung: bei diesem Ansatz wird lediglich sichergestellt, dass der Prozess ausgeführt wird. Wenn Sie die Prozess Verfügbarkeit überwachen, rufen Sie in der Regel eine Liste der Prozesse ab, die auf einem Computer ausgeführt werden, und überprüfen dann, ob ein bestimmter Prozess noch aktiv ist. Wenn der Prozess aktiv ist, gilt er als verfügbar. Wenn der Prozess nicht aktiv ist, ist er nicht verfügbar. Im folgenden VBScript-Beispiel wird die Prozess Verfügbarkeit überwacht, indem die Liste der auf einem Computer ausgelaufenden Prozesse überprüft und eine Benachrichtigung ausgegeben wird, wenn der Database.exe Prozess nicht gefunden wurde.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



Das folgende VBScript-Beispiel überwacht die Prozesserstellung mit einem temporären Ereignisconsumer.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



Das folgende VBScript überwacht die Prozess Leistungsinformationen.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Sie den Besitzer der einzelnen Prozesse auf einem lokalen Computer abrufen können. Mit diesem Skript können Sie beispielsweise Daten von einem Remote Computer abrufen, um zu bestimmen, welche Benutzer über Prozesse verfügen, auf denen Terminal Server ausgeführt wird, und den Namen des Remote Computers in der ersten Zeile durch den Namen des Remote Computers ersetzen. Sie müssen auch Administrator auf dem Remote Computer sein.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



Im folgenden VBScript-Codebeispiel wird gezeigt, wie Sie die Anmelde Sitzung abrufen, die einem laufenden Prozess zugeordnet ist. Vor dem Starten des Skripts muss ein Prozess Notepad.exe ausgeführt werden. Im Beispiel werden die Instanzen von [**Win32 \_ logonsession**](win32-logonsession.md) , die dem **Win32- \_ Prozess** zugeordnet sind, der Notepad.exe darstellt, lokalisiert. [**Win32 \_ Sessionprocess**](win32-sessionprocess.md) wird als Association-Klasse angegeben. Weitere Informationen finden Sie unter [ASSOCIATORS of Statement.](../wmisdk/associators-of-statement.md)


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Prozess**](cim-process.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[WMI-Tasks: Prozesse](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
