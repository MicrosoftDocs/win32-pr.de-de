---
description: Ändert einen Win32- \_ Dienst.
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: Change-Methode der Win32_Service-Klasse (mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 321b27239114fc86861c0360d507db6c8c520a9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523923"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a>Change-Methode der Win32_Service-Klasse (mbnapi. h)

Die **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode ändert einen [**Win32- \_ Dienst**](win32-service.md).

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
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
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

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** (0)


</dt> <dd>

Der Benutzer wird nicht benachrichtigt.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)


</dt> <dd>

Normal. Der Benutzer wird benachrichtigt.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** (2)


</dt> <dd>

Das System wird mit der letzten guten Konfiguration neu gestartet.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (3)


</dt> <dd>

Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten.

</dd> </dl> </dd> <dt>

*StartMode* \[ in\]
</dt> <dd>

Der Start Modus des Windows-Basis Dienstanbieter. Weitere Informationen finden Sie im Abschnitt "Hinweise".

<dt>

Start
</dt> <dd>

Der Gerätetreiber wurde vom Betriebssystem Lader gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

System
</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

Automatisch
</dt> <dd>

Der Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.

</dd> <dt>

Manuell
</dt> <dd>

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-service.md) -Methode aufruft.

</dd> <dt>

Disabled
</dt> <dd>

Dienst, der nicht mehr gestartet werden kann.

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

**Erfolgreich**
</dt> <dd>

0

Die Anforderung wurde akzeptiert.

</dd> <dt>

**Nicht unterstützt**
</dt> <dd>

1

Die Anforderung wird nicht unterstützt.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.

</dd> <dt>

**Abhängige Dienste werden ausgeführt**
</dt> <dd>

3

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**Ungültige Dienst Kontrolle.**
</dt> <dd>

4

Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.

</dd> <dt>

**Der Dienst kann keine Steuerung akzeptieren.**
</dt> <dd>

5

Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.

</dd> <dt>

**Dienst nicht aktiv**
</dt> <dd>

6

Der Dienst wurde nicht gestartet.

</dd> <dt>

**Service Request-Timeout**
</dt> <dd>

7

Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.

</dd> <dt>

**Unbekannter Fehler.**
</dt> <dd>

8

Unbekannter Fehler beim Starten des Dienstanbieter.

</dd> <dt>

**Pfad nicht gefunden**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.

</dd> <dt>

**Dienst wird bereits ausgeführt.**
</dt> <dd>

10

Der Dienst wird schon ausgeführt.

</dd> <dt>

**Dienst Datenbank gesperrt**
</dt> <dd>

11

Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.

</dd> <dt>

**Dienst Abhängigkeit gelöscht**
</dt> <dd>

12

Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.

</dd> <dt>

**Dienst Abhängigkeitsfehler**
</dt> <dd>

13

Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.

</dd> <dt>

**Dienst deaktiviert**
</dt> <dd>

14

Der Dienst wurde vom System deaktiviert.

</dd> <dt>

**Fehler bei der Dienst Anmeldung**
</dt> <dd>

15

Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.

</dd> <dt>

**Der Dienst wurde zum Löschen markiert.**
</dt> <dd>

16

Dieser Dienst wird aus dem System entfernt.

</dd> <dt>

**Dienst ohne Thread**
</dt> <dd>

17

Der Dienst hat keinen Ausführungs Thread.

</dd> <dt>

**Status zirkuläre Abhängigkeit**
</dt> <dd>

18

Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.

</dd> <dt>

**Doppelter Name des Status**
</dt> <dd>

19

Ein Dienst wird unter dem gleichen Namen ausgeführt.

</dd> <dt>

**Ungültiger Name**
</dt> <dd>

20

Der Dienst Name enthält ungültige Zeichen.

</dd> <dt>

**Ungültiger Parameter.**
</dt> <dd>

21

An den Dienst wurden ungültige Parameter übermittelt.

</dd> <dt>

**Ungültiges Dienst Konto.**
</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.

</dd> <dt>

**Status Dienst vorhanden**
</dt> <dd>

23

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**Der Dienst wurde bereits angehalten.**
</dt> <dd>

24

Der Dienst ist im System derzeitig angehalten.

</dd> <dt>

**Andere**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn ein Computer gestartet wird, werden alle Autostart-Dienste ebenfalls gestartet. Gelegentlich kann es vorkommen, dass einer dieser Dienste nicht zusammen mit dem Computer gestartet wird. Wenn ein Dienst beim Systemstart fehlschlägt, führt der Computer auf der Grundlage des Werts des Dienst Fehler-Steuerungs Codes Aktionen aus.

die meisten Dienste werden mithilfe des normalen fehlersteuerungs Codes installiert. Einige Ausnahmen, die mit dem Fehlercode ignorieren installiert werden, umfassen Folgendes:

-   Dateireplikationsdienst
-   Smartcard
-   Sekundäre Anmeldung
-   WMI

