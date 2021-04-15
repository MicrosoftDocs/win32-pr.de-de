---
title: Activebasicdevice physicalnetworkinterface-Eigenschaft (playondevice. h)
description: Ruft die ID der physischen Netzwerkschnittstelle ab.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- Physicalnetworkinterface-Eigenschaft Medien Streaming-API
- Physicalnetworkinterface-Eigenschaft Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, physicalnetworkinterface (Eigenschaft)
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479618ed4d22a3d78a351fb88fcb1108a27c618f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477367"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a><span data-ttu-id="10bf7-106">Activebasicdevice::P hysicalnetworkinterface-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="10bf7-106">ActiveBasicDevice::PhysicalNetworkInterface property</span></span>

<span data-ttu-id="10bf7-107">Ruft die ID der physischen Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="10bf7-107">Gets the id of the physical network interface.</span></span>

<span data-ttu-id="10bf7-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="10bf7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="10bf7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="10bf7-109">Syntax</span></span>


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="10bf7-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="10bf7-110">Property value</span></span>

<span data-ttu-id="10bf7-111">Ein Zeiger auf eine **GUID** , die die ID der physischen Netzwerkschnittstelle angibt.</span><span class="sxs-lookup"><span data-stu-id="10bf7-111">A pointer to a **GUID** that specifies the id of the physical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="10bf7-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10bf7-112">Requirements</span></span>



| <span data-ttu-id="10bf7-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10bf7-113">Requirement</span></span> | <span data-ttu-id="10bf7-114">Wert</span><span class="sxs-lookup"><span data-stu-id="10bf7-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="10bf7-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10bf7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="10bf7-116">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="10bf7-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="10bf7-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10bf7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="10bf7-118">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10bf7-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="10bf7-119">Header</span><span class="sxs-lookup"><span data-stu-id="10bf7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="10bf7-120"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="10bf7-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="10bf7-121">IDL</span><span class="sxs-lookup"><span data-stu-id="10bf7-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="10bf7-122"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="10bf7-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="10bf7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="10bf7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10bf7-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10bf7-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10bf7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10bf7-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="10bf7-126">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10bf7-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

