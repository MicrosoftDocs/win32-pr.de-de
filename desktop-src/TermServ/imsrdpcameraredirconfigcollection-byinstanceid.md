---
title: IMsRdpCameraRedirConfigCollection ByInstanceId-Eigenschaft
description: Gibt ein imsrdpcameraredirconfig-Objekt aus der Auflistung zurück, das der angegebenen Instanz-ID entspricht.
ms.tgt_platform: multiple
keywords:
- Byinstanceid-Eigenschaft Remotedesktopdienste
- Byinstanceid-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfigcollection-Schnittstelle
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, byinstanceid (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d90cb7d2f309a3df9e354ace04a840b667e5569b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480526"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a><span data-ttu-id="32e7f-106">Imsrdpcameraredirconfigcollection:: byinstanceid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="32e7f-106">IMsRdpCameraRedirConfigCollection::ByInstanceId property</span></span>

<span data-ttu-id="32e7f-107">Gibt ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt aus der Auflistung zurück, das der angegebenen Instanz-ID entspricht.</span><span class="sxs-lookup"><span data-stu-id="32e7f-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>

<span data-ttu-id="32e7f-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="32e7f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e7f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="32e7f-109">Syntax</span></span>

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="32e7f-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="32e7f-110">Property value</span></span>

<span data-ttu-id="32e7f-111">Das [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt, das der angegebenen Instanz-ID entspricht.</span><span class="sxs-lookup"><span data-stu-id="32e7f-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified instance ID.</span></span>

## <a name="requirements"></a><span data-ttu-id="32e7f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32e7f-112">Requirements</span></span>

| <span data-ttu-id="32e7f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32e7f-113">Requirement</span></span> | <span data-ttu-id="32e7f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="32e7f-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="32e7f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32e7f-115">Minimum supported client</span></span>| <span data-ttu-id="32e7f-116">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="32e7f-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="32e7f-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="32e7f-117">Type library</span></span>            | <span data-ttu-id="32e7f-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="32e7f-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="32e7f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="32e7f-119">DLL</span></span>                  | <span data-ttu-id="32e7f-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="32e7f-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="32e7f-121">IID</span><span class="sxs-lookup"><span data-stu-id="32e7f-121">IID</span></span>                      | <span data-ttu-id="32e7f-122">IID \_ imsrdpcameraredirconfigcollection ist als AE45252B-aaab-4504-B681-649d6073a37a definiert.</span><span class="sxs-lookup"><span data-stu-id="32e7f-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="32e7f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32e7f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e7f-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="32e7f-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>