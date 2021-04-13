---
description: Aktualisiert die Einstellungen für eine virtuelle Festplatte.
ms.assetid: 10f80313-bc78-447e-bdf2-5635d7354e3c
title: Setvirtualharddisksettingdata-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 969e9019d05b49f2f171f2177e1e74f135e212da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349029"
---
# <a name="setvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="72e39-103">Setvirtualharddisksettingdata-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="72e39-103">SetVirtualHardDiskSettingData method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="72e39-104">Aktualisiert die Einstellungen für eine virtuelle Festplatte.</span><span class="sxs-lookup"><span data-stu-id="72e39-104">Updates the settings for a virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="72e39-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72e39-105">Syntax</span></span>


```mof
uint32 SetVirtualHardDiskSettingData(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="72e39-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72e39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72e39-107">*Virtualdisksettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72e39-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72e39-108">Eine Zeichen folgen Darstellung der [**MSVM \_ virtualharddisksettingdata**](msvm-virtualharddisksettingdata.md) -Klasse, die die zu aktualisierenden virtuellen Festplatte angibt, die die neuen Einstellungsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="72e39-108">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the virtual hard disk to update and that contains the new setting data.</span></span> <span data-ttu-id="72e39-109">Nur die Eigenschaften **path**, **physicalsectorsize** oder **virtualdiskid** können mit dieser Methode aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="72e39-109">Only the **ParentPath**, **PhysicalSectorSize**, or **VirtualDiskId** properties can be updated with this method.</span></span> <span data-ttu-id="72e39-110">Sie können diese Eigenschaften nicht mit einem Methoden aufzurufen aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="72e39-110">You can't update these properties with one method call.</span></span> <span data-ttu-id="72e39-111">Sie können eine dieser Eigenschaften nur mit einem einzigen Methoden aufzurufen aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="72e39-111">You can only update one of these properties with a single method call.</span></span>

</dd> <dt>

<span data-ttu-id="72e39-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="72e39-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72e39-113">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="72e39-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72e39-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72e39-114">Return value</span></span>

<span data-ttu-id="72e39-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="72e39-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="72e39-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="72e39-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="72e39-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="72e39-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="72e39-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="72e39-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="72e39-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="72e39-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="72e39-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="72e39-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="72e39-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="72e39-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="72e39-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="72e39-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="72e39-129">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="72e39-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="72e39-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72e39-130">Remarks</span></span>

<span data-ttu-id="72e39-131">Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="72e39-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="72e39-132">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="72e39-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="72e39-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72e39-133">Requirements</span></span>



| <span data-ttu-id="72e39-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72e39-134">Requirement</span></span> | <span data-ttu-id="72e39-135">Wert</span><span class="sxs-lookup"><span data-stu-id="72e39-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72e39-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72e39-136">Minimum supported client</span></span><br/> | <span data-ttu-id="72e39-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72e39-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="72e39-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72e39-138">Minimum supported server</span></span><br/> | <span data-ttu-id="72e39-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72e39-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72e39-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="72e39-140">Namespace</span></span><br/>                | <span data-ttu-id="72e39-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="72e39-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="72e39-142">MOF</span><span class="sxs-lookup"><span data-stu-id="72e39-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72e39-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="72e39-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72e39-144">DLL</span><span class="sxs-lookup"><span data-stu-id="72e39-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72e39-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72e39-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72e39-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72e39-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e39-147">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="72e39-147">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

