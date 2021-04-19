---
description: Stellt das angegebene PCI-Gerät bereit, sodass es vom Host Computersystem verwendet werden kann.
ms.assetid: 2a07174e-c221-4c04-81b8-5968aa67e235
title: Mountassignabledevice-Methode der Msvm_AssignableDeviceService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.MountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: df5f8a337fbf4baf47a4f695322944ed0b97e82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373139"
---
# <a name="mountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="aa9c7-103">Mountassignabledevice-Methode der MSVM- \_ Klasse "accessabledeviceservice"</span><span class="sxs-lookup"><span data-stu-id="aa9c7-103">MountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="aa9c7-104">Stellt das angegebene PCI-Gerät bereit, sodass es vom Host Computersystem verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="aa9c7-104">Mounts the specified PCI device so that it can be used by the host computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa9c7-105">Syntax</span></span>


```mof
uint32 MountAssignableDevice(
  [in]  string              DeviceInstancePath,
  [in]  string              DeviceLocationPath,
  [out] string              MountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="aa9c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa9c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa9c7-107">Geräte *Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa9c7-107">*DeviceInstancePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9c7-108">Zeichenfolge, die den geräteinstanzpfad zu einem Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="aa9c7-108">String containing the device instance path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="aa9c7-109">*Devicelocationpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa9c7-109">*DeviceLocationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9c7-110">Zeichenfolge, die den Geräte Speicherort Pfad zu einem Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="aa9c7-110">String containing the device location path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="aa9c7-111">*Mountedbinviceinstancepath* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="aa9c7-111">*MountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9c7-112">Zeichenfolge, die den geräteinstanzpfad zum eingebundenen Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="aa9c7-112">String containing the device instance path to the mounted device.</span></span>

</dd> <dt>

<span data-ttu-id="aa9c7-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="aa9c7-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9c7-114">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="aa9c7-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa9c7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa9c7-115">Return value</span></span>

<span data-ttu-id="aa9c7-116">Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aa9c7-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="aa9c7-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="aa9c7-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="aa9c7-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="aa9c7-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="aa9c7-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="aa9c7-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="aa9c7-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="aa9c7-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="aa9c7-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-125">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="aa9c7-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="aa9c7-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="aa9c7-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="aa9c7-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="aa9c7-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="aa9c7-130">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="aa9c7-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="aa9c7-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa9c7-131">Requirements</span></span>



| <span data-ttu-id="aa9c7-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa9c7-132">Requirement</span></span> | <span data-ttu-id="aa9c7-133">Wert</span><span class="sxs-lookup"><span data-stu-id="aa9c7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9c7-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa9c7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="aa9c7-135">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa9c7-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="aa9c7-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa9c7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="aa9c7-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="aa9c7-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="aa9c7-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa9c7-138">Namespace</span></span><br/>                | <span data-ttu-id="aa9c7-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="aa9c7-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aa9c7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="aa9c7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa9c7-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aa9c7-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa9c7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="aa9c7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa9c7-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa9c7-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aa9c7-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa9c7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9c7-145">**MSVM zugewiesen \_ abledebug Service**</span><span class="sxs-lookup"><span data-stu-id="aa9c7-145">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




