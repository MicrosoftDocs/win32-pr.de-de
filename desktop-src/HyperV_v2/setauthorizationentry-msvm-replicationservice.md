---
description: Legt den Replikations Autorisierungs Eintrag für einen virtuellen Computer fest.
ms.assetid: 39b6b0c4-5515-4863-9038-4c37421abe65
title: Setauthorizationentry-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 03b2c2c37a38e957a1b560e2314845abf204ee01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357737"
---
# <a name="setauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="d3aa9-103">Setauthorizationentry-Methode der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="d3aa9-103">SetAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="d3aa9-104">Legt den Replikations Autorisierungs Eintrag für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="d3aa9-104">Sets the replication authorization entry for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3aa9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3aa9-105">Syntax</span></span>


```mof
uint32 SetAuthorizationEntry(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 AuthorizationEntry,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d3aa9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3aa9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3aa9-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3aa9-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3aa9-108">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den der Autorisierungs Eintrag festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3aa9-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to set the authorization entry for.</span></span>

</dd> <dt>

<span data-ttu-id="d3aa9-109">*Authorizationentry* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3aa9-109">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3aa9-110">Eine Zeichen folgen Darstellung einer Instanz der [**MSVM \_ replicationauthorizationsettingdata**](msvm-replicationauthorizationsettingdata.md) -Klasse, die den Autorisierungs Eintrag definiert, der für den virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3aa9-110">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be used for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="d3aa9-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d3aa9-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3aa9-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="d3aa9-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3aa9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3aa9-113">Return value</span></span>

<span data-ttu-id="d3aa9-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="d3aa9-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d3aa9-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="d3aa9-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="d3aa9-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="d3aa9-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="d3aa9-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="d3aa9-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="d3aa9-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="d3aa9-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="d3aa9-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-123">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="d3aa9-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="d3aa9-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="d3aa9-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="d3aa9-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="d3aa9-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d3aa9-128">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="d3aa9-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d3aa9-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3aa9-129">Requirements</span></span>



| <span data-ttu-id="d3aa9-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3aa9-130">Requirement</span></span> | <span data-ttu-id="d3aa9-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d3aa9-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3aa9-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3aa9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d3aa9-133">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3aa9-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d3aa9-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3aa9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d3aa9-135">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3aa9-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3aa9-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3aa9-136">Namespace</span></span><br/>                | <span data-ttu-id="d3aa9-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d3aa9-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d3aa9-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d3aa9-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3aa9-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d3aa9-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3aa9-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d3aa9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3aa9-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3aa9-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d3aa9-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3aa9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3aa9-143">**Addauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="d3aa9-143">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="d3aa9-144">**Modifyauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="d3aa9-144">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="d3aa9-145">**Removeauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="d3aa9-145">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="d3aa9-146">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="d3aa9-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

