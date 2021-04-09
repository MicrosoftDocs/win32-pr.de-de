---
title: Activebasicdevice isaudiosupported-Eigenschaft (playondevice. h)
description: Ruft einen Wert ab, der angibt, ob das Gerät Audiodaten unterstützt.
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- Isaudiosupported-Eigenschaft Medien Streaming-API
- Isaudiosupported-Eigenschaft Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, isaudiosupported-Eigenschaft
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66058da9dcdbac0ed1100b0ef21a4ed530d45a68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040983"
---
# <a name="activebasicdeviceisaudiosupported-property"></a><span data-ttu-id="0671b-106">Activebasicdevice:: isaudiosupported-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0671b-106">ActiveBasicDevice::IsAudioSupported property</span></span>

<span data-ttu-id="0671b-107">Ruft einen Wert ab, der angibt, ob das Gerät Audiodaten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0671b-107">Gets a value that indicates if the device supports audio.</span></span>

<span data-ttu-id="0671b-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0671b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0671b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0671b-109">Syntax</span></span>


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="0671b-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0671b-110">Property value</span></span>

<span data-ttu-id="0671b-111">Ein Zeiger auf einen **booleschen** Wert, der angibt, ob das Gerät Audiodaten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0671b-111">A pointer to a **boolean** that indicates if the device supports audio.</span></span>

<span data-ttu-id="0671b-112">" **true** ", wenn das Gerät Audiodaten unterstützt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="0671b-112">**true** if the device supports audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0671b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0671b-113">Requirements</span></span>



| <span data-ttu-id="0671b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0671b-114">Requirement</span></span> | <span data-ttu-id="0671b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="0671b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0671b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0671b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0671b-117">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="0671b-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0671b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0671b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0671b-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0671b-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0671b-120">Header</span><span class="sxs-lookup"><span data-stu-id="0671b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0671b-121"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="0671b-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="0671b-122">IDL</span><span class="sxs-lookup"><span data-stu-id="0671b-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0671b-123"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0671b-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="0671b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0671b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0671b-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0671b-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0671b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0671b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="0671b-127">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0671b-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

