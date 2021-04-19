---
description: 'Remotable-Version der imfworkqueueservices:: beginunregisterplatformworkqueuewithmmcss-Methode.'
ms.assetid: c3117086-268e-4e52-acfb-2c8167adaa07
title: Remotebeginunregisterplatformworkqueuewithmmcss (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab364f041d6bc8d0f6275879c82a937e98f463b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355420"
---
# <a name="remotebeginunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="b4116-103">Remotebeginunregisterplatformworkqueuewithmmcss</span><span class="sxs-lookup"><span data-stu-id="b4116-103">RemoteBeginUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="b4116-104">Remotable-Version der [**imfworkqueueservices:: beginunregisterplatformworkqueuewithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b4116-104">Remotable version of the [**IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(BeginUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginUnregisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="b4116-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4116-105">Remarks</span></span>

<span data-ttu-id="b4116-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="b4116-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="b4116-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b4116-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="b4116-108">Wenn [**beginunregisterplatformworkqueuewithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="b4116-108">If [**BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4116-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4116-109">Requirements</span></span>



| <span data-ttu-id="b4116-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4116-110">Requirement</span></span> | <span data-ttu-id="b4116-111">Wert</span><span class="sxs-lookup"><span data-stu-id="b4116-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4116-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4116-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b4116-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4116-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b4116-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4116-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b4116-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4116-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b4116-116">Header</span><span class="sxs-lookup"><span data-stu-id="b4116-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4116-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4116-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="b4116-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4116-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4116-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4116-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="b4116-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4116-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4116-121">**IMF workqueueservices**</span><span class="sxs-lookup"><span data-stu-id="b4116-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




