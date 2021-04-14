---
title: Win32_TerminalService-Klasse
description: Eine Unterklasse der Win32- \_ Dienstklasse. Win32 \_ Terminalservice stellt die-Element Eigenschaft der Win32 \_ terminalservicedesetting-Zuordnung dar.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Win32_TerminalService-Klasse Remotedesktopdienste
- Win32_TerminalService Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba5646c6ac9abf41fddc023ad39884e611681a71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478843"
---
# <a name="win32_terminalservice-class"></a>Win32 \_ Terminalservice-Klasse

Die **Win32 \_ Terminalservice** -WMI-Klasse ist eine Unterklasse der [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse. **Win32 \_ Terminalservice** stellt die- **Element** Eigenschaft der [**Win32 \_ terminalservicedesetting**](win32-terminalservicetosetting.md) -Zuordnung dar.

Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a>Member

Die **Win32 \_ Terminalservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ Terminalservice** -Klasse verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Klima**](win32-terminalservice-change.md)                               | Ändert einen Dienst.<br/>                                                                       |
| [**ChangeStartMode**](win32-terminalservice-changestartmode.md)             | Ändert den Start Modus eines Dienstanbieter.<br/>                                                     |
| [**Stelle**](win32-terminalservice-create.md)                               | Erstellt einen neuen Dienst.<br/>                                                                    |
| [**Lösch**](win32-terminalservice-delete.md)                               | Löscht einen vorhandenen Dienst.<br/>                                                              |
| [**GetSecurityDescriptor**](win32-terminalservice-getsecuritydescriptor.md) | Gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Dienst steuert.<br/>                      |
| [**"InterrogateService"**](win32-terminalservice-interrogateservice.md)       | Fordert an, dass ein Dienst seinen Status auf den Dienst-Manager aktualisiert.<br/>                          |
| [**PauseService**](win32-terminalservice-pauseservice.md)                   | Versucht, einen Dienst in den angehaltenen Zustand zu versetzen.<br/>                                          |
| [**ResumeService**](win32-terminalservice-resumeservice.md)                 | Versucht, einen Dienst in den Status "wieder aufgenommen" zu versetzen.<br/>                                         |
| [**SETSECURITYDESCRIPTOR**](win32-terminalservice-setsecuritydescriptor.md) | Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Dienst steuert.<br/> |
| [**Start Service**](win32-terminalservice-startservice.md)                   | Versucht, einen Dienst in den Startzustand zu versetzen.<br/>                                       |
| [**Stop Service**](win32-terminalservice-stopservice.md)                     | Versetzt einen Dienst in den Status "beendet".<br/>                                                    |
| [**UserControlService**](win32-terminalservice-usercontrolservice.md)       | Versucht, einen benutzerdefinierten Steuerelement Code an einen Dienst zu senden.<br/>                                |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ Terminalservice** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept \_ Pause \_ Continue"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accept Pause")
</dt> </dl>

Gibt an, ob der Dienst angehalten werden kann.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept End \_ "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("der Dienst akzeptiert das Ende")
</dt> </dl>

Gibt an, ob der Dienst beendet werden kann.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Kurze Beschreibung des Dienes für eine einzeilige Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Kal**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcheck"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point count")
</dt> </dl>

Der Wert, den der Dienst in regelmäßigen Abständen erhöht, um den Fortschritt während eines langen Starts, Anhaltevorgangs, anhalten oder fortsetzen zu melden. Der Dienst erhöht z. b. diesen Wert, da er die einzelnen Schritte seiner Initialisierung beim Starten abschließt. Das Benutzeroberflächen Programm, das den-Vorgang für den Dienst aufruft, verwendet diesen Wert, um den Status des Dienstanbieter während eines langwierigen Vorgangs zu verfolgen. Dieser Wert ist ungültig und sollte NULL sein, wenn der Dienst nicht über einen Vorgang zum Starten, beenden, anhalten oder fortsetzen verfügt.

Diese Eigenschaft wird vom [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)geerbt.

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")
</dt> </dl>

Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird. Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ verzögert \_ Auto \_ Start \_ Info**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| f delayedautostart"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("verzögerter automatischer Start")
</dt> </dl>

**True** gibt an, dass der Dienst gestartet wird, nachdem andere automatischen Start Dienste und eine kurze Verzögerung gestartet wurden.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.

Diese Eigenschaft wird vom [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype \| Service \_ Interactive \_ Process"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("interagiert with Desktop")
</dt> </dl>

Gibt an, ob der Dienst Windows auf dem Desktop erstellen oder mit ihm kommunizieren kann, sodass er auf irgendeine Weise mit einem Benutzer interagieren kann. Interaktive Dienste müssen unter dem lokalen System Konto ausgeführt werden. Die meisten Dienste sind nicht interaktiv. Das heißt, Sie kommunizieren in keiner Weise mit dem Benutzer.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**Disconnectedsessions**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der getrennten Sitzungen auf dem aktuellen Server. Diese Sitzungen verbrauchen möglicherweise weiterhin Server Ressourcen, aber Sie verfügen derzeit über keine Netzwerkverbindung mit einem Client.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpdisplayname"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Anzeige Name")
</dt> </dl>

