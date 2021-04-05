---
description: 'Remotable-Version der imfmediaeventgenerator:: endgetevent-Methode.'
ms.assetid: 5b793760-546c-43d4-8251-d89d8d7152ad
title: Remoteendgetevent (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3c4a5fe87dddf5fc1d256d61d8c863c2f1d9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753881"
---
# <a name="remoteendgetevent"></a><span data-ttu-id="b4051-103">Remoteendgetevent</span><span class="sxs-lookup"><span data-stu-id="b4051-103">RemoteEndGetEvent</span></span>

<span data-ttu-id="b4051-104">Remotable-Version der [**imfmediaeventgenerator:: endgetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b4051-104">Remotable version of the [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) method.</span></span>

``` syntax
[call_as(EndGetEvent)]
HRESULT RemoteEndGetEvent(
    IUnknown *pResult,
    DWORD *pcbEvent,
    BYTE **ppbEvent
);
```

## <a name="remarks"></a><span data-ttu-id="b4051-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4051-105">Remarks</span></span>

<span data-ttu-id="b4051-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="b4051-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="b4051-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b4051-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="b4051-108">Wenn [**endgetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="b4051-108">If [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4051-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4051-109">Requirements</span></span>



| <span data-ttu-id="b4051-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4051-110">Requirement</span></span> | <span data-ttu-id="b4051-111">Wert</span><span class="sxs-lookup"><span data-stu-id="b4051-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4051-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4051-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b4051-113">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b4051-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="b4051-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4051-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b4051-115">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b4051-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="b4051-116">Header</span><span class="sxs-lookup"><span data-stu-id="b4051-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4051-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4051-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="b4051-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4051-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4051-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4051-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="b4051-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4051-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4051-121">**IMF Media Event Generator**</span><span class="sxs-lookup"><span data-stu-id="b4051-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




