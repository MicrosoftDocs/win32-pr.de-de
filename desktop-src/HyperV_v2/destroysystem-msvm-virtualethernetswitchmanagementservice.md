---
description: Zerstört einen virtuellen Switch.
ms.assetid: f0b6b4cc-e9b7-4255-a9e1-a2a826b8f119
title: Destroysystem-Methode der Msvm_VirtualEthernetSwitchManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d8f01a3f72d15fba908c7891f76b4128a1ee8200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363628"
---
# <a name="destroysystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="9848d-103">Destroysystem-Methode der MSVM \_ virtualethernettwitchmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="9848d-103">DestroySystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="9848d-104">Zerstört einen virtuellen Switch.</span><span class="sxs-lookup"><span data-stu-id="9848d-104">Destroys a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="9848d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9848d-105">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9848d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9848d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9848d-107">*Affectedsystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9848d-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9848d-108">Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ virtualethernwitch**](msvm-virtualethernetswitch.md) ", die den virtuellen Switch darstellt, der zerstört werden soll.</span><span class="sxs-lookup"><span data-stu-id="9848d-108">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="9848d-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9848d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9848d-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="9848d-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9848d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9848d-111">Return value</span></span>

<span data-ttu-id="9848d-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="9848d-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9848d-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="9848d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9848d-114">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="9848d-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9848d-115">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="9848d-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9848d-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="9848d-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9848d-117">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="9848d-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9848d-118">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="9848d-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9848d-119">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="9848d-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9848d-120">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="9848d-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9848d-121">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="9848d-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="9848d-122">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="9848d-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9848d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9848d-123">Requirements</span></span>



| <span data-ttu-id="9848d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9848d-124">Requirement</span></span> | <span data-ttu-id="9848d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9848d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9848d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9848d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9848d-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9848d-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9848d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9848d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9848d-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9848d-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9848d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="9848d-130">Namespace</span></span><br/>                | <span data-ttu-id="9848d-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9848d-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9848d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="9848d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9848d-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9848d-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9848d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9848d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9848d-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9848d-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9848d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9848d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9848d-137">**MSVM \_ virtualethernetzwitchmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="9848d-137">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

