---
description: 'Remotable-Version der imfmediasource:: foratepresentationdescriptor-Methode.'
ms.assetid: 9ad6793e-32ca-471b-8639-41098b3e8216
title: Remotekreatepresentationdescriptor (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c02d78c1febe8c1a82ae3e91c50e06c750bcfef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130481"
---
# <a name="remotecreatepresentationdescriptor"></a><span data-ttu-id="9ff10-103">Remotekreatepresentationdescriptor</span><span class="sxs-lookup"><span data-stu-id="9ff10-103">RemoteCreatePresentationDescriptor</span></span>

<span data-ttu-id="9ff10-104">Remotable-Version der [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9ff10-104">Remotable version of the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>

``` syntax
[call_as(CreatePresentationDescriptor)]
HRESULT RemoteCreatePresentationDescriptor(
    DWORD *pcbPD,
    BYTE **pbPD,
    IMFPresentationDescriptor **ppRemotePD
);
```

## <a name="remarks"></a><span data-ttu-id="9ff10-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ff10-105">Remarks</span></span>

<span data-ttu-id="9ff10-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="9ff10-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="9ff10-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ff10-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="9ff10-108">Wenn " [**kreatepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) " über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="9ff10-108">If [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff10-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ff10-109">Requirements</span></span>



| <span data-ttu-id="9ff10-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ff10-110">Requirement</span></span> | <span data-ttu-id="9ff10-111">Wert</span><span class="sxs-lookup"><span data-stu-id="9ff10-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff10-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ff10-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff10-113">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9ff10-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="9ff10-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ff10-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff10-115">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9ff10-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="9ff10-116">Header</span><span class="sxs-lookup"><span data-stu-id="9ff10-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff10-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ff10-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="9ff10-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9ff10-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ff10-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ff10-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="9ff10-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ff10-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff10-121">**Imfmediasource**</span><span class="sxs-lookup"><span data-stu-id="9ff10-121">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




