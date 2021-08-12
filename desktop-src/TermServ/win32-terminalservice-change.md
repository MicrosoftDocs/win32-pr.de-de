---
title: Change-Methode der Win32_Service -Klasse (Mbnapi.h) (TerminalService)
description: Ändert einen \_ Win32-Terminaldienst.
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- Ändern der Remotedesktopdienste
- Change method Remotedesktopdienste , Win32_Service class
- Win32_Service klasse Remotedesktopdienste , Change-Methode
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
ms.openlocfilehash: c10e8c7b0a26ce2ca1e602478a64a888a1ad6b299f8ab7965303832bba7a3fc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604432"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a>Change-Methode der Win32_Service -Klasse (Mbnapi.h) – TerminalService

Die **Change** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) ändert einen [**Win32 \_ TerminalService.**](win32-terminalservice.md)

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

*DisplayName* \[ In\]
</dt> <dd>

Der Anzeigename des Diensts Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager beibehalten. *Bei DisplayName-Vergleichen* wird die Groß-/Kleinschreibung immer nicht beachtet.

Einschränkungen: Akzeptiert den gleichen Wert wie die **Name-Eigenschaft.**

Beispiel: "Atdisk".

</dd> <dt>

*PathName* \[ In\]
</dt> <dd>

Der vollqualifizierte Pfad zur ausführbaren Datei, die den Dienst implementiert, z. B. \\ "SystemRoot \\ System32-Treiber \\ \\afd.sys".

</dd> <dt>

*ServiceType* \[ In\]
</dt> <dd>

Der Typ der Dienste, die für Prozesse bereitgestellt werden, die sie aufrufen.

<dt>

1 (0x1)
</dt> <dd>

Kerneltreiber

</dd> <dt>

2 (0x2)
</dt> <dd>

Dateisystemtreiber

</dd> <dt>

4 (0x4)
</dt> <dd>

Adapter

</dd> <dt>

8 (0x8)
</dt> <dd>

Recognizer Driver

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

*ErrorControl* \[ In\]
</dt> <dd>

Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann. Der Wert gibt die Aktion an, die vom Startprogramm ausgeführt wird, wenn ein Fehler auftritt. Alle Fehler werden vom System protokolliert.

<dt>

0
</dt> <dd>

**Ignore** (Ignorieren): Der Startvorgang wird fortgesetzt. Der Benutzer erhält keine Benachrichtigung, dass der Dienst fehlgeschlagen ist.

</dd> <dt>

1
</dt> <dd>

**Normalen.** Der Startvorgang wird fortgesetzt. Bevor sich der Benutzer anmeldet, erhält der Benutzer die Benachrichtigung "Mindestens ein Dienst oder Gerät ist beim Start fehlgeschlagen".

</dd> <dt>

2
</dt> <dd>

**Schwere.** Der Computer versucht, mit der letzten als gut bekannten Konfiguration neu zu starten. Wenn der Dienst erneut fehlschlägt, wird der Start fortgesetzt, und der Benutzer erhält eine Benachrichtigung.

</dd> <dt>

3
</dt> <dd>

**Kritisch.** Der Computer versucht, mit der letzten als gut bekannten Konfiguration neu zu starten. Wenn der Dienst erneut ausfällt, wird der Start beendet.

</dd> </dl> </dd> <dt>

*StartMode* \[ In\]
</dt> <dd>

Startmodus des Windows Basisdiensts. Weitere Informationen finden Sie im Abschnitt "Hinweise".

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Booten**


</dt> <dd>

Vom Betriebssystemlader gestarteter Gerätetreiber.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**


</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungsprozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch**


</dt> <dd>

Der Dienst wird automatisch vom Dienststeuerungs-Manager während des Systemstarts gestartet. Autostartdienste werden gestartet, bevor sich ein Benutzer am Computer anmeldet, und werden auch dann ausgeführt, wenn sich kein Benutzer am Computer anmeldet.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell**


