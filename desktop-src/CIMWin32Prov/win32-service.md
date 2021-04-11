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
ms.openlocfilehash: b342282bfa3b49fe72e62cf79377a0ead11276eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041353"
---
# <a name="win32_service-class"></a>Win32- \_ Dienstklasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32- \_ Dienst** stellt einen Dienst auf einem Computersystem mit Windows dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

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

Die **Win32- \_ Dienst** Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32- \_ Dienst** Klasse verfügt über diese Methoden.



| Methode                                                                               | BESCHREIBUNG                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Klima**](change-method-in-class-win32-service.md)                               | Ändert einen Dienst.<br/>                                                                       |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-service.md)             | Ändert den Start Modus eines Dienstanbieter.<br/>                                                     |
| [**Stelle**](create-method-in-class-win32-service.md)                               | Erstellt einen neuen Dienst.<br/>                                                                    |
| [**Lösch**](delete-method-in-class-win32-service.md)                               | Löscht einen vorhandenen Dienst.<br/>                                                              |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-service.md) | Gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Dienst steuert.<br/>                      |
| [**"InterrogateService"**](interrogateservice-method-in-class-win32-service.md)       | Fordert an, dass ein Dienst seinen Status auf den Dienst-Manager aktualisiert.<br/>                          |
| [**PauseService**](pauseservice-method-in-class-win32-service.md)                   | Versucht, einen Dienst in den angehaltenen Zustand zu versetzen.<br/>                                          |
| [**ResumeService**](resumeservice-method-in-class-win32-service.md)                 | Versucht, einen Dienst in den Status "wieder aufgenommen" zu versetzen.<br/>                                         |
| [**SETSECURITYDESCRIPTOR**](setsecuritydescriptor-method-in-class-win32-service.md) | Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Dienst steuert.<br/> |
| [**Start Service**](startservice-method-in-class-win32-service.md)                   | Versucht, einen Dienst in den Startzustand zu versetzen.<br/>                                       |
| [**Stop Service**](stopservice-method-in-class-win32-service.md)                     | Versetzt einen Dienst in den Status "beendet".<br/>                                                    |
| [**UserControlService**](usercontrolservice-method-in-class-win32-service.md)       | Versucht, einen benutzerdefinierten Steuerelement Code an einen Dienst zu senden.<br/>                                |



 

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ Dienst** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept \_ Pause \_ Continue"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Service Accept Pause")
</dt> </dl>

Gibt an, ob der Dienst angehalten werden kann.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept End \_ "), [**Display Name**](../wmisdk/standard-qualifiers.md) ("der Dienst akzeptiert das Ende")
</dt> </dl>

Gibt an, ob der Dienst beendet werden kann.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Kurze Beschreibung des Dienstanbieter – eine einzeilige Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Kal**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwcheck"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Check Point count")
</dt> </dl>

Der Wert, den der Dienst in regelmäßigen Abständen erhöht, um den Fortschritt während eines langen Starts, Anhaltevorgangs, anhalten oder fortsetzen zu melden. Der Dienst erhöht z. b. diesen Wert, da er die einzelnen Schritte seiner Initialisierung beim Starten abschließt. Das Benutzeroberflächen Programm, das den-Vorgang für den Dienst aufruft, verwendet diesen Wert, um den Status des Dienstanbieter während eines langwierigen Vorgangs zu verfolgen. Dieser Wert ist ungültig und sollte NULL sein, wenn der Dienst nicht über einen Vorgang zum Starten, beenden, anhalten oder fortsetzen verfügt.

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Class Name")
</dt> </dl>

Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird. Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ verzögert \_ Auto \_ Start \_ Info**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| f delayedautostart"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("verzögerter automatischer Start")
</dt> </dl>

**True** gibt an, dass der Dienst gestartet wird, nachdem andere automatischen Start Dienste und eine kurze Verzögerung gestartet wurden.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype \| Service \_ Interactive \_ Process"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("interagiert with Desktop")
</dt> </dl>

Gibt an, ob der Dienst Windows auf dem Desktop erstellen oder mit ihm kommunizieren kann, sodass er auf irgendeine Weise mit einem Benutzer interagieren kann. Interaktive Dienste müssen unter dem lokalen System Konto ausgeführt werden. Die meisten Dienste sind nicht interaktiv. Das heißt, Sie kommunizieren in keiner Weise mit dem Benutzer.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpdisplayname"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Anzeige Name")
</dt> </dl>

Der Name des Diensts, wie im Dienste-Snap-in angezeigt. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Beachten Sie, dass der Anzeige Name und der Dienst Name (der in der Registrierung gespeichert ist) nicht immer identisch sind. Der DHCP-Client Dienst hat z. b. den Dienstnamen DHCP, aber den anzeigen Amen DHCP-Client. Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten. Bei **DisplayName** -vergleichen wird jedoch immer die Groß-/Kleinschreibung nicht beachtet.

