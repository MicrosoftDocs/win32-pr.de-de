---
description: 'Remotable-Version der imftopologynode:: getoutputpreftype-Methode.'
ms.assetid: 56fbbf14-0c55-4f98-bcda-7f434cff803c
title: Remotegetoutputpreftype (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46069add8f9d15a2b3742a083a1cf169a46b969f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359908"
---
# <a name="remotegetoutputpreftype"></a><span data-ttu-id="c9be4-103">Remotegetoutputpreftype</span><span class="sxs-lookup"><span data-stu-id="c9be4-103">RemoteGetOutputPrefType</span></span>

<span data-ttu-id="c9be4-104">Remotable-Version der [**imftopologynode:: getoutputpreftype**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c9be4-104">Remotable version of the [**IMFTopologyNode::GetOutputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) method.</span></span>

``` syntax
[call_as(GetOutputPrefType)] 
HRESULT RemoteGetOutputPrefType(
    DWORD dwOutputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a><span data-ttu-id="c9be4-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9be4-105">Remarks</span></span>

<span data-ttu-id="c9be4-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="c9be4-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="c9be4-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9be4-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="c9be4-108">Wenn **getoutputpreftype** über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="c9be4-108">If **GetOutputPrefType** is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9be4-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9be4-109">Requirements</span></span>



| <span data-ttu-id="c9be4-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9be4-110">Requirement</span></span> | <span data-ttu-id="c9be4-111">Wert</span><span class="sxs-lookup"><span data-stu-id="c9be4-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9be4-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9be4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c9be4-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9be4-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c9be4-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9be4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c9be4-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9be4-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c9be4-116">Header</span><span class="sxs-lookup"><span data-stu-id="c9be4-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9be4-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9be4-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="c9be4-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c9be4-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9be4-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9be4-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="c9be4-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9be4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9be4-121">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="c9be4-121">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




