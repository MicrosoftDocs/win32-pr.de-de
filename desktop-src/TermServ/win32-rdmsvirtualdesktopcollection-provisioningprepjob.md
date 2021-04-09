---
title: Provisioningprepjob-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Erstellt einen Bereitstellungs Auftrag für virtuelle Desktops.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- Provisioningprepjob-Methode Remotedesktopdienste
- Provisioningprepjob-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Schnittstelle
- Win32_RDMSVirtualDesktopCollection Interface Remotedesktopdienste, provisioningprepjob-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9727dec0e31dd199f324ed01a4510041ba3558f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949793"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="e47e4-106">Provisioningprepjob-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="e47e4-106">ProvisioningPrepJob method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="e47e4-107">Erstellt einen Bereitstellungs Auftrag für virtuelle Desktops.</span><span class="sxs-lookup"><span data-stu-id="e47e4-107">Creates a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="e47e4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e47e4-108">Syntax</span></span>


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="e47e4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e47e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e47e4-110">*Collectionalias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e47e4-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e47e4-111">Der Alias der Auflistung, die den virtuellen Desktop hostet.</span><span class="sxs-lookup"><span data-stu-id="e47e4-111">The alias of the collection that hosts the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="e47e4-112">*Vmhostname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e47e4-112">*VMHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e47e4-113">Der Hostname des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="e47e4-113">The virtual machine host name.</span></span>

</dd> <dt>

<span data-ttu-id="e47e4-114">*VMName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e47e4-114">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e47e4-115">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="e47e4-115">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e47e4-116">*Exporttolokation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e47e4-116">*ExportToLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e47e4-117">Der vollständige Pfad des Speicher Orts, an den der Bereitstellungs Auftrag exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e47e4-117">The full path the location to export the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="e47e4-118">*bsystreup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e47e4-118">*bSysPrep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e47e4-119">Gibt an, ob der Bereitstellungs Auftrag eine System Vorbereitungs Bereitstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e47e4-119">Indicates whether the provisioning job represents a Sysprep deployment.</span></span>

</dd> <dt>

<span data-ttu-id="e47e4-120">*MachineName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e47e4-120">*MachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e47e4-121">Der Computername des Computers, der die virtuelle Maschine hostet.</span><span class="sxs-lookup"><span data-stu-id="e47e4-121">The machine name of the computer that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e47e4-122">*Benutzername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e47e4-122">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e47e4-123">Der Benutzername des Administrators der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="e47e4-123">The user name of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e47e4-124">*Kennwort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e47e4-124">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e47e4-125">Das Kennwort des Administrators des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="e47e4-125">The password of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e47e4-126">*Jobguid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e47e4-126">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e47e4-127">Die **GUID** , die den Bereitstellungs Auftrag eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e47e4-127">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e47e4-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e47e4-128">Return value</span></span>

<span data-ttu-id="e47e4-129">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e47e4-129">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e47e4-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e47e4-130">Requirements</span></span>



| <span data-ttu-id="e47e4-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e47e4-131">Requirement</span></span> | <span data-ttu-id="e47e4-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e47e4-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e47e4-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e47e4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e47e4-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e47e4-134">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e47e4-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e47e4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e47e4-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e47e4-136">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="e47e4-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="e47e4-137">Namespace</span></span><br/>                | <span data-ttu-id="e47e4-138">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="e47e4-138">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e47e4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e47e4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e47e4-140"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e47e4-140"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e47e4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e47e4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e47e4-142"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e47e4-142"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e47e4-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e47e4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e47e4-144">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="e47e4-144">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





