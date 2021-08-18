---
description: Ändert einen \_ Win32-Dienst.
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: Change-Methode der Win32_Service-Klasse (Mbnapi.h)
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
ms.openlocfilehash: ca513a31eded5202639da13b8e9f2e817c9df336b227ba93d903e44068b98898
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440190"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a>Change-Methode der Win32_Service-Klasse (Mbnapi.h)

Die **Change** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) ändert einen [**Win32-Dienst. \_**](win32-service.md)

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

Erkennungstreiber

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

*StartMode* \[ In\]
</dt> <dd>

Startmodus des Windows Basisdiensts. Weitere Informationen finden Sie im Abschnitt "Hinweise".

<dt>

Start
</dt> <dd>

Vom Betriebssystemladeprogramm gestarteter Gerätetreiber. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

System
</dt> <dd>

Der Vom Initialisierungsprozess des Betriebssystems gestartete Gerätetreiber. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

Automatisch
</dt> <dd>

Der Dienst wird während des Systemstarts automatisch vom Dienststeuerungs-Manager gestartet.

</dd> <dt>

Manuell
</dt> <dd>

Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService-Methode**](startservice-method-in-class-win32-service.md) aufruft.

</dd> <dt>

Disabled
</dt> <dd>

Dienst, der nicht mehr gestartet werden kann.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ In\]
</dt> <dd>

**True** gibt an, dass der Dienst ein Fenster auf dem Desktop erstellen oder mit diesem kommunizieren kann.

</dd> <dt>

*StartName* \[ In\]
</dt> <dd>

Kontoname, unter dem der Dienst ausgeführt wird. Je nach Diensttyp kann der Kontoname in form von DomainName \\ Username oder lauten. \\ Nutzername. Der Dienstprozess wird in einer dieser beiden Formen protokolliert, wenn er ausgeführt wird. Wenn das Konto zur integrierten Domäne gehört, . \\ Der Benutzername kann angegeben werden. Wenn **NULL** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Für Kernel- oder Treiber auf Systemebene enthält *StartName* den Namen des Treiberobjekts (d. \\ h. FileSystem \\ Rdr oder \\ Driver \\ Xns), den das E/A-System zum Laden des Gerätetreibers verwendet. Wenn **NULL** angegeben wird, wird der Treiber mit einem Standardobjektnamen ausgeführt, der vom E/A-System basierend auf dem Dienstnamen erstellt wird, z. B. "DWDOM \\ Admin".

Sie können auch das UPN-Format (User Principal Name) verwenden, um den **StartName** anzugeben, z. *Username@DomainName* B. .

</dd> <dt>

*StartPassword* \[ In\]
</dt> <dd>

Kennwort für den vom *StartName-Parameter* angegebenen Kontonamen. Geben Sie **NULL** an, wenn Sie das Kennwort nicht ändern. Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.

> [!Note]  
> Beim Ändern eines Diensts von einem lokalen System in ein Netzwerk oder von einem Netzwerk in ein lokales System muss *StartPassword* eine leere Zeichenfolge ("") und nicht **NULL** sein.

 

</dd> <dt>

*LoadOrderGroup* \[ In\]
</dt> <dd>

Gruppenname, dem er zugeordnet ist. Ladereihenfolgengruppen sind in der Systemregistrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden. Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe. Weitere Informationen finden Sie im Abschnitt "Hinweise".

Abhängigkeiten zwischen Gruppen sollten im *LoadOrderGroupDependencies-Parameter* aufgeführt werden. Dienste in der Liste der Ladereihenfolgegruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die nicht in der Liste der Lastenreihenfolgegruppen enthalten sind, gefolgt von Diensten, die keiner Gruppe angehören. Die Systemregistrierung verfügt über eine Liste der Lastreihenfolgegruppen unter:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ In\]
</dt> <dd>

Liste der Lastreihenfolgegruppen, die gestartet werden müssen, bevor dieser Dienst gestartet wird. Das Array ist doppelt **NULL**-terminiert. Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Gruppennamen muss das **Zeichen SC GROUP \_ \_ IDENTIFIER** (definiert in der Datei Winsvc.h) vorangestellt sein, um sie von Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden. Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

</dd> <dt>

*ServiceDependencies* \[ In\]
</dt> <dd>

Liste, die die Namen der Dienste enthält, die gestartet werden müssen, bevor dieser Dienst gestartet wird. Das Array ist doppelt **NULL**-terminiert. Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Die Abhängigkeit von einem Dienst gibt an, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

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

Der Benutzer hatte nicht den erforderlichen Zugriff.

</dd> <dt>

**Abhängige Dienste, die ausgeführt werden**
</dt> <dd>

