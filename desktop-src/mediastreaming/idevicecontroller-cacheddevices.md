---
title: Idevicecontroller-cacheddevices-Methode
description: Ruft eine Auflistung von ibasicdevice-Schnittstellen Zeigern ab, die die zwischengespeicherte Ansicht aller ermittelbaren DLNA-Geräte darstellt. | Idevicecontroller-cacheddevices-Methode
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- Cacheddevices-Methode Medien Streaming-API
- Cacheddevices-Methode Medien Streaming-API, idevicecontroller-Schnittstelle
- Idevicecontroller-Schnittstelle Medien Streaming-API, cacheddevices-Methode
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961520"
---
# <a name="idevicecontrollercacheddevices-method"></a>Idevicecontroller:: cacheddevices-Methode

Ruft eine Auflistung von [**ibasicdevice**](ibasicdevice.md) -Schnittstellen Zeigern ab, die die zwischengespeicherte Ansicht aller ermittelbaren DLNA-Geräte darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Empfängt eine Aufzähl Bare Auflistung von [**ibasicdevice**](ibasicdevice.md) -Schnittstellen Zeigern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idevicecontroller**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