Einschränkung: akzeptiert denselben Wert wie die **Name** -Eigenschaft.

Beispiel: "ATDISK"

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwerrorcontrol"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Schweregrad des Start Fehlers")
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

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

</dd> <dt>

**Exitcode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Exitcode")
</dt> </dl>

Windows-Fehlercode, der Fehler definiert, die beim Starten oder Beenden des Dienstes aufgetreten sind. Diese Eigenschaft ist auf **Fehler \_ Dienst \_ spezifischer \_ Fehler** (1066) festgelegt, wenn der Fehler für den Dienst eindeutig ist, der durch diese Klasse dargestellt wird. Informationen über den Fehler sind in der **ServiceSpecificExitCode** -Eigenschaft verfügbar. Der Dienst legt diesen Wert bei der Ausführung und erneut bei normaler Beendigung auf **keinen \_ Fehler** fest.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")
</dt> </dl>

Date-Objekt ist installiert. Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](../wmisdk/key-qualifier.md)
</dt> </dl>

Eindeutiger Bezeichner des dienstanweises, der angibt, welche Funktionen verwaltet werden. Diese Funktionalität wird in der **Description** -Eigenschaft des-Objekts beschrieben.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpbinarypathname"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Dateipfadname")
</dt> </dl>

Der voll qualifizierte Pfad der Dienst Binärdatei, die den Dienst implementiert.

Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys"

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status \_ Process**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Process ID")
</dt> </dl>

Prozess Bezeichner des Dienstanbieter.

Beispiel: 324

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwservicespecificexitcode"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Server spezifischer Exitcode")
</dt> </dl>

Dienst spezifischer Fehlercode für Fehler, die auftreten, während der Dienst gestartet oder beendet wird. Die Exitcodes werden von dem Dienst definiert, der durch diese Klasse dargestellt wird. Dieser Wert wird nur festgelegt, wenn der **Exitcode** -Eigenschafts Wert **Fehler \_ Dienst \_ spezifisch \_** ist (1066).

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Service Type")
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

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

</dd> <dt>

**Gestartet**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Started")
</dt> </dl>

Gibt an, ob der Dienst gestartet wurde.

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

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-service.md) -Methode aufruft. Diese Dienste werden erst gestartet, wenn sich ein Benutzer anmeldet und startet.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")


</dt> <dd>

Dienst, der erst gestartet werden kann, wenn sein StartMode entweder in "Auto" oder "manuell" geändert wurde.

</dd> </dl>

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpservicestartname"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")
</dt> </dl>

Der Kontoname, unter dem ein Dienst ausgeführt wird. Abhängig vom Diensttyp kann der Kontoname die Form "Domainname \\ username" oder das UPN-Format (" *Username@DomainName* ") aufweisen. Der Dienst Prozess wird mit einer dieser beiden Formulare protokolliert, wenn er ausgeführt wird. Wenn das Konto zur integrierten Domäne gehört, dann ". \\ Username "kann angegeben werden. Für Treiber auf Kernel-oder Systemebene enthält **StartName** den Treiber Objektnamen (d. h. " \\ File System \\ rdr" oder " \\ Driver \\ XNS"), den das e/a-System zum Laden des Gerätetreibers verwendet. Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde.

Beispiel: "dwdom \\ Admin"

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwcurrentstate"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("State")
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

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen). Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

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

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("System Klassenname")
</dt> </dl>

Der Typname des Systems, das den Dienst hostet.

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

**TagID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwtagid"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Tag ID")
</dt> </dl>

Eindeutiger Tagwert für diesen Dienst in der Gruppe. Der Wert 0 (null) gibt an, dass der Dienst nicht über ein Tag verfügt. Ein-Tag kann verwendet werden, um den Dienst Start innerhalb einer Gruppe von Lade Reihenfolgen zu sortieren, indem Sie in der Registrierung einen taganordnungs Vektor angeben:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Steuer** Element \\ **grouporderlist**    

Tags werden nur für Kernel Treiber-und Datei System Treiber-Starttyp Dienste ausgewertet, die über Start-oder System Start Modi verfügen.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwwaithint"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("geschätzte Wartezeit")
</dt> </dl>

