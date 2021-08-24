---
title: SetSecureIdAllowed-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Diese Methode ist für eine spätere Verwendung vorgesehen.
ms.assetid: 9f49e69a-c004-4e3e-b238-69865e3bf00b
ms.tgt_platform: multiple
keywords:
- SetSecureIdAllowed-Methode Remotedesktopdienste
- SetSecureIdAllowed-Methode Remotedesktopdienste , Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy Klasse Remotedesktopdienste , SetSecureIdAllowed-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSecureIdAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99039cd541ad8ab1746ace55de13f35722ea1ba7ccf52fd1a3de93e39e56798
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865110"
---
# <a name="setsecureidallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>SetSecureIdAllowed-Methode der Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse

Diese Methode ist für eine spätere Verwendung vorgesehen.

Legt die **SecureIdAllowed-Eigenschaft** fest, die für die zukünftige Verwendung reserviert ist.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSecureIdAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zulässig* \[ In\]
</dt> <dd>

Neuer **SecureIdAllowed-Wert.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

