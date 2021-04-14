---
title: Activebasicdevice setcachedbitratemeasurement-Methode (playondevice. h)
description: Legt die zwischengespeicherte Bitrate fest.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- Setcachedbitratemeasurement-Methode Medien Streaming-API
- Setcachedbitratemeasurement-Methode Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, setcachedbitratemeasurement-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681776b00eb9d911a4fa75a9d360b39a3d2b8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478975"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a>Activebasicdevice:: setcachedbitratemeasurement-Methode

Legt die zwischengespeicherte Bitrate fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCachedBitrateMeasurement(
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

Der Wert, auf den die Bitrate festgelegt werden soll.

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

 