3

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**Ungültige Dienststeuerung**
</dt> <dd>

4

Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.

</dd> <dt>

**Der Dienst kann die Steuerung nicht akzeptieren**
</dt> <dd>

5

Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](win32-baseservice.md)**State-Eigenschaft)** ist gleich 0, 1 oder 2.

</dd> <dt>

**Dienst nicht aktiv**
</dt> <dd>

6

Der Dienst wurde nicht gestartet.

</dd> <dt>

**Timeout für Dienstanforderungen**
</dt> <dd>

7

Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.

</dd> <dt>

**Unbekannter Fehler**
</dt> <dd>

8

Unbekannter Fehler beim Starten des Diensts.

</dd> <dt>

**Pfad nicht gefunden**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.

</dd> <dt>

**Dienst wird bereits ausgeführt**
</dt> <dd>

10

Der Dienst wird schon ausgeführt.

</dd> <dt>

**Dienstdatenbank gesperrt**
</dt> <dd>

11

Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.

</dd> <dt>

**Dienstabhängigkeit gelöscht**
</dt> <dd>

12

Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.

</dd> <dt>

**Dienstabhängigkeitsfehler**
</dt> <dd>

13

Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.

</dd> <dt>

**Dienst deaktiviert**
</dt> <dd>

14

Der Dienst wurde vom System deaktiviert.

</dd> <dt>

**Dienstanmeldung fehlgeschlagen**
</dt> <dd>

15

Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.

</dd> <dt>

**Dienst zum Löschen markiert**
</dt> <dd>

16

Dieser Dienst wird aus dem System entfernt.

</dd> <dt>

**Dienst kein Thread**
</dt> <dd>

17

Der Dienst verfügt über keinen Ausführungsthread.

</dd> <dt>

**Statuskreisabhängigkeit**
</dt> <dd>

18

Der Dienst verfügt beim Starten über zirkuläre Abhängigkeiten.

</dd> <dt>

**Doppelter Name des Status**
</dt> <dd>

19

Ein Dienst wird unter demselben Namen ausgeführt.

</dd> <dt>

**Status Ungültiger Name**
</dt> <dd>

20

Der Dienstname enthält ungültige Zeichen.

</dd> <dt>

**Status Ungültiger Parameter**
</dt> <dd>

21

Ungültige Parameter wurden an den Dienst übergeben.

</dd> <dt>

**Status Ungültiges Dienstkonto**
</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.

</dd> <dt>

**Statusdienst vorhanden**
</dt> <dd>

23

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**Dienst wurde bereits angehalten**
</dt> <dd>

24

Der Dienst ist im System derzeitig angehalten.

</dd> <dt>

**Andere**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn ein Computer gestartet wird, werden auch alle Autostartdienste gestartet. Gelegentlich kann einer dieser Dienste nicht zusammen mit dem Computer gestartet werden. Wenn ein Dienst während des Systemstarts ausfällt, führt der Computer aktionen basierend auf dem Wert des Dienstfehlersteuerungscodes aus.

Die meisten Dienste werden mit dem Code für die normale Fehlersteuerung installiert. Zu den Ausnahmen, die mit dem Fehlercode Ignorieren installiert werden, gehören:

-   Dateireplikationsdienst
-   Smartcard
-   Sekundäre Anmeldung
-   WMI

Für die Dienste, die mit dem Fehlercode Ignorieren installiert wurden, wird dem Benutzer keine Benachrichtigung angezeigt, dass der Dienst fehlgeschlagen ist. Wenn Sie die Benachrichtigung auf dem Bildschirm bevorzugen, dass ein Dienst nicht gestartet werden konnte, können Sie den Fehlersteuerungscode mithilfe von WMI ändern. Fehlersteuerungscodes gelten nur für den Computerstart. Fehlersteuerungscodes werden nicht verwendet, wenn Sie einen Dienst beenden und dann versuchen, einen Dienst neu zu starten, nachdem der Computer ausgeführt wird.

Gelegentlich müssen Sie möglicherweise das Konto ändern, unter dem ein angegebener Dienst ausgeführt wird. Beispielsweise können Sie einen Dienst unter einem Administratorkonto ausführen. Da dies zu einem Sicherheitsrisiko führen kann, können Sie den Dienst auf ein Konto mit weniger Berechtigungen umschalten. Alternativ können Dienste unter einem Konto ausgeführt werden, das gelöscht werden soll, oder Sie möchten sicherstellen, dass bestimmte Dienste auf allen Servern unter bestimmten Konten ausgeführt werden. Sie können die **Change-Methode** der [**Win32-Dienstklasse \_**](win32-service.md) verwenden, um Dienste so zu konfigurieren, dass sie unter einem angegebenen Benutzerkonto ausgeführt werden. Beachten Sie bei der Auswahl eines Kontos Folgendes:

