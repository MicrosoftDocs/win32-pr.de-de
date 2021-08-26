---
description: 'Create method of the Win32_Service class (CIMWin32 WMI Providers) ( Create method of the Win32_Service Class (CIMWin32 WMI Providers)): Erstellt einen neuen Systemdienst.'
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: Create-Methode der Win32_Service -Klasse (CIMWin32-WMI-Anbieter)
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
ms.openlocfilehash: 3baa83179ac6c5040aa85a5fcf2af0d932a4c8e9cdc2d10742c5c8aaa66abb5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003800"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Create-Methode der Win32_Service -Klasse (CIMWin32-WMI-Anbieter)

Die **Create** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) erstellt einen neuen Systemdienst.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

*Name* \[ In\]
</dt> <dd>

Name des Diensts, der in der **Create-Methode installiert werden** soll. Die maximale Zeichenfolgenlänge beträgt 256 Zeichen. Die Service Control Manager-Datenbank behält die Groß-/Kleinschreibung der Zeichen bei, bei Dienstnamenvergleichen wird die Groß-/Kleinschreibung jedoch immer nicht beachtet. Schrägstriche (/) und doppelte schräge Schrägstriche \\ () sind ungültige Dienstnamenzeichen.

</dd> <dt>

*DisplayName* \[ In\]
</dt> <dd>

Anzeigename des Diensts. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager beibehalten. *Bei DisplayName-Vergleichen* wird die Groß-/Kleinschreibung immer nicht beachtet.

Einschränkungen: Akzeptiert den gleichen Wert wie der *Name-Parameter.*

Beispiel: "Atdisk".

</dd> <dt>

*PathName* \[ In\]
</dt> <dd>

Vollqualifizierter Pfad zur ausführbaren Datei, die den Dienst implementiert.

Beispiel: \\ "SystemRoot \\ \\ System32-Treiber \\afd.sys".

</dd> <dt>

*ServiceType* \[ In\]
</dt> <dd>

Typ der Dienste, die für Prozesse bereitgestellt werden, die sie aufrufen.

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

Schweregrad des Fehlers, wenn die **Create-Methode** nicht gestartet werden kann. Der Wert gibt die Aktion an, die vom Startprogramm ausgeführt wird, wenn ein Fehler auftritt. Alle Fehler werden vom System protokolliert.

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

*StartMode* \[ In\]
</dt> <dd>

Startmodus des Windows Basisdiensts.

<dt>

Start
</dt> <dd>

Vom Betriebssystemlader gestarteter Gerätetreiber. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

System
</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungsprozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

Automatisch
</dt> <dd>

Der Dienst wird automatisch vom Dienststeuerungs-Manager während des Systemstarts gestartet.

</dd> <dt>

Manuell
</dt> <dd>

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService-Methode**](startservice-method-in-class-win32-service.md) aufruft.

</dd> <dt>

Disabled
</dt> <dd>

Dienst, der nicht mehr gestartet werden kann.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ In\]
</dt> <dd>

True **gibt an,** dass der Dienst Fenster auf dem Desktop erstellen oder mit ihnen kommunizieren kann.

</dd> <dt>

*StartName* \[ In\]
</dt> <dd>

