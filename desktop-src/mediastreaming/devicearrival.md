---
title: DeviceAvaval-Ereignis
description: Tritt ein, wenn ein neues Gerät der Liste der Geräte hinzugefügt wird, die von der CachedDevices-Methode zurückgegeben werden.
ms.assetid: C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2
keywords:
- Media Streaming-API für DevicePolicyval-Ereignis
topic_type:
- apiref
api_name:
- DeviceArrival
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed65c2b1c37eb91f9bf0a0c060fb76b85cd1f5b3d06b6ff1ab795ec89a0db6bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721210"
---
# <a name="devicearrival-event"></a>DeviceAvaval-Ereignis

Tritt ein, wenn ein neues Gerät der Liste der Geräte hinzugefügt wird, die von der [**CachedDevices-Methode**](idevicecontroller-cacheddevices.md) zurückgegeben werden.

## <a name="syntax"></a>Syntax


```C++
void DeviceArrival();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um Benachrichtigungen von diesem Ereignis zu behandeln, registrieren Sie eine [**DeviceControllerHandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) mithilfe der [**Add Device \_ Handler-Methode.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) Um die Registrierung des Ereignishandlers aufzuheben, verwenden Sie die [**\_ Remove Device Ausdrückungsmethode.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival)

 

 