-   Das als Dienstkonto verwendete Konto muss über das Recht verfügen, sich als Dienst anmelden zu können. Dieses Recht kann mithilfe von Gruppenrichtlinie.
-   Das konto, das als Dienstkonto verwendet wird, darf kein Mitglied einer lokalen, Domänen- oder Unternehmensadministratorgruppe sein.
-   Jede Instanz eines Diensts sollte unter einem eindeutigen Benutzerkonto ausgeführt werden. Dies bietet zusätzliche Sicherheit und ermöglicht die Überwachung einzelner Dienstinstanzen.
-   Wenn der Dienst interaktiv ist, muss der Dienst unter dem LocalSystem-Konto ausgeführt werden.

    LocalSystem ist erforderlich, da jeweils nur eine Fensterstation (WinSta0) sichtbar und interaktiv sein kann. Wenn ein Dienst unter einem anderen Konto als LocalSystem ausgeführt wird, wird er in der Standardfensterstation Service-0x03e7$ ausgeführt. Dies \\ ist ein unsichtbares Fenster. Dienste, die in dieser Fensterstation ausgeführt werden, können keine Eingabe- oder Anzeigeausgabe empfangen.

Wenn Sie einem Dienst ein Konto zuweisen, benötigt der SCM das richtige Kennwort für dieses Konto, bevor er die Zuweisung vornimmt. Wenn Sie ein falsches Kennwort eingeben, lehnt der SCM das Konto ab. Wenn Sie ein Dienstkonto mit dem Konto LocalSystem, LocalService oder NetworkService konfigurieren, müssen Sie kein Kontokennwort angeben, da diese Konten keine Kennwörter besitzen.

Der SCM speichert das Kontokennwort in der Dienstdatenbank. Nachdem das Kennwort zugewiesen wurde, stellt der SCM jedoch nicht sicher, dass das in der Dienstdatenbank gespeicherte Kennwort und das dem Benutzerkonto in Active Directory zugewiesene Kennwort weiterhin übereinstimmen. Folglich kann eine Situation ähnlich der folgenden auftreten:

-   Sie konfigurieren einen Dienst für die Ausführung unter einem bestimmten Benutzerkonto.
-   Der Dienst wird unter diesem Konto mithilfe des aktuellen Kontokennworts gestartet.
-   Sie ändern das Kennwort für das Benutzerkonto.
-   Der Dienst wird weiterhin ausgeführt. Wenn der Dienst jedoch beendet wird, können Sie ihn nicht neu starten, da der SCM weiterhin das alte, ungültige Kennwort verwendet. Durch das Ändern des Kennworts in Active Directory wird das in der Dienstdatenbank gespeicherte Kennwort nicht geändert.

Wenn Sie Dienste unter regulären Benutzerkonten ausführen, müssen Sie diese Dienstkennwörter bei jeder Änderung des Benutzerkontokennworts aktualisieren. Dies kann besonders zeitaufwändig sein, wenn Sie nicht sicher sind, welche Dienste unter diesem Konto ausgeführt werden oder auf welchen Computern Dienste unter diesem Konto ausgeführt werden. Glücklicherweise können Sie WMI verwenden, um die Dienstkonten auf allen Ihren Computern zu überprüfen und ggf. das Kennwort für das Dienstkonto zu ändern.

Der [**Win32 \_ LoadOrderGroup-Parameter**](win32-loadordergroup.md) stellt eine Gruppe von Systemdiensten dar, die Ausführungsabhängigkeiten definieren. Die Dienste müssen in der von der Load Order Group angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern, dass die Vorgängerdienste vorhanden sind, damit sie ordnungsgemäß funktionieren.

Um einen Dienst von einem Netzwerkdienst in ein lokales System zu ändern, sollten die Parameter *StartName* und *StartPassword* die folgenden Werte aufweisen:


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Um einen Dienst von einem lokalen Systemdienst in ein Netzwerk zu ändern, müssen die Parameter *StartName* und *StartPassword* die folgenden Werte aufweisen:


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a>Beispiele

Mit dem folgenden VBScript-Code wird das Dienstkonto für Dienste von unter einem angegebenen Benutzerkonto in LocalSystem geändert.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



Der folgende VBScript-Code ändert das Dienstkontokennwort für alle Skripts, die unter Netsvc ausgeführt werden.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Mbnapi.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Win32-Dienst**](win32-service.md)
</dt> <dt>

[WMI-Aufgaben: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

