---
title: Executekcc-Methode der MSAD_DomainController-Klasse
description: Ruft die DsReplicaConsistencyCheck-Funktion auf, die die Konsistenzprüfung (KCC) zum Überprüfen der Replikations Topologie aufruft.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Executekcc-Methode Active Directory
- Executekcc-Methode Active Directory, MSAD_DomainController-Klasse
- MSAD_DomainController-Klasse Active Directory, executekcc-Methode
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342841"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a><span data-ttu-id="6edd9-106">Executekcc-Methode der MSAD \_ Domain Controller-Klasse</span><span class="sxs-lookup"><span data-stu-id="6edd9-106">ExecuteKCC method of the MSAD\_DomainController class</span></span>

<span data-ttu-id="6edd9-107">Ruft die [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) -Funktion auf, die die Konsistenzprüfung (KCC) zum Überprüfen der Replikations Topologie aufruft.</span><span class="sxs-lookup"><span data-stu-id="6edd9-107">Calls the [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) function, which invokes the Knowledge Consistency Checker (KCC) to verify the replication topology.</span></span>

## <a name="syntax"></a><span data-ttu-id="6edd9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6edd9-108">Syntax</span></span>


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6edd9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6edd9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6edd9-110">*TaskID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6edd9-110">*TaskID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6edd9-111">Der Task, der von der KCC ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6edd9-111">The task that the KCC should execute.</span></span> <span data-ttu-id="6edd9-112">**DS \_ Die KCC \_ TaskID- \_ Update \_ Topologie** ist der einzige Wert, der derzeit unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6edd9-112">**DS\_KCC\_TASKID\_UPDATE\_TOPOLOGY** is the only value that is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="6edd9-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6edd9-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6edd9-114">Ein Satz von Flags, die das Verhalten der **executekcc** -Methode ändern.</span><span class="sxs-lookup"><span data-stu-id="6edd9-114">A set of flags that modify the behavior of the **ExecuteKCC** method.</span></span> <span data-ttu-id="6edd9-115">Dieser Parameter kann NULL sein oder eine Kombination aus einem oder mehreren der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6edd9-115">This parameter can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span data-ttu-id="6edd9-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS- \_ KCC- \_ Flag \_ Async \_ op**</span><span class="sxs-lookup"><span data-stu-id="6edd9-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS\_KCC\_FLAG\_ASYNC\_OP**</span></span>


</dt> <dd>

<span data-ttu-id="6edd9-117">Der Task wird in die Warteschlange eingereiht, und die Funktion wird zurückgegeben, ohne auf den Abschluss der Aufgabe zu warten</span><span class="sxs-lookup"><span data-stu-id="6edd9-117">The task is queued and then the function returns without waiting for the task to complete.</span></span>

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span data-ttu-id="6edd9-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**DS- \_ KCC- \_ Flag \_ gedämpft**</span><span class="sxs-lookup"><span data-stu-id="6edd9-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**DS\_KCC\_FLAG\_DAMPED**</span></span>


</dt> <dd>

<span data-ttu-id="6edd9-119">Der Task wird der Warteschlange nicht hinzugefügt, wenn ein anderer Task in der Warteschlange bald ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6edd9-119">The task will not be added to the queue if another queued task will run soon.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6edd9-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6edd9-120">Return value</span></span>

<span data-ttu-id="6edd9-121">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6edd9-121">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6edd9-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6edd9-122">Requirements</span></span>



| <span data-ttu-id="6edd9-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6edd9-123">Requirement</span></span> | <span data-ttu-id="6edd9-124">Wert</span><span class="sxs-lookup"><span data-stu-id="6edd9-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6edd9-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6edd9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6edd9-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6edd9-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6edd9-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6edd9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6edd9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6edd9-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6edd9-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6edd9-129">Namespace</span></span><br/>                | <span data-ttu-id="6edd9-130">\\Microsoftactivedirectory-Stammverzeichnis</span><span class="sxs-lookup"><span data-stu-id="6edd9-130">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="6edd9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6edd9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6edd9-132"><dt>ReplProv. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6edd9-132"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="6edd9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6edd9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6edd9-134"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6edd9-134"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6edd9-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6edd9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6edd9-136">**MSAD \_ Domain Controller**</span><span class="sxs-lookup"><span data-stu-id="6edd9-136">**MSAD\_DomainController**</span></span>](msad-domaincontroller.md)
</dt> </dl>

 

 





