---
description: Abfragen von Cluster Informationen vom Hyper-V-Host zum Gast.
ms.assetid: 28983984-a2af-4eab-8b1f-2f7d6a3d70ea
title: Queryguestclusterinformation-Methode der Msvm_VssService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService.QueryGuestClusterInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 36f88441729cc1e6e36bcad9ca84b46049bce2a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525178"
---
# <a name="queryguestclusterinformation-method-of-the-msvm_vssservice-class"></a><span data-ttu-id="19a4d-103">Queryguestclusterinformation-Methode der MSVM- \_ VssService-Klasse</span><span class="sxs-lookup"><span data-stu-id="19a4d-103">QueryGuestClusterInformation method of the Msvm\_VssService class</span></span>

<span data-ttu-id="19a4d-104">Abfragen von Cluster Informationen vom Hyper-V-Host zum Gast.</span><span class="sxs-lookup"><span data-stu-id="19a4d-104">Querying cluster information from the Hyper-V host to the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="19a4d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19a4d-105">Syntax</span></span>


```mof
uint32 QueryGuestClusterInformation(
  [out] Msvm_GuestClusterInformation GuestClusterInformation
);
```



## <a name="parameters"></a><span data-ttu-id="19a4d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19a4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19a4d-107">*Guestclusterinformation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="19a4d-107">*GuestClusterInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19a4d-108">Bei Erfolg enthält eine [**MSVM \_ guestclusterinformation**](msvm-guestclusterinformation.md) , die den Gast Cluster beschreibt.</span><span class="sxs-lookup"><span data-stu-id="19a4d-108">On success, contains an [**Msvm\_GuestClusterInformation**](msvm-guestclusterinformation.md) that describes the guest cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19a4d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19a4d-109">Return value</span></span>

<span data-ttu-id="19a4d-110">Bei Erfolg wird 0 (abgeschlossen ohne Fehler) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="19a4d-110">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="19a4d-111">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="19a4d-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="19a4d-112">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="19a4d-112">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="19a4d-113">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="19a4d-113">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="19a4d-114">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="19a4d-114">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="19a4d-115">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="19a4d-115">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="19a4d-116">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="19a4d-116">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="19a4d-117">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="19a4d-117">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="19a4d-118">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="19a4d-118">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="19a4d-119">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="19a4d-119">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="19a4d-120">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="19a4d-120">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="19a4d-121">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="19a4d-121">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="19a4d-122">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="19a4d-122">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="19a4d-123">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="19a4d-123">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="19a4d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19a4d-124">Requirements</span></span>



| <span data-ttu-id="19a4d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19a4d-125">Requirement</span></span> | <span data-ttu-id="19a4d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="19a4d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a4d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19a4d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="19a4d-128">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19a4d-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="19a4d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19a4d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="19a4d-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="19a4d-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="19a4d-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="19a4d-131">Namespace</span></span><br/>                | <span data-ttu-id="19a4d-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="19a4d-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="19a4d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="19a4d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19a4d-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="19a4d-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="19a4d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="19a4d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19a4d-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="19a4d-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="19a4d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19a4d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19a4d-138">**MSVM- \_ VssService**</span><span class="sxs-lookup"><span data-stu-id="19a4d-138">**Msvm\_VssService**</span></span>](msvm-vssservice.md)
</dt> </dl>

 

 




