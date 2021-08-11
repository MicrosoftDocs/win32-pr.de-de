---
title: DeviceController.CachedDevices-Methode
description: Ruft eine Auflistung von IBasicDevice-Schnittstellenzeige ab, die die zwischengespeicherte Ansicht aller erkennbaren DLNA-Geräte darstellt. | DeviceController.CachedDevices-Methode
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- 'CachedDevices-Methode: Medienstreaming-API'
- 'CachedDevices-Methode: Media Streaming-API, DeviceController-Schnittstelle'
- DeviceController-Schnittstelle Medienstreaming-API, CachedDevices-Methode
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86e2c4209649450fb3a8df46cde151a0b9899cd26e58bfc0b35fd7ac6e7d02b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236360"
---
# <a name="devicecontrollercacheddevices-method"></a>DeviceController.CachedDevices-Methode

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

[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))
</dt> </dl>

 

