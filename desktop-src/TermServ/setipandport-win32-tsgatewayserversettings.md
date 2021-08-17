---
title: SetIPAndPort-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt die lauschende IP-Adresse und portnummer für den angegebenen Transport fest.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- SetIPAndPort-Methode Remotedesktopdienste
- SetIPAndPort-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings Klasse Remotedesktopdienste , SetIPAndPort-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af40c52523869e07268a26d858e0e70b933431a6583998c9d0041f476678d243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137973"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a>SetIPAndPort-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Legt die lauschende IP-Adresse und portnummer für den angegebenen Transport fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
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

*IPAddress* \[ In\]
</dt> <dd>

Gibt die lauschende IP-Adresse in Oktettform an (z.B. "192.168.1.1").

</dd> <dt>

*Port* \[ In\]
</dt> <dd>

Gibt die Nummer des Lauschenports an.

</dd> <dt>

*OverrideExisting* \[ In\]
</dt> <dd>

Gibt an, ob die vorhandene IP-/Portbindung für HTTP überschrieben werden soll. Dieser Parameter wird nur verwendet, wenn der *TransportType-Parameter* 0 (RPC über HTTP) oder 1 (HTTP) enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





