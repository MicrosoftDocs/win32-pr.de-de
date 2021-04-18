---
description: 'Remotable-Version der imfmediastream:: requestsample-Methode.'
ms.assetid: 05ed4de0-fe5c-4183-8f1d-55d5a27e436a
title: Remoterequestsample (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c8b06f0501de9cc041bf5776adb5e17e59a8c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357430"
---
# <a name="remoterequestsample"></a><span data-ttu-id="8bc98-103">Remoterequestsample</span><span class="sxs-lookup"><span data-stu-id="8bc98-103">RemoteRequestSample</span></span>

<span data-ttu-id="8bc98-104">Remotable-Version der [**imfmediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8bc98-104">Remotable version of the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

``` syntax
[call_as(RequestSample)]
HRESULT RemoteRequestSample();
```

## <a name="remarks"></a><span data-ttu-id="8bc98-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8bc98-105">Remarks</span></span>

<span data-ttu-id="8bc98-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="8bc98-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="8bc98-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8bc98-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="8bc98-108">Wenn [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="8bc98-108">If [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bc98-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bc98-109">Requirements</span></span>



| <span data-ttu-id="8bc98-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bc98-110">Requirement</span></span> | <span data-ttu-id="8bc98-111">Wert</span><span class="sxs-lookup"><span data-stu-id="8bc98-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bc98-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8bc98-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8bc98-113">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8bc98-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="8bc98-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8bc98-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8bc98-115">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8bc98-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="8bc98-116">Header</span><span class="sxs-lookup"><span data-stu-id="8bc98-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bc98-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8bc98-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="8bc98-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8bc98-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="8bc98-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bc98-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="8bc98-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bc98-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bc98-121">**IMF Media Stream**</span><span class="sxs-lookup"><span data-stu-id="8bc98-121">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)
</dt> </dl>

 

 




