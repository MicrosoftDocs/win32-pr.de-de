---
description: 'Remotable-Version der imfsourceresolver:: endkreateobjectfromurl-Methode.'
ms.assetid: 42764869-9cbc-4f41-a3af-f2d869db9f99
title: Remoteendkreateobjectfromurl (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fff650dca012b58dc6fd46b26f13b1c2ac3c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368141"
---
# <a name="remoteendcreateobjectfromurl"></a><span data-ttu-id="460d1-103">Remoteendkreateobjectfromurl</span><span class="sxs-lookup"><span data-stu-id="460d1-103">RemoteEndCreateObjectFromURL</span></span>

<span data-ttu-id="460d1-104">Remotable-Version der [**imfsourceresolver:: endkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) -Methode.</span><span class="sxs-lookup"><span data-stu-id="460d1-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromURL)]
HRESULT RemoteEndCreateObjectFromURL(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="460d1-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="460d1-105">Remarks</span></span>

<span data-ttu-id="460d1-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="460d1-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="460d1-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="460d1-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="460d1-108">Wenn [**endkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="460d1-108">If [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="460d1-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="460d1-109">Requirements</span></span>



| <span data-ttu-id="460d1-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="460d1-110">Requirement</span></span> | <span data-ttu-id="460d1-111">Wert</span><span class="sxs-lookup"><span data-stu-id="460d1-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="460d1-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="460d1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="460d1-113">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="460d1-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="460d1-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="460d1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="460d1-115">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="460d1-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="460d1-116">Header</span><span class="sxs-lookup"><span data-stu-id="460d1-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="460d1-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="460d1-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="460d1-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="460d1-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="460d1-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="460d1-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="460d1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="460d1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="460d1-121">**IMF sourceresolver**</span><span class="sxs-lookup"><span data-stu-id="460d1-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




