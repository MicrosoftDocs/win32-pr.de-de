---
title: ActiveBasicDevice GetEffectiveBandwidth-Methode (PlayToDevice.h)
description: Ruft die aktuelle effektive Bandbreite für das Gerät ab.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- 'GetEffectiveBandwidth-Methode: Medienstreaming-API'
- 'GetEffectiveBandwidth-Methode: Medienstreaming-API, ActiveBasicDevice-Schnittstelle'
- Media Streaming-API der ActiveBasicDevice-Schnittstelle, GetEffectiveBandwidth-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac51318997e80c043e36dc87b052a5e21bf9933f93e34f2e5071fb20d4bb75b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236782"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a>ActiveBasicDevice::GetEffectiveBandwidth-Methode

Ruft die aktuelle effektive Bandbreite für das Gerät ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*transmitSpeed* \[ in, retval\]
</dt> <dd>

Gibt an, ob die Übertragungsgeschwindigkeit abgerufen oder die Empfangsgeschwindigkeit abgerufen wird.

**TRUE,** um die Übertragungsgeschwindigkeit abzurufen. **FALSE,** um die Empfangsgeschwindigkeit abzurufen.

</dd> <dt>

*currentSpeed* \[ out\]
</dt> <dd>

Empfängt die aktuelle effektive Bandbreite.

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

 

