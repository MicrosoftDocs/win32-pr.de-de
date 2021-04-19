---
title: Change-Methode der Win32_Service-Klasse (mbnapi. h) (Terminalservice)
description: Ändert einen Win32 \_ Terminalservice.
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- Änderungs Methode Remotedesktopdienste
- Change-Methode Remotedesktopdienste, Win32_Service-Klasse
- Win32_Service-Klasse Remotedesktopdienste, Methode ändern
topic_type:
- apiref
api_name:
- Win32_Service.Change
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa34ea0c9c38cd0b11f97a0bbf651f1aebf37a46
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389204"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a>Change-Methode der Win32_Service-Klasse (mbnapi. h)-Terminalservice

Die **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode ändert einen [**Win32 \_ Terminalservice**](win32-terminalservice.md).

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies,
  [in] string  ServiceDependencies
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Display Name* \[ in\]
</dt> <dd>

Der Anzeigename des Diensts Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten. Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet.

Einschränkungen: akzeptiert denselben Wert wie die **Name** -Eigenschaft.

Beispiel: "ATDISK".

</dd> <dt>

*Pfadname* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad zur ausführbaren Datei, die den Dienst implementiert, z. b \\ . "SystemRoot \\ system32 \\ Drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ in\]
</dt> <dd>

Der Typ der Dienste, die für Prozesse bereitgestellt werden, die Sie anrufen.

<dt>

1 (0x1)
</dt> <dd>

Kernel Treiber

</dd> <dt>

2 (0x2)
</dt> <dd>

Datei System Treiber

</dd> <dt>

4 (0x4)
</dt> <dd>

Adapter

</dd> <dt>

8 (0x8)
</dt> <dd>

Erkennungs Treiber

</dd> <dt>

16 (0x10)
</dt> <dd>

Eigener Prozess

</dd> <dt>

32 (0x20)
</dt> <dd>

Freigabeprozess

</dd> <dt>

256 (0x100)
</dt> <dd>

Interaktiver Prozess

</dd> </dl> </dd> <dt>

*ErrorControl* \[ in\]
</dt> <dd>

Der Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann. Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt. Alle Fehler werden vom System protokolliert.

<dt>

0
</dt> <dd>

**Ignore** (Ignorieren): Der Startvorgang fortgesetzt Der Benutzer erhält keine Benachrichtigung, dass der Dienst fehlgeschlagen ist.

</dd> <dt>

1
</dt> <dd>

**Normaler.** Der Startvorgang fortgesetzt Bevor der Benutzer sich anmeldet, erhält der Benutzer die Benachrichtigung, dass mindestens ein Dienst oder ein Gerät während des Starts fehlgeschlagen ist.

</dd> <dt>

2
</dt> <dd>

**Starkem.** Der Computer versucht, mit der zuletzt bekannten guten Konfiguration neu zu starten. Wenn der Dienst erneut ausfällt, wird der Startvorgang fortgesetzt, und der Benutzer erhält eine Benachrichtigung.

</dd> <dt>

3
</dt> <dd>

**Kritisch.** Der Computer versucht, mit der zuletzt bekannten guten Konfiguration neu zu starten. Wenn der Dienst erneut ausfällt, wird der Startvorgang beendet.

</dd> </dl> </dd> <dt>

*StartMode* \[ in\]
</dt> <dd>

Der Start Modus des Windows-Basis Dienstanbieter. Weitere Informationen finden Sie im Abschnitt "Hinweise".

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Starten**


</dt> <dd>

Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Anlage**


</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch**


</dt> <dd>

Der Dienst wird vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet. Autostart-Dienste werden gestartet, bevor sich ein Benutzer am Computer anmeldet und ausgeführt wird, selbst wenn sich kein Benutzer am Computer anmeldet.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell**


</dt> <dd>

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](win32-terminalservice-startservice.md) -Methode aufruft. Obwohl manuelle Dienste speziell von einem Benutzer (oder einem Skript) gestartet werden müssen, werden Sie weiterhin ausgeführt, selbst wenn sich der Benutzer abmeldet. Manuelle Dienste werden häufig als Bedarfs gesteuerte Dienste bezeichnet.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**


