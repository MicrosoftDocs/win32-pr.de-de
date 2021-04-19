---
title: Deviceabflug-Ereignis
description: Tritt auf, wenn ein neues Gerät aus der Liste der Geräte entfernt wird, die von der cacheddevices-Methode zurückgegeben werden.
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- Devicedeparture-Ereignis Medien-Streaming-API
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e225afcbe8b373b22584eaa3d9fcb09e1eff29c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341931"
---
# <a name="devicedeparture-event"></a>Deviceabflug-Ereignis

Tritt auf, wenn ein neues Gerät aus der Liste der Geräte entfernt wird, die von der [**cacheddevices**](idevicecontroller-cacheddevices.md) -Methode zurückgegeben werden.

## <a name="syntax"></a>Syntax


```C++
void DeviceDeparture();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um Benachrichtigungen von diesem Ereignis zu behandeln, registrieren Sie eine [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) -Ereignishandlerfunktion mithilfe der [**Add \_ devicedeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) -Methode. Um die Registrierung des Ereignis Handlers aufzuheben, verwenden Sie die [**Remove \_ devicedeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) -Methode.

 

 