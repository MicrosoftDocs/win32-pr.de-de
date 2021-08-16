---
description: Verbindet ein Computersystem mit einer Domäne oder Arbeitsgruppe.
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
ms.openlocfilehash: b9faf923cf6c771e95a7dfb4f0b04f896c54d79c6b5548e97850d867057b065b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834647"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a>JoinDomainOrWorkgroup-Methode der Win32 \_ ComputerSystem-Klasse

Die **JoinDomainOrWorkgroup-Methode** verbindet ein Computersystem mit einer Domäne oder Arbeitsgruppe.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

*Name* \[ In\]
</dt> <dd>

Gibt die Domäne oder Arbeitsgruppe an, der bzw. die beitreten soll. Darf nicht **NULL** sein.

</dd> <dt>

*Kennwort* \[ In\]
</dt> <dd>

Wenn der *UserName-Parameter* einen Kontonamen angibt, muss der *Parameter Password* auf das Kennwort verweisen, das beim Herstellen einer Verbindung mit dem Domänencontroller verwendet werden soll. Andernfalls muss dieser Parameter **NULL** sein.

</dd> <dt>

*UserName* \[ In\]
</dt> <dd>

Zeiger auf eine konstante NULL-terminierte Zeichenfolge, die den Kontonamen angibt, der beim Herstellen einer Verbindung mit dem Domänencontroller verwendet werden soll. Muss einen NetBIOS-Domänennamen und ein Benutzerkonto angeben, z. \\ B. Domänenbenutzer. Wenn dieser Parameter **NULL** ist, werden die Aufruferinformationen verwendet.

Sie können auch den Benutzerprinzipalnamen (UPPED) im Format user@domain verwenden.

</dd> <dt>

*AccountOU* \[ In\]
</dt> <dd>

