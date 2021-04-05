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
# <a name="devicearrival-event"></a><span data-ttu-id="3aa92-104">Devicearrival-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3aa92-104">DeviceArrival event</span></span>

<span data-ttu-id="3aa92-105">Tritt auf, wenn der Liste der Geräte, die von der [**cacheddevices**](idevicecontroller-cacheddevices.md) -Methode zurückgegeben werden, ein neues Gerät hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="3aa92-105">Occurs when a new device is added to the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa92-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3aa92-106">Syntax</span></span>


```C++
void DeviceArrival();
```



## <a name="parameters"></a><span data-ttu-id="3aa92-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3aa92-107">Parameters</span></span>

<span data-ttu-id="3aa92-108">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="3aa92-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3aa92-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3aa92-109">Return value</span></span>

<span data-ttu-id="3aa92-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3aa92-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aa92-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3aa92-111">Remarks</span></span>

<span data-ttu-id="3aa92-112">Um Benachrichtigungen von diesem Ereignis zu behandeln, registrieren Sie eine [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) -Ereignishandlerfunktion mithilfe der [**Add \_ devicearrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3aa92-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) method.</span></span> <span data-ttu-id="3aa92-113">Um die Registrierung des Ereignis Handlers aufzuheben, verwenden Sie die [**Remove \_ devicearrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3aa92-113">To unregister the event handler, use the [**remove\_DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) method.</span></span>

 

 