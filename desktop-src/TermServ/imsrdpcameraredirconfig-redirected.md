---
title: IMsRdpCameraRedirConfig Redirected-Eigenschaft
description: Gibt an, ob die Kamera umgeleitet wird oder nicht.
ms.tgt_platform: multiple
keywords:
- Umgeleitete Eigenschaften Remotedesktopdienste
- Umgeleitete Eigenschaften Remotedesktopdienste, imsrdpcameraredirconfig-Schnittstelle
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste, umgeleitete Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.Redirected
- IMsRdpCameraRedirConfig.put_Redirected
- IMsRdpCameraRedirConfig.get_Redirected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: f81dc643f7911029df088bbb692d7c8c06fddac4
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480555"
---
# <a name="imsrdpcameraredirconfigredirected-property"></a><span data-ttu-id="f79c4-106">Imsrdpcameraredirconfig:: umgeleitet-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f79c4-106">IMsRdpCameraRedirConfig::Redirected property</span></span>

<span data-ttu-id="f79c4-107">Gibt an, ob die Kamera umgeleitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="f79c4-107">Specifies whether or not the camera is redirected.</span></span>

<span data-ttu-id="f79c4-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f79c4-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f79c4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f79c4-109">Syntax</span></span>

```C++
HRESULT put_Redirected(
    [in] VARIANT_BOOL fRedirected
);

HRESULT get_Redirected(
    [out, retval] VARIANT_BOOL* pfRedirected
);
```

## <a name="property-value"></a><span data-ttu-id="f79c4-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f79c4-110">Property value</span></span>

<span data-ttu-id="f79c4-111">Ein-Wert, der angibt, ob die Kamera umgeleitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="f79c4-111">A value that specifies whether or not the camera is redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="f79c4-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f79c4-112">Requirements</span></span>

| <span data-ttu-id="f79c4-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f79c4-113">Requirement</span></span> | <span data-ttu-id="f79c4-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f79c4-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="f79c4-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f79c4-115">Minimum supported client</span></span>| <span data-ttu-id="f79c4-116">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="f79c4-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="f79c4-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f79c4-117">Type library</span></span>            | <span data-ttu-id="f79c4-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f79c4-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="f79c4-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f79c4-119">DLL</span></span>                  | <span data-ttu-id="f79c4-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f79c4-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="f79c4-121">IID</span><span class="sxs-lookup"><span data-stu-id="f79c4-121">IID</span></span>                      | <span data-ttu-id="f79c4-122">IID \_ imsrdpcameraredirconfig ist als 09750604-D625-47c1-9bcd-F09F735705D7 definiert.</span><span class="sxs-lookup"><span data-stu-id="f79c4-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="f79c4-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f79c4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f79c4-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="f79c4-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>