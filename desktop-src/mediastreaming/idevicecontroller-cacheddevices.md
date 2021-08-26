---
title: IDeviceController CachedDevices-Methode
description: Ruft eine Auflistung von IBasicDevice-Schnittstellenzeige ab, die die zwischengespeicherte Ansicht aller erkennbaren DLNA-Geräte darstellt. | IDeviceController CachedDevices-Methode
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- 'CachedDevices-Methode: Medienstreaming-API'
- CachedDevices-Methode Media Streaming-API, IDeviceController-Schnittstelle
- IDeviceController-Schnittstelle Media Streaming-API, CachedDevices-Methode
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c624597fb88a45cc9ff91770f164e7c6e6e83ff5eb1b6369ded9d0fc1bbc225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952640"
---
# <a name="idevicecontrollercacheddevices-method"></a>IDeviceController::CachedDevices-Methode

Ruft eine Auflistung von [**IBasicDevice-Schnittstellenzeige**](ibasicdevice.md) ab, die die zwischengespeicherte Ansicht aller erkennbaren DLNA-Geräte darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Empfängt eine aufzählbare Auflistung von [**IBasicDevice-Schnittstellenzeigern.**](ibasicdevice.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

