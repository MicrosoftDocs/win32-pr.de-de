---
title: Activebasicdevice geteffectivebandwidth-Methode (playondevice. h)
description: Ruft die aktuelle effektive Bandbreite für das Gerät ab.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- Geteffectivebandwidth-Methode Medien Streaming-API
- Geteffectivebandwidth-Methode Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, geteffectivebandwidth-Methode
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
ms.openlocfilehash: 05a97e9f1dc77040d4f55bc8997e553e0cdc5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040959"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a>Activebasicdevice:: geteffectivebandwidth-Methode

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

*transmitspeed* \[ in, retval\]
</dt> <dd>

Gibt an, ob die Übertragungsgeschwindigkeit abgerufen oder die Empfangs Geschwindigkeit abgerufen wird.

" **true** ", um die Übertragungsgeschwindigkeit abzurufen. **false** zum Abrufen der Empfangs Geschwindigkeit.

</dd> <dt>

*currentspeed* \[ vorgenommen\]
</dt> <dd>

Empfängt die aktuelle effektive Bandbreite.

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

 