</dt> <dd>

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService-Methode**](win32-terminalservice-startservice.md) aufruft. Obwohl manuelle Dienste speziell von einem Benutzer (oder einem Skript) gestartet werden müssen, werden sie auch dann weiterhin ausgeführt, wenn sich der Benutzer abmeldet. Manuelle Dienste werden häufig als bedarfsbasierte Dienste bezeichnet.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**


</dt> <dd>

Dienst, der nicht mehr gestartet werden kann. Um einen deaktivierten Dienst zu starten, müssen Sie zuerst die Startoption in Auto oder Manuell ändern.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ In\]
</dt> <dd>

True **gibt an,** dass der Dienst ein Fenster auf dem Desktop erstellen oder mit diesem kommunizieren kann.

</dd> <dt>

*StartName* \[ In\]
</dt> <dd>

Kontoname, unter dem der Dienst ausgeführt wird. Je nach Diensttyp kann der Kontoname in Form von DomainName Username oder \\ sein. \\ Nutzername. Der Dienstprozess wird mit einer dieser beiden Formen protokolliert, wenn er ausgeführt wird. Wenn das Konto zur integrierten Domäne gehört, . \\ Der Benutzername kann angegeben werden. Wenn **NULL** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Für Treiber auf Kernel- oder Systemebene enthält *StartName* den Treiberobjektnamen (d. h. FileSystem Rdr oder Driver Xns), den das Eingabe- und Ausgabesystem \\ \\ \\ (E/A) zum Laden des \\ Gerätetreibers verwendet. Wenn **NULL** angegeben ist, wird der Treiber mit einem Standardobjektnamen ausgeführt, der vom E/A-System basierend auf dem Dienstnamen erstellt wird, z. B. "DWDOM \\ Admin".

Sie können auch das UPN-Format (User Principal Name) verwenden, um **den StartName** anzugeben, z. *Username@DomainName* B. .

</dd> <dt>

*StartPassword* \[ In\]
</dt> <dd>

Kennwort für den Kontonamen, der durch den *StartName-Parameter angegeben* wird. Geben **Sie NULL** an, wenn Sie das Kennwort nicht ändern. Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.

> [!Note]  
> Beim Ändern eines Diensts von einem lokalen System in ein Netzwerk oder von einem Netzwerk in ein lokales System muss *StartPassword* eine leere Zeichenfolge ("") und nicht **NULL sein.**

 

</dd> <dt>

*LoadOrderGroup* \[ In\]
</dt> <dd>

Gruppenname, dem er zugeordnet ist. Lastreihenfolgegruppen sind in der Systemregistrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden. Wenn der Zeiger NULL **ist** oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe. Weitere Informationen finden Sie im Abschnitt "Hinweise".

Abhängigkeiten zwischen Gruppen sollten im *LoadOrderGroupDependencies-Parameter aufgeführt* werden. Dienste in der Liste der Last reihenfolgengruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die nicht in der Liste der Last reihenfolgengruppen enthalten sind, gefolgt von Diensten, die nicht zu einer Gruppe gehören. Die Systemregistrierung verfügt über eine Liste der Lade reihenfolgengruppen unter:

**HKEY \_ LOCAL \_ MACHINE-System** \\  \\ **CurrentControlSet-Steuerelement** \\  \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ In\]
</dt> <dd>

Liste der Last reihenfolgengruppen, die gestartet werden müssen, bevor dieser Dienst gestartet wird. Das Array ist doppelt NULL-terminiert. Wenn der Zeiger NULL **ist** oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Gruppennamen muss das SC **\_ GROUP \_ IDENTIFIER-Zeichen** (definiert in der Datei Winsvc.h) vorangestellt werden, um sie von Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden. Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

</dd> <dt>

*ServiceDependencies* \[ In\]
</dt> <dd>

Liste, die die Namen der Dienste enthält, die gestartet werden müssen, bevor dieser Dienst gestartet wird. Das Array ist doppelt NULL-terminiert. Wenn der Zeiger NULL **ist** oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Abhängigkeit von einem Dienst gibt an, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst ausgeführt wird, von dem er abhängig ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

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

