---
title: SetCookieAuthenticationAllowed-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die CookieAuthenticationAllowed-Eigenschaft fest.
ms.assetid: 481b89cb-d73b-4dae-941c-a629c2ae5ac4
ms.tgt_platform: multiple
keywords:
- SetCookieAuthenticationAllowed-Remotedesktopdienste
- SetCookieAuthenticationAllowed-Methode Remotedesktopdienste , Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy klasse Remotedesktopdienste , SetCookieAuthenticationAllowed-Methode
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
ms.openlocfilehash: d9302c4847346cf6d58c6f7ecb178760db9b7c0760331da94bbab2b95cccd7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118851628"
---
# <a name="setcookieauthenticationallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>SetCookieAuthenticationAllowed-Methode der Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse

Legt die **CookieAuthenticationAllowed-Eigenschaft** fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetCookieAuthenticationAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zulässig* \[ In\]
</dt> <dd>

Typ: **boolescher Wert**

Der neue Eigenschaftswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

