---
title: Die Methode "stipandport" der Win32_TSGatewayServerSettings-Klasse
description: Legt die Abhör-IP-Adresse und die Portnummer für den angegebenen Transport fest.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Remotedesktopdienste der Methode "" der Klasse "Win32_TSGatewayServerSettings"
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, Methode "".
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
ms.openlocfilehash: 88870cce628a94ca34b38ccf315edc87a1a734b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517687"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Die Methode "stipandport" der Win32-Klasse "- \_ gatewayserversettings"

Legt die Abhör-IP-Adresse und die Portnummer für den angegebenen Transport fest.

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

*IPAddress* \[ in\]
</dt> <dd>

Gibt die Abhör-IP-Adresse im Oktett-Format an (z. b. "192.168.1.1").

</dd> <dt>

*Port* \[ in\]
</dt> <dd>

Gibt die Abhör Portnummer an.

</dd> <dt>

*Überschrieben* \[ in\]
</dt> <dd>

Gibt an, ob die vorhandene IP/Port-Bindung für http überschrieben werden soll. Dieser Parameter wird nur verwendet, wenn der *Transport Type* -Parameter 0 (RPC über HTTP) oder 1 (http) enthält.

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

 

 





