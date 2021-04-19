---
description: Fügt einen nicht maskierbaren Interrupt in den virtuellen Computer ein.
ms.assetid: 897AD1B9-0EDD-4DCE-963D-D5DE03AF55A9
title: 'Msvm_ComputerSystem:: injetnonmaskableinterrupt-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.InjectNonMaskableInterrupt
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5798079a8866d9fb67356adff43c0ac1e993e6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346695"
---
# <a name="msvm_computersysteminjectnonmaskableinterrupt-method"></a><span data-ttu-id="8b0b3-103">MSVM \_ Computersystem:: injetnonmaskableinterrupt-Methode</span><span class="sxs-lookup"><span data-stu-id="8b0b3-103">Msvm\_ComputerSystem::InjectNonMaskableInterrupt method</span></span>

<span data-ttu-id="8b0b3-104">Fügt einen nicht maskierbaren Interrupt in den virtuellen Computer ein.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-104">Injects a non-maskable interrupt into the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b0b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b0b3-105">Syntax</span></span>


```C++
uint32 InjectNonMaskableInterrupt(
  [out] CIM_ConcreteJob Job
);
```



## <a name="parameters"></a><span data-ttu-id="8b0b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b0b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b0b3-107">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8b0b3-107">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b0b3-108">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85)) abgeleitet wird, um den Status der Interrupt-Injektion zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-108">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) to track the status of the interrupt injection.</span></span> <span data-ttu-id="8b0b3-109">Dieser Verweis kann **null** sein, wenn der Task beendet ist.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-109">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b0b3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b0b3-110">Return value</span></span>

<span data-ttu-id="8b0b3-111">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-111">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8b0b3-112">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="8b0b3-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b0b3-113">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="8b0b3-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8b0b3-114">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="8b0b3-114">**Access Denied** (32769)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8b0b3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b0b3-115">Requirements</span></span>



| <span data-ttu-id="8b0b3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b0b3-116">Requirement</span></span> | <span data-ttu-id="8b0b3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8b0b3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0b3-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b0b3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8b0b3-119">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="8b0b3-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8b0b3-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b0b3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8b0b3-121">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b0b3-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8b0b3-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b0b3-122">Namespace</span></span><br/>                | <span data-ttu-id="8b0b3-123">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8b0b3-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="8b0b3-124">MOF</span><span class="sxs-lookup"><span data-stu-id="8b0b3-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b0b3-125"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8b0b3-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b0b3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8b0b3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b0b3-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b0b3-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b0b3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b0b3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b0b3-129">**MSVM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="8b0b3-129">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

