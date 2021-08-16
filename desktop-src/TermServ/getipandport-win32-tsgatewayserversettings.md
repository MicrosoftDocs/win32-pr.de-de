---
title: GetIPAndPort-Methode der Win32_TSGatewayServerSettings-Klasse
description: Erhält die lauschende IP-Adresse und Portnummer für den angegebenen Transport.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- GetIPAndPort-Remotedesktopdienste
- GetIPAndPort-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings klasse Remotedesktopdienste , GetIPAndPort-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf1cb1d4f597e734ac66456cd515193afed5ad31b7b6543d4e52c09717346a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353851"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a>GetIPAndPort-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Erhält die lauschende IP-Adresse und Portnummer für den angegebenen Transport.

## <a name="syntax"></a>Syntax


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
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

*IPAddress* \[ out\]
</dt> <dd>

Eine Zeichenfolge, die die lauschende IP-Adresse in Oktettform empfängt (z. B. "192.168.1.1").

</dd> <dt>

*Port* \[ out\]
</dt> <dd>

Gibt die Lauschenportnummer an.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





