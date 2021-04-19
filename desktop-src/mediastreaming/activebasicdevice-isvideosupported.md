---
title: Activebasicdevice isvideosupported-Eigenschaft (playondevice. h)
description: Ruft einen Wert ab, der angibt, ob das Gerät Video unterstützt.
ms.assetid: E8D33A04-748D-42F8-878F-35D973A6B559
keywords:
- Isvideosupported-Eigenschaft Medien Streaming-API
- Isvideosupported-Eigenschaft Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, isvideosupported-Eigenschaft
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsVideoSupported
- ActiveBasicDevice.get_IsVideoSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be369b34355b199cd47518065724242b9a422e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338797"
---
# <a name="activebasicdeviceisvideosupported-property"></a><span data-ttu-id="8589c-106">Activebasicdevice:: isvideosupported-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8589c-106">ActiveBasicDevice::IsVideoSupported property</span></span>

<span data-ttu-id="8589c-107">Ruft einen Wert ab, der angibt, ob das Gerät Video unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8589c-107">Gets a value that indicates if the device supports video.</span></span>

<span data-ttu-id="8589c-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8589c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8589c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8589c-109">Syntax</span></span>


```C++
HRESULT get_IsVideoSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="8589c-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8589c-110">Property value</span></span>

<span data-ttu-id="8589c-111">Ein Zeiger auf einen **booleschen** Wert, der angibt, ob das Gerät Video unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8589c-111">A pointer to a **boolean** that indicates if the device supports video.</span></span>

<span data-ttu-id="8589c-112">" **true** ", wenn das Gerät Video unterstützt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="8589c-112">**true** if the device supports video; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8589c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8589c-113">Requirements</span></span>



| <span data-ttu-id="8589c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8589c-114">Requirement</span></span> | <span data-ttu-id="8589c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8589c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8589c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8589c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8589c-117">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="8589c-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8589c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8589c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8589c-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8589c-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8589c-120">Header</span><span class="sxs-lookup"><span data-stu-id="8589c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8589c-121"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="8589c-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="8589c-122">IDL</span><span class="sxs-lookup"><span data-stu-id="8589c-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8589c-123"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8589c-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="8589c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8589c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8589c-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8589c-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8589c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8589c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="8589c-127">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8589c-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

