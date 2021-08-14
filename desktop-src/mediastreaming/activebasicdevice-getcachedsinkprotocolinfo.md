---
title: ActiveBasicDevice GetCachedSinkProtocolInfo-Methode (PlayToDevice.h)
description: Ruft die zwischengespeicherten Senkenprotokollinformationen für das Gerät ab. | ActiveBasicDevice GetCachedSinkProtocolInfo-Methode (PlayToDevice.h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- GetCachedSinkProtocolInfo-Methode Medienstreaming-API
- GetCachedSinkProtocolInfo-Methode Media Streaming-API, ActiveBasicDevice-Schnittstelle
- ActiveBasicDevice-Schnittstelle Medienstreaming-API, GetCachedSinkProtocolInfo-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a9ebda71f59dc4bd887479b5ff9e763844b32985736f8cf224ed4981f04b34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736396"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a>ActiveBasicDevice::GetCachedSinkProtocolInfo-Methode

Ruft die zwischengespeicherten Senkenprotokollinformationen für das Gerät ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Die zwischengespeicherten Senkenprotokollinformationen für das Gerät.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

