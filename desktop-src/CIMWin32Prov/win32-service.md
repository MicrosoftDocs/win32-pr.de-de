---
description: Stellt einen Dienst auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Win32_Service-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a33265b3dfc3b114d55b381a229b717e291bbd258716e8305d9995282d29b3f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759260"
---
# <a name="win32_service-class"></a>\_Win32-Dienstklasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) des **Win32-Diensts \_** stellt einen Dienst auf einem Computersystem dar, auf dem Windows ausgeführt wird.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge sortiert.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
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
};
```

## <a name="members"></a>Member

Die **\_ Win32-Dienstklasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **\_ Win32-Dienstklasse** verfügt über diese Methoden.



| Methode                                                                               | Beschreibung                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Change**](change-method-in-class-win32-service.md)                               | Ändert einen Dienst.<br/>                                                                       |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-service.md)             | Ändert den Startmodus eines Diensts.<br/>                                                     |
| [**Erstellen**](create-method-in-class-win32-service.md)                               | Erstellt einen neuen Dienst.<br/>                                                                    |
| [**Löschen**](delete-method-in-class-win32-service.md)                               | Löscht einen vorhandenen Dienst.<br/>                                                              |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-service.md) | Gibt die Sicherheitsbeschreibung zurück, die den Zugriff auf den Dienst steuert.<br/>                      |
| [**InterrogateService**](interrogateservice-method-in-class-win32-service.md)       | Fordert an, dass ein Dienst seinen Zustand an den Dienst-Manager aktualisiert.<br/>                          |
| [**PauseService**](pauseservice-method-in-class-win32-service.md)                   | Versucht, einen Dienst im angehaltenen Zustand zu platzieren.<br/>                                          |
| [**ResumeService**](resumeservice-method-in-class-win32-service.md)                 | Versucht, einen Dienst im Status "Fortgesetzt" zu platzieren.<br/>                                         |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-service.md) | Schreibt eine aktualisierte Version der Sicherheitsbeschreibung, die den Zugriff auf den Dienst steuert.<br/> |
| [**Startservice**](startservice-method-in-class-win32-service.md)                   | Versucht, einen Dienst in den Startzustand zu bringen.<br/>                                       |
| [**StopService**](stopservice-method-in-class-win32-service.md)                     | Versetzt einen Dienst in den Zustand "Beendet".<br/>                                                    |
| [**UserControlService**](usercontrolservice-method-in-class-win32-service.md)       | Versucht, einen benutzerdefinierten Steuerelementcode an einen Dienst zu senden.<br/>                                |



 

### <a name="properties"></a>Eigenschaften

Die **\_ Win32-Dienstklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Dienststrukturen \| \| [**SERVICE \_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT PAUSE \_ \_ \_ CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Dienst akzeptiert Pause")
</dt> </dl>

Gibt an, ob der Dienst angehalten werden kann.

Diese Eigenschaft wird von [**Win32 \_ BaseService**](win32-baseservice.md)geerbt.

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT \_ \_ STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")
</dt> </dl>

Gibt an, ob der Dienst beendet werden kann.

Diese Eigenschaft wird von [**Win32 \_ BaseService**](win32-baseservice.md)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Kurze Beschreibung des Diensts – eine einzeilige Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Prüfpunkt**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Dienststrukturen \| \| [**SERVICE \_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")
</dt> </dl>

Der Wert, den der Dienst in regelmäßigen Abständen erhöht, um den Fortschritt während eines langen Start-, Stopp-, Pausen- oder Fortsetzungsvorgangs zu melden. Beispielsweise erhöht der Dienst diesen Wert, wenn er jeden Schritt seiner Initialisierung abschließt, wenn er gestartet wird. Das Benutzeroberflächenprogramm, das den Vorgang für den Dienst aufruft, verwendet diesen Wert, um den Fortschritt des Diensts während eines längeren Vorgangs nachzuverfolgen. Dieser Wert ist ungültig und sollte 0 (null) sein, wenn für den Dienst kein Start-, Stopp-, Pausen- oder Fortsetzungsvorgang aussteht.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](../wmisdk/standard-wmi-qualifiers.md) [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Klassenname")
</dt> </dl>

Name der ersten konkreten Klasse, die in der Vererbungskette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit den anderen Schlüsseleigenschaften der -Klasse ermöglicht diese Eigenschaft die eindeutige Identifizierung aller Instanzen dieser Klasse und ihrer Unterklassen.

Diese Eigenschaft wird vom [**\_ CIM-Dienst**](cim-service.md)geerbt.

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Dienststrukturen \| \| [**SERVICE \_ DELAYED AUTO START \_ \_ \_ INFO**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Delayed Auto-Start")
</dt> </dl>

**True** gibt an, dass der Dienst gestartet wird, nachdem andere dienste automatisch gestartet wurden, plus einer kurzen Verzögerung.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Beschreibung")
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Dienststrukturen \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| SERVICE INTERACTIVE \_ \_ PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interagiert mit Desktop")
</dt> </dl>

Gibt an, ob der Dienst Fenster auf dem Desktop erstellen oder mit ihnen kommunizieren kann und somit in irgendeiner Weise mit einem Benutzer interagiert. Interaktive Dienste müssen unter dem lokalen Systemkonto ausgeführt werden. Die meisten Dienste sind nicht interaktiv. Das heißt, sie kommunizieren in keiner Weise mit dem Benutzer.

Diese Eigenschaft wird von [**Win32 \_ BaseService**](win32-baseservice.md)geerbt.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Dienststrukturen \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Anzeigename")
</dt> </dl>

Name des Diensts, wie er im Snap-In Dienste angezeigt wird. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Beachten Sie, dass der Anzeigename und der Dienstname (der in der Registrierung gespeichert ist) nicht immer identisch sind. Der DHCP-Clientdienst hat beispielsweise den Dienstnamen Dhcp, aber den Anzeigenamen DHCP-Client. Der Name wird im Dienststeuerungs-Manager beibehalten. Bei **DisplayName-Vergleichen** wird die Groß-/Kleinschreibung jedoch immer nicht beachtet.

Einschränkung: Akzeptiert den gleichen Wert wie die **Name-Eigenschaft.**

Beispiel: "Atdisk"

Diese Eigenschaft wird von [**Win32 \_ BaseService geerbt.**](win32-baseservice.md)

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Dienststrukturen \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Schweregrad des Startfehlers")
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

Diese Eigenschaft wird von [**Win32 \_ BaseService geerbt.**](win32-baseservice.md)

</dd> <dt>

**Exitcode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")
</dt> </dl>

Windows Fehlercode, der Fehler definiert, die beim Starten oder Beenden des Diensts aufgetreten sind. Diese Eigenschaft wird auf **ERROR \_ SERVICE SPECIFIC \_ \_ ERROR** (1066) festgelegt, wenn der Fehler für den durch diese Klasse dargestellten Dienst eindeutig ist und Informationen zum Fehler in der **ServiceSpecificExitCode-Eigenschaft verfügbar** sind. Der Dienst legt diesen Wert bei der Ausführung **auf NO \_ ERROR** und bei normaler Beendigung erneut fest.

Diese Eigenschaft wird von [**Win32 \_ BaseService geerbt.**](win32-baseservice.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Installation date")
</dt> </dl>

Das Date-Objekt wird installiert. Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](../wmisdk/key-qualifier.md)
</dt> </dl>

Eindeutiger Bezeichner des Diensts, der einen Hinweis auf die verwaltete Funktionalität bietet. Diese Funktionalität wird in der **Description-Eigenschaft** des -Objekts beschrieben.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Dateipfadname")
</dt> </dl>

Vollqualifizierter Pfad zur Binärdatei des Diensts, die den Dienst implementiert.

Beispiel: \\ "SystemRoot \\ \\ System32-Treiber \\afd.sys"

Diese Eigenschaft wird von [**Win32 \_ BaseService geerbt.**](win32-baseservice.md)

</dd> <dt>

**Processid**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE STATUS \| [**\_ \_ PROCESS**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")
</dt> </dl>

Prozessbezeichner des Diensts.

Beispiel: 324

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Dienststrukturen \| \| [**SERVICE \_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Serverspezifischer Exitcode")
</dt> </dl>

Dienstspezifischer Fehlercode für Fehler, die auftreten, während der Dienst gestartet oder beendet wird. Die Exitcodes werden durch den von dieser Klasse dargestellten Dienst definiert. Dieser Wert wird nur festgelegt, wenn der **ExitCode-Eigenschaftswert** **ERROR SERVICE SPECIFIC \_ \_ \_ ERROR** (1066) ist.

Diese Eigenschaft wird von [**Win32 \_ BaseService geerbt.**](win32-baseservice.md)

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Dienststrukturen \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Diensttyp")
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

Diese Eigenschaft wird von [**Win32 \_ BaseService geerbt.**](win32-baseservice.md)

</dd> <dt>

**Begann**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")
</dt> </dl>

Gibt an, ob der Dienst gestartet wird.

Diese Eigenschaft wird vom [**CIM-Dienst \_ geerbt.**](cim-service.md)

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Startmodus")
</dt> </dl>

Startmodus des Windows Basisdiensts.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Start** ("Boot")


</dt> <dd>

Vom Betriebssystemlader gestarteter Gerätetreiber (nur für Treiberdienste gültig).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")


</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungsprozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")


</dt> <dd>

Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden. Automatische Dienste werden auch dann gestartet, wenn sich ein Benutzer nicht anmeldet.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell** ("Manuell")


</dt> <dd>

Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService-Methode**](startservice-method-in-class-win32-service.md) aufruft. Diese Dienste werden erst gestartet, wenn sich ein Benutzer anmeldet und startet.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("Deaktiviert")


</dt> <dd>

Dienst, der erst gestartet werden kann, wenn startMode in Auto oder Manual geändert wurde.

</dd> </dl>

Diese Eigenschaft wird vom [**\_ CIM-Dienst**](cim-service.md)geerbt.

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Dienststrukturen \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Startkontoname")
</dt> </dl>

Kontoname, unter dem ein Dienst ausgeführt wird. Je nach Diensttyp kann der Kontoname das Format \\ "Domänenname-Benutzername" oder UPN-Format *Username@DomainName* ("") aufweisen. Der Dienstprozess wird bei der Ausführung mit einer dieser beiden Formen protokolliert. Wenn das Konto zur integrierten Domäne gehört, dann ". \\ Username" kann angegeben werden. Für Kernel- oder Treiber auf Systemebene enthält **StartName** den Treiberobjektnamen (d.h. \\ "FileSystem \\ Rdr" oder \\ "Driver \\ Xns"), den das E/A-System zum Laden des Gerätetreibers verwendet. Wenn **NULL** angegeben wird, wird der Treiber außerdem mit einem Standardobjektnamen ausgeführt, der vom E/A-System basierend auf dem Dienstnamen erstellt wurde.

Beispiel: "DWDOM \\ Admin"

Diese Eigenschaft wird von [**Win32 \_ BaseService**](win32-baseservice.md)geerbt.

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Dienststrukturen \| \| [**SERVICE \_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")
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

Diese Eigenschaft wird von [**Win32 \_ BaseService**](win32-baseservice.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs- und Nichtoperationsstatus definiert werden. Betriebsstatus: "OK", "Heruntergestuft" und "Pred Fail" (ein Element, z. B. ein SMART-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, sagt aber einen Fehler in naher Zukunft vorher). Nichtoperationale Status: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann während des Spiegelungsresilverings eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Verwaltungsaufgaben angewendet werden. Nicht alle dieser Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

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

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](../wmisdk/standard-qualifiers.md) ("[**\_ CIM-System**](cim-system.md).**CreationClassName**"), [**\_ CIM-Schlüssel,**](../wmisdk/standard-wmi-qualifiers.md) [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Systemklassenname")
</dt> </dl>

Geben Sie den Namen des Systems ein, das diesen Dienst hostet.

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

**TagId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Dienststrukturen \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag-ID")
</dt> </dl>

Eindeutiger Tagwert für diesen Dienst in der Gruppe. Der Wert 0 (null) gibt an, dass der Dienst kein Tag besitzt. Ein Tag kann verwendet werden, um den Dienststart innerhalb einer Lastreihenfolgegruppe zu bestellen, indem in der Registrierung unter ein Tagreihenfolgevektor angegeben wird:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **GroupOrderList**    

Tags werden nur für Starttypdienste des Kerneltreibers und des Dateisystemtreibers ausgewertet, die den Start- oder Systemstartmodus aufweisen.

Diese Eigenschaft wird von [**Win32 \_ BaseService**](win32-baseservice.md)geerbt.

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Dienststrukturen \| \| [**SERVICE \_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Geschätzte Wartezeit")
</dt> </dl>

Geschätzte Zeit in Millisekunden für einen ausstehenden Start-, Beendigungs-, Pausen- oder Fortsetzungsvorgang. Nach Ablauf der angegebenen Zeit ruft der Dienst die **SetServiceStatus-Methode** entweder mit einem erhöhten **CheckPoint-Wert** oder einer Änderung in **CurrentState** auf. Wenn die von **WaitHint** angegebene Zeit vergeht und **CheckPoint** nicht erhöht wurde oder **CurrentState** nicht geändert wurde, geht der Dienststeuerungs-Manager oder das Dienststeuerungsprogramm davon aus, dass ein Fehler aufgetreten ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ Win32-Dienstklasse** wird von [**Win32 \_ BaseService**](win32-baseservice.md)abgeleitet.

Die Art und Weise, wie Sie einen bestimmten Computer verwalten, hängt stark von der Rolle ab, die der Computer spielt. Beispielsweise überwachen Sie im Allgemeinen andere Aspekte eines DNS-Servers als ein DHCP-Server. Obwohl keine einzelne Eigenschaft Ihnen mitteilen kann, ob ein bestimmter Computer ein Datenbankserver, ein E-Mail-Server oder ein Multimediaserver ist, können Sie häufig die Rolle eines Computers identifizieren, indem Sie die darauf installierten Dienste identifizieren.

In großen Organisationen wird wahrscheinlich nur einer der wichtigsten Dienste (z. B. E-Mail) auf einem einzelnen Computer installiert. Es wäre ungewöhnlich, dass ein E-Mail-Server auch als Server für Microsoft® Windows Media® Technologies Player-Dateien ausgeführt wird. Aus diesem Grund kann die Identifizierung eines auf einem Computer installierten Diensts dazu beitragen, die Rolle des Computers im Netzwerk zu identifizieren. Wenn der Microsoft® Exchange Server-Dienst auf einem Computer installiert ist und ausgeführt wird, kann in der Regel davon ausgegangen werden, dass dieser Computer als E-Mail-Server fungiert.

Sie können die WMI **Win32 \_ Service-Klasse** verwenden, um die auf einem Computer installierten Dienste aufzuzählen. Darüber hinaus können Sie diese Klasse verwenden, um zu bestimmen, ob diese Dienste derzeit ausgeführt werden, und um weitere erforderliche Informationen zu diesem Dienst und seiner Konfiguration zurückzugeben.

Eine Dienstanwendung entspricht den Schnittstellenregeln des Dienststeuerungs-Managers (Service Control Manager, SCM) und kann automatisch von einem Benutzer beim Systemstart über das Systemsteuerungshilfsprogramm Dienste oder durch eine Anwendung gestartet werden, die die in der Windows-API enthaltenen Dienstfunktionen verwendet. Dienste können gestartet werden, wenn keine Benutzer am Computer angemeldet sind.

Für einen Benutzer, der eine Verbindung von einem Remotecomputer herstellt, muss die **SC \_ MANAGER \_ CONNECT-Berechtigung** aktiviert sein, um diese Klasse aufzählen zu können. Weitere Informationen finden Sie unter [Dienstsicherheit und Zugriffsrechte.](../services/service-security-and-access-rights.md)

## <a name="examples"></a>Beispiele

Die [PS-WMI-Abfrage, die den Dienst "State" für eine Gruppe von Geräten zurückgibt,](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) im TechNet-Katalog verwendet das PowerShell-Beispiel **win32 \_ Service,** um eine Liste von Geräten aus Active Directory zu erstellen und dann jedes Gerät abzufragen, das mit Ping für einen bestimmten ausgeführten Dienst antwortet.

Im PowerShell-Beispiel für [Serverbericht](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) im TechNet-Katalog wird **win32 \_ Service** verwendet, um Serverinformationen zu sammeln und im Word-Dokument zu veröffentlichen.

Im folgenden VBScript-Codebeispiel werden alle derzeit installierten Dienste angezeigt.


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



Im folgenden VBScript-Codebeispiel werden die angehaltenen, ausgeführten und beendeten Dienste auf dem angegebenen Computer beschrieben.


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



Das folgende Perl-Skript veranschaulicht, wie sie eine Liste der ausgeführten Dienste aus Instanzen von **Win32 \_ Service** abrufen.


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



Im folgenden \# c-Beispiel wird [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) verwendet, um alle ausgeführten Dienste auf dem lokalen Computer abzurufen.


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



Im folgenden \# C-Codebeispiel wird der [System.Management-Namespace](/dotnet/api/system.management) verwendet, um alle ausgeführten Dienste auf dem lokalen Computer abzurufen.

> [!Note]  
> [System.Management](/dotnet/api/system.management) enthält die ursprünglichen Klassen, die für den Zugriff auf WMI verwendet werden. Sie gelten jedoch als langsamer und skalieren im Allgemeinen nicht so gut wie ihre [Microsoft.Management.Infrastructure-Entsprechungen.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


        }
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[WMI-Aufgaben: Dienste](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
