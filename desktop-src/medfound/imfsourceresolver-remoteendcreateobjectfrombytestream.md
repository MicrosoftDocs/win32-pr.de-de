---
description: 'Remotable-Version der imfsourceresolver:: endkreateobjectfromb-Methode.'
ms.assetid: 6e4e9ace-e18a-45df-b20c-28e352fcdee7
title: Remoteendkreateobjectfromb testream (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba53b7d22ed79cb97edba034dc4c61d9aa27fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130149"
---
# <a name="remoteendcreateobjectfrombytestream"></a><span data-ttu-id="3d39f-103">Remoteendkreateobjectfromb testream</span><span class="sxs-lookup"><span data-stu-id="3d39f-103">RemoteEndCreateObjectFromByteStream</span></span>

<span data-ttu-id="3d39f-104">Remotable-Version der [**imfsourceresolver:: endkreateobjectfromb**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3d39f-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromByteStream)]
HRESULT RemoteEndCreateObjectFromByteStream(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="3d39f-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d39f-105">Remarks</span></span>

<span data-ttu-id="3d39f-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="3d39f-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="3d39f-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d39f-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="3d39f-108">Wenn [**endkreateobjectfromb-testream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="3d39f-108">If [**EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d39f-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d39f-109">Requirements</span></span>



| <span data-ttu-id="3d39f-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d39f-110">Requirement</span></span> | <span data-ttu-id="3d39f-111">Wert</span><span class="sxs-lookup"><span data-stu-id="3d39f-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d39f-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d39f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3d39f-113">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="3d39f-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="3d39f-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d39f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3d39f-115">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="3d39f-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="3d39f-116">Header</span><span class="sxs-lookup"><span data-stu-id="3d39f-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d39f-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d39f-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="3d39f-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3d39f-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d39f-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d39f-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="3d39f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d39f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d39f-121">**IMF sourceresolver**</span><span class="sxs-lookup"><span data-stu-id="3d39f-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




