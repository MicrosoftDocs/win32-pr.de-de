---
title: Win32_TerminalService-Klasse
description: Eine Unterklasse der \_ Win32-Dienstklasse. Win32 \_ TerminalService stellt die Element-Eigenschaft der Win32 \_ TerminalServiceToSetting-Zuordnung dar.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Win32_TerminalService-Klassen-Remotedesktopdienste
- Win32_TerminalService -Klasse Remotedesktopdienste beschrieben
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
ms.openlocfilehash: 735b033017958816e8e9a40caea935847104fdcbe3e9acf3128890d88685d09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867850"
---
# <a name="win32_terminalservice-class"></a>Win32 \_ TerminalService-Klasse

Die **Win32 \_ TerminalService** WMI-Klasse ist eine Unterklasse der [**Win32 \_ Service-Klasse.**](/windows/desktop/CIMWin32Prov/win32-service) **Win32 \_ TerminalService** stellt die **Element-Eigenschaft** der [**Win32 \_ TerminalServiceToSetting-Zuordnung**](win32-terminalservicetosetting.md) dar.

Die folgende Syntax wird aus MOF-Code vereinfacht und enthält alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.

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

Die **Win32 \_ TerminalService-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TerminalService-Klasse** verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Change**](win32-terminalservice-change.md)                               | Ändert einen Dienst.<br/>                                                                       |
| [**ChangeStartMode**](win32-terminalservice-changestartmode.md)             | Ändert den Startmodus eines Diensts.<br/>                                                     |
| [**Erstellen**](win32-terminalservice-create.md)                               | Erstellt einen neuen Dienst.<br/>                                                                    |
| [**Löschen**](win32-terminalservice-delete.md)                               | Löscht einen vorhandenen Dienst.<br/>                                                              |
| [**GetSecurityDescriptor**](win32-terminalservice-getsecuritydescriptor.md) | Gibt die Sicherheitsbeschreibung zurück, die den Zugriff auf den Dienst steuert.<br/>                      |
| [**InterrogateService**](win32-terminalservice-interrogateservice.md)       | Fordert an, dass ein Dienst seinen Zustand an den Dienst-Manager aktualisiert.<br/>                          |
| [**PauseService**](win32-terminalservice-pauseservice.md)                   | Versucht, einen Dienst im angehaltenen Zustand zu platzieren.<br/>                                          |
| [**ResumeService**](win32-terminalservice-resumeservice.md)                 | Versucht, einen Dienst im Status "Fortgesetzt" zu platzieren.<br/>                                         |
| [**SetSecurityDescriptor**](win32-terminalservice-setsecuritydescriptor.md) | Schreibt eine aktualisierte Version der Sicherheitsbeschreibung, die den Zugriff auf den Dienst steuert.<br/> |
| [**Startservice**](win32-terminalservice-startservice.md)                   | Versucht, einen Dienst in den Startzustand zu bringen.<br/>                                       |
| [**StopService**](win32-terminalservice-stopservice.md)                     | Versetzt einen Dienst in den Zustand "Beendet".<br/>                                                    |
| [**UserControlService**](win32-terminalservice-usercontrolservice.md)       | Versucht, einen benutzerdefinierten Steuerelementcode an einen Dienst zu senden.<br/>                                |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TerminalService-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Dienststrukturen \| \| [**SERVICE \_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT PAUSE \_ \_ \_ CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dienst akzeptiert Pause")
</dt> </dl>

Gibt an, ob der Dienst angehalten werden kann.

Diese Eigenschaft wird von [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT \_ \_ STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")
</dt> </dl>

Gibt an, ob der Dienst beendet werden kann.

Diese Eigenschaft wird von [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Kurze Beschreibung des Diensts: eine einzeilige Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Prüfpunkt**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Dienststrukturen \| \| [**SERVICE \_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")
</dt> </dl>

Der Wert, den der Dienst in regelmäßigen Abständen erhöht, um den Fortschritt während eines langen Start-, Stopp-, Pausen- oder Fortsetzungsvorgangs zu melden. Beispielsweise erhöht der Dienst diesen Wert, wenn er jeden Schritt seiner Initialisierung abschließt, wenn er gestartet wird. Das Benutzeroberflächenprogramm, das den Vorgang für den Dienst aufruft, verwendet diesen Wert, um den Fortschritt des Diensts während eines längeren Vorgangs nachzuverfolgen. Dieser Wert ist ungültig und sollte 0 (null) sein, wenn für den Dienst kein Start-, Stopp-, Pausen- oder Fortsetzungsvorgang aussteht.

Diese Eigenschaft wird vom [**\_ Win32-Dienst**](/windows/desktop/CIMWin32Prov/win32-service)geerbt.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Klassenname")
</dt> </dl>

Name der ersten konkreten Klasse, die in der Vererbungskette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit den anderen Schlüsseleigenschaften der -Klasse ermöglicht diese Eigenschaft die eindeutige Identifizierung aller Instanzen dieser Klasse und ihrer Unterklassen.

Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Dienststrukturen \| \| [**SERVICE \_ DELAYED AUTO START \_ \_ \_ INFO**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Delayed Auto-Start")
</dt> </dl>

**True** gibt an, dass der Dienst gestartet wird, nachdem andere dienste automatisch gestartet wurden, plus einer kurzen Verzögerung.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.

Diese Eigenschaft wird vom [**\_ Win32-Dienst**](/windows/desktop/CIMWin32Prov/win32-service)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Beschreibung")
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Dienststrukturen \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| SERVICE INTERACTIVE \_ \_ PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interagiert mit Desktop")
</dt> </dl>

Gibt an, ob der Dienst Fenster auf dem Desktop erstellen oder mit ihnen kommunizieren kann und somit in irgendeiner Weise mit einem Benutzer interagiert. Interaktive Dienste müssen unter dem lokalen Systemkonto ausgeführt werden. Die meisten Dienste sind nicht interaktiv. Das heißt, sie kommunizieren in keiner Weise mit dem Benutzer.

Diese Eigenschaft wird von [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**DisconnectedSessions**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der getrennten Sitzungen auf dem aktuellen Server. Diese Sitzungen verbrauchen möglicherweise weiterhin aktiv Serverressourcen, verfügen aber derzeit über keine Netzwerkverbindung mit einem Client.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")
</dt> </dl>

Name des Diensts, wie im Snap-In Dienste angezeigt. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Beachten Sie, dass der Anzeigename und der Dienstname (der in der Registrierung gespeichert ist) nicht immer identisch sind. Der DHCP-Clientdienst hat beispielsweise den Dienstnamen Dhcp, aber den Anzeigenamen DHCP-Client. Der Name wird im Dienststeuerungs-Manager beibehalten. Bei [**DisplayName-Vergleichen**](/windows/desktop/CIMWin32Prov/win32-service) wird die Groß-/Kleinschreibung jedoch immer nicht beachtet.

Einschränkung: Akzeptiert den gleichen Wert wie die [**Name-Eigenschaft.**](/windows/desktop/CIMWin32Prov/win32-service)

Beispiel: "Atdisk"

Diese Eigenschaft wird von [**Win32 \_ BaseService geerbt.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Dienststrukturen \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Schweregrad des Startfehlers")
</dt> </dl>

Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann. Der Wert gibt die Aktion an, die vom Startprogramm ausgeführt wird, wenn ein Fehler auftritt. Alle Fehler werden vom Computersystem protokolliert.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** ("Ignorieren")


</dt> <dd>

Der Benutzer wird nicht benachrichtigt.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")


</dt> <dd>

Der Benutzer wird benachrichtigt. In der Regel ist dies ein Meldungsfeld, in dem der Benutzer über das Problem benachrichtigt wird.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** ("schwerwiegend")


</dt> <dd>

Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** ("Kritisch")


</dt> <dd>

Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten. Wenn der Dienst ein zweites Mal nicht gestartet werden kann, schlägt der Start fehl.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** ("Unbekannt")


</dt> <dd>

Der Schweregrad des Fehlers ist unbekannt.

</dd> </dl>

Diese Eigenschaft wird von [**Win32 \_ BaseService geerbt.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Exitcode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")
</dt> </dl>

Windows Fehlercode, der Fehler definiert, die beim Starten oder Beenden des Diensts auftreten. Diese Eigenschaft wird auf **ERROR \_ SERVICE SPECIFIC \_ \_ ERROR** (1066) festgelegt, wenn der Fehler für den durch diese Klasse dargestellten Dienst eindeutig ist und Informationen zum Fehler in der [**ServiceSpecificExitCode-Eigenschaft verfügbar**](/windows/desktop/CIMWin32Prov/win32-service) sind. Der Dienst legt diesen Wert bei der Ausführung **auf NO \_ ERROR** und bei normaler Beendigung erneut fest.

Diese Eigenschaft wird von [**Win32 \_ BaseService geerbt.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installationsdatum")
</dt> </dl>

Das Date-Objekt wird installiert. Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Eindeutiger Bezeichner des Diensts, der einen Hinweis auf die verwaltete Funktionalität bietet. Diese Funktionalität wird in der [**Description-Eigenschaft**](/windows/desktop/CIMWin32Prov/win32-service) des -Objekts beschrieben.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateipfadname")
</dt> </dl>

Vollqualifizierter Pfad zur Binärdatei des Diensts, die den Dienst implementiert.

Beispiel: \\ "SystemRoot \\ \\ System32-Treiber \\afd.sys"

Diese Eigenschaft wird von [**Win32 \_ BaseService geerbt.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Processid**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE STATUS \| [**\_ \_ PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process Id")
</dt> </dl>

Prozessbezeichner des Diensts.

Beispiel: 324

Diese Eigenschaft wird vom [**Win32-Dienst \_ geerbt.**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Dienststrukturen \| \| [**SERVICE \_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Serverspezifischer Exitcode")
</dt> </dl>

Dienstspezifischer Fehlercode für Fehler, die auftreten, während der Dienst gestartet oder beendet wird. Die Exitcodes werden durch den von dieser Klasse dargestellten Dienst definiert. Dieser Wert wird nur festgelegt, wenn der [**ExitCode-Eigenschaftswert**](/windows/desktop/CIMWin32Prov/win32-service) **ERROR SERVICE SPECIFIC \_ \_ \_ ERROR** (1066) ist.

Diese Eigenschaft wird von [**Win32 \_ BaseService geerbt.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Dienststrukturen \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Diensttyp")
</dt> </dl>

Der für aufrufende Prozesse bereitgestellte Diensttyp.

Die Werte sind:

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

**Kerneltreiber** ("Kerneltreiber")


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

**Dateisystemtreiber** ("Dateisystemtreiber")


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

**Adapter** ("Adapter")


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

**Recognizer Driver** ("Recognizer Driver")


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

**Eigener Prozess** ("Eigener Prozess")


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

**Freigabeprozess** ("Freigabeprozess")


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

**Interaktiver Prozess** ("interaktiver Prozess")


</dt> <dd></dd> </dl>

Diese Eigenschaft wird von [**Win32 \_ BaseService geerbt.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Begann**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")
</dt> </dl>

Gibt an, ob der Dienst gestartet wird.

Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Startmodus")
</dt> </dl>

Startmodus des Windows Basisdiensts.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Start** ("Boot")


</dt> <dd>

Vom Betriebssystemladeprogramm gestarteter Gerätetreiber (nur für Treiberdienste gültig).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")


</dt> <dd>

Der Vom Initialisierungsprozess des Betriebssystems gestartete Gerätetreiber. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")


</dt> <dd>

Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden. Automatische Dienste werden auch dann gestartet, wenn sich ein Benutzer nicht anmeldet.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell** ("Manuell")


</dt> <dd>

Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService-Methode**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) aufruft. Diese Dienste werden erst gestartet, wenn sich ein Benutzer anmeldet und startet.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("Deaktiviert")


</dt> <dd>

Dienst, der erst gestartet werden kann, wenn startMode in Auto oder Manual geändert wurde.

</dd> </dl>

Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Dienststrukturen \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Startkontoname")
</dt> </dl>

Kontoname, unter dem ein Dienst ausgeführt wird. Je nach Diensttyp kann der Kontoname das Format \\ "Domänenname-Benutzername" oder UPN-Format *Username@DomainName* ("") aufweisen. Der Dienstprozess wird bei der Ausführung mit einer dieser beiden Formen protokolliert. Wenn das Konto zur integrierten Domäne gehört, dann ". \\ Username" kann angegeben werden. Für Kernel- oder Treiber auf Systemebene enthält [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) den Treiberobjektnamen (d.h. \\ "FileSystem \\ Rdr" oder \\ "Driver \\ Xns"), den das E/A-System zum Laden des Gerätetreibers verwendet. Wenn **NULL** angegeben wird, wird der Treiber außerdem mit einem Standardobjektnamen ausgeführt, der vom E/A-System basierend auf dem Dienstnamen erstellt wurde.

Beispiel: "DWDOM \\ Admin"

Diese Eigenschaft wird von [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Dienststrukturen \| \| [**SERVICE \_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")
</dt> </dl>

Aktueller Status des Basisdiensts.

Die Werte sind:

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

**Beendet** ("Beendet")


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

**Ausstehend starten** ("Start ausstehend")


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

**Stop Pending** ("Stop Pending")


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**Wird ausgeführt** ("Wird ausgeführt")


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

**Continue Pending** ("Continue Pending")


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

**Anhalten ausstehend** ("Ausstehend anhalten")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Angehalten** ("Angehalten")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Unbekannt")


</dt> <dd></dd> </dl>

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows 7 und Windows Server 2008 R2 schreibgeschützt.

Diese Eigenschaft wird von [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs- und Nichtoperationsstatus definiert werden. Betriebsstatus: "OK", "Heruntergestuft" und "Pred Fail" (ein Element, z. B. ein SMART-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, sagt aber einen Fehler in naher Zukunft vorher). Nichtoperationale Status: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann während des Spiegelungsresilverings eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Verwaltungsaufgaben angewendet werden. Nicht alle dieser Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Die Werte sind:

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

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-System**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName"), [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Systemklassenname")
</dt> </dl>

Geben Sie den Namen des Systems ein, das diesen Dienst hostet.

Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-System**](/windows/desktop/CIMWin32Prov/cim-system). Name"), [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Systemname")
</dt> </dl>

Name des Systems, das diesen Dienst hostet.

Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Dienststrukturen \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag-ID")
</dt> </dl>

Eindeutiger Tagwert für diesen Dienst in der Gruppe. Der Wert 0 (null) gibt an, dass der Dienst kein Tag besitzt. Ein Tag kann verwendet werden, um den Dienststart innerhalb einer Lastreihenfolgegruppe zu bestellen, indem in der Registrierung unter ein Tagreihenfolgevektor angegeben wird:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **GroupOrderList**    

Tags werden nur für Starttypdienste des Kerneltreibers und des Dateisystemtreibers ausgewertet, die den Start- oder Systemstartmodus aufweisen.

Diese Eigenschaft wird von [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.

</dd> <dt>

**TotalSessions**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtzahl der Sitzungen auf dem aktuellen Server. Dies schließt sowohl verbundene als auch getrennte Sitzungen ein.

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estimated Wait Time")
</dt> </dl>

Geschätzte Zeit in Millisekunden für einen ausstehenden Start-, Stopp-, Pause- oder Fortsetzungsvorgang. Nach Ablauf der angegebenen Zeit wird die **SetServiceStatus-Methode** des Diensts mit einem inkrementierten [**CheckPoint-Wert**](/windows/desktop/CIMWin32Prov/win32-service) oder einer Änderung in **CurrentState als nächster Aufruf ausgeführt.** Wenn die von **WaitHint** angegebene Zeit vergeht und **CheckPoint** nicht erhöht wurde oder **CurrentState** nicht geändert wurde, geht der Dienststeuerungs-Manager oder das Dienststeuerungsprogramm davon aus, dass ein Fehler aufgetreten ist.

Diese Eigenschaft wird vom [**Win32-Dienst \_ geerbt.**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Da die **Win32 \_ TerminalService-Klasse** eine Unterklasse der [**Win32 \_ Service-Klasse**](/windows/desktop/CIMWin32Prov/win32-service) ist, erbt die -Klasse alle Eigenschaften und Methoden des **Win32-Diensts. \_**

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) ist **Win32 \_ TerminalService** als **Einstellungseigenschaft** der [**Win32 \_ TerminalServiceToSetting-Zuordnung**](win32-terminalservicetosetting.md) zugeordnet.

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) ist **Win32 \_ TerminalService** als **Setting-Eigenschaft** der [**Win32 \_ TSSessionDirectorySetting-Zuordnung**](win32-tssessiondirectorysetting.md) zugeordnet.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Dienst \_**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> <dt>

[**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[**\_CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

