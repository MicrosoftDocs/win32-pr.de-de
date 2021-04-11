---
description: Eine Methode, um diesen Auftrag und alle zugrunde liegenden Prozesse zu beenden und um alle verbleibenden Zuordnungen zu entfernen. Diese Methode ist veraltet. Verwenden Sie stattdessen requestchangestate.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: Killjob-Methode der CIM_Job-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 967e5e8510d4456a085f393291f8c41afb5be446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959562"
---
# <a name="killjob-method-of-the-cim_job-class"></a><span data-ttu-id="e6afa-104">Killjob-Methode der CIM- \_ Auftrags Klasse</span><span class="sxs-lookup"><span data-stu-id="e6afa-104">KillJob method of the CIM\_Job class</span></span>

<span data-ttu-id="e6afa-105">Eine Methode, um diesen Auftrag und alle zugrunde liegenden Prozesse zu beenden und alle "verbleibenden" Zuordnungen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e6afa-105">A method to kill this job and any underlying processes, and to remove any 'dangling' associations.</span></span> <span data-ttu-id="e6afa-106">Diese Methode ist veraltet. Verwenden Sie stattdessen **requestchangestate** .</span><span class="sxs-lookup"><span data-stu-id="e6afa-106">This method is deprecated; use **RequestChangeState** instead.</span></span> <span data-ttu-id="e6afa-107">" **Killjob** " ist veraltet, da zwischen einem ordnungsgemäßen Herunterfahren und einem sofortigen Abbruch kein Unterschied besteht.</span><span class="sxs-lookup"><span data-stu-id="e6afa-107">**KillJob** is being deprecated because there is no distinction made between an orderly shutdown and an immediate kill.</span></span> <span data-ttu-id="e6afa-108">[**CIM \_ "Concretejob**](cim-concretejob.md)". **RequestStateChange**() stellt die Optionen "beenden" und "Kill" bereit, um diesen Unterschied zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="e6afa-108">[**CIM\_ConcreteJob**](cim-concretejob.md).**RequestStateChange**() provides 'Terminate' and 'Kill' options to allow this distinction.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6afa-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6afa-109">Syntax</span></span>


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a><span data-ttu-id="e6afa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6afa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6afa-111">*Deleteonkill* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6afa-111">*DeleteOnKill* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6afa-112">Gibt an, ob der Auftrag bei Beendigung automatisch gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6afa-112">Indicates whether or not the Job should be automatically deleted upon termination.</span></span> <span data-ttu-id="e6afa-113">Dieser Parameter hat Vorrang vor der **deleteoncompletion** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e6afa-113">This parameter takes precedence over the **DeleteOnCompletion** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6afa-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6afa-114">Return value</span></span>

<span data-ttu-id="e6afa-115">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e6afa-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e6afa-116">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="e6afa-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6afa-117">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="e6afa-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e6afa-118">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="e6afa-118">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e6afa-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="e6afa-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e6afa-120">Fehler **(4** )</span><span class="sxs-lookup"><span data-stu-id="e6afa-120">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e6afa-121">**Zugriff verweigert** (6)</span><span class="sxs-lookup"><span data-stu-id="e6afa-121">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e6afa-122">**Nicht gefunden** (7)</span><span class="sxs-lookup"><span data-stu-id="e6afa-122">**Not Found** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e6afa-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e6afa-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e6afa-124">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="e6afa-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e6afa-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6afa-125">Requirements</span></span>



| <span data-ttu-id="e6afa-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6afa-126">Requirement</span></span> | <span data-ttu-id="e6afa-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e6afa-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6afa-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6afa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e6afa-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e6afa-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e6afa-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6afa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e6afa-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e6afa-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e6afa-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6afa-132">Namespace</span></span><br/>                | <span data-ttu-id="e6afa-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e6afa-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e6afa-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e6afa-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6afa-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e6afa-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6afa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e6afa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6afa-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6afa-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e6afa-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6afa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6afa-139">**CIM- \_ Auftrag**</span><span class="sxs-lookup"><span data-stu-id="e6afa-139">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

 




