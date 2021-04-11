---
title: IMsRdpCameraRedirConfigCollection EncodeVideo-Eigenschaft
description: Gibt an, ob der Videostream H. 264-codiert ist.
ms.tgt_platform: multiple
keywords:
- Encodebug-Eigenschaft Remotedesktopdienste
- Encodebug-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfigcollection-Schnittstelle
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, encodebug-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 6b2994f4db3de04f339bb242120b6c63cd2e0c7b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123289"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a><span data-ttu-id="79fee-106">Imsrdpcameraredirconfigcollection:: encodebug-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="79fee-106">IMsRdpCameraRedirConfigCollection::EncodeVideo property</span></span>

<span data-ttu-id="79fee-107">Gibt an, ob der Videostream H. 264-codiert ist.</span><span class="sxs-lookup"><span data-stu-id="79fee-107">Specifies whether or not the video stream is H.264 encoded.</span></span>

<span data-ttu-id="79fee-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="79fee-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="79fee-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="79fee-109">Syntax</span></span>

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a><span data-ttu-id="79fee-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="79fee-110">Property value</span></span>

<span data-ttu-id="79fee-111">Ein Wert, der angibt, ob der Videostream H. 264-codiert ist.</span><span class="sxs-lookup"><span data-stu-id="79fee-111">A value that indicates whether or not the video stream is H.264 encoded.</span></span>

## <a name="requirements"></a><span data-ttu-id="79fee-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79fee-112">Requirements</span></span>

| <span data-ttu-id="79fee-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79fee-113">Requirement</span></span> | <span data-ttu-id="79fee-114">Wert</span><span class="sxs-lookup"><span data-stu-id="79fee-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="79fee-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79fee-115">Minimum supported client</span></span>| <span data-ttu-id="79fee-116">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="79fee-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="79fee-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="79fee-117">Type library</span></span>            | <span data-ttu-id="79fee-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="79fee-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="79fee-119">DLL</span><span class="sxs-lookup"><span data-stu-id="79fee-119">DLL</span></span>                  | <span data-ttu-id="79fee-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="79fee-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="79fee-121">IID</span><span class="sxs-lookup"><span data-stu-id="79fee-121">IID</span></span>                      | <span data-ttu-id="79fee-122">IID \_ imsrdpcameraredirconfigcollection ist als AE45252B-aaab-4504-B681-649d6073a37a definiert.</span><span class="sxs-lookup"><span data-stu-id="79fee-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="79fee-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79fee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79fee-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="79fee-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>