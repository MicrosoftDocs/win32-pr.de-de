---
description: Die \_ WMI-Klasse der WMI-Klasse "Win32 baseservice" stellt ausführbare Objekte dar, die in einer vom Dienststeuerungs-Manager verwalteten Registrierungsdatenbank installiert werden
ms.assetid: 63673df9-3e41-4668-98fe-dc0e048328c1
ms.tgt_platform: multiple
title: Win32_BaseService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService
- Win32_BaseService.AcceptPause
- Win32_BaseService.AcceptStop
- Win32_BaseService.Caption
- Win32_BaseService.CreationClassName
- Win32_BaseService.Description
- Win32_BaseService.DesktopInteract
- Win32_BaseService.DisplayName
- Win32_BaseService.ErrorControl
- Win32_BaseService.ExitCode
- Win32_BaseService.InstallDate
- Win32_BaseService.Name
- Win32_BaseService.PathName
- Win32_BaseService.ServiceSpecificExitCode
- Win32_BaseService.ServiceType
- Win32_BaseService.Started
- Win32_BaseService.StartMode
- Win32_BaseService.StartName
- Win32_BaseService.State
- Win32_BaseService.Status
- Win32_BaseService.SystemCreationClassName
- Win32_BaseService.SystemName
- Win32_BaseService.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b46f3b4bd37770a5f3a7c1a2d2faa93d49bc079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127488"
---
# <a name="win32_baseservice-class"></a>Win32 \_ baseservice-Klasse

Die [WMI-Klasse der WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ baseservice** " stellt ausführbare Objekte dar, die in einer vom Dienststeuerungs-Manager verwalteten Registrierungsdatenbank installiert werden Die mit einem Dienst verknüpfte ausführbare Datei kann beim Start von einem Start Programm oder vom System gestartet werden. Sie kann auch bei Bedarf vom Dienststeuerungs-Manager gestartet werden. Dienste oder Prozesse, die nicht im Besitz eines bestimmten Benutzers sind und eine Schnittstelle für einige Funktionen bereitstellen, die vom Computersystem unterstützt werden, sind ein Nachfolger (oder Mitglied) dieser Klasse.

Beispiel: der DHCP-Client Dienst (Dynamic Host Configuration-Protokoll) auf einem Computersystem, auf dem Windows Server ausgeführt wird.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C4C4-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("System Drivers and Services"), AMENDMENT]
class Win32_BaseService : CIM_Service
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

Die **Win32 \_ baseservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ baseservice** -Klasse verfügt über diese Methoden.



| Methode                                                                             | BESCHREIBUNG                                                                   |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Klima**](change-method-in-class-win32-baseservice.md)                         | Ändert einen Dienst.<br/>                                                |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-baseservice.md)       | Ändert den Start Modus eines Dienstanbieter.<br/>                              |
| [**Stelle**](create-method-in-class-win32-baseservice.md)                         | Erstellt einen neuen Dienst.<br/>                                             |
| [**Lösch**](delete-method-in-class-win32-baseservice.md)                         | Löscht einen vorhandenen Dienst.<br/>                                       |
| [**"InterrogateService"**](interrogateservice-method-in-class-win32-baseservice.md) | Fordert an, dass der Dienst seinen Status an Service Manager aktualisiert.<br/> |
| [**PauseService**](pauseservice-method-in-class-win32-baseservice.md)             | Versucht, den Dienst anzuhalten.<br/>                 |
| [**ResumeService**](resumeservice-method-in-class-win32-baseservice.md)           | Versucht, den Dienst fortzusetzen.<br/>                |
| [**Start Service**](startservice-method-in-class-win32-baseservice.md)             | Versucht, den Dienst in seinen Startzustand zu versetzen.<br/>              |
| [**Stop Service**](stopservice-method-in-class-win32-baseservice.md)               | Klassenmethode, die den Dienst in den Zustand "beendet" versetzt.<br/>         |
| [**UserControlService**](usercontrolservice-method-in-class-win32-baseservice.md) | Versucht, einen benutzerdefinierten Steuerelement Code an einen Dienst zu senden.<br/>         |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ baseservice** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept \_ Pause \_ Continue"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accept Pause")
</dt> </dl>

