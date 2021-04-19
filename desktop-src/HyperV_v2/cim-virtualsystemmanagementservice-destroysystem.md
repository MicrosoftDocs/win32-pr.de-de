---
description: Zerstört ein virtuelles System.
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: Destroysystem-Methode der CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41355970bb70063b8e90deb8f49b5e6f4b439017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347925"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="3a57f-103">Destroysystem-Methode der CIM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="3a57f-103">DestroySystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="3a57f-104">Zerstört ein virtuelles System.</span><span class="sxs-lookup"><span data-stu-id="3a57f-104">Destroys a virtual system.</span></span>

<span data-ttu-id="3a57f-105">Das virtuelle System, auf das verwiesen wird, wird zerstört, einschließlich der Elemente, auf die es verweist.</span><span class="sxs-lookup"><span data-stu-id="3a57f-105">The referenced virtual system is destroyed, including any elements scoped by it.</span></span> <span data-ttu-id="3a57f-106">Virtuelle Ressourcen werden an Ihre Ressourcenpools zurückgegeben, was möglicherweise die Zerstörung dieser Ressourcen impliziert (implementierungsabhängig).</span><span class="sxs-lookup"><span data-stu-id="3a57f-106">Virtual resources are returned to their resource pools, which may imply the destruction of those resources (implementation dependent).</span></span> <span data-ttu-id="3a57f-107">Wenn das virtuelle System aktiv ist, wenn der Vorgang aufgerufen wird, wird es zuerst deaktiviert und anschließend zerstört.</span><span class="sxs-lookup"><span data-stu-id="3a57f-107">If the virtual system is active when the operation is invoked, it is first deactivated and then destroyed.</span></span> <span data-ttu-id="3a57f-108">Wenn Momentaufnahmen aus dem virtuellen System erstellt wurden, werden diese ebenfalls zerstört.</span><span class="sxs-lookup"><span data-stu-id="3a57f-108">If snapshots were created from the virtual system, these are destroyed as well.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a57f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a57f-109">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3a57f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a57f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a57f-111">*Affectedsystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a57f-111">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a57f-112">Verweis auf eine Instanz der Klasse " [**CIM \_ Computersystem**](cim-computersystem.md) ", die das virtuelle Computersystem darstellt, das zerstört werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a57f-112">Reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the virtual computer system that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="3a57f-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3a57f-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a57f-114">Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM-" \_ concretejob**](cim-concretejob.md) " zurückgegeben werden, der den Auftrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="3a57f-114">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a57f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a57f-115">Return value</span></span>

<span data-ttu-id="3a57f-116">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3a57f-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="3a57f-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3a57f-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a57f-118">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="3a57f-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3a57f-119">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="3a57f-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3a57f-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="3a57f-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3a57f-121">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="3a57f-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3a57f-122">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="3a57f-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3a57f-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="3a57f-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3a57f-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="3a57f-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3a57f-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="3a57f-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3a57f-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="3a57f-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3a57f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a57f-127">Requirements</span></span>



| <span data-ttu-id="3a57f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a57f-128">Requirement</span></span> | <span data-ttu-id="3a57f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3a57f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a57f-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a57f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3a57f-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3a57f-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3a57f-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a57f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3a57f-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3a57f-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3a57f-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a57f-134">Namespace</span></span><br/>                | <span data-ttu-id="3a57f-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3a57f-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3a57f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3a57f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a57f-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3a57f-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a57f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3a57f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a57f-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a57f-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a57f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a57f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a57f-141">**CIM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="3a57f-141">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