Kontoname, unter dem der Dienst ausgeführt wird. Je nach Diensttyp kann der Kontoname das Format DomainName Username oder \\ UpN (UpN) (Benutzerprinzipalname ( ) Username@DomainName haben. Der Dienstprozess wird mit einer dieser beiden Formen protokolliert, wenn er ausgeführt wird. Wenn das Konto zur integrierten Domäne gehört, . \\ Der Benutzername kann angegeben werden. Wenn **NULL** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Für Einen Kernel oder Treiber auf Systemebene enthält *StartName* den Treiberobjektnamen (d. h. FileSystem Rdr oder Driver Xns), den das Eingabe- und Ausgabesystem \\ \\ \\ (E/A) zum Laden des \\ Gerätetreibers verwendet. Wenn **NULL** angegeben wird, wird der Treiber mit einem Standardobjektnamen ausgeführt, der vom E/A-System basierend auf dem Dienstnamen erstellt wird. Beispiel: \\ DWDOM-Administrator.

</dd> <dt>

*StartPassword* \[ In\]
</dt> <dd>

Kennwort für den Kontonamen, der durch den *StartName-Parameter angegeben* wird. Geben **Sie NULL** an, wenn Sie das Kennwort nicht ändern. Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.

</dd> <dt>

*LoadOrderGroup* \[ In\]
</dt> <dd>

Gruppenname, der dem neuen Dienst zugeordnet ist. Ladereihenfolgegruppen sind in der Registrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden. Wenn der Zeiger NULL **ist** oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe. Abhängigkeiten zwischen Gruppen sollten im *LoadOrderGroupDependencies-Parameter aufgeführt* werden. Dienste in der Liste der Last reihenfolgengruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die nicht in der Liste der Last reihenfolgengruppen enthalten sind, gefolgt von Diensten, die nicht zu einer Gruppe gehören. Die Registrierung verfügt über eine Liste der Last reihenfolgengruppen unter:

**HKEY \_ LOCAL \_ MACHINE-System** \\  \\ **CurrentControlSet-Steuerelement** \\  \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ In\]
</dt> <dd>

Array von Last reihenfolgengruppen, die vor diesem Dienst gestartet werden müssen. Jedes Element im Array wird durch **NULL** getrennt, und die Liste wird durch zwei **NULL-Werte** beendet. In Visual Basic skript können Sie ein vbArray übergeben. Wenn der Zeiger NULL **ist** oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Gruppennamen muss das SC **\_ GROUP \_ IDENTIFIER-Zeichen** (definiert in der Datei Winsvc.h) vorangestellt werden, um es von einem Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden. Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

</dd> <dt>

*ServiceDependencies* \[ In\]
</dt> <dd>

Array, das Namen von Diensten enthält, die gestartet werden müssen, bevor dieser Dienst gestartet wird. Jedes Element im Array wird durch **NULL** getrennt, und die Liste wird durch zwei **NULL-Werte** beendet. In Visual Basic skript können Sie ein vbArray übergeben. Wenn der Zeiger NULL **ist** oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst ausgeführt wird, von dem er abhängig ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um auf einen Fehler hindeuten zu können. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

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

Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts **(State-Eigenschaft** der [**Win32 \_ BaseService-Klasse)**](win32-baseservice.md) gleich 0, 1 oder 2 ist.

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

Der Dienst verfügt beim Start über zirkuläre Abhängigkeiten.

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

Dienste werden in der Regel auf zwei Arten installiert: entweder als Teil der Betriebssysteminstallation oder mithilfe eines vom Dienstentwickler bereitgestellten Installationsprogramms. Einige Dienste, insbesondere solche, die im Unternehmen erstellt wurden, verfügen jedoch möglicherweise nicht über ein Installationsprogramm. In diesen Fällen können Sie die **Create-Methode** verwenden, um Dienste programmgesteuert zu installieren.

Trotz des Namens erstellt die Create-Methode keinen Dienst. Es wird lediglich ein vorhandener Dienst installiert. Um diesen Befehl verwenden zu können, müssen Sie die ausführbare Datei des Diensts auf einen Computer kopieren und dann **erstellen** verwenden, um den Dienst zu installieren.

Die **Create-Methode** ähnelt der [**Change-Methode.**](change-method-in-class-win32-service.md) In beiden Fällen werden die Eigenschaften des Diensts als Parameter an die -Methode übergeben. Wie bei den Parametern, die mit der **Change-Methode** verwendet werden, ist die Reihenfolge, in der diese Parameter übergeben werden, sehr wichtig.

Der *LoadOrderGroup-Parameter* stellt eine Gruppierung von Systemdiensten dar, die Ausführungsabhängigkeiten definieren. Die Dienste müssen in der von der Lastauftragsgruppe angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern das Vorhandensein der voraussenten Dienste, damit sie ordnungsgemäß funktionieren.

## <a name="examples"></a>Beispiele

Das folgende VBScript installiert einen Dienst namens DbService.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32-Dienst \_**](win32-service.md)
</dt> <dt>

[WMI-Aufgaben: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