Der Name des Diensts, wie im Dienste-Snap-in angezeigt. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Beachten Sie, dass der Anzeige Name und der Dienst Name (der in der Registrierung gespeichert ist) nicht immer identisch sind. Der DHCP-Client Dienst hat z. b. den Dienstnamen DHCP, aber den anzeigen Amen DHCP-Client. Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten. Bei [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) -vergleichen wird jedoch immer die Groß-/Kleinschreibung nicht beachtet.

Einschränkung: akzeptiert denselben Wert wie die [**Name**](/windows/desktop/CIMWin32Prov/win32-service) -Eigenschaft.

Beispiel: "ATDISK"

Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwerrorcontrol"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Schweregrad des Start Fehlers")
</dt> </dl>

Der Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann. Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt. Alle Fehler werden vom Computersystem protokolliert.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** ("ignorieren")


</dt> <dd>

Der Benutzer wird nicht benachrichtigt.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")


</dt> <dd>

Der Benutzer wird benachrichtigt. Normalerweise ist dies ein Meldungs Feld, in dem der Benutzer über das Problem benachrichtigt wird.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** ("schwerwiegend")


</dt> <dd>

Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** ("kritisch")


</dt> <dd>

Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten. Wenn der Dienst nicht ein zweites Mal gestartet werden kann, schlägt der Startvorgang fehl.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** ("unbekannt")


</dt> <dd>

Der Schweregrad des Fehlers ist unbekannt.

</dd> </dl>

Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**Exitcode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exitcode")
</dt> </dl>

Windows-Fehlercode, der Fehler definiert, die beim Starten oder Beenden des Dienstes aufgetreten sind. Diese Eigenschaft ist auf **Fehler \_ Dienst \_ spezifischer \_ Fehler** (1066) festgelegt, wenn der Fehler für den Dienst eindeutig ist, der durch diese Klasse dargestellt wird. Informationen über den Fehler sind in der [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) -Eigenschaft verfügbar. Der Dienst legt diesen Wert bei der Ausführung und erneut bei normaler Beendigung auf **keinen \_ Fehler** fest.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")
</dt> </dl>

Date-Objekt ist installiert. Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Eindeutiger Bezeichner des dienstanweises, der angibt, welche Funktionen verwaltet werden. Diese Funktionalität wird in der [**Description**](/windows/desktop/CIMWin32Prov/win32-service) -Eigenschaft des-Objekts beschrieben.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpbinarypathname"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateipfadname")
</dt> </dl>

Der voll qualifizierte Pfad der Dienst Binärdatei, die den Dienst implementiert.

Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys"

Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status \_ Process**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process ID")
</dt> </dl>

Prozess Bezeichner des Dienstanbieter.

Beispiel: 324

Diese Eigenschaft wird vom [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)geerbt.

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwservicespecificexitcode"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server spezifischer Exitcode")
</dt> </dl>

Dienst spezifischer Fehlercode für Fehler, die auftreten, während der Dienst gestartet oder beendet wird. Die Exitcodes werden von dem Dienst definiert, der durch diese Klasse dargestellt wird. Dieser Wert wird nur festgelegt, wenn der [**Exitcode**](/windows/desktop/CIMWin32Prov/win32-service) -Eigenschafts Wert **Fehler \_ Dienst \_ spezifisch \_** ist (1066).

Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")
</dt> </dl>

Der für aufrufende Prozesse bereitgestellte Diensttyp.

Die Werte sind:

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

**Kernel Treiber** ("Kernel Treiber")


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

**Dateisystem Treiber** ("Dateisystem Treiber")


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

**Adapter** ("Adapter")


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

**Erkennungs Treiber** ("Erkennungs Treiber")


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

**Eigener Prozess** ("eigener Prozess")


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

**Freigabeprozess** ("Freigabeprozess")


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

**Interaktiver Prozess** ("interaktiver Prozess")


</dt> <dd></dd> </dl>

Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**Gestartet**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")
</dt> </dl>

Gibt an, ob der Dienst gestartet wurde.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Modus")
</dt> </dl>

Der Start Modus des Windows-Basis Dienstanbieter.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Start** ("Start")


</dt> <dd>

Der Gerätetreiber wurde vom Betriebssystem Lader gestartet (nur für Treiber Dienste gültig).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")


</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")


</dt> <dd>

Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden. Automatische Dienste werden auch dann gestartet, wenn sich ein Benutzer nicht anmelden kann.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell** ("manuell")