Der Benutzer hatte nicht den erforderlichen Zugriff.

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

Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](/windows/desktop/CIMWin32Prov/win32-baseservice)**State-Eigenschaft)** ist gleich 0, 1 oder 2.

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

Unbekannter Fehler beim Starten des Diensts.

</dd> <dt>

**9**
</dt> <dd>

Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.

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

Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.

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

Der Dienst verfügt über keinen Ausführungsthread.

</dd> <dt>

**18**
</dt> <dd>

Der Dienst verfügt beim Starten über zirkuläre Abhängigkeiten.

</dd> <dt>

**19**
</dt> <dd>

Ein Dienst wird unter demselben Namen ausgeführt.

</dd> <dt>

**20**
</dt> <dd>

Der Dienstname enthält ungültige Zeichen.

</dd> <dt>

**21**
</dt> <dd>

Ungültige Parameter wurden an den Dienst übergeben.

</dd> <dt>

**22**
</dt> <dd>

Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.

</dd> <dt>

**23**
</dt> <dd>

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**24**
</dt> <dd>

Der Dienst ist im System derzeitig angehalten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn ein Computer gestartet wird, werden auch alle Autostartdienste gestartet. Gelegentlich kann einer dieser Dienste nicht zusammen mit dem Computer gestartet werden. Wenn ein Dienst während des Systemstarts ausfällt, führt der Computer aktionen basierend auf dem Wert des Dienstfehlersteuerungscodes aus.

Die meisten Dienste werden mit dem Code für die normale Fehlersteuerung installiert. Zu den Ausnahmen, die mit dem Fehlercode Ignorieren installiert werden, gehören:

-   Dateireplikationsdienst
-   Smartcard
-   Sekundäre Anmeldung
-   WMI

Für die Dienste, die mit dem Fehlercode Ignorieren installiert wurden, wird dem Benutzer keine Benachrichtigung angezeigt, dass der Dienst fehlgeschlagen ist. Wenn Sie die Benachrichtigung auf dem Bildschirm bevorzugen, dass ein Dienst nicht gestartet werden konnte, können Sie den Fehlersteuerungscode mithilfe von WMI ändern. Fehlersteuerungscodes gelten nur für den Computerstart. Fehlersteuerungscodes werden nicht verwendet, wenn Sie einen Dienst beenden und dann versuchen, einen Dienst neu zu starten, nachdem der Computer ausgeführt wird.

Gelegentlich müssen Sie möglicherweise das Konto ändern, unter dem ein angegebener Dienst ausgeführt wird. Beispielsweise können Sie einen Dienst unter einem Administratorkonto ausführen. Da dies zu einem Sicherheitsrisiko führen kann, können Sie den Dienst auf ein Konto mit weniger Berechtigungen umschalten. Alternativ können Dienste unter einem Konto ausgeführt werden, das gelöscht werden soll, oder Sie möchten sicherstellen, dass bestimmte Dienste auf allen Servern unter bestimmten Konten ausgeführt werden. Sie können die **Change-Methode** der [**Win32 \_ TerminalService-Klasse**](win32-terminalservice.md) verwenden, um Dienste so zu konfigurieren, dass sie unter einem angegebenen Benutzerkonto ausgeführt werden. Beachten Sie bei der Auswahl eines Kontos Folgendes:

