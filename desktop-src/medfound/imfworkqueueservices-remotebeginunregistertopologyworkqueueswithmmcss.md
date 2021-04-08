---
description: 'Remotable-Version der imfworkqueueservices:: beginunregistertopologyworkqueueswithmmcss-Methode.'
ms.assetid: 1a168462-400d-46c9-a489-7b861770469f
title: Remotebeginunregistertopologyworkqueueswithmmcss (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f52f82c55d692a2e1d9160c7a619338d82956ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866191"
---
# <a name="remotebeginunregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="8b0ce-103">Remotebeginunregistertopologyworkqueueswithmmcss</span><span class="sxs-lookup"><span data-stu-id="8b0ce-103">RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="8b0ce-104">Remotable-Version der [**imfworkqueueservices:: beginunregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-104">Remotable version of the [**IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(BeginUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="8b0ce-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b0ce-105">Remarks</span></span>

<span data-ttu-id="8b0ce-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="8b0ce-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="8b0ce-108">Wenn [**beginunregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-108">If [**BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b0ce-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b0ce-109">Requirements</span></span>



| <span data-ttu-id="8b0ce-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b0ce-110">Requirement</span></span> | <span data-ttu-id="8b0ce-111">Wert</span><span class="sxs-lookup"><span data-stu-id="8b0ce-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0ce-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b0ce-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8b0ce-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b0ce-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8b0ce-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b0ce-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8b0ce-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b0ce-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8b0ce-116">Header</span><span class="sxs-lookup"><span data-stu-id="8b0ce-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b0ce-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b0ce-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="8b0ce-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8b0ce-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b0ce-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b0ce-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="8b0ce-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b0ce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b0ce-121">**IMF workqueueservices**</span><span class="sxs-lookup"><span data-stu-id="8b0ce-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