</dt> <dd>

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) -Methode aufruft. Diese Dienste werden erst gestartet, wenn sich ein Benutzer anmeldet und startet.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")


</dt> <dd>

Dienst, der erst gestartet werden kann, wenn sein StartMode entweder in "Auto" oder "manuell" geändert wurde.

</dd> </dl>

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpservicestartname"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")
</dt> </dl>

Der Kontoname, unter dem ein Dienst ausgeführt wird. Abhängig vom Diensttyp kann der Kontoname die Form "Domainname \\ username" oder das UPN-Format (" *Username@DomainName* ") aufweisen. Der Dienst Prozess wird mit einer dieser beiden Formulare protokolliert, wenn er ausgeführt wird. Wenn das Konto zur integrierten Domäne gehört, dann ". \\ Username "kann angegeben werden. Für Treiber auf Kernel-oder Systemebene enthält [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) den Treiber Objektnamen (d. h. " \\ File System \\ rdr" oder " \\ Driver \\ XNS"), den das e/a-System zum Laden des Gerätetreibers verwendet. Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde.

Beispiel: "dwdom \\ Admin"

Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcurrentstate"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")
</dt> </dl>

Aktueller Status des Basis Dienes.

Die Werte sind:

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

**Beendet** ("beendet")


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

**Start steht aus** ("ausstehende Start")


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

**Ausstehende Beendigung** ("ausstehenden Vorgang nicht mehr")


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

Wird **ausgeführt** ("wird ausgeführt")


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

**Ausstehende Fortsetzung** ("ausstehende Fortsetzung")


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

Anhalten steht **aus** ("ausstehende Pause")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Angeh** alten ("angehalten")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> </dl>

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows 7 und Windows Server 2008 R2 schreibgeschützt.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen). Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Die Werte sind:

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

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system). "Kreationclassname"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Klassenname")
</dt> </dl>

Der Typname des Systems, das den Dienst hostet.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system). Name "), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")
</dt> </dl>

Der Name des Systems, das den Dienst hostet.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**TagID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwtagid"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag ID")
</dt> </dl>

Eindeutiger Tagwert für diesen Dienst in der Gruppe. Der Wert 0 (null) gibt an, dass der Dienst nicht über ein Tag verfügt. Ein-Tag kann verwendet werden, um den Dienst Start innerhalb einer Gruppe von Lade Reihenfolgen zu sortieren, indem Sie in der Registrierung einen taganordnungs Vektor angeben:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Steuer** Element \\ **grouporderlist**    

Tags werden nur für Kernel Treiber-und Datei System Treiber-Starttyp Dienste ausgewertet, die über Start-oder System Start Modi verfügen.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**Totalsessions**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der Sitzungen auf dem aktuellen Server. Dies schließt sowohl verbundene als auch getrennte Sitzungen ein.

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwwaithint"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("geschätzte Wartezeit")
</dt> </dl>

Geschätzte benötigte Zeit (in Millisekunden) für einen ausstehenden Start-, anhalte-, Anhaltevorgang-oder continue-Vorgang. Nachdem die angegebene Zeit abgelaufen ist, führt der Dienst den nächsten Aufruf der **SetServiceStatus** -Methode mit einem [**inkrementierten**](/windows/desktop/CIMWin32Prov/win32-service) Prüf Punkt Wert oder einer Änderung in **CurrentState** aus. Wenn die von **WaitHint** angegebene Zeitspanne verstrichen **ist und der** Prüfpunkt nicht inkrementiert wurde, oder **CurrentState** nicht geändert wurde, geht der Dienststeuerungs-Manager oder das Dienst Steuerungsprogramm davon aus, dass ein Fehler aufgetreten ist.

Diese Eigenschaft wird vom [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Da die **Win32 \_ Terminalservice** -Klasse eine Unterklasse der [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse ist, erbt die-Klasse alle Eigenschaften und Methoden des **Win32- \_ Dienstanbieter**.

[**Win32 \_ Terminalservicesete**](win32-terminalservicesetting.md) ist **Win32 \_ Terminalservice** als **Einstellungs** Eigenschaft der [**Win32 \_ terminalservicedesetting**](win32-terminalservicetosetting.md) -Zuordnung zugeordnet.

[**Win32 \_ Tssessiondirectory**](win32-tssessiondirectory.md) ist **Win32 \_ Terminalservice** als **Einstellungs** Eigenschaft der [**Win32 \_ tssessiondirectorysetting**](win32-tssessiondirectorysetting.md) -Zuordnung zugeordnet.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**Win32 \_ terminalservicede Setting**](win32-terminalservicetosetting.md)
</dt> <dt>

[**Win32- \_ tssessiondirectory**](win32-tssessiondirectory.md)
</dt> <dt>

[**Win32- \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

