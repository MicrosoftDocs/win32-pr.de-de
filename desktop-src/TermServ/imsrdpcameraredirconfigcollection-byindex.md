---
title: IMsRdpCameraRedirConfigCollection ByIndex-Eigenschaft
description: Gibt ein imsrdpcameraredirconfig-Objekt nach dem Index in der Auflistung zurück.
ms.tgt_platform: multiple
keywords:
- Byindex-Eigenschaft Remotedesktopdienste
- Byindex-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfigcollection-Schnittstelle
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, byindex-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 68c179023e93295ee846da22357d5f8efb75b15c
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106344559"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a><span data-ttu-id="39b54-106">Imsrdpcameraredirconfigcollection:: byindex-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="39b54-106">IMsRdpCameraRedirConfigCollection::ByIndex property</span></span>

<span data-ttu-id="39b54-107">Gibt ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt nach dem Index in der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="39b54-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>

<span data-ttu-id="39b54-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="39b54-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b54-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="39b54-109">Syntax</span></span>

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="39b54-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="39b54-110">Property value</span></span>

<span data-ttu-id="39b54-111">Das [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="39b54-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified index.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b54-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39b54-112">Requirements</span></span>

| <span data-ttu-id="39b54-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39b54-113">Requirement</span></span> | <span data-ttu-id="39b54-114">Wert</span><span class="sxs-lookup"><span data-stu-id="39b54-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="39b54-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39b54-115">Minimum supported client</span></span>| <span data-ttu-id="39b54-116">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="39b54-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="39b54-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="39b54-117">Type library</span></span>            | <span data-ttu-id="39b54-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="39b54-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="39b54-119">DLL</span><span class="sxs-lookup"><span data-stu-id="39b54-119">DLL</span></span>                  | <span data-ttu-id="39b54-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="39b54-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="39b54-121">IID</span><span class="sxs-lookup"><span data-stu-id="39b54-121">IID</span></span>                      | <span data-ttu-id="39b54-122">IID \_ imsrdpcameraredirconfigcollection ist als AE45252B-aaab-4504-B681-649d6073a37a definiert.</span><span class="sxs-lookup"><span data-stu-id="39b54-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="39b54-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39b54-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b54-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="39b54-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>