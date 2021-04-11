---
description: 'Remotable-Version von imfworkqueueservicesex:: BeginRegisterPlatformWorkQueueWithMMCSSEx.'
ms.assetid: 75af7ce6-9b74-4d61-b7f2-5d07538f91cf
title: RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d519d13f1e23927f1d34a18d5c5f860e007881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218121"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcssex"></a><span data-ttu-id="6bb37-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span><span class="sxs-lookup"><span data-stu-id="6bb37-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span></span>

<span data-ttu-id="6bb37-104">Remotable-Version von [**imfworkqueueservicesex:: BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).</span><span class="sxs-lookup"><span data-stu-id="6bb37-104">Remotable version of [**IMFWorkQueueServicesEX::BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).</span></span>

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSSEx)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId, 
    LONG lPriority,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="6bb37-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bb37-105">Remarks</span></span>

<span data-ttu-id="6bb37-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="6bb37-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="6bb37-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6bb37-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="6bb37-108">Wenn [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="6bb37-108">If [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb37-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bb37-109">Requirements</span></span>



| <span data-ttu-id="6bb37-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6bb37-110">Requirement</span></span> | <span data-ttu-id="6bb37-111">Wert</span><span class="sxs-lookup"><span data-stu-id="6bb37-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb37-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6bb37-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb37-113">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bb37-113">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6bb37-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6bb37-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb37-115">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bb37-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6bb37-116">Header</span><span class="sxs-lookup"><span data-stu-id="6bb37-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bb37-117"><dt>MFI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6bb37-117"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb37-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bb37-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb37-119">**IMF workqueueservicesex**</span><span class="sxs-lookup"><span data-stu-id="6bb37-119">**IMFWorkQueueServicesEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
</dt> </dl>

 

 




