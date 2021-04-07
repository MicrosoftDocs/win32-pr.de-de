---
description: Erstellt einen neuen-Systemdienst.
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: Create-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f23bc2a5c49a85a20765172d4c5d361a8d18316
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749040"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Create-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)

Die **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode erstellt einen neuen-Systemdienst.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Create(
  [in] string  Name,
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
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

*Name* \[ in\]
</dt> <dd>

Name des Dienstanbieter, der in der **Create** -Methode installiert werden soll. Die maximale Zeichen folgen Länge beträgt 256 Zeichen. Die Dienst Steuerungs Verwaltung behält die Groß-/Kleinschreibung der Zeichen bei. bei Dienstnamen vergleichen wird jedoch immer die Groß-/Kleinschreibung beachtet. Vorwärts Schrägstriche (/) und doppelte umgekehrte Schrägstriche ( \\ ) sind ungültige Dienstnamen Zeichen.

</dd> <dt>

*Display Name* \[ in\]
</dt> <dd>

Der Anzeige Name des Dienstanbieter. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten. Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet.

Einschränkungen: akzeptiert denselben Wert wie der *Name* -Parameter.

Beispiel: "ATDISK".

</dd> <dt>

*Pfadname* \[ in\]
</dt> <dd>

Voll qualifizierter Pfad zur ausführbaren Datei, die den Dienst implementiert.

Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ in\]
</dt> <dd>

Typ der Dienste, die für Prozesse bereitgestellt werden, die Sie anrufen.

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

Der Schweregrad des Fehlers, wenn die **Create** -Methode nicht gestartet werden kann. Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt. Alle Fehler werden vom System protokolliert.

<dt>

0
</dt> <dd>

Der Benutzer wird nicht benachrichtigt.

</dd> <dt>

1
</dt> <dd>

Der Benutzer wird benachrichtigt.

</dd> <dt>

2
</dt> <dd>

Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.

</dd> <dt>

3
</dt> <dd>

Das System versucht, mit einer guten Konfiguration zu beginnen.

</dd> </dl> </dd> <dt>

*StartMode* \[ in\]
</dt> <dd>

Der Start Modus des Windows-Basis Dienstanbieter.

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

**True** gibt an, dass der Dienst Windows auf dem Desktop erstellen oder mit ihm kommunizieren kann.

</dd> <dt>

*StartName* \[ in\]
</dt> <dd>

Der Kontoname, unter dem der Dienst ausgeführt wird. Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name \\ Benutzername" oder "Benutzer Prinzipal Name (UPN) Format ()" aufweisen Username@DomainName . Der Dienst Prozess wird mit einer dieser beiden Formulare protokolliert, wenn er ausgeführt wird. , Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden. Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Bei Kernel-oder System Treibern enthält *StartName* den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden. Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde. Beispiel: dwdom- \\ Administrator.

</dd> <dt>

*Startpassword* \[ in\]
</dt> <dd>

Das Kennwort für den Kontonamen, der durch den *StartName* -Parameter angegeben wird. Geben Sie **null** an, wenn Sie das Kennwort nicht ändern. Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.

</dd> <dt>

*LoadOrderGroup* \[ in\]
</dt> <dd>

Der dem neuen Dienst zugeordnete Gruppenname. Lade Auftrags Gruppen sind in der Registrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden. Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge verweist, gehört der Dienst nicht zu einer Gruppe. Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden. Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören. Die Registrierung enthält eine Liste der Lade Auftrags Gruppen unter:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder**

</dd> <dt>

*Loadordergroupabhängigkeiten* \[ in\]
</dt> <dd>

Array von Gruppen für die Auslastungs Anordnung, die vor diesem Dienst gestartet werden müssen. Jedes Element im Array wird durch **null** getrennt, und die Liste wird durch zwei **null** -Werte beendet. In Visual Basic oder Skript können Sie ein VBArray übergeben. Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten. Gruppennamen muss der **SC- \_ Gruppen \_ Bezeichner** (definiert in der Datei "winsvc. h") vorangestellt werden, um ihn von einem Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden. Die Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

</dd> <dt>

*Service Abhängigkeiten* \[ in\]
</dt> <dd>

Ein Array, das Namen von Diensten enthält, die vor dem Start dieses Diensts gestartet werden müssen. Jedes Element im Array wird durch **null** getrennt, und die Liste wird durch zwei **null** -Werte beendet. In Visual Basic oder Skript können Sie ein VBArray übergeben. Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten. Die Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.

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

Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts (**State** -Eigenschaft der [**Win32- \_ baseservice**](win32-baseservice.md) -Klasse) gleich 0, 1 oder 2 ist.

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

Dienste werden im Allgemeinen auf zwei Arten installiert: entweder als Teil der Installation des Betriebssystems oder mithilfe eines Installationsprogramms, das vom Dienst Entwickler bereitgestellt wird. Einige Dienste, insbesondere solche, die intern erstellt wurden, verfügen jedoch möglicherweise nicht über ein Installationsprogramm. In diesen Fällen können Sie die **Create** -Methode verwenden, um-Dienste Programm gesteuert zu installieren.

Trotz des Namens erstellt die Create-Methode keinen Dienst. Es wird lediglich ein vorhandener Dienst installiert. Um diesen Befehl verwenden zu können, müssen Sie die ausführbare Dienst Datei auf einen Computer kopieren und dann **Create** verwenden, um den Dienst zu installieren.

Die **Create** -Methode ähnelt der- [**Änderungs**](change-method-in-class-win32-service.md) Methode. In beiden Fällen werden die Eigenschaften des Dienes als Parameter an die-Methode übermittelt. Wie bei den Parametern, die mit der **Änderungs** Methode verwendet werden, ist die Reihenfolge, in der diese Parameter übermittelt werden, sehr wichtig.

Der *LoadOrderGroup* -Parameter stellt eine Gruppierung von System Diensten dar, die Ausführungs Abhängigkeiten definieren. Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.

## <a name="examples"></a>Beispiele

Mit dem folgenden VBScript wird ein Dienst mit dem Namen dbservice installiert.


```VB
Const OWN_PROCESS = 16
Const NOT_INTERACTIVE = True
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objService = objWMIService.Get("Win32_BaseService")
errReturn = objService.Create ("DbService", "Personnel Database", _
"c:\windows\system32\db.exe", OWN_PROCESS ,2 ,"Automatic" , _
 NOT_INTERACTIVE ,".\LocalSystem" ,"")
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

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ Dienst**](win32-service.md)
</dt> <dt>

[WMI-Tasks: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

