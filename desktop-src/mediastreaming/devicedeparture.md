---
title: DeviceDeparture-Ereignis
description: Tritt ein, wenn ein neues Gerät aus der Liste der Geräte entfernt wird, die von der CachedDevices-Methode zurückgegeben werden.
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- Media Streaming-API für DeviceDeparture-Ereignisse
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496fa0fcae3cba51228b37b5f06eb9b06c416322aad22f77be542274088eae32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712950"
---
# <a name="devicedeparture-event"></a>DeviceDeparture-Ereignis

Tritt ein, wenn ein neues Gerät aus der Liste der Geräte entfernt wird, die von der [**CachedDevices-Methode zurückgegeben**](idevicecontroller-cacheddevices.md) werden.

## <a name="syntax"></a>Syntax


```C++
void DeviceDeparture();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um Benachrichtigungen von diesem Ereignis zu verarbeiten, registrieren Sie eine [**DeviceControllerHandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) mithilfe der [**\_ add DeviceDeparture-Methode.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) Verwenden Sie zum Aufheben der Registrierung des Ereignishandlers [**die \_ Remove DeviceDeparture-Methode.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture)

 

 