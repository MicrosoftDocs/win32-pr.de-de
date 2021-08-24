---
title: IBasicDevice CanWakeDevices-Methode
description: Ruft einen Wert ab, der angibt, ob das Gerät reaktiviert werden kann.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- Media Streaming-API der CanWakeDevices-Methode
- CanWakeDevices-Methode Media Streaming API , IBasicDevice-Schnittstelle
- IBasicDevice-Schnittstelle Medienstreaming-API , CanWakeDevices-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ebd0cfe9bf773d78297454d4a7643a74c3d6ea23aea01eeb54cd5c014ce73e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847670"
---
# <a name="ibasicdevicecanwakedevices-method"></a>IBasicDevice::CanWakeDevices-Methode

Ruft einen Wert ab, der angibt, ob das Gerät reaktiviert werden kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf einen booleschen Wert, der **True** ist, wenn das Gerät reaktiviert werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





