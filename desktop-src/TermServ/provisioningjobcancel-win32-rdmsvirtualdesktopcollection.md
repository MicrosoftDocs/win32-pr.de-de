---
title: Provisioningjobcancel-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Bricht einen Bereitstellungs Auftrag für virtuelle Desktops ab.
ms.assetid: 933ea0f3-b916-4e70-89de-597f9eb23976
ms.tgt_platform: multiple
keywords:
- Provisioningjobcancel-Methode Remotedesktopdienste
- Provisioningjobcancel-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, provisioningjobcancel-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobCancel
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f414bcdc264d682817898bae98fcf60a716452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341808"
---
# <a name="provisioningjobcancel-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="11d84-106">Provisioningjobcancel-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="11d84-106">ProvisioningJobCancel method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="11d84-107">Bricht einen Bereitstellungs Auftrag für virtuelle Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="11d84-107">Cancels a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="11d84-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="11d84-108">Syntax</span></span>


```mof
uint32 ProvisioningJobCancel(
  [in] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="11d84-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="11d84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11d84-110">*Jobguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11d84-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d84-111">Die **GUID** , die den Abbruch des Bereitstellungs Auftrags eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="11d84-111">The **GUID** that uniquely identifies the provisioning job to cancel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11d84-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11d84-112">Return value</span></span>

<span data-ttu-id="11d84-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="11d84-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="11d84-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11d84-114">Requirements</span></span>



| <span data-ttu-id="11d84-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11d84-115">Requirement</span></span> | <span data-ttu-id="11d84-116">Wert</span><span class="sxs-lookup"><span data-stu-id="11d84-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="11d84-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11d84-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11d84-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="11d84-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="11d84-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11d84-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11d84-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11d84-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="11d84-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="11d84-121">Namespace</span></span><br/>                | <span data-ttu-id="11d84-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="11d84-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="11d84-123">MOF</span><span class="sxs-lookup"><span data-stu-id="11d84-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11d84-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="11d84-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="11d84-125">DLL</span><span class="sxs-lookup"><span data-stu-id="11d84-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11d84-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11d84-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="11d84-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11d84-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d84-128">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="11d84-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





