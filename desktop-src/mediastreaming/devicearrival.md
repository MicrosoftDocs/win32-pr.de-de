---
title: Devicearrival-Ereignis
description: Tritt auf, wenn der Liste der Geräte, die von der cacheddevices-Methode zurückgegeben werden, ein neues Gerät hinzugefügt wird.
ms.assetid: C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2
keywords:
- Devicearrival-Ereignis Medien-Streaming-API
topic_type:
- apiref
api_name:
- DeviceArrival
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79fbdd68ae6c77c6a0f3e7bbd3cf976b5d056987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725393"
---
# <a name="devicearrival-event"></a>Devicearrival-Ereignis

Tritt auf, wenn der Liste der Geräte, die von der [**cacheddevices**](idevicecontroller-cacheddevices.md) -Methode zurückgegeben werden, ein neues Gerät hinzugefügt wird.

## <a name="syntax"></a>Syntax


```C++
void DeviceArrival();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um Benachrichtigungen von diesem Ereignis zu behandeln, registrieren Sie eine [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) -Ereignishandlerfunktion mithilfe der [**Add \_ devicearrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) -Methode. Um die Registrierung des Ereignis Handlers aufzuheben, verwenden Sie die [**Remove \_ devicearrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) -Methode.

 

 