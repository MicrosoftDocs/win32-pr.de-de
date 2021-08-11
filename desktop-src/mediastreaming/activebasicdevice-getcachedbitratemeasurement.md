---
title: ActiveBasicDevice GetCachedBitrateMeasurement-Methode (PlayToDevice.h)
description: Ruft die zwischengespeicherte Bitrate ab.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- GetCachedBitrateMeasurement-Methode– Medienstreaming-API
- GetCachedBitrateMeasurement-Methode Media Streaming-API, ActiveBasicDevice-Schnittstelle
- Media Streaming-API der ActiveBasicDevice-Schnittstelle, GetCachedBitrateMeasurement-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 031d77595298651be11c793f8fd96471808ab1aef3f5a2b6398be9c1ff10de02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236865"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a>ActiveBasicDevice::GetCachedBitrateMeasurement-Methode

Ruft die zwischengespeicherte Bitrate ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*physicalNetworkInterface* \[ In\]
</dt> <dd>

Gibt die physische Netzwerkschnittstelle an.

</dd> <dt>

*Bitrate* \[ out, retval\]
</dt> <dd>

Empfängt den Bitratewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

