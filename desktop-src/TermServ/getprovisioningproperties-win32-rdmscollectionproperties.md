---
title: Getprovisioningproperties-Methode der Win32_RDMSCollectionProperties-Klasse
description: Ruft die Bereitstellungs Eigenschaften der Sammlung virtueller Desktops ab.
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- Getprovisioningproperties-Methode Remotedesktopdienste
- Getprovisioningproperties-Methode Remotedesktopdienste, Win32_RDMSCollectionProperties-Klasse
- Win32_RDMSCollectionProperties-Klasse Remotedesktopdienste, getprovisioningproperties-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ca58f82d2918441e5da3cf53d442497c1a6a2eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337529"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a><span data-ttu-id="a1425-106">Getprovisioningproperties-Methode der Win32- \_ Klasse rdmscollectionproperties</span><span class="sxs-lookup"><span data-stu-id="a1425-106">GetProvisioningProperties method of the Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="a1425-107">Ruft die Bereitstellungs Eigenschaften der Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="a1425-107">Retrieves the provisioning properties of the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1425-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1425-108">Syntax</span></span>


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a><span data-ttu-id="a1425-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1425-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1425-110">*Poolvhdtype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1425-110">*PoolVhdType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1425-111">Gibt das VHD-Format (virtuelle Festplatte) des virtuellen Computerpools in der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="a1425-111">Specifies the VHD (virtual hard disk) format of the virtual machine pool in the collection.</span></span>

<dt>

<span data-ttu-id="a1425-112">Klon</span><span class="sxs-lookup"><span data-stu-id="a1425-112">Clone</span></span>
</dt> <dd>

<span data-ttu-id="a1425-113">Eine geklonte VHD.</span><span class="sxs-lookup"><span data-stu-id="a1425-113">A cloned VHD.</span></span>

</dd> <dt>

<span data-ttu-id="a1425-114">Diffdisk</span><span class="sxs-lookup"><span data-stu-id="a1425-114">DiffDisk</span></span>
</dt> <dd>

<span data-ttu-id="a1425-115">Eine differenzierende VHD.</span><span class="sxs-lookup"><span data-stu-id="a1425-115">A differencing VHD.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a1425-116">*Mastervmlocation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1425-116">*MasterVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1425-117">Empfängt den Pfad zum Master-VM-Image.</span><span class="sxs-lookup"><span data-stu-id="a1425-117">Receives the path to the master VM image.</span></span>

</dd> <dt>

<span data-ttu-id="a1425-118">*NamePrefix* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1425-118">*NamePrefix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1425-119">Empfängt das namens Präfix, das am Anfang der Namen virtueller Computer angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1425-119">Receives the name prefix to append to the beginning of virtual machine names.</span></span>

</dd> <dt>

<span data-ttu-id="a1425-120">*Namestartindex* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1425-120">*NameStartIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1425-121">Start Index.</span><span class="sxs-lookup"><span data-stu-id="a1425-121">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="a1425-122">*Localvmlocation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1425-122">*LocalVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1425-123">Empfängt den lokalen Pfad zu den virtuellen Maschinen auf den Hyper-V-Servern.</span><span class="sxs-lookup"><span data-stu-id="a1425-123">Receives the local path to the virtual machines on the Hyper-V servers.</span></span> <span data-ttu-id="a1425-124">Wenn dieser Parameter auf **null** festgelegt ist oder leer ist, wird das Standardverzeichnis der virtuellen Maschine verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1425-124">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="a1425-125">*Localgoldvmlocation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1425-125">*LocalGoldVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1425-126">Empfängt den lokalen Pfad zum Golden VHD-Abbild, wenn der *poolvhdtpe* -Parameter auf "diffdisk" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a1425-126">Receives the local path to the golden VHD image when the *PoolVhdTpe* parameter is set to "DiffDisk".</span></span> <span data-ttu-id="a1425-127">Wenn dieser Parameter auf **null** festgelegt ist oder leer ist, wird das Standardverzeichnis der virtuellen Maschine verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1425-127">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="a1425-128">*Runfromsmb* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1425-128">*RunFromSMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1425-129">Empfängt einen Wert, der angibt, ob die Auflistung von einer SMB-Freigabe (Server Message Block) ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1425-129">Receives a value that indicates whether to run the collection from an Server Message Block (SMB) share.</span></span> <span data-ttu-id="a1425-130">" **True** ", um die virtuellen Computer über eine SBM-Freigabe auszuführen. sonst **False**.</span><span class="sxs-lookup"><span data-stu-id="a1425-130">**TRUE** to run the virtual machines from an SBM share; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a1425-131">*Smblozierung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1425-131">*SMBLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1425-132">Empfängt den Pfad zur SMB-Freigabe, wenn die SMB-Freigabe aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a1425-132">Receives the path to the SMB share if SMB sharing is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="a1425-133">*Smbstreaming* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1425-133">*SMBStreaming* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1425-134">Empfängt einen Wert, der angibt, ob SMB-Streaming aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a1425-134">Receives a value that indicates whether SMB streaming is enabled.</span></span> <span data-ttu-id="a1425-135">**True** , wenn die SMB-Freigabe aktiviert ist. sonst **False**.</span><span class="sxs-lookup"><span data-stu-id="a1425-135">**TRUE** if SMB sharing is enabled; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a1425-136">*Vmdomain* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1425-136">*VmDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1425-137">Empfängt den Domänen Namen der virtuellen Computer in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="a1425-137">Receives the domain name of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="a1425-138">*Vmou* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1425-138">*VmOU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1425-139">Empfängt die Active Directory Organisationseinheit (OU) der virtuellen Computer in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="a1425-139">Receives the Active Directory organization unit (OU) of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="a1425-140">*ProductKey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1425-140">*ProductKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1425-141">Empfängt die Betriebssystem-Product Keys für die virtuellen Computer in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="a1425-141">Receives the OS product keys for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1425-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1425-142">Return value</span></span>

<span data-ttu-id="a1425-143">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1425-143">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1425-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1425-144">Requirements</span></span>



| <span data-ttu-id="a1425-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1425-145">Requirement</span></span> | <span data-ttu-id="a1425-146">Wert</span><span class="sxs-lookup"><span data-stu-id="a1425-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1425-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1425-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a1425-148">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a1425-148">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a1425-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1425-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a1425-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1425-150">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a1425-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1425-151">Namespace</span></span><br/>                | <span data-ttu-id="a1425-152">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="a1425-152">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a1425-153">MOF</span><span class="sxs-lookup"><span data-stu-id="a1425-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1425-154"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a1425-154"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1425-155">DLL</span><span class="sxs-lookup"><span data-stu-id="a1425-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1425-156"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1425-156"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a1425-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1425-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1425-158">**Win32- \_ rdmscollectionproperties**</span><span class="sxs-lookup"><span data-stu-id="a1425-158">**Win32\_RDMSCollectionProperties**</span></span>](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





