---
title: Activebasicdevice issearchsupported-Eigenschaft (playondevice. h)
description: Ruft einen Wert ab, der angibt, ob das Gerät die Suche unterstützt.
ms.assetid: 091D467A-1FF6-4635-BF89-4E62AC9C660A
keywords:
- Issearchsupported-Eigenschaft Medien Streaming-API
- Issearchsupported-Eigenschaft Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, issearchsupported-Eigenschaft
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSearchSupported
- ActiveBasicDevice.get_IsSearchSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff97b20697388b1e3079f6993b97b948fa12091e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392186"
---
# <a name="activebasicdeviceissearchsupported-property"></a><span data-ttu-id="55c3a-106">Activebasicdevice:: issearchsupported-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55c3a-106">ActiveBasicDevice::IsSearchSupported property</span></span>

<span data-ttu-id="55c3a-107">Ruft einen Wert ab, der angibt, ob das Gerät die Suche unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55c3a-107">Gets a value that indicates if the device supports search.</span></span>

<span data-ttu-id="55c3a-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="55c3a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="55c3a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="55c3a-109">Syntax</span></span>


```C++
HRESULT get_IsSearchSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="55c3a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="55c3a-110">Property value</span></span>

<span data-ttu-id="55c3a-111">Ein Zeiger auf einen **booleschen** Wert, der angibt, ob das Gerät die Suche unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55c3a-111">A pointer to a **boolean** that indicates if the device supports search.</span></span>

<span data-ttu-id="55c3a-112">" **true** ", wenn das Gerät die Suche unterstützt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="55c3a-112">**true** if the device supports search; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="55c3a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55c3a-113">Requirements</span></span>



| <span data-ttu-id="55c3a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55c3a-114">Requirement</span></span> | <span data-ttu-id="55c3a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="55c3a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="55c3a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55c3a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="55c3a-117">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="55c3a-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="55c3a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55c3a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="55c3a-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55c3a-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="55c3a-120">Header</span><span class="sxs-lookup"><span data-stu-id="55c3a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="55c3a-121"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="55c3a-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="55c3a-122">IDL</span><span class="sxs-lookup"><span data-stu-id="55c3a-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55c3a-123"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55c3a-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="55c3a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="55c3a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55c3a-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55c3a-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55c3a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55c3a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="55c3a-127">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="55c3a-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