Der Dienst kann angehalten werden.

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept End \_ "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("der Dienst akzeptiert das Ende")
</dt> </dl>

Der Dienst kann angehalten werden.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
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

Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")
</dt> </dl>

Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.

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

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype \| Service \_ Interactive \_ Process"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("interagiert with Desktop")
</dt> </dl>

Der Dienst kann Windows auf dem Desktop erstellen oder mit ihm kommunizieren.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpdisplayname"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Anzeige Name")
</dt> </dl>

Der Anzeige Name des Dienstanbieter. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten. Bei Vergleichen von **Display Name** wird immer die Groß-/Kleinschreibung nicht beachtet.

Einschränkungen: akzeptiert denselben Wert wie die **Name** -Eigenschaft.

Beispiel: "ATDISK"

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwerrorcontrol"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Schweregrad des Start Fehlers")
</dt> </dl>

Der Schweregrad des Fehlers. Der Dienst kann nicht gestartet werden. Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt. Alle Fehler werden vom Computersystem protokolliert.

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

Das System wurde mit der zuletzt bekannten, guten Konfiguration neu gestartet.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** ("kritisch")


</dt> <dd>

Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** ("unbekannt")


</dt> <dd>

Die ausgeführte Aktion ist nicht angegeben.

</dd> </dl>

</dd> <dt>

**Exitcode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exitcode")
</dt> </dl>

Definieren von Problemen, die beim Starten oder Beenden des Dienstanbieter aufgetreten sind. Diese Eigenschaft ist auf **Fehler \_ Dienst \_ spezifischer \_ Fehler** (1066) festgelegt, wenn der Fehler für den Dienst eindeutig ist, der durch diese Klasse dargestellt wird. Informationen über den Fehler sind in der **ServiceSpecificExitCode** -Eigenschaft verfügbar. Der Dienst legt diesen Wert bei der Ausführung und erneut bei normaler Beendigung auf **keinen \_ Fehler** fest.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")
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

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Eindeutiger Bezeichner für den Dienst, der eine Angabe der verwalteten Funktionalität bereitstellt. Diese Funktionalität wird in der **Description** -Eigenschaft des Objekts ausführlicher beschrieben.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

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

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwservicespecificexitcode"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server spezifischer Exitcode")
</dt> </dl>

Dienst spezifischer Fehlercode für Fehler, die auftreten, während der Dienst gestartet oder beendet wird. Die Exitcodes werden von dem Dienst definiert, der durch diese Klasse dargestellt wird. Dieser Wert wird nur festgelegt, wenn der **exitcodeproperty** -Wert " **Error \_ Service \_ Specific \_ Error** " (1066) ist.

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")
</dt> </dl>

Der Dienst wurde für aufrufenden Prozesse bereitgestellt.

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

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")
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

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Modus")
</dt> </dl>

Der Start Modus des Windows-Basis Dienstanbieter.

Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.

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

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-baseservice.md) -Methode aufruft.

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

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpservicestartname"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")
</dt> </dl>

Der Kontoname, unter dem der Dienst ausgeführt wird. Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name \\ Benutzername" oder das UPN-Format ( Username@DomainName ) aufweisen. Der Dienst Prozess wird bei der Ausführung mithilfe einer dieser beiden Formulare protokolliert. Wenn das Konto zur integrierten Domäne gehört, ". \\ Username "kann angegeben werden. Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Bei Kernel-oder System Treibern enthält **StartName** den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden. Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde. Beispiel: "dwdom \\ Admin".

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

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist schreibgeschützt.

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

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Klassenname")
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

Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")
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

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwtagid"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag ID")
</dt> </dl>

Eindeutiger Tagwert für diesen Dienst in der Gruppe. Der Wert 0 (null) gibt an, dass dem Dienst kein Tag zugewiesen wurde. Ein-Tag kann verwendet werden, um das Service Star TUP in einer Lade Auftrags Gruppe zu sortieren, indem Sie in der Registrierung unter HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ grouporderlist einen taganordnungs Vektor angeben. Tags werden nur für die Start-und Systemstart Modi des Kernel Treibers und des Datei System-Treibers ausgewertet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ baseservice** -Klasse wird vom [**CIM- \_ Dienst**](cim-service.md)abgeleitet.

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

[**CIM- \_ Dienst**](cim-service.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

