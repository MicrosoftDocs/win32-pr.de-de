---
title: IMsRdpCameraRedirConfigCollection BySymbolicLink-Eigenschaft
description: Gibt ein imsrdpcameraredirconfig-Objekt aus der Auflistung zurück, das der angegebenen symbolischen Verknüpfung der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera entspricht.
ms.tgt_platform: multiple
keywords:
- Bysymboliclink-Eigenschaft Remotedesktopdienste
- Bysymboliclink-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfigcollection-Schnittstelle
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, bysymboliclink (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.BySymbolicLink
- IMsRdpCameraRedirConfigCollection.get_BySymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d4888c7e468e0522240d8ef922563ab28eb33e77
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106346379"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a><span data-ttu-id="eac8e-106">Imsrdpcameraredirconfigcollection::. Bysymboliclink (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="eac8e-106">IMsRdpCameraRedirConfigCollection::.BySymbolicLink property</span></span>

<span data-ttu-id="eac8e-107">Gibt ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt aus der Auflistung zurück, das der angegebenen symbolischen Verknüpfung der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera entspricht.</span><span class="sxs-lookup"><span data-stu-id="eac8e-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="eac8e-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="eac8e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eac8e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="eac8e-109">Syntax</span></span>

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="eac8e-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="eac8e-110">Property value</span></span>

<span data-ttu-id="eac8e-111">Das [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt, das der angegebenen symbolischen Verknüpfung entspricht.</span><span class="sxs-lookup"><span data-stu-id="eac8e-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified symbolic link.</span></span>

## <a name="requirements"></a><span data-ttu-id="eac8e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eac8e-112">Requirements</span></span>

| <span data-ttu-id="eac8e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eac8e-113">Requirement</span></span> | <span data-ttu-id="eac8e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="eac8e-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="eac8e-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eac8e-115">Minimum supported client</span></span>| <span data-ttu-id="eac8e-116">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="eac8e-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="eac8e-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="eac8e-117">Type library</span></span>            | <span data-ttu-id="eac8e-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="eac8e-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="eac8e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="eac8e-119">DLL</span></span>                  | <span data-ttu-id="eac8e-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="eac8e-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="eac8e-121">IID</span><span class="sxs-lookup"><span data-stu-id="eac8e-121">IID</span></span>                      | <span data-ttu-id="eac8e-122">IID \_ imsrdpcameraredirconfigcollection ist als AE45252B-aaab-4504-B681-649d6073a37a definiert.</span><span class="sxs-lookup"><span data-stu-id="eac8e-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="eac8e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eac8e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac8e-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="eac8e-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>