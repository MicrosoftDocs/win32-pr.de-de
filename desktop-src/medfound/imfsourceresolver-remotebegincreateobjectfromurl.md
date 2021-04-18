---
description: 'Remotable-Version der imfsourceresolver:: beginkreateobjectfromurl-Methode.'
ms.assetid: 3c0b0aaf-832b-4708-bed9-6f448770ee77
title: Remotebeginkreateobjectfromurl (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9d9a72ab5522b56fc0b78238f6a1dbc9aae0c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357414"
---
# <a name="remotebegincreateobjectfromurl"></a><span data-ttu-id="41613-103">Remotebeginkreateobjectfromurl</span><span class="sxs-lookup"><span data-stu-id="41613-103">RemoteBeginCreateObjectFromURL</span></span>

<span data-ttu-id="41613-104">Remotable-Version der [**imfsourceresolver:: beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) -Methode.</span><span class="sxs-lookup"><span data-stu-id="41613-104">Remotable version of the [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method.</span></span>

``` syntax
[call_as(BeginCreateObjectFromURL)]
HRESULT RemoteBeginCreateObjectFromURL(
    LPCWSTR pwszURL,
    DWORD dwFlags,
    IPropertyStore *pProps,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="41613-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41613-105">Remarks</span></span>

<span data-ttu-id="41613-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="41613-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="41613-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="41613-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="41613-108">Wenn [**beginfroateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="41613-108">If [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="41613-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41613-109">Requirements</span></span>



| <span data-ttu-id="41613-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41613-110">Requirement</span></span> | <span data-ttu-id="41613-111">Wert</span><span class="sxs-lookup"><span data-stu-id="41613-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41613-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41613-112">Minimum supported client</span></span><br/> | <span data-ttu-id="41613-113">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="41613-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="41613-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41613-114">Minimum supported server</span></span><br/> | <span data-ttu-id="41613-115">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="41613-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="41613-116">Header</span><span class="sxs-lookup"><span data-stu-id="41613-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="41613-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41613-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="41613-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="41613-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="41613-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41613-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="41613-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41613-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41613-121">**IMF sourceresolver**</span><span class="sxs-lookup"><span data-stu-id="41613-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




