---
title: ActiveBasicDevice SetCachedBitrateMeasurement-Methode (PlayToDevice.h)
description: Legt die zwischengespeicherte Bitrate fest.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- SetCachedBitrateMeasurement-Methode– Medienstreaming-API
- SetCachedBitrateMeasurement-Methode Media Streaming-API, ActiveBasicDevice-Schnittstelle
- Media Streaming-API der ActiveBasicDevice-Schnittstelle, SetCachedBitrateMeasurement-Methode
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
ms.openlocfilehash: adf79b7e9066aacfcce1f82c998463d6d620f5061fef4af788104a0c01a44ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952770"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a>ActiveBasicDevice::SetCachedBitrateMeasurement-Methode

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

*physicalNetworkInterface* \[ In\]
</dt> <dd>

Gibt die physische Netzwerkschnittstelle an.

</dd> <dt>

*Bitrate* \[ In\]
</dt> <dd>

Der Wert, auf den die Bitrate festgelegt werden soll.

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

 

