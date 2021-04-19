---
title: Activebasicdevice setcachedsinkprotocolinfo-Methode (playtodevice. h)
description: Ruft die zwischengespeicherten senkenprotokollinformationen für das Gerät ab. | Activebasicdevice setcachedsinkprotocolinfo-Methode (playtodevice. h)
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- Setcachedsinkprotocolinfo-Methode Medien Streaming-API
- Setcachedsinkprotocolinfo-Methode Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, setcachedsink protocolinfo-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9100cb8faeb685a0cc7a8b7b73deb11afca29a3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366431"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a>Activebasicdevice:: setcachedsink protocolinfo-Methode

Ruft die zwischengespeicherten senkenprotokollinformationen für das Gerät ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCachedSinkProtocolInfo(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*physicalnetworkinterface* \[ in\]
</dt> <dd>

Gibt die physische Netzwerkschnittstelle an.

</dd> <dt>

*Bitrate* \[ in\]
</dt> <dd>

Der Bitrate-Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Playondevice. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Playto Device. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