Für die Dienste, die mit dem Fehlercode ignorieren installiert werden, erhält der Benutzer keine Benachrichtigung, dass der Dienst fehlgeschlagen ist. Wenn Sie die Benachrichtigung auf dem Bildschirm bevorzugen, dass ein Dienst nicht gestartet werden konnte, können Sie den Fehlercode mithilfe von WMI ändern. Fehler Steuerungs Codes gelten nur für den Computer Start. Es werden keine Fehlercodes verwendet, wenn Sie einen Dienst nach dem Ausführen des Computers abbrechen und neu starten.

Gelegentlich müssen Sie möglicherweise das Konto ändern, unter dem ein bestimmter Dienst ausgeführt wird. Beispielsweise können Sie einen Dienst unter einem Administrator Konto ausführen. Da dadurch ein Sicherheitsrisiko entstehen kann, können Sie den Dienst zu einem Konto mit weniger Berechtigungen wechseln. Möglicherweise verfügen Sie auch über Dienste, die unter einem Konto ausgeführt werden, das gelöscht werden soll, oder Sie möchten sicherstellen, dass bestimmte Dienste auf allen Servern unter bestimmten Konten ausgeführt werden. Sie können die **Änderungs** Methode der Win32- [**\_ Dienst**](win32-service.md) Klasse verwenden, um Dienste so zu konfigurieren, dass Sie unter einem angegebenen Benutzerkonto ausgeführt werden. Wenn Sie ein Konto auswählen, beachten Sie Folgendes:

-   Das Konto, das als Dienst Konto verwendet wird, muss über die Berechtigung verfügen, sich als Dienst anzumelden. Dieses Recht kann mithilfe von Gruppenrichtlinie erteilt werden.
-   Das Konto, das als Dienst Konto verwendet wird, sollte nicht Mitglied einer lokalen Gruppe, einer Domäne oder einer Organisations Administratoren Gruppe sein.
-   Jede Instanz eines Dienstanbieter sollte unter einem eindeutigen Benutzerkonto ausgeführt werden. Dies bietet zusätzliche Sicherheit und ermöglicht die Überwachung einzelner Dienst Instanzen.
-   Wenn der Dienst interaktiv ist, muss der Dienst unter dem Konto "LocalSystem" ausgeführt werden.

    "LocalSystem" ist erforderlich, da jeweils nur eine Fenster Station (WinSta0) sichtbar und interaktiv sein kann. Wenn ein Dienst unter einem anderen Konto als "LocalSystem" ausgeführt wird, wird er auf der Standard Station des Dienst-0x03e7 $-Fensters ausgeführt, bei dem es sich \\ um ein unsichtbares Fenster handelt. Dienste, die in dieser Fenster Station ausgeführt werden, können keine Eingabe-oder Anzeige Ausgabe empfangen.

Wenn Sie ein Konto einem Dienst zuweisen, benötigt der SCM das richtige Kennwort für dieses Konto, bevor die Zuweisung erfolgt. Wenn Sie ein falsches Kennwort angeben, lehnt der SCM das Konto ab. Wenn Sie ein Dienst Konto mit dem Konto "LocalSystem", "LocalService" oder "Network Service" konfigurieren, müssen Sie kein Konto Kennwort angeben, da diese Konten keine Kenn Wörter aufweisen.

Der SCM speichert das Konto Kennwort in der Dienst Datenbank. Nachdem das Kennwort zugewiesen wurde, stellt der SCM jedoch nicht sicher, dass das Kennwort, das in der Dienst Datenbank gespeichert ist, und das Kennwort, das dem Benutzerkonto in zugewiesen ist, weiterhin mit der Active Directory. Folglich könnte eine ähnliche Situation wie die folgende auftreten:

-   Sie konfigurieren einen Dienst, der unter einem bestimmten Benutzerkonto ausgeführt werden soll.
-   Der Dienst wird mit dem aktuellen Konto Kennwort unter diesem Konto gestartet.
-   Sie ändern das Kennwort für das Benutzerkonto.
-   Der Dienst wird weiterhin ausgeführt. Wenn der Dienst jedoch beendet wird, können Sie ihn nicht neu starten, da der SCM weiterhin das alte, ungültige Kennwort verwendet. Wenn Sie das Kennwort in Active Directory ändern, wird das in der Dienst Datenbank gespeicherte Kennwort nicht geändert.

Wenn Sie Dienste unter regulären Benutzerkonten ausführen, müssen Sie diese Dienst Kennwörter jedes Mal aktualisieren, wenn das Kennwort des Benutzerkontos geändert wird. Dies kann besonders zeitaufwändig sein, wenn Sie nicht sicher sind, welche Dienste unter diesem Konto ausgeführt werden oder welche Computer über Dienste verfügen, die unter diesem Konto ausgeführt werden. Glücklicherweise können Sie WMI verwenden, um die Dienst Konten auf allen Computern zu überprüfen und ggf. das Kennwort des Dienst Kontos zu ändern.

Der [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md) -Parameter stellt eine Gruppe von System Diensten dar, die Ausführungs Abhängigkeiten definieren. Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.

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
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



Das folgende VBScript ändert das Dienst Konto Kennwort für alle Skripts, die unter "nettsvc" ausgeführt werden


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Mbnapi. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ Dienst**](win32-service.md)
</dt> <dt>

[WMI-Tasks: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

