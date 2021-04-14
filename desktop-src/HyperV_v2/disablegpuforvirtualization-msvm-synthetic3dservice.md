---
description: Deaktiviert eine physische GPU für die Virtualisierung.
ms.assetid: 280a3c25-7b8f-4113-bf35-171d15f4aea7
title: Disablegpuforvirtualization-Methode der Msvm_Synthetic3DService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.DisableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2634a3196e0c59368002151426e6f1407a13db8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342638"
---
# <a name="disablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="af33c-103">Disablegpuforvirtualization-Methode der Synthetic3DService-Klasse von MSVM \_</span><span class="sxs-lookup"><span data-stu-id="af33c-103">DisableGPUForVirtualization method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="af33c-104">Deaktiviert eine physische GPU für die Virtualisierung.</span><span class="sxs-lookup"><span data-stu-id="af33c-104">Disables a physical GPU for virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="af33c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="af33c-105">Syntax</span></span>


```mof
uint32 DisableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="af33c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="af33c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af33c-107">*Physicalgpu* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af33c-107">*PhysicalGPU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af33c-108">Ein Verweis auf eine Instanz der [**MSVM \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) -Klasse, die die zu deaktivier Ende physische GPU darstellt.</span><span class="sxs-lookup"><span data-stu-id="af33c-108">A reference to an instance of the [**Msvm\_Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) class that represents the physical GPU to be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="af33c-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="af33c-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af33c-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="af33c-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af33c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af33c-111">Return value</span></span>

<span data-ttu-id="af33c-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="af33c-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="af33c-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="af33c-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="af33c-114">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="af33c-114">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="af33c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af33c-115">Requirements</span></span>



| <span data-ttu-id="af33c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af33c-116">Requirement</span></span> | <span data-ttu-id="af33c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="af33c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af33c-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af33c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af33c-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af33c-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="af33c-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af33c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af33c-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af33c-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af33c-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="af33c-122">Namespace</span></span><br/>                | <span data-ttu-id="af33c-123">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="af33c-123">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="af33c-124">MOF</span><span class="sxs-lookup"><span data-stu-id="af33c-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af33c-125"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="af33c-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="af33c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="af33c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af33c-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="af33c-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="af33c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af33c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af33c-129">**MSVM \_ Synthetic3DService**</span><span class="sxs-lookup"><span data-stu-id="af33c-129">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

