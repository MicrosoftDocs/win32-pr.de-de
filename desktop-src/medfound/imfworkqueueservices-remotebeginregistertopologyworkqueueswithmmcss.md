---
description: 'Remotable-Version der imfworkqueueservices:: beginregistertopologyworkqueueswithmmcss-Methode.'
ms.assetid: 1ea258c9-1f7f-4324-a17a-d044a4864ea4
title: Remotebeginregistertopologyworkqueueswithmmcss (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448008c29e34574263f04ebbc7dee54d60b6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357003"
---
# <a name="remotebeginregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="1e6d0-103">Remotebeginregistertopologyworkqueueswithmmcss</span><span class="sxs-lookup"><span data-stu-id="1e6d0-103">RemoteBeginRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="1e6d0-104">Remotable-Version der [**imfworkqueueservices:: beginregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1e6d0-104">Remotable version of the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(BeginRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginRegisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
); 
```

## <a name="remarks"></a><span data-ttu-id="1e6d0-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e6d0-105">Remarks</span></span>

<span data-ttu-id="1e6d0-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="1e6d0-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="1e6d0-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e6d0-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="1e6d0-108">Wenn [**beginregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="1e6d0-108">If [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e6d0-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e6d0-109">Requirements</span></span>



| <span data-ttu-id="1e6d0-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e6d0-110">Requirement</span></span> | <span data-ttu-id="1e6d0-111">Wert</span><span class="sxs-lookup"><span data-stu-id="1e6d0-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e6d0-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e6d0-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1e6d0-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e6d0-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1e6d0-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e6d0-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1e6d0-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e6d0-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1e6d0-116">Header</span><span class="sxs-lookup"><span data-stu-id="1e6d0-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e6d0-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e6d0-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="1e6d0-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e6d0-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e6d0-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e6d0-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="1e6d0-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e6d0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e6d0-121">**IMF workqueueservices**</span><span class="sxs-lookup"><span data-stu-id="1e6d0-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




