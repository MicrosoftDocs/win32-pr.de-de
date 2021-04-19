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
# <a name="devicedeparture-event"></a><span data-ttu-id="2e2dc-104">Deviceabflug-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2e2dc-104">DeviceDeparture event</span></span>

<span data-ttu-id="2e2dc-105">Tritt auf, wenn ein neues Gerät aus der Liste der Geräte entfernt wird, die von der [**cacheddevices**](idevicecontroller-cacheddevices.md) -Methode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2e2dc-105">Occurs when a new device is removed from the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2dc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e2dc-106">Syntax</span></span>


```C++
void DeviceDeparture();
```



## <a name="parameters"></a><span data-ttu-id="2e2dc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e2dc-107">Parameters</span></span>

<span data-ttu-id="2e2dc-108">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="2e2dc-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e2dc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e2dc-109">Return value</span></span>

<span data-ttu-id="2e2dc-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2e2dc-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e2dc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e2dc-111">Remarks</span></span>

<span data-ttu-id="2e2dc-112">Um Benachrichtigungen von diesem Ereignis zu behandeln, registrieren Sie eine [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) -Ereignishandlerfunktion mithilfe der [**Add \_ devicedeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2e2dc-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) method.</span></span> <span data-ttu-id="2e2dc-113">Um die Registrierung des Ereignis Handlers aufzuheben, verwenden Sie die [**Remove \_ devicedeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2e2dc-113">To unregister the event handler, use the [**remove\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) method.</span></span>

 

 