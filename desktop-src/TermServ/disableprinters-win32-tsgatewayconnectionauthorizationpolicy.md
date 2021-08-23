---
title: DisablePrinters-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die PrinterDisabled-Eigenschaft fest. Wenn die DeviceRedirectionType-Eigenschaft über den Wert \ 0034;2 \ 0034; verfügt, steuert die PrinterDisabled-Eigenschaft die Umleitung der Drucker für Sitzungen, die über den Remotedesktop Gateway-Server (RD-Gateway) eingerichtet werden.
ms.assetid: bf58d226-e3de-4c2b-aaa9-9e7ddbf49d31
ms.tgt_platform: multiple
keywords:
- DisablePrinters-Methode Remotedesktopdienste
- DisablePrinters-Methode Remotedesktopdienste , Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste , DisablePrinters-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisablePrinters
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f89ba8110d60df83410d0904d68b32cb849bfadbff7205f969842cb71a385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657980"
---
# <a name="disableprinters-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>DisablePrinters-Methode der Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse

Legt die **PrinterDisabled-Eigenschaft fest.** Wenn die **DeviceRedirectionType-Eigenschaft** den Wert "2" hat, steuert die **PrinterDisabled-Eigenschaft** die Umleitung der Drucker für Sitzungen, die über den Remotedesktop Gatewayserver (RD Gateway) eingerichtet werden.

## <a name="syntax"></a>Syntax


```mof
uint32 DisablePrinters(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deaktiviert* \[ In\]
</dt> <dd>

Neuer Wert für die **PrinterDisabled-Eigenschaft.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 

