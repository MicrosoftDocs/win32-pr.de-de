---
title: Getpatchproperties-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Ruft die Eigenschaften eines Bereitstellungs Auftrags für Software Updates für die virtuellen Computer in einer Sammlung virtueller Desktops ab.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- Getpatchproperties-Methode Remotedesktopdienste
- Getpatchproperties-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, getpatchproperties-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f0ca45c97512818aa5f8a9ea851d18fa5554c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518185"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="db6a9-106">Getpatchproperties-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="db6a9-106">GetPatchProperties method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="db6a9-107">Ruft die Eigenschaften eines Bereitstellungs Auftrags für Software Updates für die virtuellen Computer in einer Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="db6a9-107">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="db6a9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="db6a9-108">Syntax</span></span>


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a><span data-ttu-id="db6a9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="db6a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6a9-110">*StartTime* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="db6a9-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db6a9-111">Das Datum und die Uhrzeit der Installation der Updates.</span><span class="sxs-lookup"><span data-stu-id="db6a9-111">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="db6a9-112">*Forcelogofftime* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="db6a9-112">*ForceLogOffTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db6a9-113">Das Datum und die Uhrzeit, zu denen das Systembenutzer der virtuellen Maschinen abmeldet.</span><span class="sxs-lookup"><span data-stu-id="db6a9-113">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="db6a9-114">*Jobguid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="db6a9-114">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db6a9-115">Eine **GUID** , die den Bereitstellungs Auftrag eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="db6a9-115">A **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="db6a9-116">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="db6a9-116">*State* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db6a9-117">Der Status des Bereitstellungs Auftrags.</span><span class="sxs-lookup"><span data-stu-id="db6a9-117">The state of the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db6a9-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db6a9-118">Return value</span></span>

<span data-ttu-id="db6a9-119">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db6a9-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="db6a9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db6a9-120">Requirements</span></span>



| <span data-ttu-id="db6a9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db6a9-121">Requirement</span></span> | <span data-ttu-id="db6a9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="db6a9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="db6a9-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db6a9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="db6a9-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="db6a9-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="db6a9-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db6a9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="db6a9-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db6a9-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="db6a9-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="db6a9-127">Namespace</span></span><br/>                | <span data-ttu-id="db6a9-128">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="db6a9-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="db6a9-129">MOF</span><span class="sxs-lookup"><span data-stu-id="db6a9-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db6a9-130"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="db6a9-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="db6a9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="db6a9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db6a9-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db6a9-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="db6a9-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db6a9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6a9-134">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="db6a9-134">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





