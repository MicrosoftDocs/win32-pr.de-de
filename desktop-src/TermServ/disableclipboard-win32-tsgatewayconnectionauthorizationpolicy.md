---
title: Disableclipboard-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die clipboarddeaktiviert-Eigenschaft fest. Wenn die deviceredirectiontype-Eigenschaft den Wert \ 0034; 2 \ 0034; hat, steuert die clipboarddeaktiviert-Eigenschaft die Umleitung der Zwischenablage für Sitzungen, die über den Remotedesktop Gateway-Server (RD-Gateway) eingerichtet werden.
ms.assetid: c53fc802-958b-452d-9af9-0ce89ed46079
ms.tgt_platform: multiple
keywords:
- Disableclipboard-Methode Remotedesktopdienste
- Disableclipboard-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy Klasse Remotedesktopdienste, disableclipboard-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableClipboard
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ae2070a35fa31f1c9d9ad31e9e632e31c0193f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337495"
---
# <a name="disableclipboard-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Disableclipboard-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"

Legt die **clipboarddeaktiviert** -Eigenschaft fest. Wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" hat, steuert die **clipboarddeaktiviert** -Eigenschaft die Umleitung der Zwischenablage für Sitzungen, die über den Remotedesktop Gateway-Server (RD-Gateway) eingerichtet werden.

## <a name="syntax"></a>Syntax


```mof
uint32 DisableClipboard(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deaktiviert* \[ in\]
</dt> <dd>

Neuer Wert für die **clipboarddeaktiviert** -Eigenschaft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ faigatewayconnectionauthorizationpolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

