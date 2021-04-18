---
title: Activebasicdevice ismutesupportiert-Eigenschaft (playondevice. h)
description: Ruft einen Wert ab, der angibt, ob das Gerät die audioformatierung unterstützt.
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- Ismutesupportiert-Eigenschaft Medien Streaming-API
- Ismutesupportiert-Eigenschaft Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, ismutesupportiert (Eigenschaft)
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcec2e4520bd3b15b715c01e4369da87887355e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477370"
---
# <a name="activebasicdeviceismutesupported-property"></a><span data-ttu-id="f9c7a-106">Activebasicdevice:: ismutesupportiert-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f9c7a-106">ActiveBasicDevice::IsMuteSupported property</span></span>

<span data-ttu-id="f9c7a-107">Ruft einen Wert ab, der angibt, ob das Gerät die audioformatierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9c7a-107">Gets a value that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="f9c7a-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f9c7a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c7a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9c7a-109">Syntax</span></span>


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="f9c7a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f9c7a-110">Property value</span></span>

<span data-ttu-id="f9c7a-111">Ein Zeiger auf einen **booleschen** Wert, der angibt, ob das Gerät die audioformatierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9c7a-111">A pointer to a **boolean** that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="f9c7a-112">" **true** ", wenn das Gerät die audioformatierung unterstützt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="f9c7a-112">**true** if the device supports muting the audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9c7a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9c7a-113">Requirements</span></span>



| <span data-ttu-id="f9c7a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9c7a-114">Requirement</span></span> | <span data-ttu-id="f9c7a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f9c7a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c7a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9c7a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c7a-117">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="f9c7a-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f9c7a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9c7a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c7a-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9c7a-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f9c7a-120">Header</span><span class="sxs-lookup"><span data-stu-id="f9c7a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9c7a-121"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9c7a-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9c7a-122">IDL</span><span class="sxs-lookup"><span data-stu-id="f9c7a-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9c7a-123"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9c7a-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="f9c7a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f9c7a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9c7a-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9c7a-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9c7a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9c7a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f9c7a-127">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f9c7a-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