</dt> <dd>

Dienst, der nicht mehr gestartet werden kann. Um einen deaktivierten Dienst zu starten, müssen Sie zuerst die Startoption entweder in Auto oder manuell ändern.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ in\]
</dt> <dd>

**True** gibt an, dass der Dienst ein Fenster auf dem Desktop erstellen oder mit diesem kommunizieren kann.

</dd> <dt>

*StartName* \[ in\]
</dt> <dd>

Der Kontoname, unter dem der Dienst ausgeführt wird. Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name Benutzername" oder "" aufweisen \\ . \\ User. Der Dienst Prozess wird bei der Ausführung mithilfe einer dieser beiden Formulare protokolliert. , Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden. Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Bei Kernel-oder System Treibern enthält *StartName* den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden. Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System auf Basis des Dienst namens erstellt wird, z. b. "dwdom \\ Admin".

Sie können auch das UPN-Format (User Principal Name, Benutzer Prinzipal Name) verwenden, um den **StartName** anzugeben, z *Username@DomainName* . b..

</dd> <dt>

*Startpassword* \[ in\]
</dt> <dd>

Das Kennwort für den Kontonamen, der durch den *StartName* -Parameter angegeben wird. Geben Sie **null** an, wenn Sie das Kennwort nicht ändern. Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.

> [!Note]  
> Wenn ein Dienst von einem lokalen System in ein Netzwerk oder von einem Netzwerk auf ein lokales System geändert wird, muss *startpassword* eine leere Zeichenfolge ("") und nicht **null** sein.

 

</dd> <dt>

*LoadOrderGroup* \[ in\]
</dt> <dd>

Der Gruppenname, dem er zugeordnet ist. Lade Auftrags Gruppen sind in der Systemregistrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden. Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe. Weitere Informationen finden Sie im Abschnitt "Hinweise".

Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden. Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören. Die Systemregistrierung enthält eine Liste der Lade Auftrags Gruppen unter:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder**

</dd> <dt>

*Loadordergroupabhängigkeiten* \[ in\]
</dt> <dd>

Liste der Lade Gruppen, die vor dem Start dieses Dienstanbieter gestartet werden müssen. Das Array ist doppelt **null**-terminiert. Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten. Gruppennamen müssen dem **SC- \_ Gruppen \_ Bezeichner** (definiert in der Datei "winsvc. h") vorangestellt werden, damit Sie von Dienstnamen unterschieden werden, weil Dienste und Dienstgruppen denselben Namespace verwenden. Die Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

</dd> <dt>

*Service Abhängigkeiten* \[ in\]
</dt> <dd>

Liste mit den Namen der Dienste, die vor dem Start dieses Diensts gestartet werden müssen. Das Array ist doppelt **null**-terminiert. Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten. Die Abhängigkeit von einem Dienst gibt an, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Die Anforderung wurde akzeptiert.

</dd> <dt>

**1**
</dt> <dd>

Die Anforderung wird nicht unterstützt.

</dd> <dt>

**2**
</dt> <dd>

Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.

</dd> <dt>

**3**
</dt> <dd>

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**4**
</dt> <dd>

Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.

</dd> <dt>

**5**
</dt> <dd>

Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** -Eigenschaft) ist gleich 0, 1 oder 2.

</dd> <dt>

**6**
</dt> <dd>

Der Dienst wurde nicht gestartet.

</dd> <dt>

**7**
</dt> <dd>

Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.

</dd> <dt>

**8**
</dt> <dd>

Unbekannter Fehler beim Starten des Dienstanbieter.

</dd> <dt>

**9**
</dt> <dd>

Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.

</dd> <dt>

**10**
</dt> <dd>

Der Dienst wird schon ausgeführt.

</dd> <dt>

**11**
</dt> <dd>

Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.

</dd> <dt>

