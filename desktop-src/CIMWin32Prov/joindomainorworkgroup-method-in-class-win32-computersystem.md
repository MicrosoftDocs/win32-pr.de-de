---
description: Fügt ein Computersystem einer Domäne oder Arbeitsgruppe hinzu.
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: JoinDomainOrWorkgroup-Methode der Win32_ComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 927dd6b2664c92ff07e94407fdc59fdd917363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861527"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a>JoinDomainOrWorkgroup-Methode der Win32 \_ Computersystem-Klasse

Die **JoinDomainOrWorkgroup** -Methode verbindet ein Computersystem mit einer Domäne oder Arbeitsgruppe.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

Gibt die Domäne oder Arbeitsgruppe an, der beigetreten werden soll. Darf nicht **null** sein.

</dd> <dt>

*Kennwort* \[ in\]
</dt> <dd>

Wenn der Parameter *username* einen Kontonamen angibt, muss der *Password* -Parameter auf das Kennwort verweisen, das beim Herstellen einer Verbindung mit dem Domänen Controller verwendet werden soll. Andernfalls muss dieser Parameter **null** sein.

</dd> <dt>

*Benutzername* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante mit **null** endende Zeichenfolge, die den Kontonamen angibt, der beim Herstellen einer Verbindung mit dem Domänen Controller verwendet werden soll. Sie müssen einen Domänen-NetBIOS-Namen und ein Benutzerkonto angeben, z. b. Domänen \\ Benutzer. Wenn dieser Parameter **null** ist, werden die Aufruferinformationen verwendet.

Sie können auch den Benutzer Prinzipal Namen (User Principal Name, upped) im Formular verwenden user@domain .

</dd> <dt>

*AccountOU* \[ in\]
</dt> <dd>

Gibt den Zeiger auf eine Konstante mit **null** endenden Zeichenfolge an, die den [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) -Format Namen der Organisationseinheit (OU) für das Computer Konto enthält. Wenn Sie diesen Parameter angeben, muss die Zeichenfolge einen vollständigen Pfad enthalten. andernfalls muss der *Akzent* **null** sein.

Beispiel: "ou = testOU; DC = Domäne; DC = Domäne; DC = com "

</dd> <dt>

"F"- *Optionen* \[ in\]
</dt> <dd>

Ein Satz von Bitflags, die die joinoptionen definieren.

<dt>



  (0)


</dt> <dd>

Standard. Keine Join-Optionen.

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**Netsetup \_ Beitreten zur \_ Domäne** (0x00000001)


</dt> <dd>

Fügt den Computer einer Domäne hinzu. Wenn dieser Wert nicht angegeben wird, wird der Computer mit einer Arbeitsgruppe verbunden.

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**Netsetup \_ Acct \_ Erstellen** (0x00000002)


</dt> <dd>

Erstellt das Konto für die Domäne.

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**Netsetup \_ WIN9X- \_ Upgrade** (0x00000010)


</dt> <dd>

Der Joinvorgang tritt im Rahmen eines Upgrades auf.

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**Netsetup \_ Domänen \_ Beitritt, \_ Wenn \_** verknüpft (0x00000020)


</dt> <dd>

Ermöglicht das beitreten zu einer neuen Domäne, auch wenn der Computer bereits einer Domäne hinzugefügt wurde.

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**Netsetup \_ \_Nicht sicher beitreten** (0x00000040)


</dt> <dd>

Führt einen unsicheren Beitritt durch.

Diese Option fordert einen Domänen Beitritt zu einem vorab erstellten Konto ohne Authentifizierung mit Domänen Benutzer-Anmelde Informationen an. Diese Option kann in Verbindung mit der Option **netsetup \_ Machine \_ pwd- \_ weitergegeben** verwendet werden. In diesem Fall ist *Password* das Kennwort des vorab erstellten Computer Kontos.

Vor Windows Vista mit SP1 und Windows Server 2008 wurde ein unsicherer Join nicht beim Domänen Controller authentifiziert. Die gesamte Kommunikation wurde mithilfe einer NULL-Sitzung (nicht authentifiziert) durchgeführt. Ab Windows Vista mit SP1 und Windows Server 2008 werden der Computer Konto Name und das Kennwort verwendet, um sich beim Domänen Controller zu authentifizieren.

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**Netsetup \_ Computer- \_ pwd \_ übergeben** (0x00000080)


</dt> <dd>

Gibt an, dass der Kenn *Wort* Parameter anstelle eines Benutzer Kennworts ein Kennwort für das lokale Computer Konto angibt. Dieses Flag ist nur für unsichere Joins gültig, die Sie angeben müssen, indem Sie auch das unsecure-Flag "netsetup Join" festlegen \_ \_ .

Wenn Sie dieses Flag festlegen, wird das Computer Kennwort nach erfolgreicher Verbindungs Ausführung auf den Wert des *Kennworts* festgelegt, wenn es sich bei diesem Wert um ein gültiges Computer Kennwort handelt.

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**Netsetup \_ \_SPN- \_ Satz zurücksetzen** (0x00000100)


</dt> <dd>

Gibt an, dass der Dienst Prinzipal Name (SPN) und die DNSHostName-Eigenschaften des Computer Objekts zu diesem Zeitpunkt nicht aktualisiert werden sollen.

Diese Eigenschaften werden in der Regel während des Join-Vorgangs aktualisiert. Stattdessen sollten diese Eigenschaften bei einem nachfolgenden Rückruf der [**Rename**](rename-method-in-class-win32-computersystem.md) -Methode aktualisiert werden. Diese Eigenschaften werden während des Umbenennungs Vorgangs immer aktualisiert.

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**Netsetup \_ \_DC- \_ Konto beitreten** (0x00000200)


