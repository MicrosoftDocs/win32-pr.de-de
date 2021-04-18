---
title: IMsRdpCameraRedirConfig FriendlyName-Eigenschaft
description: Ruft den anzeigen amen der Kamera ab.
ms.tgt_platform: multiple
keywords:
- FriendlyName-Eigenschaft Remotedesktopdienste
- FriendlyName-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfig-Schnittstelle
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste, FriendlyName-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.FriendlyName
- IMsRdpCameraRedirConfig.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 2ffded502f64426392e89c2d18831770133e352d
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106341084"
---
# <a name="imsrdpcameraredirconfigfriendlyname-property"></a><span data-ttu-id="fb0fd-106">Imsrdpcameraredirconfig:: FriendlyName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fb0fd-106">IMsRdpCameraRedirConfig::FriendlyName property</span></span>

<span data-ttu-id="fb0fd-107">Ruft den anzeigen amen der Kamera ab.</span><span class="sxs-lookup"><span data-stu-id="fb0fd-107">Gets the camera’s friendly name.</span></span>

<span data-ttu-id="fb0fd-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fb0fd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb0fd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb0fd-109">Syntax</span></span>

```C++
HRESULT get_FriendlyName(
    [out, retval] BSTR* pFriendlyName
);
```

## <a name="property-value"></a><span data-ttu-id="fb0fd-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fb0fd-110">Property value</span></span>

<span data-ttu-id="fb0fd-111">Der Anzeige Name der Kamera.</span><span class="sxs-lookup"><span data-stu-id="fb0fd-111">The camera’s friendly name.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb0fd-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb0fd-112">Requirements</span></span>

| <span data-ttu-id="fb0fd-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb0fd-113">Requirement</span></span> | <span data-ttu-id="fb0fd-114">Wert</span><span class="sxs-lookup"><span data-stu-id="fb0fd-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="fb0fd-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb0fd-115">Minimum supported client</span></span>| <span data-ttu-id="fb0fd-116">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="fb0fd-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="fb0fd-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fb0fd-117">Type library</span></span>            | <span data-ttu-id="fb0fd-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fb0fd-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="fb0fd-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fb0fd-119">DLL</span></span>                  | <span data-ttu-id="fb0fd-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fb0fd-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="fb0fd-121">IID</span><span class="sxs-lookup"><span data-stu-id="fb0fd-121">IID</span></span>                      | <span data-ttu-id="fb0fd-122">IID \_ imsrdpcameraredirconfig ist als 09750604-D625-47c1-9bcd-F09F735705D7 definiert.</span><span class="sxs-lookup"><span data-stu-id="fb0fd-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="fb0fd-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb0fd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb0fd-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="fb0fd-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>