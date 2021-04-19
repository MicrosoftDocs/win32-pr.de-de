---
description: Aktiviert eine physische GPU für die Virtualisierung.
ms.assetid: 700cb46b-97f1-40cf-88d2-64242f4bd2c6
title: Enablegpuforvirtualization-Methode der Msvm_Synthetic3DService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.EnableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cf21424e9af8398cd435dce409bccde03543a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353830"
---
# <a name="enablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="8898b-103">Enablegpuforvirtualization-Methode der MSVM \_ Synthetic3DService-Klasse</span><span class="sxs-lookup"><span data-stu-id="8898b-103">EnableGPUForVirtualization method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="8898b-104">Aktiviert eine physische GPU für die Virtualisierung.</span><span class="sxs-lookup"><span data-stu-id="8898b-104">Enables a physical GPU for virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="8898b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8898b-105">Syntax</span></span>


```mof
uint32 EnableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8898b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8898b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8898b-107">*Physicalgpu* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8898b-107">*PhysicalGPU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8898b-108">Ein Verweis auf eine Instanz der [**MSVM \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) -Klasse, die die zu aktivierende physische GPU darstellt.</span><span class="sxs-lookup"><span data-stu-id="8898b-108">A reference to an instance of the [**Msvm\_Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) class that represents the physical GPU to be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="8898b-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8898b-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8898b-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="8898b-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8898b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8898b-111">Return value</span></span>

<span data-ttu-id="8898b-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="8898b-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8898b-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="8898b-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8898b-114">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="8898b-114">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8898b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8898b-115">Requirements</span></span>



| <span data-ttu-id="8898b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8898b-116">Requirement</span></span> | <span data-ttu-id="8898b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8898b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8898b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8898b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8898b-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8898b-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8898b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8898b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8898b-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8898b-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8898b-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="8898b-122">Namespace</span></span><br/>                | <span data-ttu-id="8898b-123">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8898b-123">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8898b-124">MOF</span><span class="sxs-lookup"><span data-stu-id="8898b-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8898b-125"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8898b-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8898b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8898b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8898b-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8898b-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8898b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8898b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8898b-129">**MSVM \_ Synthetic3DService**</span><span class="sxs-lookup"><span data-stu-id="8898b-129">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

