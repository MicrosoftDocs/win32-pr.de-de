---
title: Activebasicdevice logicalnetworkinterface-Eigenschaft (playondevice. h)
description: Ruft die ID der logischen Netzwerkschnittstelle ab.
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- Logicalnetworkinterface-Eigenschaft Medien Streaming-API
- Logicalnetworkinterface-Eigenschaft Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, logicalnetworkinterface (Eigenschaft)
topic_type:
- apiref
api_name:
- ActiveBasicDevice.LogicalNetworkInterface
- ActiveBasicDevice.get_LogicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95a87f2951ea09a0bba3d56da50b8f77a9d4a980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391837"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a><span data-ttu-id="84a25-106">Activebasicdevice:: logicalnetworkinterface (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="84a25-106">ActiveBasicDevice::LogicalNetworkInterface property</span></span>

<span data-ttu-id="84a25-107">Ruft die ID der logischen Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="84a25-107">Gets the id of the logical network interface.</span></span>

<span data-ttu-id="84a25-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="84a25-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="84a25-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="84a25-109">Syntax</span></span>


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="84a25-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="84a25-110">Property value</span></span>

<span data-ttu-id="84a25-111">Ein Zeiger auf eine **GUID** , die die ID der logischen Netzwerkschnittstelle angibt.</span><span class="sxs-lookup"><span data-stu-id="84a25-111">A pointer to a **GUID** that specifies the id of the logical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="84a25-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84a25-112">Requirements</span></span>



| <span data-ttu-id="84a25-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84a25-113">Requirement</span></span> | <span data-ttu-id="84a25-114">Wert</span><span class="sxs-lookup"><span data-stu-id="84a25-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a25-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84a25-115">Minimum supported client</span></span><br/> | <span data-ttu-id="84a25-116">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="84a25-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="84a25-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84a25-117">Minimum supported server</span></span><br/> | <span data-ttu-id="84a25-118">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84a25-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="84a25-119">Header</span><span class="sxs-lookup"><span data-stu-id="84a25-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="84a25-120"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="84a25-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="84a25-121">IDL</span><span class="sxs-lookup"><span data-stu-id="84a25-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84a25-122"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84a25-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="84a25-123">DLL</span><span class="sxs-lookup"><span data-stu-id="84a25-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84a25-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84a25-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84a25-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84a25-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="84a25-126">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84a25-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

