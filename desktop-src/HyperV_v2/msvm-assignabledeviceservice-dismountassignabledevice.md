---
description: Hebt die Einbindung des angegebenen PCI-Geräts auf, sodass es zugewiesen werden kann.
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: Dismountassignabledevice-Methode der Msvm_AssignableDeviceService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 53036cd09113430d1045c8e9eae7a8d782b35960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368030"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="bc12a-103">Dismountassignabledevice-Methode der MSVM- \_ Klasse "accessabledeviceservice"</span><span class="sxs-lookup"><span data-stu-id="bc12a-103">DismountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="bc12a-104">Hebt die Einbindung des angegebenen PCI-Geräts auf, sodass es zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc12a-104">Dismounts the specified PCI device so that it can be assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc12a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc12a-105">Syntax</span></span>


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bc12a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc12a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc12a-107">*Dismountsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc12a-107">*DismountSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc12a-108">Eingebettete Instanz eines Einstellungsdaten Objekts, das das PCI-Gerät angibt, dessen Einbindung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc12a-108">Embedded instance of a setting data object that specifies the PCI device to dismount.</span></span>

</dd> <dt>

<span data-ttu-id="bc12a-109">*Dismountedbinviceinstancepath* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc12a-109">*DismountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc12a-110">Eine Zeichenfolge, die den geräteinstanzpfad zum Gerät der disbereit Stellung enthält.</span><span class="sxs-lookup"><span data-stu-id="bc12a-110">String containing the device instance path to the dismounted device.</span></span>

</dd> <dt>

<span data-ttu-id="bc12a-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc12a-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc12a-112">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="bc12a-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc12a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc12a-113">Return value</span></span>

<span data-ttu-id="bc12a-114">Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bc12a-114">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="bc12a-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="bc12a-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="bc12a-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="bc12a-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="bc12a-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="bc12a-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="bc12a-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="bc12a-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="bc12a-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-123">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="bc12a-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="bc12a-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="bc12a-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="bc12a-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="bc12a-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="bc12a-128">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="bc12a-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bc12a-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc12a-129">Requirements</span></span>



| <span data-ttu-id="bc12a-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc12a-130">Requirement</span></span> | <span data-ttu-id="bc12a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="bc12a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc12a-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc12a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bc12a-133">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc12a-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bc12a-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc12a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bc12a-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bc12a-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bc12a-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc12a-136">Namespace</span></span><br/>                | <span data-ttu-id="bc12a-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="bc12a-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bc12a-138">MOF</span><span class="sxs-lookup"><span data-stu-id="bc12a-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc12a-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bc12a-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc12a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="bc12a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc12a-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc12a-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc12a-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc12a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc12a-143">**MSVM zugewiesen \_ abledebug Service**</span><span class="sxs-lookup"><span data-stu-id="bc12a-143">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