**12**
</dt> <dd>

Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.

</dd> <dt>

**13**
</dt> <dd>

Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.

</dd> <dt>

**14**
</dt> <dd>

Der Dienst wurde vom System deaktiviert.

</dd> <dt>

**15**
</dt> <dd>

Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.

</dd> <dt>

**16**
</dt> <dd>

Dieser Dienst wird aus dem System entfernt.

</dd> <dt>

**17**
</dt> <dd>

Der Dienst hat keinen Ausführungs Thread.

</dd> <dt>

**Jahren**
</dt> <dd>

Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.

</dd> <dt>

**19**
</dt> <dd>

Ein Dienst wird unter dem gleichen Namen ausgeführt.

</dd> <dt>

**20**
</dt> <dd>

Der Dienst Name enthält ungültige Zeichen.

</dd> <dt>

**21**
</dt> <dd>

An den Dienst wurden ungültige Parameter übermittelt.

</dd> <dt>

**22**
</dt> <dd>

Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.

</dd> <dt>

**23**
</dt> <dd>

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**24**
</dt> <dd>

Der Dienst ist im System derzeitig angehalten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn ein Computer gestartet wird, werden alle Autostart-Dienste ebenfalls gestartet. Gelegentlich kann es vorkommen, dass einer dieser Dienste nicht zusammen mit dem Computer gestartet wird. Wenn ein Dienst beim Systemstart fehlschlägt, führt der Computer auf der Grundlage des Werts des Dienst Fehler-Steuerungs Codes Aktionen aus.

die meisten Dienste werden mithilfe des normalen fehlersteuerungs Codes installiert. Einige Ausnahmen, die mit dem Fehlercode ignorieren installiert werden, umfassen Folgendes:

-   Dateireplikationsdienst
-   Smartcard
-   Sekundäre Anmeldung
-   WMI

Für die Dienste, die mit dem Fehlercode ignorieren installiert werden, erhält der Benutzer keine Benachrichtigung, dass der Dienst fehlgeschlagen ist. Wenn Sie die Benachrichtigung auf dem Bildschirm bevorzugen, dass ein Dienst nicht gestartet werden konnte, können Sie den Fehlercode mithilfe von WMI ändern. Fehler Steuerungs Codes gelten nur für den Computer Start. Es werden keine Fehlercodes verwendet, wenn Sie einen Dienst nach dem Ausführen des Computers abbrechen und neu starten.

Gelegentlich müssen Sie möglicherweise das Konto ändern, unter dem ein bestimmter Dienst ausgeführt wird. Beispielsweise können Sie einen Dienst unter einem Administrator Konto ausführen. Da dadurch ein Sicherheitsrisiko entstehen kann, können Sie den Dienst zu einem Konto mit weniger Berechtigungen wechseln. Möglicherweise verfügen Sie auch über Dienste, die unter einem Konto ausgeführt werden, das gelöscht werden soll, oder Sie möchten sicherstellen, dass bestimmte Dienste auf allen Servern unter bestimmten Konten ausgeführt werden. Sie können die **Change** -Methode der [**Win32 \_ Terminalservice**](win32-terminalservice.md) -Klasse verwenden, um Dienste so zu konfigurieren, dass Sie unter einem angegebenen Benutzerkonto ausgeführt werden. Wenn Sie ein Konto auswählen, beachten Sie Folgendes:

-   Das Konto, das als Dienst Konto verwendet wird, muss über die Berechtigung verfügen, sich als Dienst anzumelden. Dieses Recht kann mithilfe von Gruppenrichtlinie erteilt werden.
-   Das Konto, das als Dienst Konto verwendet wird, sollte nicht Mitglied einer lokalen Gruppe, einer Domäne oder einer Organisations Administratoren Gruppe sein.
-   Jede Instanz eines Dienstanbieter sollte unter einem eindeutigen Benutzerkonto ausgeführt werden. Dies bietet zusätzliche Sicherheit und ermöglicht die Überwachung einzelner Dienst Instanzen.
-   Wenn der Dienst interaktiv ist, muss der Dienst unter dem Konto "LocalSystem" ausgeführt werden.

    "LocalSystem" ist erforderlich, da jeweils nur eine Fenster Station (WinSta0) sichtbar und interaktiv sein kann. Wenn ein Dienst unter einem anderen Konto als "LocalSystem" ausgeführt wird, wird er auf der Standard Station des Dienst-0x03e7 $-Fensters ausgeführt, bei dem es sich \\ um ein unsichtbares Fenster handelt. Dienste, die in dieser Fenster Station ausgeführt werden, können keine Eingabe-oder Anzeige Ausgabe empfangen.

