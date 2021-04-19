---
description: 'Remotable-Version der imfmediatypeer Handler:: getcurrentmediatype-Methode.'
ms.assetid: f7f69adb-2a4a-47a9-bb92-ad9d005b962f
title: Remotegetcurrentmediatype (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc168198e8402d83538c046967d1d851ae2532b1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106349762"
---
# <a name="remotegetcurrentmediatype"></a><span data-ttu-id="21eea-103">Remotegetcurrentmediatype</span><span class="sxs-lookup"><span data-stu-id="21eea-103">RemoteGetCurrentMediaType</span></span>

<span data-ttu-id="21eea-104">Remotable-Version der [**imfmediatypeer Handler:: getcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) -Methode.</span><span class="sxs-lookup"><span data-stu-id="21eea-104">Remotable version of the [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) method.</span></span>

``` syntax
[call_as(GetCurrentMediaType)]
HRESULT RemoteGetCurrentMediaType(
    BYTE **ppbData,
    DWORD *pcbData
);
```

## <a name="remarks"></a><span data-ttu-id="21eea-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21eea-105">Remarks</span></span>

<span data-ttu-id="21eea-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="21eea-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="21eea-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="21eea-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="21eea-108">Wenn [**getcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="21eea-108">If [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

<span data-ttu-id="21eea-109">Diese Schnittstelle ist auf den folgenden Plattformen verfügbar, wenn die weitervertreibbaren Komponenten für das Windows Media-Format 11 SDK installiert sind:</span><span class="sxs-lookup"><span data-stu-id="21eea-109">This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:</span></span>

-   <span data-ttu-id="21eea-110">Windows XP mit Service Pack 2 (SP2) und höher.</span><span class="sxs-lookup"><span data-stu-id="21eea-110">Windows XP with Service Pack 2 (SP2) and later.</span></span>
-   <span data-ttu-id="21eea-111">Windows XP Media Center Edition 2005 mit KB900325 (Windows XP Media Center Edition 2005) und KB925766 (Oktober 2006 Updaterollup für Windows XP Media Center Edition) ist installiert.</span><span class="sxs-lookup"><span data-stu-id="21eea-111">Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="21eea-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21eea-112">Requirements</span></span>



| <span data-ttu-id="21eea-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21eea-113">Requirement</span></span> | <span data-ttu-id="21eea-114">Wert</span><span class="sxs-lookup"><span data-stu-id="21eea-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21eea-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21eea-115">Minimum supported client</span></span><br/> | <span data-ttu-id="21eea-116">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="21eea-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="21eea-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21eea-117">Minimum supported server</span></span><br/> | <span data-ttu-id="21eea-118">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="21eea-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="21eea-119">Header</span><span class="sxs-lookup"><span data-stu-id="21eea-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="21eea-120"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21eea-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="21eea-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="21eea-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="21eea-122"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21eea-122"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="21eea-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21eea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21eea-124">**IMF mediatypeer Handler**</span><span class="sxs-lookup"><span data-stu-id="21eea-124">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
</dt> </dl>

 

 