-   Das als Dienstkonto verwendete Konto muss über das Recht verfügen, sich als Dienst anmelden zu können. Dieses Recht kann mithilfe von Gruppenrichtlinie.
-   Das konto, das als Dienstkonto verwendet wird, darf kein Mitglied einer lokalen, Domänen- oder Unternehmensadministratorgruppe sein.
-   Jede Instanz eines Diensts sollte unter einem eindeutigen Benutzerkonto ausgeführt werden. Dies bietet zusätzliche Sicherheit und ermöglicht die Überwachung einzelner Dienstinstanzen.
-   Wenn der Dienst interaktiv ist, muss der Dienst unter dem Konto LocalSystem ausgeführt werden.

    LocalSystem ist erforderlich, da nur eine Fensterstation (WinSta0) gleichzeitig sichtbar und interaktiv sein kann. Wenn ein Dienst unter einem anderen Konto als LocalSystem ausgeführt wird, wird er in der Service-0x03e7$-Standardfensterstation ausgeführt, bei der es sich um ein \\ unsichtbares Fenster handelt. Dienste, die in dieser Fensterstation ausgeführt werden, können keine Eingabe- oder Anzeigeausgabe empfangen.

Wenn Sie einem Dienst ein Konto zuweisen, benötigt der SCM das richtige Kennwort für dieses Konto, bevor er die Zuweisung vor der Zuweisung vorsingt. Wenn Sie ein falsches Kennwort angeben, lehnt der SCM das Konto ab. Wenn Sie ein Dienstkonto mit dem Konto LocalSystem, LocalService oder NetworkService konfigurieren, müssen Sie kein Kontokennwort angeben, da diese Konten keine Kennwörter haben.

Der SCM speichert das Kontokennwort in der Dienstdatenbank. Nachdem das Kennwort zugewiesen wurde, stellt der SCM jedoch nicht sicher, dass das in der Dienstdatenbank gespeicherte Kennwort und das Kennwort, das dem Benutzerkonto in Active Directory zugewiesen ist, weiterhin übereinstimmen. Folglich kann eine Situation ähnlich der folgenden auftreten:

-   . Sie konfigurieren einen Dienst so, dass er unter einem bestimmten Benutzerkonto ausgeführt wird.
-   Der Dienst wird unter diesem Konto mithilfe des aktuellen Kontokennworts gestartet.
-   Sie ändern das Kennwort für das Benutzerkonto.
-   Der Dienst wird weiterhin ausgeführt. Wenn der Dienst jedoch beendet wird, können Sie ihn nicht neu starten, da der SCM weiterhin das alte, ungültige Kennwort verwendet. Durch das Ändern des Kennworts in Active Directory wird das in der Dienstdatenbank gespeicherte Kennwort nicht geändert.

Wenn Sie Dienste unter regulären Benutzerkonten ausführen, müssen Sie diese Dienstkennwörter jedes Mal aktualisieren, wenn sich das Kennwort des Benutzerkontos ändert. Dies kann besonders zeitaufwändig sein, wenn Sie nicht sicher sind, welche Dienste unter diesem Konto ausgeführt werden oder auf welchen Computern Dienste unter diesem Konto ausgeführt werden. Glücklicherweise können Sie WMI verwenden, um die Dienstkonten auf allen Ihren Computern zu überprüfen und bei Bedarf das Kennwort des Dienstkontos zu ändern.

Der [**Win32 \_ LoadOrderGroup-Parameter**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) stellt eine Gruppe von Systemdiensten dar, die Ausführungsabhängigkeiten definieren. Die Dienste müssen in der von der Load Order Group angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern das Vorhandensein der voraussenten Dienste, damit sie ordnungsgemäß funktionieren.

Um einen Dienst von einem Netzwerkdienst in ein lokales System zu ändern, sollten die *Parameter StartName* und *StartPassword* die folgenden Werte haben:


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Um einen Dienst von einem lokalen Systemdienst in ein Netzwerk zu ändern, müssen die *Parameter StartName* und *StartPassword* die folgenden Werte haben:


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a>Beispiele

Das folgende VBScript ändert das Dienstkonto für Dienste von der Ausführung unter einem angegebenen Benutzerkonto in LocalSystem.


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



Das folgende VBScript ändert das Dienstkontokennwort für alle Skripts, die unter Netsvc ausgeführt werden.


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
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| Header<br/>                   | <dl> <dt>Mbnapi.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32-Dienst \_**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Betriebssystemklassen](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[WMI-Aufgaben: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

