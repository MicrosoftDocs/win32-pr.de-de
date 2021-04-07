---
description: 'Remotable-Version der imfworkqueueservices:: endregisterplatformworkqueuewithmmcss-Methode.'
ms.assetid: cb15129e-a3ad-4351-a7d6-dd4b883437bd
title: Remoteendregisterplatformworkqueuewithmmcss (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673281a8ed4e4c4174ecd2d874e7032776ea44c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749200"
---
# <a name="remoteendregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="0d9ee-103">Remoteendregisterplatformworkqueuewithmmcss</span><span class="sxs-lookup"><span data-stu-id="0d9ee-103">RemoteEndRegisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="0d9ee-104">Remotable-Version der [**imfworkqueueservices:: endregisterplatformworkqueuewithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0d9ee-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndRegisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult,
    DWORD *pdwTaskId
);
```

## <a name="remarks"></a><span data-ttu-id="0d9ee-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d9ee-105">Remarks</span></span>

<span data-ttu-id="0d9ee-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="0d9ee-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="0d9ee-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0d9ee-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="0d9ee-108">Wenn [**endregisterplatformworkqueuewithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="0d9ee-108">If [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d9ee-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d9ee-109">Requirements</span></span>



| <span data-ttu-id="0d9ee-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d9ee-110">Requirement</span></span> | <span data-ttu-id="0d9ee-111">Wert</span><span class="sxs-lookup"><span data-stu-id="0d9ee-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9ee-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d9ee-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0d9ee-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d9ee-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0d9ee-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d9ee-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0d9ee-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d9ee-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0d9ee-116">Header</span><span class="sxs-lookup"><span data-stu-id="0d9ee-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d9ee-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d9ee-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="0d9ee-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0d9ee-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d9ee-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d9ee-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="0d9ee-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d9ee-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d9ee-121">**IMF workqueueservices**</span><span class="sxs-lookup"><span data-stu-id="0d9ee-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




