---
title: IMsRdpCameraRedirConfig SymbolicLink-Eigenschaft
description: Ruft den symbolischen Link der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera ab.
ms.tgt_platform: multiple
keywords:
- Eigenschaften Remotedesktopdienste SymbolicLink
- Eigenschaften Remotedesktopdienste SymbolicLink, imsrdpcameraredirconfig-Schnittstelle
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste, SymbolicLink-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "103859937"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a><span data-ttu-id="7266a-106">Imsrdpcameraredirconfig:: SymbolicLink (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7266a-106">IMsRdpCameraRedirConfig::SymbolicLink property</span></span>

<span data-ttu-id="7266a-107">Ruft den symbolischen Link der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera ab.</span><span class="sxs-lookup"><span data-stu-id="7266a-107">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="7266a-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7266a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7266a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7266a-109">Syntax</span></span>

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a><span data-ttu-id="7266a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7266a-110">Property value</span></span>

<span data-ttu-id="7266a-111">Die symbolische Verknüpfung der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera.</span><span class="sxs-lookup"><span data-stu-id="7266a-111">The symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="7266a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7266a-112">Requirements</span></span>

| <span data-ttu-id="7266a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7266a-113">Requirement</span></span> | <span data-ttu-id="7266a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7266a-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="7266a-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7266a-115">Minimum supported client</span></span>| <span data-ttu-id="7266a-116">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="7266a-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="7266a-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7266a-117">Type library</span></span>            | <span data-ttu-id="7266a-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="7266a-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="7266a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="7266a-119">DLL</span></span>                  | <span data-ttu-id="7266a-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="7266a-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="7266a-121">IID</span><span class="sxs-lookup"><span data-stu-id="7266a-121">IID</span></span>                      | <span data-ttu-id="7266a-122">IID \_ imsrdpcameraredirconfig ist als 09750604-D625-47c1-9bcd-F09F735705D7 definiert.</span><span class="sxs-lookup"><span data-stu-id="7266a-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="7266a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7266a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7266a-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="7266a-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>