Gibt den Zeiger auf eine konstante NULL-terminierte Zeichenfolge an, die den [RFC 1779-Formatnamen](https://www.ietf.org/rfc/rfc1779.txt) der Organisationseinheit (OE) für das Computerkonto enthält. Wenn Sie diesen Parameter angeben, muss die Zeichenfolge einen vollständigen Pfad enthalten, andernfalls muss *Accent* **NULL** sein.

Beispiel: "OU=testOU; DC=domain; DC=Domäne; DC=com"

</dd> <dt>

*FJoinOptions* \[ In\]
</dt> <dd>

Satz von Bitflags, die die Joinoptionen definieren.

<dt>



  (0)


</dt> <dd>

Standard. Keine Joinoptionen.

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP \_ JOIN \_ DOMAIN** (0x00000001)


</dt> <dd>

Verbindet den Computer mit einer Domäne. Wenn dieser Wert nicht angegeben ist, wird der Computer in eine Arbeitsgruppe aufgenommen.

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP \_ ACCT \_ CREATE** (0x00000002)


</dt> <dd>

Erstellt das Konto in der Domäne.

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP \_ WIN9X \_ UPGRADE** (0x00000010)


</dt> <dd>

Der Joinvorgang erfolgt im Rahmen eines Upgrades.

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP \_ DOMÄNEN \_ JOIN \_ BEI \_ BEITRITT** (0x00000020)


</dt> <dd>

Ermöglicht den Beitritt zu einer neuen Domäne, auch wenn der Computer bereits in eine Domäne eingebunden ist.

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP \_ JOIN \_ UNSECURE** (0x00000040)


</dt> <dd>

Führt einen unsicheren Beitritt durch.

Diese Option fordert einen Domänenbeitritt zu einem vorab erstellten Konto an, ohne sich mit Domänenbenutzeranmeldeinformationen zu authentifizieren. Diese Option kann in Verbindung mit der **\_ \_ PWD \_ PASSED-Option von NETSETUP MACHINE** verwendet werden. In diesem Fall ist *Kennwort* das Kennwort des vorab erstellten Computerkontos.

Vor Windows Vista mit SP1 und Windows Server 2008 hat sich ein unsicherer Join nicht beim Domänencontroller authentifiziert. Die gesamte Kommunikation wurde mit einer NULL-Sitzung (nicht authentifiziert) durchgeführt. Ab Windows Vista mit SP1 und Windows Server 2008 werden der Computerkontoname und das Kennwort für die Authentifizierung beim Domänencontroller verwendet.

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP \_ MACHINE \_ PWD \_ PASSED** (0x00000080)


</dt> <dd>

Gibt an, dass der *Parameter Password* ein Lokales Computerkontokennwort anstelle eines Benutzerkennworts angibt. Dieses Flag ist nur für unsichere Joins gültig, die Sie angeben müssen, indem Sie auch das NETSETUP \_ JOIN \_ UNSECURE-Flag festlegen.

Wenn Sie dieses Flag festlegen, wird nach erfolgreichem Joinvorgang das Computerkennwort auf den Wert *Kennwort* festgelegt, wenn dieser Wert ein gültiges Computerkennwort ist.

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP \_ DEFER \_ SPN \_ SET** (0x00000100)


</dt> <dd>

Gibt an, dass der Dienstprinzipalname (SPN) und die DnsHostName-Eigenschaften des Computerobjekts zu diesem Zeitpunkt nicht aktualisiert werden sollen.

In der Regel werden diese Eigenschaften während des Joinvorgangs aktualisiert. Stattdessen sollten diese Eigenschaften während eines nachfolgenden Aufrufs der [**Rename-Methode**](rename-method-in-class-win32-computersystem.md) aktualisiert werden. Diese Eigenschaften werden während des Umbenennungsvorgangs immer aktualisiert.

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP \_ \_JOIN DC \_ ACCOUNT** (0x00000200)


</dt> <dd>

Lassen Sie den Domänen join zu, wenn ein vorhandenes Konto ein Domänencontroller ist.

> [!Note]  
> Dieses Flag wird auf Windows Vista und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP \_ MEHRDEUTIGER \_ DC** (0x00001000)


</dt> <dd>

Versuchen Sie beim Beitreten zur Domäne nicht, den bevorzugten Domänencontroller in der Registrierung festzulegen.

> [!Note]  
> Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP \_ NO \_ NETLOGON \_ CACHE** (0x00002000)


</dt> <dd>

Wenn Sie der Domäne beitreten, erstellen Sie nicht den Netlogon-Cache.

> [!Note]  
> Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP \_ DONT \_ CONTROL \_ SERVICES** (0x00004000)


</dt> <dd>

Wenn Sie der Domäne beitreten, erzwingen Sie nicht den Start des Netlogon-Diensts.

> [!Note]  
> Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP \_ SET \_ MACHINE \_ NAME** (0x00008000)


</dt> <dd>

Legen Sie beim Beitritt zur Domäne nur für den Offlinebeitritt den Hostnamen des Zielcomputers und den NetBIOS-Namen fest.

> [!Note]  
> Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP \_ FORCE \_ SPN \_ SET** (0x00010000)


</dt> <dd>

Wenn Sie der Domäne beitreten, überschreiben Sie andere Einstellungen während des Domänenbeitritts, und legen Sie den Dienstprinzipalnamen (Service Principal Name, SPN) fest.

> [!Note]  
> Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP \_ KEINE \_ \_ ACCT-WIEDERVERWENDUNG** (0x00020000)


</dt> <dd>

Wenn Sie der Domäne beitreten, sollten Sie kein vorhandenes Konto wiederverwenden.

> [!Note]  
> Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP \_ IGNORIEREN \_ NICHT UNTERSTÜTZTER \_ FLAGS** (0x10000000)


</dt> <dd>

Wenn dieses Bit festgelegt ist, werden nicht erkannte Flags von der **JoinDomainOrWorkgroup-Funktion** ignoriert, und [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) verhält sich so, als wären die Flags nicht festgelegt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [Systemfehlercode](/windows/desktop/Debug/system-error-codes)zurück, der einen der folgenden numerischen Werte enthalten kann. Jede andere Zahl gibt einen Fehler an. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

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

Das angegebene Objekt kann vom System nicht geöffnet werden.

</dd> <dt>

**1323**
</dt> <dd>

Das Kennwort kann nicht aktualisiert werden.

</dd> <dt>

**1326**
</dt> <dd>

Anmeldefehler: unbekannter Benutzername oder ungültiges Kennwort.

</dd> <dt>

**1355**
</dt> <dd>

Die angegebene Domäne ist entweder nicht vorhanden oder konnte nicht kontaktiert werden.

</dd> <dt>

**2224**
</dt> <dd>

Das Konto ist bereits vorhanden.

</dd> <dt>

**2691**
</dt> <dd>

Der Computer ist bereits in die Domäne eingebunden.

</dd> <dt>

**2692**
</dt> <dd>

Der Computer ist derzeit keiner Domäne beigetreten.

</dd> <dt>

**WBEM \_ E ENCRYPTED CONNECTION \_ \_ \_ ERFORDERLICH**
</dt> <dd>

0x80041087

*Kennwort* und *Benutzername* werden angegeben, aber die Authentifizierungsebene ist nicht **RPC C \_ \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Für Visual Basic wird **wbemErrEncryptedConnectionRequired** zurückgegeben.

</dd> <dt>

**Andere**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie einen Computer aus einer Domäne in eine Arbeitsgruppe verschieben, müssen Sie den Computer aus der Domäne entfernen (mit einem Aufruf von [**UnjoinDomainOrWorkgroup),**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)bevor Sie diese Methode aufrufen, um einer Arbeitsgruppe beizutreten (mit einem Aufruf von **JoinDomainOrWorkgroup**). Starten Sie nach dem Aufrufen dieser Methode den betroffenen Computer neu, um die Änderungen anzuwenden.

*UserName* und *Password* können **NULL** bleiben. Die Authentifizierung der Verbindung mit WMI muss jedoch 6 im Skript oder **WbemAuthenticationLevelPktPrivacy** in Visual Basic und anderen Sprachen sein, die die [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) Bibliothek verwenden können. Weitere Informationen finden Sie unter [Festlegen der Standardprozesssicherheitsstufe mit VBScript.](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript)

Legen Sie in C++ die Authentifizierung auf **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** entweder in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), für den gesamten Prozess oder in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)für eine Verbindung mit dem [**IWbemServices-Proxy**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) fest. Weitere Informationen finden Sie unter [Festlegen der Authentifizierung mit C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) und [Festlegen der Sicherheit für IWbemServices und andere Proxys.](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies)

## <a name="examples"></a>Beispiele

Im PowerShell-Beispiel [Join a computer to a domain](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) (Computer einer Domäne beitreten) wird ein Computer in eine Domäne aufgenommen.

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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ ComputerSystem**](win32-computersystem.md)
</dt> <dt>

[**UnjoinDomainOrWorkgroup-Methode**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

