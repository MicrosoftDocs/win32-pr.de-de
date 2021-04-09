---
title: Setcookieauthenticationallowed-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die cookieauthenticationallowed-Eigenschaft fest.
ms.assetid: 481b89cb-d73b-4dae-941c-a629c2ae5ac4
ms.tgt_platform: multiple
keywords:
- Setcookieauthenticationallowed-Methode Remotedesktopdienste
- Setcookieauthenticationallowed-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, setcookieauthenticationallowed-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetCookieAuthenticationAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9293123ab6ce5b1ddcdb172f9258ba73b23fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103154"
---
# <a name="setcookieauthenticationallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Setcookieauthenticationallowed-Methode der Win32- \_ Klasse "sgatewayconnectionauthorizationpolicy"

Legt die **cookieauthenticationallowed** -Eigenschaft fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetCookieAuthenticationAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zulässig* \[ in\]
</dt> <dd>

Typ: **booleschen**

Der neue Eigenschaftswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ faigatewayconnectionauthorizationpolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

