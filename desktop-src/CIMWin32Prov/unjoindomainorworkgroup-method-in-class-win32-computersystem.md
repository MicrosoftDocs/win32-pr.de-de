---
description: Entfernt ein Computersystem aus einer Domäne oder Arbeitsgruppe.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: UnjoinDomainOrWorkgroup-Methode der Win32_ComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861600"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a>UnjoinDomainOrWorkgroup-Methode der Win32 \_ Computersystem-Klasse

Mit der **UnjoinDomainOrWorkgroup** -Methode wird ein Computersystem aus einer Domäne oder Arbeitsgruppe entfernt.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kennwort* \[ in\]
</dt> <dd>

Wenn der Parameter *username* einen Kontonamen angibt, muss der *Password* -Parameter auf das Kennwort verweisen, das beim Herstellen einer Verbindung mit dem Domänen Controller verwendet werden soll. Andernfalls muss dieser Parameter **null** sein.

> [!Note]  
> Das *Kennwort* muss bei der Verbindung mit winmgmt oder [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) auf dem [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) -Zeiger eine hohe Authentifizierungs Ebene und nicht weniger als die **\_ \_ \_ \_ Pkt- \_ Datenschutzebene der RPC-C-authn-Ebene** verwenden. Wenn es sich um ein lokales in WinMgmt handelt, ist dies kein Problem.

 

</dd> <dt>

*Benutzername* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante mit NULL endende Zeichenfolge, die den Kontonamen angibt, der beim Herstellen einer Verbindung mit dem Domänen Controller verwendet werden soll. Sie müssen ein Domänen-und Benutzerkonto angeben, z. b. "Domänen \\ Benutzer" oder " user@domain ". Wenn dieser Parameter **null** ist, wird der Aufruferkontext verwendet.

> [!Note]  
> Der *Benutzername* muss beim Herstellen einer Verbindung mit winmgmt oder [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) auf dem [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) -Zeiger eine hohe Authentifizierungs Ebene und nicht weniger als die **\_ \_ \_ \_ Pkt- \_ Datenschutzebene der RPC-C-authn-Ebene** verwenden. Wenn es sich um ein lokales in WinMgmt handelt, ist dies kein Problem.

 

</dd> <dt>

*FUnjoinOptions* \[ in\]
</dt> <dd>

Ein Satz von Bitflags, die die Optionen für den entfernen definieren.

<dt>



  (0)


</dt> <dd>

Standard. Keine Optionen.

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**Netsetup \_ \_Löschen** (4)


</dt> <dd>

Deaktivieren Sie das Active Directory Konto nach dem Vorgang zum nicht beitreten, aber löschen Sie das Konto nicht.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **UnjoinDomainOrWorkgroup** -Methode gibt bei Erfolg 0 (null) zurück oder wenn keine Optionen beteiligt sind. Jeder andere Wert gibt einen Fehler an. Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Sonstige** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Starten Sie nach dem Aufrufen dieser Methode den betroffenen Computer neu, um die Änderungen zu übernehmen.

## <a name="examples"></a>Beispiele

[Die Verknüpfung eines Computers aus einer Domäne entfernen](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) Im VBScript-Beispiel wird der lokale Computer aus der aktuellen Domäne entfernt, und das Computer Konto wird deaktiviert.

Das Beispiel zum [Entfernen eines Computers aus einer Domäne mithilfe eines vbskripts](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) entfernt die Verknüpfung eines angegebenen Computers zu einer Domäne. .

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

[**JoinDomainOrWorkgroup-Methode**](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

