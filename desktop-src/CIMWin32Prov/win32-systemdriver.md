---
description: Stellt den System Treiber für einen Basis Dienst dar.
ms.assetid: 67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2
ms.tgt_platform: multiple
title: Win32_SystemDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver
- Win32_SystemDriver.AcceptPause
- Win32_SystemDriver.AcceptStop
- Win32_SystemDriver.Caption
- Win32_SystemDriver.CreationClassName
- Win32_SystemDriver.Description
- Win32_SystemDriver.DesktopInteract
- Win32_SystemDriver.DisplayName
- Win32_SystemDriver.ErrorControl
- Win32_SystemDriver.ExitCode
- Win32_SystemDriver.InstallDate
- Win32_SystemDriver.Name
- Win32_SystemDriver.PathName
- Win32_SystemDriver.ServiceSpecificExitCode
- Win32_SystemDriver.ServiceType
- Win32_SystemDriver.Started
- Win32_SystemDriver.StartMode
- Win32_SystemDriver.StartName
- Win32_SystemDriver.State
- Win32_SystemDriver.Status
- Win32_SystemDriver.SystemCreationClassName
- Win32_SystemDriver.SystemName
- Win32_SystemDriver.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15be9b176680e8abb259d3d011da9d6cec0c2fa8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748401"
---
# <a name="win32_systemdriver-class"></a>Win32 \_ systemdriver-Klasse

Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) des Win32-System **\_ Treibers** stellt den System Treiber für einen Basis Dienst dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4C5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDriver : Win32_BaseService
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a>Member

Die **Win32 \_ System Driver** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ System Driver** -Klasse verfügt über diese Methoden.



| Methode                                                                              | BESCHREIBUNG                                                                                     |
|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Klima**](change-method-in-class-win32-systemdriver.md)                         | Klassenmethode, die einen Dienst ändert.<br/>                                                |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-systemdriver.md)       | Klassenmethode, mit der der Start Modus eines Dienstanbieter geändert wird.<br/>                              |
| [**Stelle**](create-method-in-class-win32-systemdriver.md)                         | Klassenmethode, mit der ein neuer Dienst erstellt wird.<br/>                                             |
| [**Lösch**](delete-method-in-class-win32-systemdriver.md)                         | Klassenmethode, mit der ein vorhandener Dienst gelöscht wird.<br/>                                       |
| [**"InterrogateService"**](interrogateservice-method-in-class-win32-systemdriver.md) | Class-Methode, die anfordert, dass der Dienst seinen Status an den Dienst-Manager aktualisiert.<br/> |
| [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md)             | Klassenmethode, die versucht, den Dienst in den angehaltenen Zustand zu versetzen.<br/>                 |
| [**ResumeService**](resumeservice-method-in-class-win32-systemdriver.md)           | Klassenmethode, die versucht, den Dienst in den Status "wieder aufgenommen" zu versetzen.<br/>                |
| [**Start Service**](startservice-method-in-class-win32-systemdriver.md)             | Klassenmethode, die versucht, den Dienst in seinen Startzustand zu versetzen.<br/>              |
| [**Stop Service**](stopservice-method-in-class-win32-systemdriver.md)               | Klassenmethode, die den Dienst in den Zustand "beendet" versetzt.<br/>                           |
| [**UserControlService**](usercontrolservice-method-in-class-win32-systemdriver.md) | Klassenmethode, die versucht, einen benutzerdefinierten Steuerelement Code an einen Dienst zu senden.<br/>         |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ System Driver** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept \_ Pause \_ Continue"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Service Accept Pause")
</dt> </dl>

Der Dienst kann angehalten werden.

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

Der Dienst kann angehalten werden.

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

Kurze Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

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

Dieser Dienst kann Windows auf dem Desktop erstellen oder mit ihm kommunizieren.

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

Der Anzeige Name des Dienstanbieter. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten. Bei **Display Name** -vergleichen wird immer die Groß-/Kleinschreibung beachtet.

Einschränkungen: akzeptiert denselben Wert wie die **Name** -Eigenschaft.

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

Der Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann. Dieser Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt. Alle Fehler werden vom Computersystem protokolliert.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** ("ignorieren")


</dt> <dd>

Der Benutzer wird nicht benachrichtigt.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")


</dt> <dd>

Der Benutzer wird benachrichtigt.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** ("schwerwiegend")


</dt> <dd>

Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** ("kritisch")


</dt> <dd>

Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** ("unbekannt")


</dt> <dd>

Die Ursache des Fehlers ist unbekannt.

</dd> </dl>

</dd> <dt>

**Exitcode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Exitcode")
</dt> </dl>

Windows-Fehlercode, der Probleme definiert, die beim Starten oder Beenden des Dienstes aufgetreten sind. Diese Eigenschaft ist auf **Fehler \_ Dienst \_ spezifischer \_ Fehler** (1066) festgelegt, wenn der Fehler für den Dienst eindeutig ist, der durch diese Klasse dargestellt wird. Informationen über den Fehler sind in der **ServiceSpecificExitCode** -Eigenschaft verfügbar. Der Dienst legt diesen Wert bei der Ausführung und erneut bei normaler Beendigung auf **keinen \_ Fehler** fest.

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

Das Objekt wurde installiert. Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.

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

Eindeutiger Bezeichner für den Dienst, der eine Angabe der verwalteten Funktionalität bereitstellt. Diese Funktionalität wird in der Objekt **Beschreibungs** Eigenschaft ausführlicher beschrieben.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.

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

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

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

</dd> <dt>

**Gestartet**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Started")
</dt> </dl>

Der Dienst wurde gestartet.

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

Der Start Modus des System Treibers.

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

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

Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell** ("manuell")


</dt> <dd>

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-systemdriver.md) -Methode aufruft.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")


</dt> <dd>

Dienst, der nicht mehr gestartet werden kann.

</dd> </dl>

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpservicestartname"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")
</dt> </dl>

Der Kontoname, unter dem der Dienst ausgeführt wird. Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name \\ Benutzername" aufweisen. Der Dienst Prozess wird bei der Ausführung mithilfe einer dieser beiden Formulare protokolliert. , Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden. Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Bei Kernel-oder System Treibern enthält **StartName** den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden. Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde.

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

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

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

Eindeutiger Tagwert für diesen Dienst in der Gruppe. Der Wert 0 (null) gibt an, dass dem Dienst kein Tag zugewiesen wurde. Ein Tag kann zum Sortieren des Dienst Starts innerhalb einer Gruppe von Lade Reihenfolgen verwendet werden, indem ein taganordnungs Vektor in der Registrierung unter angegeben wird:

Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.

**HKEY \_ Lokales \_ Computer \\ System \\ CurrentControlSet \\ Steuerelement \\ grouporderlist**.

Tags werden nur für die Start-und Systemstart Modi des Kernel Treibers und des Datei System-Treibers ausgewertet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ System Driver** -Klasse wird von [**Win32 \_ baseservice**](win32-baseservice.md)abgeleitet.

## <a name="examples"></a>Beispiele

Im Beispiel " [List System Drivers](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript" werden installierte System Treiber in einer HTML-Datei angezeigt.

Das folgende PowerShell-Beispiel ruft eine Reihe von Eigenschaften aus den System Treibern auf einem Computer ab.


```PowerShell
Get-WmiObject -Class Win32_SystemDriver | Where-Object -FilterScript {$_.State -eq "Running"} | Where-Object -FilterScript {$_.StartMode -eq "Manual"} | Format-Table -Property Name,DisplayName
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
</dt> </dl>

 

 
