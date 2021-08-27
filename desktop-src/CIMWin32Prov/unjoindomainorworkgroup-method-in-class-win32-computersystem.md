---
description: Entfernt ein Computersystem aus einer Domäne oder Arbeitsgruppe.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: UnjoinDomainOrWorkgroup-Methode der Win32_ComputerSystem Klasse
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
ms.openlocfilehash: 992aa6c84f912f705e02252d1ac6d24422934edb991c049de188ab5fb0ccbfa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105070"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a>UnjoinDomainOrWorkgroup-Methode der Win32 \_ ComputerSystem-Klasse

Die **UnjoinDomainOrWorkgroup-Methode** entfernt ein Computersystem aus einer Domäne oder Arbeitsgruppe.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

*Kennwort* \[ In\]
</dt> <dd>

Wenn der *UserName-Parameter* einen Kontonamen angibt, muss der *Password-Parameter* auf das Kennwort verweisen, das beim Herstellen einer Verbindung mit dem Domänencontroller verwendet werden soll. Andernfalls muss dieser Parameter NULL **sein.**

> [!Note]  
> *Das* Kennwort muss beim Herstellen einer Verbindung mit Winmgmt oder [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) auf dem [**IWbemServices-Zeiger**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) eine hohe Authentifizierungsebene und nicht weniger als RPC **C \_ \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** verwenden. Wenn es sich um eine lokale Winmgmt-Datei handelt, ist dies kein Problem.

 

</dd> <dt>

*UserName* \[ In\]
</dt> <dd>

Zeiger auf eine konstante Zeichenfolge mit NULL-Terminierung, die den Kontonamen angibt, der beim Herstellen einer Verbindung mit dem Domänencontroller verwendet werden soll. Muss eine Domäne und ein Benutzerkonto angeben, z. B. \\ "Domänenbenutzer" oder " user@domain ". Wenn dieser Parameter **NULL ist,** wird der Aufruferkontext verwendet.

> [!Note]  
> *UserName* muss beim Herstellen einer Verbindung mit Winmgmt oder [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) im [**IWbemServices-Zeiger**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) eine hohe Authentifizierungsebene verwenden, nicht weniger als **RPC C \_ \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY.** Wenn es sich um eine lokale Winmgmt-Datei handelt, ist dies kein Problem.

 

</dd> <dt>

*FUnjoinOptions* \[ In\]
</dt> <dd>

Eine Reihe von Bitflags, die die Optionen für die Nichtjoinierung definieren.

<dt>



  (0)


</dt> <dd>

Standard. Keine Optionen.

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP \_ ACCT \_ DELETE** (4)


</dt> <dd>

Deaktivieren Sie das Active Directory-Konto nach dem Vorgang zum Abschalten, löschen Sie das Konto jedoch nicht.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **UnjoinDomainOrWorkgroup-Methode** gibt bei Erfolg oder ohne Optionen 0 (null) zurück. Jeder andere Wert gibt einen Fehler an. Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Andere** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Starten Sie nach dem Aufrufen dieser Methode den betroffenen Computer neu, um die Änderungen anzuwenden.

## <a name="examples"></a>Beispiele

[Die Unjoin a Computer from a Domain](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) Das VBScript-Beispiel entschalten den lokalen Computer von seiner aktuellen Domäne und deaktiviert das Computerkonto.

Im [Beispiel Unjoin a Computer from a Domain using VBS script (Entjoinen](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) eines Computers aus einer Domäne mithilfe des VBS-Skripts) wird ein angegebener Computer aus einer Domäne entfernt. .

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

[**Win32 \_ ComputerSystem**](win32-computersystem.md)
</dt> <dt>

[**JoinDomainOrWorkgroup-Methode**](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

