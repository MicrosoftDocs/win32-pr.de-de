---
title: IMsRdpCameraRedirConfigCollection RedirectByDefault-Eigenschaft
description: Gibt an, ob eine neue Kamera standardmäßig umgeleitet wird.
ms.tgt_platform: multiple
keywords:
- Redirectbydefault-Eigenschaft Remotedesktopdienste
- Redirectbydefault-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfigcollection-Schnittstelle
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, redirectbydefault (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.RedirectByDefault
- IMsRdpCameraRedirConfigCollection.put_RedirectByDefault
- IMsRdpCameraRedirConfigCollection.get_RedirectByDefault
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 810af200eefee0008aea21af684c02b6d31325eb
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123284"
---
# <a name="imsrdpcameraredirconfigcollectionredirectbydefault-property"></a><span data-ttu-id="fd436-106">Imsrdpcameraredirconfigcollection:: redirectbydefault (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fd436-106">IMsRdpCameraRedirConfigCollection::RedirectByDefault property</span></span>

<span data-ttu-id="fd436-107">Gibt an, ob eine neue Kamera standardmäßig umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="fd436-107">Specifies whether or not any new camera gets redirected by default.</span></span>

<span data-ttu-id="fd436-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="fd436-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd436-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd436-109">Syntax</span></span>

```C++
HRESULT put_RedirectByDefault(
    [in] VARIANT_BOOL fRedirect
);

HRESULT get_RedirectByDefault(
    [out, retval] VARIANT_BOOL* pfRedirect
);
```

## <a name="property-value"></a><span data-ttu-id="fd436-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fd436-110">Property value</span></span>

<span data-ttu-id="fd436-111">Ein Wert, der angibt, ob eine neue Kamera standardmäßig umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="fd436-111">A value that indicates whether or not any new camera gets redirected by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd436-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd436-112">Requirements</span></span>

| <span data-ttu-id="fd436-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd436-113">Requirement</span></span> | <span data-ttu-id="fd436-114">Wert</span><span class="sxs-lookup"><span data-stu-id="fd436-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="fd436-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd436-115">Minimum supported client</span></span>| <span data-ttu-id="fd436-116">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="fd436-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="fd436-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fd436-117">Type library</span></span>            | <span data-ttu-id="fd436-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fd436-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="fd436-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fd436-119">DLL</span></span>                  | <span data-ttu-id="fd436-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fd436-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="fd436-121">IID</span><span class="sxs-lookup"><span data-stu-id="fd436-121">IID</span></span>                      | <span data-ttu-id="fd436-122">IID \_ imsrdpcameraredirconfigcollection ist als AE45252B-aaab-4504-B681-649d6073a37a definiert.</span><span class="sxs-lookup"><span data-stu-id="fd436-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="fd436-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd436-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd436-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="fd436-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>