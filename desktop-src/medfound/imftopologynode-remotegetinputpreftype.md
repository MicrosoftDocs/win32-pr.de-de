---
description: 'Remotable-Version der imftopologynode:: getinputpreftype-Methode.'
ms.assetid: b02cf739-97a9-4bb0-abb1-0da491857c50
title: Remotegetinputpreftype (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6461e804d6066b467378742ff02c8e708f5f6714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752888"
---
# <a name="remotegetinputpreftype"></a><span data-ttu-id="988f6-103">Remotegetinputpreftype</span><span class="sxs-lookup"><span data-stu-id="988f6-103">RemoteGetInputPrefType</span></span>

<span data-ttu-id="988f6-104">Remotable-Version der [**imftopologynode:: getinputpreftype**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) -Methode.</span><span class="sxs-lookup"><span data-stu-id="988f6-104">Remotable version of the [**IMFTopologyNode::GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) method.</span></span>

``` syntax
[call_as(GetInputPrefType)] 
HRESULT RemoteGetInputPrefType(
    DWORD dwInputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a><span data-ttu-id="988f6-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="988f6-105">Remarks</span></span>

<span data-ttu-id="988f6-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="988f6-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="988f6-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="988f6-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="988f6-108">Wenn [**getinputpreftype**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="988f6-108">If [**GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="988f6-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="988f6-109">Requirements</span></span>



| <span data-ttu-id="988f6-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="988f6-110">Requirement</span></span> | <span data-ttu-id="988f6-111">Wert</span><span class="sxs-lookup"><span data-stu-id="988f6-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="988f6-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="988f6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="988f6-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="988f6-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="988f6-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="988f6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="988f6-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="988f6-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="988f6-116">Header</span><span class="sxs-lookup"><span data-stu-id="988f6-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="988f6-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="988f6-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="988f6-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="988f6-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="988f6-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="988f6-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="988f6-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="988f6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="988f6-121">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="988f6-121">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




