---
description: Diese Methode wird verwendet, um die tatsächliche Reserve zu finden, bei der der Eingabeparameter die Anzahl der Prozessoren virtueller Maschinen ist, für die die Reservierung berechnet wird.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Calculatepossiblereserve-Methode der Msvm_ProcessorPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7f88bcf3295b1792fca6be88ae0c9282b72646e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756624"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a><span data-ttu-id="4adbd-103">Calculatepossiblereserve-Methode der MSVM \_ processorpool-Klasse</span><span class="sxs-lookup"><span data-stu-id="4adbd-103">CalculatePossibleReserve method of the Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="4adbd-104">Diese Methode wird verwendet, um die tatsächliche Reserve zu finden, bei der der Eingabeparameter die Anzahl der Prozessoren virtueller Maschinen ist, für die die Reservierung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="4adbd-104">This method is used to find the actual reserve with the input parameter being the number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="4adbd-105">Diese Methode ist erforderlich, da die Reservierung von Prozessorressourcen stark von der Anzahl der Prozessoren abhängig ist, die parallel geplant werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4adbd-105">This method is necessary because the reservation of processor resources is highly dependent on the number of processors which must be scheduled in parallel.</span></span>

## <a name="syntax"></a><span data-ttu-id="4adbd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4adbd-106">Syntax</span></span>


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a><span data-ttu-id="4adbd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4adbd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4adbd-108">*ProcessorCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4adbd-108">*ProcessorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4adbd-109">Typ: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4adbd-109">Type: **uint16**</span></span>

<span data-ttu-id="4adbd-110">Die Anzahl der Prozessoren virtueller Maschinen, für die die Reservierung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="4adbd-110">The number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="4adbd-111">Der Maximalwert für diese Eigenschaft ist die Anzahl logischer Prozessoren für den Host Computer.</span><span class="sxs-lookup"><span data-stu-id="4adbd-111">The maximum value for this property is the logical processor count for the host computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4adbd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4adbd-112">Return value</span></span>

<span data-ttu-id="4adbd-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4adbd-113">Type: **uint32**</span></span>

<span data-ttu-id="4adbd-114">Die CPU-Ressourcen Menge, die für einen virtuellen Computer reserviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4adbd-114">The amount of CPU resources that may be reserved for a virtual machine.</span></span>

## <a name="remarks"></a><span data-ttu-id="4adbd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4adbd-115">Remarks</span></span>

<span data-ttu-id="4adbd-116">Der Zugriff auf die [**MSVM \_ processorpool**](msvm-processorpool.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="4adbd-116">Access to the [**Msvm\_ProcessorPool**](msvm-processorpool.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4adbd-117">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4adbd-117">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4adbd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4adbd-118">Requirements</span></span>



| <span data-ttu-id="4adbd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4adbd-119">Requirement</span></span> | <span data-ttu-id="4adbd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4adbd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4adbd-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4adbd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4adbd-122">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4adbd-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4adbd-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4adbd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4adbd-124">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4adbd-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4adbd-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="4adbd-125">Namespace</span></span><br/>                | <span data-ttu-id="4adbd-126">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4adbd-126">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4adbd-127">MOF</span><span class="sxs-lookup"><span data-stu-id="4adbd-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4adbd-128"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4adbd-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4adbd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4adbd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4adbd-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4adbd-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4adbd-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4adbd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4adbd-132">**MSVM \_ processorpool**</span><span class="sxs-lookup"><span data-stu-id="4adbd-132">**Msvm\_ProcessorPool**</span></span>](msvm-processorpool.md)
</dt> </dl>

 

