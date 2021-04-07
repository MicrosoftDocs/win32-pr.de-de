---
description: 'Remotable-Version der imfmediaeventgenerator:: begingetevent-Methode.'
ms.assetid: 96a16fd3-10bc-4cd9-967a-ceb92e26ccc8
title: Remotebegingetevent (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d728653df99baf0e816c53d8d22d7720c9aefac9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863416"
---
# <a name="remotebegingetevent"></a><span data-ttu-id="6da7b-103">Remotebegingetevent</span><span class="sxs-lookup"><span data-stu-id="6da7b-103">RemoteBeginGetEvent</span></span>

<span data-ttu-id="6da7b-104">Remotable-Version der [**imfmediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6da7b-104">Remotable version of the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method.</span></span>

``` syntax
[call_as(BeginGetEvent)]
HRESULT RemoteBeginGetEvent(
    IMFRemoteAsyncCallback* pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="6da7b-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6da7b-105">Remarks</span></span>

<span data-ttu-id="6da7b-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="6da7b-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="6da7b-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6da7b-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="6da7b-108">Wenn [**begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="6da7b-108">If [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="6da7b-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6da7b-109">Requirements</span></span>



| <span data-ttu-id="6da7b-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6da7b-110">Requirement</span></span> | <span data-ttu-id="6da7b-111">Wert</span><span class="sxs-lookup"><span data-stu-id="6da7b-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6da7b-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6da7b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6da7b-113">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6da7b-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="6da7b-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6da7b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6da7b-115">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6da7b-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="6da7b-116">Header</span><span class="sxs-lookup"><span data-stu-id="6da7b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="6da7b-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6da7b-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="6da7b-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6da7b-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="6da7b-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6da7b-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6da7b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6da7b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da7b-121">**IMF Media Event Generator**</span><span class="sxs-lookup"><span data-stu-id="6da7b-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




