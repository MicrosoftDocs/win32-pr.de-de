---
description: Aktualisiert das übergeordnete Element für das angegebene Blatt und die untergeordneten virtuellen Festplatten Dateien.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Setparameentvirtualharddisk-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetParentVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f1d14d3b2ee19a9768e1ee9ed9333a452153cc9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349400"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="61fc3-103">Setparameentvirtualharddisk-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="61fc3-103">SetParentVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="61fc3-104">Aktualisiert das übergeordnete Element für das angegebene Blatt und die untergeordneten virtuellen Festplatten Dateien.</span><span class="sxs-lookup"><span data-stu-id="61fc3-104">Updates the parent for the specified leaf and child virtual hard disk files.</span></span> <span data-ttu-id="61fc3-105">Weitere Informationen zu Nutzungseinschränkungen für diese Methode finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="61fc3-105">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="61fc3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="61fc3-106">Syntax</span></span>


```mof
uint32 SetParentVirtualHardDisk(
  [in]  string              ChildPath,
  [in]  string              ParentPath,
  [in]  string              LeafPath,
  [in]  boolean             IgnoreIDMismatch,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="61fc3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="61fc3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61fc3-108">*Childpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61fc3-108">*ChildPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61fc3-109">Ein voll qualifizierter Pfad, der den Speicherort der untergeordneten virtuellen Festplatten Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="61fc3-109">A fully qualified path that specifies the location of the child virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="61fc3-110">Element *Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61fc3-110">*ParentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61fc3-111">Ein voll qualifizierter Pfad, der den Speicherort der übergeordneten virtuellen Festplatten Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="61fc3-111">A fully qualified path that specifies the location of the parent virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="61fc3-112">*Blattpfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61fc3-112">*LeafPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61fc3-113">Ein voll qualifizierter Pfad, der den Speicherort der virtuellen Festplatten Datei für das Blatt angibt.</span><span class="sxs-lookup"><span data-stu-id="61fc3-113">A fully qualified path that specifies the location of the leaf virtual hard disk file.</span></span> <span data-ttu-id="61fc3-114">Der-Parameter kann **null** sein, wenn die virtuelle Festplatte offline ist, muss jedoch angegeben werden, wenn die virtuelle Festplatte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61fc3-114">The parameter can be **Null** if the virtual hard disk is offline, but must be specified if the virtual hard disk is in use.</span></span>

</dd> <dt>

<span data-ttu-id="61fc3-115">*Ignoreidmismatch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61fc3-115">*IgnoreIDMismatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61fc3-116">Gibt an, ob das übergeordnete Element zwangsweise festgelegt werden soll, wenn die IDs der virtuellen Datenträger nicht stimmen.</span><span class="sxs-lookup"><span data-stu-id="61fc3-116">Indicates if the parent should be forcibly set when the virtual disk identifiers do not match.</span></span> <span data-ttu-id="61fc3-117">Dieser Parameter muss mit Bedacht verwendet werden, denn wenn die neue übergeordnete virtuelle Festplatte nicht mit der ursprünglichen übergeordneten Festplatte identisch ist, können Daten beschädigt werden.</span><span class="sxs-lookup"><span data-stu-id="61fc3-117">This parameter must be used with caution because if the new parent virtual hard disk is not identical to the original parent, data corruption can occur.</span></span>

</dd> <dt>

<span data-ttu-id="61fc3-118">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="61fc3-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61fc3-119">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="61fc3-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61fc3-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61fc3-120">Return value</span></span>

<span data-ttu-id="61fc3-121">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="61fc3-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="61fc3-122">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="61fc3-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="61fc3-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-124">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="61fc3-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-125">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="61fc3-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-126">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="61fc3-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-127">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="61fc3-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-128">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="61fc3-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-129">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="61fc3-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-130">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="61fc3-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-131">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="61fc3-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-132">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="61fc3-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-133">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="61fc3-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-134">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="61fc3-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="61fc3-135">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="61fc3-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="61fc3-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61fc3-136">Remarks</span></span>

<span data-ttu-id="61fc3-137">Mit dieser Methode können nur die folgenden Typen von virtuellen Festplatten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="61fc3-137">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="61fc3-138">Differenzierende VHD</span><span class="sxs-lookup"><span data-stu-id="61fc3-138">Differencing VHD</span></span>
-   <span data-ttu-id="61fc3-139">Differenzierende vhdx</span><span class="sxs-lookup"><span data-stu-id="61fc3-139">Differencing VHDX</span></span>

<span data-ttu-id="61fc3-140">Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="61fc3-140">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="61fc3-141">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="61fc3-141">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="61fc3-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61fc3-142">Requirements</span></span>



| <span data-ttu-id="61fc3-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61fc3-143">Requirement</span></span> | <span data-ttu-id="61fc3-144">Wert</span><span class="sxs-lookup"><span data-stu-id="61fc3-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61fc3-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61fc3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="61fc3-146">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61fc3-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="61fc3-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61fc3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="61fc3-148">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61fc3-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61fc3-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="61fc3-149">Namespace</span></span><br/>                | <span data-ttu-id="61fc3-150">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="61fc3-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="61fc3-151">MOF</span><span class="sxs-lookup"><span data-stu-id="61fc3-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61fc3-152"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="61fc3-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61fc3-153">DLL</span><span class="sxs-lookup"><span data-stu-id="61fc3-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61fc3-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61fc3-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61fc3-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61fc3-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61fc3-156">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="61fc3-156">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

