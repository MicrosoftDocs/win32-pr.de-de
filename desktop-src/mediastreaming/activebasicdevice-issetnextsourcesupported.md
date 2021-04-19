---
title: Activebasicdevice issetnextsourcesupportiert-Eigenschaft (playondevice. h)
description: Ruft einen Wert ab, der angibt, ob das Festlegen der nächsten Quelle unterstützt wird.
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- Issetnextsourcesupportiert-Eigenschaft Medien Streaming-API
- Issetnextsourcesupportiert-Eigenschaft Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, issetnextsourcesupportiert (Eigenschaft)
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b84190336678e677ad3f0436d7233a49d4587574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346126"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a><span data-ttu-id="f32a9-106">Activebasicdevice:: issetnextsourcesupportiert (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f32a9-106">ActiveBasicDevice::IsSetNextSourceSupported property</span></span>

<span data-ttu-id="f32a9-107">Ruft einen Wert ab, der angibt, ob das Festlegen der nächsten Quelle unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f32a9-107">Gets a value that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="f32a9-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f32a9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f32a9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f32a9-109">Syntax</span></span>


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="f32a9-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f32a9-110">Property value</span></span>

<span data-ttu-id="f32a9-111">Ein Zeiger auf einen **booleschen** Wert, der angibt, ob das Festlegen der nächsten Quelle unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f32a9-111">A pointer to a **boolean** that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="f32a9-112">**true** , wenn das Festlegen der nächsten Quelle unterstützt wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="f32a9-112">**true** if setting the next source is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f32a9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f32a9-113">Requirements</span></span>



| <span data-ttu-id="f32a9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f32a9-114">Requirement</span></span> | <span data-ttu-id="f32a9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f32a9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f32a9-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f32a9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f32a9-117">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="f32a9-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f32a9-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f32a9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f32a9-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f32a9-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f32a9-120">Header</span><span class="sxs-lookup"><span data-stu-id="f32a9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f32a9-121"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="f32a9-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="f32a9-122">IDL</span><span class="sxs-lookup"><span data-stu-id="f32a9-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f32a9-123"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f32a9-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="f32a9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f32a9-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f32a9-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f32a9-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f32a9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f32a9-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f32a9-127">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f32a9-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

