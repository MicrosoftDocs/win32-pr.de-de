---
title: Activebasicdevice-Eigenschaft von isimagesupported (playondevice. h)
description: Ruft einen Wert ab, der angibt, ob das Gerät Bilder unterstützt.
ms.assetid: FC53B87C-D739-4AD4-9DD3-415AC8692224
keywords:
- Isimagesupported-Eigenschaft Medien Streaming-API
- Isimagesupported-Eigenschaft Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, isimagesupported-Eigenschaft
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsImageSupported
- ActiveBasicDevice.get_IsImageSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2e90f51d2dd59ffec8221787b9ee7c247536abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340306"
---
# <a name="activebasicdeviceisimagesupported-property"></a><span data-ttu-id="95fe7-106">Activebasicdevice:: isimagesupported-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="95fe7-106">ActiveBasicDevice::IsImageSupported property</span></span>

<span data-ttu-id="95fe7-107">Ruft einen Wert ab, der angibt, ob das Gerät Bilder unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95fe7-107">Gets a value that indicates if the device supports images.</span></span>

<span data-ttu-id="95fe7-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="95fe7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="95fe7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="95fe7-109">Syntax</span></span>


```C++
HRESULT get_IsImageSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="95fe7-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="95fe7-110">Property value</span></span>

<span data-ttu-id="95fe7-111">Ein Zeiger auf einen **booleschen** Wert, der angibt, ob das Gerät Bilder unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95fe7-111">A pointer to a **boolean** that indicates if the device supports images.</span></span>

<span data-ttu-id="95fe7-112">" **true** ", wenn das Gerät Bilder unterstützt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="95fe7-112">**true** if the device supports images; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="95fe7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95fe7-113">Requirements</span></span>



| <span data-ttu-id="95fe7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95fe7-114">Requirement</span></span> | <span data-ttu-id="95fe7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="95fe7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="95fe7-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95fe7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="95fe7-117">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="95fe7-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="95fe7-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95fe7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="95fe7-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95fe7-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="95fe7-120">Header</span><span class="sxs-lookup"><span data-stu-id="95fe7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="95fe7-121"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="95fe7-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="95fe7-122">IDL</span><span class="sxs-lookup"><span data-stu-id="95fe7-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95fe7-123"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95fe7-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="95fe7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="95fe7-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95fe7-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95fe7-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95fe7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95fe7-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="95fe7-127">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95fe7-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

