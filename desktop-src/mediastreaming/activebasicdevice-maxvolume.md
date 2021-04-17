---
title: Activebasicdevice maxvolume-Eigenschaft (playondevice. h)
description: Ruft das maximale Volume ab, das vom Gerät unterstützt wird.
ms.assetid: EA0EC323-4A18-4CC1-8FA4-7BD302318863
keywords:
- Maxvolume-Eigenschaft Medien Streaming-API
- Maxvolume-Eigenschaft Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, maxvolume-Eigenschaft
topic_type:
- apiref
api_name:
- ActiveBasicDevice.MaxVolume
- ActiveBasicDevice.get_MaxVolume
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48c25ef6c0e25c35ba07914c00fb063b4e8dc79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479089"
---
# <a name="activebasicdevicemaxvolume-property"></a><span data-ttu-id="b7c56-106">Activebasicdevice:: maxvolume-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b7c56-106">ActiveBasicDevice::MaxVolume property</span></span>

<span data-ttu-id="b7c56-107">Ruft das maximale Volume ab, das vom Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b7c56-107">Gets the maximum volume supported by the device.</span></span>

<span data-ttu-id="b7c56-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b7c56-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c56-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c56-109">Syntax</span></span>


```C++
HRESULT get_MaxVolume(
  [out] boolean *UINT32
);
```



## <a name="property-value"></a><span data-ttu-id="b7c56-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b7c56-110">Property value</span></span>

<span data-ttu-id="b7c56-111">Ein Zeiger auf ein **UInt32** -Wert, der das vom Gerät unterstützte maximale Volume angibt.</span><span class="sxs-lookup"><span data-stu-id="b7c56-111">A pointer to a **UINT32** that specifies the maximum volume supported by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7c56-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7c56-112">Requirements</span></span>



| <span data-ttu-id="b7c56-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7c56-113">Requirement</span></span> | <span data-ttu-id="b7c56-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c56-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c56-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7c56-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b7c56-116">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b7c56-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b7c56-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7c56-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b7c56-118">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7c56-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b7c56-119">Header</span><span class="sxs-lookup"><span data-stu-id="b7c56-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7c56-120"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7c56-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7c56-121">IDL</span><span class="sxs-lookup"><span data-stu-id="b7c56-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7c56-122"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7c56-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="b7c56-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b7c56-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7c56-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7c56-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7c56-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7c56-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="b7c56-126">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7c56-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

