---
title: SetDeviceRedirectionType-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die DeviceRedirectionType-Eigenschaft fest, die steuert, welche Geräte umgeleitet werden.
ms.assetid: d97a0a7d-a08e-4703-b0f0-ba5d20688dc8
ms.tgt_platform: multiple
keywords:
- SetDeviceRedirectionType-Methode Remotedesktopdienste
- SetDeviceRedirectionType-Methode Remotedesktopdienste , Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy Klasse Remotedesktopdienste , SetDeviceRedirectionType-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetDeviceRedirectionType
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdd3ccbe06acbc75e8c7c29632d7fd83dc0af222eb004c6b83976e3f6478f705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604659"
---
# <a name="setdeviceredirectiontype-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>SetDeviceRedirectionType-Methode der Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse

Legt die **DeviceRedirectionType-Eigenschaft** fest, die steuert, welche Geräte umgeleitet werden.

## <a name="syntax"></a>Syntax


```mof
uint32 SetDeviceRedirectionType(
  [in] uint32 DeviceRedirectionType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DeviceRedirectionType* \[ In\]
</dt> <dd>

Der Typ der Geräteumleitung.

<dt>

0
</dt> <dd>

Alle Geräte werden umgeleitet.

</dd> <dt>

1
</dt> <dd>

Es werden keine Geräte umgeleitet.

</dd> <dt>

2
</dt> <dd>

Angegebene Geräte werden nicht umgeleitet. Die Eigenschaften **DiskDrivesDisabled,** **PrinterDisabled,** **SerialPortsDisabled,** **ClipboardDisabled** und **PlugAndPlayDevicesDisabled** steuern, welche Geräte nicht umgeleitet werden.

</dd> </dl> </dd> </dl>

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