Geschätzte benötigte Zeit (in Millisekunden) für einen ausstehenden Start-, anhalte-, Anhaltevorgang-oder continue-Vorgang. Nachdem die angegebene Zeit abgelaufen ist, führt der Dienst den nächsten Aufruf der **SetServiceStatus** -Methode mit einem **inkrementierten** Prüf Punkt Wert oder einer Änderung in **CurrentState** aus. Wenn die von **WaitHint** angegebene Zeitspanne verstrichen **ist und der** Prüfpunkt nicht inkrementiert wurde, oder **CurrentState** nicht geändert wurde, geht der Dienststeuerungs-Manager oder das Dienst Steuerungsprogramm davon aus, dass ein Fehler aufgetreten ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ Dienst** Klasse wird von [**Win32 \_ baseservice**](win32-baseservice.md)abgeleitet.

Die Art und Weise, in der Sie einen bestimmten Computer verwalten, hängt stark von der Rolle des Computers ab. Beispielsweise überwachen Sie im allgemeinen verschiedene Aspekte eines DNS-Servers als einen DHCP-Server. Obwohl keine einzelne Eigenschaft Aufschluss darüber geben kann, ob es sich bei einem bestimmten Computer um einen Datenbankserver, einen e-Mail-Server oder einen Multimedia-Server handelt, können Sie die Rolle eines Computers häufig ermitteln, indem Sie die installierten Dienste identifizieren.

In großen Organisationen ist es wahrscheinlich, dass nur einer der Haupt Dienste (z. b. e-Mail) auf einem einzelnen Computer installiert wird. Es ist nicht ungewöhnlich, dass ein Mailserver auch als Server für Microsoft® Windows Media® Technologies-Technologien Player-Dateien ausführt. Aus diesem Grund kann das Identifizieren eines auf einem Computer installierten Dienstanbieter helfen, die Rolle des Computers im Netzwerk zu identifizieren. Wenn der Microsoft® Exchange Server-Dienst installiert ist und auf einem Computer ausgeführt wird, ist es im Allgemeinen sicher, dass dieser Computer als e-Mail-Server fungiert.

Sie können die WMI- **Win32- \_ Dienst** Klasse verwenden, um die auf einem Computer installierten Dienste aufzuzählen. Außerdem können Sie diese Klasse verwenden, um zu bestimmen, ob diese Dienste derzeit ausgeführt werden, und um alle anderen erforderlichen Informationen zu diesem Dienst und dessen Konfiguration zurückzugeben.

Eine-Dienst Anwendung entspricht den Schnittstellen Regeln des Dienststeuerungs-Managers (Service Control Manager, SCM) und kann von einem Benutzer automatisch beim Systemstart über das System Steuerungsprogramm "Dienste" oder durch eine Anwendung gestartet werden, die die in der Windows-API enthaltenen Dienstfunktionen verwendet. Dienste können gestartet werden, wenn keine Benutzer am Computer angemeldet sind.

Ein Benutzer, der eine Verbindung über einen Remote Computer herstellt, muss über die Berechtigung **SC- \_ Manager \_ Connect** verfügen, damit diese Klasse aufgelistet werden kann. Weitere Informationen finden Sie unter [Dienst Sicherheit und Zugriffsrechte](../services/service-security-and-access-rights.md).

## <a name="examples"></a>Beispiele

Die [PS-WMI-Abfrage, die den Dienst "State" für eine Gruppe von Geräten](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell-Beispiel in der TechNet Gallery zurückgibt, verwendet den **Win32- \_ Dienst** , um eine Liste der Geräte aus Active Directory zu erstellen und anschließend jedes Gerät abzufragen, das mit pingfor einen bestimmten Dienst ausgeführt wird.

Das PowerShell-Beispiel für [Server Berichte](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) in der TechNet Gallery verwendet den **Win32- \_ Dienst** zum Erfassen von Server Informationen und veröffentlichen im Word-Dokument.

Im folgenden VBScript-Codebeispiel werden alle zurzeit installierten Dienste angezeigt.


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



Im folgenden VBScript-Codebeispiel werden die angehaltenen, laufenden und beendeten Dienste auf dem angegebenen Computer beschrieben.


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



Das folgende perl-Skript veranschaulicht, wie Sie eine Liste der laufenden Dienste aus Instanzen des **Win32- \_ Diensts** abrufen.


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



Im folgenden c- \# Beispiel wird [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) verwendet, um alle laufenden Dienste auf dem lokalen Computer abzurufen.


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



Im folgenden C- \# Codebeispiel wird der [System. Management](/dotnet/api/system.management) -Namespace verwendet, um alle laufenden Dienste auf dem lokalen Computer abzurufen.

> [!Note]  
> [System. Management](/dotnet/api/system.management) enthält die ursprünglichen Klassen, die für den Zugriff auf WMI verwendet werden. Allerdings gelten Sie als langsamer und werden im Allgemeinen nicht ebenso skaliert wie Ihre [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) -Entsprechungen.

 


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ baseservice**](win32-baseservice.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[WMI-Tasks: Dienste](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
