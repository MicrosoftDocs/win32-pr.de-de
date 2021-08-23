---
title: EnableTransport-Methode der Win32_TSGatewayServerSettings Klasse
description: Aktiviert oder deaktiviert den angegebenen Transport.
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- EnableTransport-Remotedesktopdienste
- EnableTransport-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings klasse Remotedesktopdienste , EnableTransport-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08087c4a28b0867f7457bed597a71c5156ea968fb50f3f2509c8da5ef3057fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059598"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a>EnableTransport-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Aktiviert oder deaktiviert den angegebenen Transport.

## <a name="syntax"></a>Syntax


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TransportType* \[ In\]
</dt> <dd>

Gibt den Transporttyp an. Dies muss einer der folgenden Werte sein.

<dt>

0
</dt> <dd>

RPC über HTTP-Transport.

</dd> <dt>

1
</dt> <dd>

HTTP-Transport.

</dd> <dt>

2
</dt> <dd>

UDP-Transport.

</dd> </dl> </dd> <dt>

*Aktivieren* \[ In\]
</dt> <dd>

Gibt an, ob der Transport aktiviert oder deaktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                           |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





