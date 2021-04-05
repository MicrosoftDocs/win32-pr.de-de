---
description: Ruft die Gesamtgröße der Systemdateien des virtuellen Computers ab.
ms.assetid: 492aa0df-1562-4d83-a0ea-43776b12c1b1
title: Getsizeofsystemfiles-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSizeOfSystemFiles
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ed9fcf93093e17c2989121bf33ee5f5fbf09bab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752217"
---
# <a name="getsizeofsystemfiles-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="8e317-103">Getsizeofsystemfiles-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="8e317-103">GetSizeOfSystemFiles method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="8e317-104">Ruft die Gesamtgröße der Systemdateien des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="8e317-104">Retrieves the total size of the system files of virtual machine.</span></span> <span data-ttu-id="8e317-105">Dies schließt die Konfigurations-und die gespeicherten Zustands Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="8e317-105">These include the configuration and saved state files.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e317-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e317-106">Syntax</span></span>


```mof
uint32 GetSizeOfSystemFiles(
  [in]  CIM_VirtualSystemSettingData REF Vssd,
  [out] uint64                           Size
);
```



## <a name="parameters"></a><span data-ttu-id="8e317-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e317-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e317-108">*VSSD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e317-108">*Vssd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e317-109">Ein Verweis auf die [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Instanz, deren Systemdateien abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8e317-109">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance whose system files size are to be retrieved.</span></span> <span data-ttu-id="8e317-110">Diese Instanz kann entweder die aktuelle Instanziierung der virtuellen Maschine oder eine Instanz einer Momentaufnahme eines virtuellen Computers darstellen.</span><span class="sxs-lookup"><span data-stu-id="8e317-110">This instance may represent either the current instantiation of the virtual machine, or an instance of a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="8e317-111">*Größe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8e317-111">*Size* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e317-112">Die Gesamtgröße der Systemdateien in Bytes.</span><span class="sxs-lookup"><span data-stu-id="8e317-112">The total size, in bytes, of system files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e317-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e317-113">Return value</span></span>

<span data-ttu-id="8e317-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="8e317-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8e317-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="8e317-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8e317-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="8e317-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8e317-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="8e317-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8e317-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="8e317-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8e317-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="8e317-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8e317-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="8e317-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8e317-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="8e317-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8e317-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="8e317-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8e317-123">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="8e317-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8e317-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="8e317-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8e317-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="8e317-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8e317-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="8e317-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8e317-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="8e317-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8e317-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e317-128">Requirements</span></span>



| <span data-ttu-id="8e317-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e317-129">Requirement</span></span> | <span data-ttu-id="8e317-130">Wert</span><span class="sxs-lookup"><span data-stu-id="8e317-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e317-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e317-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8e317-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e317-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8e317-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e317-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8e317-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e317-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e317-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e317-135">Namespace</span></span><br/>                | <span data-ttu-id="8e317-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8e317-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8e317-137">MOF</span><span class="sxs-lookup"><span data-stu-id="8e317-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e317-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8e317-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e317-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8e317-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e317-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8e317-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8e317-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e317-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e317-142">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="8e317-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