</dt> <dd>

Erlauben Sie den Domänen Beitritt, wenn ein vorhandenes Konto ein Domänen Controller ist.

> [!Note]  
> Dieses Flag wird unter Windows Vista und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**Netsetup \_ Mehrdeutiger \_ DC** (0x00001000)


</dt> <dd>

Versuchen Sie beim Beitreten zur Domäne nicht, den bevorzugten Domänen Controller in der Registrierung festzulegen.

> [!Note]  
> Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**Netsetup \_ Kein \_ Netlogon- \_ Cache** (0x00002000)


</dt> <dd>

Wenn Sie der Domäne beitreten, erstellen Sie den Netlogon-Cache nicht.

> [!Note]  
> Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**Netsetup \_ Nicht \_ Steuerungs \_ Dienste** (0x00004000)


</dt> <dd>

Wenn Sie der Domäne beitreten, erzwingen Sie nicht, dass der Netlogon-Dienst startet.

> [!Note]  
> Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**Netsetup \_ \_Computer \_ Namen festlegen** (0x00008000)


</dt> <dd>

Wenn Sie die Domäne nur für den Offline Beitritt beitreten, legen Sie den Hostnamen des Ziel Computers und den NetBIOS-Namen fest.

> [!Note]  
> Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**Netsetup \_ \_SPN- \_ Satz erzwingen** (0x00010000 bis)


</dt> <dd>

Überschreiben Sie beim Beitreten zur Domäne andere Einstellungen während des Domänen Beitritts, und legen Sie den Dienst Prinzipal Namen (SPN) fest.

> [!Note]  
> Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**Netsetup \_ Keine \_ Acct- \_ Wiederverwendung** (0x00020000)


</dt> <dd>

Verwenden Sie beim Beitreten zur Domäne kein vorhandenes Konto.

> [!Note]  
> Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**Netsetup \_ \_Nicht unterstützte \_ Flags ignorieren** (0x10000000)


</dt> <dd>

Wenn dieses Bit festgelegt ist, werden unbekannte Flags von der **JoinDomainOrWorkgroup** -Funktion ignoriert, und [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) verhält sich so, als ob die Flags nicht festgelegt wurden.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [Systemfehler Code](/windows/desktop/Debug/system-error-codes)zurück, der einen der folgenden numerischen Werte enthalten kann. Jede andere Zahl gibt einen Fehler an. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

</dd> <dt>

**5**
</dt> <dd>

Zugriff verweigert.“

</dd> <dt>

**87**
</dt> <dd>

„Der Parameter ist falsch.“

</dd> <dt>

**110**
</dt> <dd>

Das System kann das angegebene Objekt nicht öffnen.

</dd> <dt>

**1323**
</dt> <dd>

Das Kennwort kann nicht aktualisiert werden.

</dd> <dt>

**1326**
</dt> <dd>

Anmeldefehler: Unbekannter Benutzername oder ungültiges Kennwort.

</dd> <dt>

**1355**
</dt> <dd>

Die angegebene Domäne ist entweder nicht vorhanden, oder es konnte keine Verbindung mit ihr hergestellt werden.

</dd> <dt>

**2224**
</dt> <dd>

Das Konto ist bereits vorhanden.

</dd> <dt>

**2691**
</dt> <dd>

Der Computer ist bereits der Domäne beigetreten.

</dd> <dt>

**2692**
</dt> <dd>

Der Computer ist zurzeit keiner Domäne beigetreten.

</dd> <dt>

**WBEM \_ E- \_ verschlüsselte \_ Verbindung \_ erforderlich**
</dt> <dd>

0x80041087

Das *Kennwort* und der *Benutzername* sind angegeben, aber die Authentifizierungs Ebene entspricht nicht der **RPC-C- \_ \_ authn- \_ Ebene \_ Pkt \_ Privacy** Für Visual Basic wird **wbemErrEncryptedConnectionRequired** zurückgegeben.

</dd> <dt>

**Andere**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Computer von einer Domäne in eine Arbeitsgruppe verschieben, müssen Sie den Computer aus der Domäne entfernen (mit einem Aufruf von [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)), bevor Sie diese Methode aufrufen, um einer Arbeitsgruppe beizutreten (mit einem Aufruf von **JoinDomainOrWorkgroup**). Starten Sie nach dem Aufrufen dieser Methode den betroffenen Computer neu, um die Änderungen zu übernehmen.

Der *Benutzername* und das *Kennwort* können **null** bleiben. Allerdings muss die Authentifizierung der Verbindung mit WMI in den Skripts "6" oder " **wbemauthenticationlevelpktprivacy** " in Visual Basic und anderen Sprachen erfolgen, die die [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) Bibliothek verwenden können. Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).

Legen Sie in C++ die Authentifizierung auf **RPC- \_ C- \_ authn- \_ Ebene \_ Pkt \_ Privacy** entweder in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), für den gesamten Prozess oder in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)für eine Verbindung mit dem [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) -Proxy fest. Weitere Informationen finden Sie unter [Festlegen der Authentifizierung mit C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) und [Festlegen der Sicherheit für IWbemServices und andere](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies)Proxys.

## <a name="examples"></a>Beispiele

Im Beispiel [Hinzufügen eines Computers zu einer Domäne in](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell wird ein Computer einer Domäne hinzugefügt.

Im folgenden VBScript-Codebeispiel wird ein Computer mit einer Domäne verbunden und das Konto des Computers in Active Directory erstellt.


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
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

[**Win32- \_ Computersystem**](win32-computersystem.md)
</dt> <dt>

[**UnjoinDomainOrWorkgroup-Methode**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

