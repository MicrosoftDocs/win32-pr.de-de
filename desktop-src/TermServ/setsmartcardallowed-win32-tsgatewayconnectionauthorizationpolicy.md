---
title: SetSmartcardAllowed-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die SmartcardAllowed-Eigenschaft fest, die die Unterstützung für die Verwendung einer Smartcard aktiviert oder deaktiviert, um eine Verbindung mit dem Remotedesktop Gatewayserver (RD-Gateway) herzustellen.
ms.assetid: 9fe1c7a9-2bab-439f-8dc2-421ed876fcf7
ms.tgt_platform: multiple
keywords:
- SetSmartcardAllowed-Methode Remotedesktopdienste
- SetSmartcardAllowed-Methode Remotedesktopdienste , Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy Klasse Remotedesktopdienste , SetSmartcardAllowed-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSmartcardAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54ea5618bd974c2051a588f532cac9fa741563f6d96be312c50fd9923497d9ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870070"
---
# <a name="setsmartcardallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>SetSmartcardAllowed-Methode der Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse

Legt die **SmartcardAllowed-Eigenschaft** fest, die die Unterstützung für die Verwendung einer Smartcard zum Herstellen einer Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway) aktiviert oder deaktiviert.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSmartcardAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zulässig* \[ In\]
</dt> <dd>

Neuer **SmartcardAllowed-Wert.**

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

 

