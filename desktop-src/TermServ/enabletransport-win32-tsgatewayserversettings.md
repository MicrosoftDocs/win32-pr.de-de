---
title: Enabletransport-Methode der Win32_TSGatewayServerSettings-Klasse
description: Aktiviert oder deaktiviert den angegebenen Transport.
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- Enabletransport-Methode Remotedesktopdienste
- Enabletransport-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, enabletransport-Methode
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
ms.openlocfilehash: 4a14e7ee94eb02e1358d66b9965ecc2323d5b773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342676"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a>Enabletransport-Methode der Win32-Klasse "t- \_ gatewayserversettings"

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

*TransportType* \[ in\]
</dt> <dd>

Gibt den Transporttyp an. Dabei muss es sich um einen der folgenden Werte handeln:

<dt>

0
</dt> <dd>

RPC-über-HTTP-Transport.

</dd> <dt>

1
</dt> <dd>

HTTP-Transport.

</dd> <dt>

2
</dt> <dd>

UDP-Transport.

</dd> </dl> </dd> <dt>

*Aktivieren* \[ von in\]
</dt> <dd>

Gibt an, ob der Transport aktiviert oder deaktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Datei- \_ gatewayserversettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





