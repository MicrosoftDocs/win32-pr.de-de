---
description: 'Remotable-Version der imfworkqueueservices:: endregistertopologyworkqueueswithmmcss-Methode.'
ms.assetid: 94dce412-6a72-4ddf-86a3-5176ee1eb6d2
title: Remoteendregistertopologyworkqueueswithmmcss (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3333becfcd7a3c5e2621b628b6435b96af017cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369847"
---
# <a name="remoteendregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="66966-103">Remoteendregistertopologyworkqueueswithmmcss</span><span class="sxs-lookup"><span data-stu-id="66966-103">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="66966-104">Remotable-Version der [**imfworkqueueservices:: endregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) -Methode.</span><span class="sxs-lookup"><span data-stu-id="66966-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndRegisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="66966-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66966-105">Remarks</span></span>

<span data-ttu-id="66966-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="66966-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="66966-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="66966-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="66966-108">Wenn [**endregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="66966-108">If [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="66966-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66966-109">Requirements</span></span>



| <span data-ttu-id="66966-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66966-110">Requirement</span></span> | <span data-ttu-id="66966-111">Wert</span><span class="sxs-lookup"><span data-stu-id="66966-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66966-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66966-112">Minimum supported client</span></span><br/> | <span data-ttu-id="66966-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66966-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="66966-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66966-114">Minimum supported server</span></span><br/> | <span data-ttu-id="66966-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66966-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="66966-116">Header</span><span class="sxs-lookup"><span data-stu-id="66966-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="66966-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66966-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="66966-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="66966-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="66966-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66966-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="66966-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66966-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66966-121">**IMF workqueueservices**</span><span class="sxs-lookup"><span data-stu-id="66966-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




