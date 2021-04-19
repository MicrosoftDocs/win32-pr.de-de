---
title: Devicecontroller. cacheddevices-Methode
description: Ruft eine Auflistung von ibasicdevice-Schnittstellen Zeigern ab, die die zwischengespeicherte Ansicht aller ermittelbaren DLNA-Geräte darstellt. | Devicecontroller. cacheddevices-Methode
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- Cacheddevices-Methode Medien Streaming-API
- Cacheddevices-Methode Medien Streaming-API, devicecontroller-Schnittstelle
- Devicecontroller-Schnittstelle Medien Streaming-API, cacheddevices-Methode
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0bb39e03a9788e0c444f682b61d39fc1c65781b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350627"
---
# <a name="devicecontrollercacheddevices-method"></a>Devicecontroller. cacheddevices-Methode

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

[**Geräte-econtroller**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))
</dt> </dl>

 

