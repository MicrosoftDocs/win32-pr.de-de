---
description: 'Remotable-Version der imfworkqueueservices:: endunregisterplatformworkqueuewithmmcss-Methode.'
ms.assetid: 92eef511-0af0-4146-ac81-7dfa4a649016
title: Remoteendunregisterplatformworkqueuewithmmcss (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a03f8cdc1bfdded539c8143c3fa50c6bafb54de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868031"
---
# <a name="remoteendunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="c5e94-103">Remoteendunregisterplatformworkqueuewithmmcss</span><span class="sxs-lookup"><span data-stu-id="c5e94-103">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="c5e94-104">Remotable-Version der [**imfworkqueueservices:: endunregisterplatformworkqueuewithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c5e94-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndUnregisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="c5e94-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5e94-105">Remarks</span></span>

<span data-ttu-id="c5e94-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="c5e94-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="c5e94-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c5e94-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="c5e94-108">Wenn [**endunregisterplatformworkqueuewithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="c5e94-108">If [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e94-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5e94-109">Requirements</span></span>



| <span data-ttu-id="c5e94-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5e94-110">Requirement</span></span> | <span data-ttu-id="c5e94-111">Wert</span><span class="sxs-lookup"><span data-stu-id="c5e94-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e94-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5e94-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e94-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5e94-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c5e94-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5e94-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e94-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5e94-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c5e94-116">Header</span><span class="sxs-lookup"><span data-stu-id="c5e94-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5e94-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5e94-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="c5e94-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c5e94-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="c5e94-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5e94-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="c5e94-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5e94-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e94-121">**IMF workqueueservices**</span><span class="sxs-lookup"><span data-stu-id="c5e94-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




