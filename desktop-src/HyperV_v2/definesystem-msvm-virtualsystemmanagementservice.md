---
description: Erstellt eine neue Instanz eines virtuellen Computers.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Definesystem-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 965d24313607a767d546503d005a6493234b2f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217187"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="41e01-103">Definesystem-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="41e01-103">DefineSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="41e01-104">Erstellt eine neue Instanz eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="41e01-104">Creates a new virtual machine instance.</span></span> <span data-ttu-id="41e01-105">Eigenschaften, die nicht angegeben sind, werden mit Standardwerten aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="41e01-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e01-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="41e01-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="41e01-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="41e01-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e01-108">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41e01-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e01-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41e01-109">Type: **string**</span></span>

<span data-ttu-id="41e01-110">Eine eingebettete Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die verwendet wird, um die Attribute der zu erstellenden virtuellen Maschine zu definieren.</span><span class="sxs-lookup"><span data-stu-id="41e01-110">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is used to define the attributes of the virtual machine to be created.</span></span> <span data-ttu-id="41e01-111">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="41e01-111">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="41e01-112">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41e01-112">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e01-113">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="41e01-113">Type: **string\[\]**</span></span>

<span data-ttu-id="41e01-114">Eine Reihe von eingebetteten Instanzen der [**MSVM \_ resourcezucationsettingdata**](msvm-resourceallocationsettingdata.md) -Klasse (oder abgeleitete Klassen).</span><span class="sxs-lookup"><span data-stu-id="41e01-114">A number of embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class (or derived classes thereof).</span></span> <span data-ttu-id="41e01-115">Diese Instanzen beschreiben die virtuellen Ressourcen des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="41e01-115">Together these instances describe the virtual resources of the virtual machine.</span></span> <span data-ttu-id="41e01-116">Ein Standardsatz von Geräten wird für den virtuellen Computer erstellt, unabhängig davon, ob dieser Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="41e01-116">A default set of devices will be created for the virtual machine regardless of whether this parameter is set.</span></span> <span data-ttu-id="41e01-117">Beispielsweise werden Prozessor und Arbeitsspeicher automatisch mit Standardwerten erstellt und konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="41e01-117">For example, processor and memory are automatically created and configured with default values.</span></span>

</dd> <dt>

<span data-ttu-id="41e01-118">*Referenceconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41e01-118">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e01-119">Typ: **CIM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="41e01-119">Type: **CIM\_VirtualSystemSettingData**</span></span>

<span data-ttu-id="41e01-120">Ein Verweis auf eine Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, bei der es sich um das Objekt der obersten Ebene einer Referenz Konfiguration für virtuelle Maschinen handelt.</span><span class="sxs-lookup"><span data-stu-id="41e01-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is the top level object of a reference virtual machine configuration.</span></span> <span data-ttu-id="41e01-121">Die Referenz Konfiguration wird verwendet, um die Konfiguration der neuen virtuellen Maschine zu ergänzen, wenn die Parameter " *SystemSettings* " und " *resourcesettings* " keine entsprechenden Informationen bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="41e01-121">The reference configuration is used to complement the configuration of the new virtual machine if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="41e01-122">*Resultingsystem* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="41e01-122">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41e01-123">Typ: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="41e01-123">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="41e01-124">Ein Verweis auf eine Instanz der [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse, die den neu erstellten virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="41e01-124">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly created virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="41e01-125">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="41e01-125">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41e01-126">Typ: **CIM \_ bettejob**</span><span class="sxs-lookup"><span data-stu-id="41e01-126">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="41e01-127">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="41e01-127">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41e01-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41e01-128">Return value</span></span>

<span data-ttu-id="41e01-129">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41e01-129">Type: **uint32**</span></span>

<span data-ttu-id="41e01-130">Wenn diese Methode synchron ausgeführt wird, wird 0 zurückgegeben, wenn Sie erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41e01-130">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="41e01-131">Wenn diese Methode asynchron ausgeführt wird, wird 4096 zurückgegeben, und der *Auftrags* Ausgabeparameter kann verwendet werden, um den Fortschritt des asynchronen Vorgangs zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="41e01-131">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="41e01-132">Jeder andere Rückgabewert gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="41e01-132">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="41e01-133">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="41e01-133">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41e01-134">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="41e01-134">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41e01-135">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="41e01-135">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41e01-136">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="41e01-136">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41e01-137">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="41e01-137">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="41e01-138">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="41e01-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41e01-139">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="41e01-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="41e01-140">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="41e01-140">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="41e01-141">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="41e01-141">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="41e01-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41e01-142">Remarks</span></span>

<span data-ttu-id="41e01-143">Der Zugriff auf die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="41e01-143">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="41e01-144">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="41e01-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="41e01-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41e01-145">Requirements</span></span>



| <span data-ttu-id="41e01-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41e01-146">Requirement</span></span> | <span data-ttu-id="41e01-147">Wert</span><span class="sxs-lookup"><span data-stu-id="41e01-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41e01-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41e01-148">Minimum supported client</span></span><br/> | <span data-ttu-id="41e01-149">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41e01-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="41e01-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41e01-150">Minimum supported server</span></span><br/> | <span data-ttu-id="41e01-151">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41e01-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41e01-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="41e01-152">Namespace</span></span><br/>                | <span data-ttu-id="41e01-153">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="41e01-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="41e01-154">MOF</span><span class="sxs-lookup"><span data-stu-id="41e01-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41e01-155"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="41e01-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41e01-156">DLL</span><span class="sxs-lookup"><span data-stu-id="41e01-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41e01-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41e01-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="41e01-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41e01-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e01-159">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="41e01-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

