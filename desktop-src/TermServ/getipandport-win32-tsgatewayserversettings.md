---
title: Getipandport-Methode der Win32_TSGatewayServerSettings-Klasse
description: Ruft die Abhör-IP-Adresse und die Portnummer für den angegebenen Transport ab.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- Getipandport-Methode Remotedesktopdienste
- Getipandport-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, getipandport-Methode
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
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340458"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Getipandport-Methode der Win32-Klasse "t- \_ gatewayserversettings"

Ruft die Abhör-IP-Adresse und die Portnummer für den angegebenen Transport ab.

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

*IPAddress* \[ vorgenommen\]
</dt> <dd>

Eine Zeichenfolge, die die Abhör-IP-Adresse im Oktett-Format empfängt (z. b. "192.168.1.1").

</dd> <dt>

*Port* \[ vorgenommen\]
</dt> <dd>

Gibt die Abhör Portnummer an.

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

 

 