Wenn Sie ein Konto einem Dienst zuweisen, benötigt der SCM das richtige Kennwort für dieses Konto, bevor die Zuweisung erfolgt. Wenn Sie ein falsches Kennwort angeben, lehnt der SCM das Konto ab. Wenn Sie ein Dienst Konto mit dem Konto "LocalSystem", "LocalService" oder "Network Service" konfigurieren, müssen Sie kein Konto Kennwort angeben, da diese Konten keine Kenn Wörter aufweisen.

Der SCM speichert das Konto Kennwort in der Dienst Datenbank. Nachdem das Kennwort zugewiesen wurde, stellt der SCM jedoch nicht sicher, dass das Kennwort, das in der Dienst Datenbank gespeichert ist, und das Kennwort, das dem Benutzerkonto in zugewiesen ist, weiterhin mit der Active Directory. Folglich könnte eine ähnliche Situation wie die folgende auftreten:

-   . Sie konfigurieren einen Dienst, der unter einem bestimmten Benutzerkonto ausgeführt werden soll.
-   Der Dienst wird mit dem aktuellen Konto Kennwort unter diesem Konto gestartet.
-   Sie ändern das Kennwort für das Benutzerkonto.
-   Der Dienst wird weiterhin ausgeführt. Wenn der Dienst jedoch beendet wird, können Sie ihn nicht neu starten, da der SCM weiterhin das alte, ungültige Kennwort verwendet. Wenn Sie das Kennwort in Active Directory ändern, wird das in der Dienst Datenbank gespeicherte Kennwort nicht geändert.

Wenn Sie Dienste unter regulären Benutzerkonten ausführen, müssen Sie diese Dienst Kennwörter jedes Mal aktualisieren, wenn das Kennwort des Benutzerkontos geändert wird. Dies kann besonders zeitaufwändig sein, wenn Sie nicht sicher sind, welche Dienste unter diesem Konto ausgeführt werden oder welche Computer über Dienste verfügen, die unter diesem Konto ausgeführt werden. Glücklicherweise können Sie WMI verwenden, um die Dienst Konten auf allen Computern zu überprüfen und ggf. das Kennwort des Dienst Kontos zu ändern.

Der [**Win32 \_ LoadOrderGroup**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) -Parameter stellt eine Gruppe von System Diensten dar, die Ausführungs Abhängigkeiten definieren. Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.

Um einen Dienst von einem Netzwerkdienst in ein lokales System zu ändern, müssen die Parameter " *StartName* " und " *startpassword* " die folgenden Werte aufweisen:


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Um einen Dienst von einem lokalen Systemdienst in ein Netzwerk zu ändern, müssen die Parameter " *StartName* " und " *startpassword* " die folgenden Werte aufweisen:


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a>Beispiele

Das folgende VBScript ändert das Dienst Konto für Dienste von der Ausführung unter einem angegebenen Benutzerkonto in "LocalSystem".


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change _
 ( , , , , , , ".\LocalSystem" , "")
Next
```



Das folgende VBScript ändert das Dienst Konto Kennwort für alle Skripts, die unter "nettsvc" ausgeführt werden


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| Header<br/>                   | <dl> <dt>Mbnapi. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Betriebssystemklassen](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**Win32 \_ Terminalservice**](win32-terminalservice.md)
</dt> <dt>

[WMI-Tasks: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

