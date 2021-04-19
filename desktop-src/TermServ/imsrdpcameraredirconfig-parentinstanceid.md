---
title: IMsRdpCameraRedirConfig ParentInstanceId-Eigenschaft
description: Ruft die Instanz-ID der übergeordneten Instanz der Kamera ab.
ms.tgt_platform: multiple
keywords:
- Eigenschaft "parametriinstanceid" Remotedesktopdienste
- Eigenschaften Remotedesktopdienste der Eigenschaft "imsrdpcameraredirconfig"
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste, parameteninstanceid (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e4a399659c33000207930bfe7d17818a2ad8438f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106342537"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a><span data-ttu-id="e3bfd-106">Imsrdpcameraredirconfig::P arentinstanceid-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e3bfd-106">IMsRdpCameraRedirConfig::ParentInstanceId property</span></span>

<span data-ttu-id="e3bfd-107">Ruft die Instanz-ID der übergeordneten Instanz der Kamera ab.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-107">Gets the parent device instance ID of the camera.</span></span>

<span data-ttu-id="e3bfd-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3bfd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3bfd-109">Syntax</span></span>

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a><span data-ttu-id="e3bfd-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e3bfd-110">Property value</span></span>

<span data-ttu-id="e3bfd-111">Die ID der übergeordneten Geräte Instanz der Kamera.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-111">The parent device instance ID of the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3bfd-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3bfd-112">Requirements</span></span>

| <span data-ttu-id="e3bfd-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3bfd-113">Requirement</span></span> | <span data-ttu-id="e3bfd-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e3bfd-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="e3bfd-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3bfd-115">Minimum supported client</span></span>| <span data-ttu-id="e3bfd-116">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="e3bfd-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="e3bfd-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e3bfd-117">Type library</span></span>            | <span data-ttu-id="e3bfd-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e3bfd-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="e3bfd-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e3bfd-119">DLL</span></span>                  | <span data-ttu-id="e3bfd-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e3bfd-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="e3bfd-121">IID</span><span class="sxs-lookup"><span data-stu-id="e3bfd-121">IID</span></span>                      | <span data-ttu-id="e3bfd-122">IID \_ imsrdpcameraredirconfig ist als 09750604-D625-47c1-9bcd-F09F735705D7 definiert.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="e3bfd-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3bfd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3bfd-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="e3bfd-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>