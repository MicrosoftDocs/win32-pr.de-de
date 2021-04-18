---
description: 'Remotable-Version der imfworkqueueservices:: endunregistertopologyworkqueueswithmmcss-Methode.'
ms.assetid: 8767a145-07b9-4427-9446-cee25e9074fa
title: Remoteendunregistertopologyworkqueueswithmmcss (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1131fcd920e306bc6d5f2954c283d41d61310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347657"
---
# <a name="remoteendunregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="67cc2-103">Remoteendunregistertopologyworkqueueswithmmcss</span><span class="sxs-lookup"><span data-stu-id="67cc2-103">RemoteEndUnregisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="67cc2-104">Remotable-Version der [**imfworkqueueservices:: endunregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) -Methode.</span><span class="sxs-lookup"><span data-stu-id="67cc2-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndUnregisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="67cc2-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67cc2-105">Remarks</span></span>

<span data-ttu-id="67cc2-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="67cc2-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="67cc2-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="67cc2-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="67cc2-108">Wenn [**endunregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="67cc2-108">If [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="67cc2-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67cc2-109">Requirements</span></span>



| <span data-ttu-id="67cc2-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67cc2-110">Requirement</span></span> | <span data-ttu-id="67cc2-111">Wert</span><span class="sxs-lookup"><span data-stu-id="67cc2-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67cc2-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67cc2-112">Minimum supported client</span></span><br/> | <span data-ttu-id="67cc2-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67cc2-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="67cc2-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67cc2-114">Minimum supported server</span></span><br/> | <span data-ttu-id="67cc2-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67cc2-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="67cc2-116">Header</span><span class="sxs-lookup"><span data-stu-id="67cc2-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="67cc2-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67cc2-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="67cc2-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="67cc2-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="67cc2-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67cc2-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="67cc2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67cc2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67cc2-121">**IMF workqueueservices**</span><span class="sxs-lookup"><span data-stu-id="67cc2-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




