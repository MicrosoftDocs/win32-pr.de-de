---
title: Schedulepatch-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Plant einen Bereitstellungs Auftrag für Software Updates, mit dem Software Updates auf den virtuellen Computern in einer Sammlung virtueller Desktops installiert werden.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- Schedulepatch-Methode Remotedesktopdienste
- Schedulepatch-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, schedulepatch-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9585e3d13ea1f02115506741c153d62c33fcc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476422"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="db9ec-106">Schedulepatch-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="db9ec-106">SchedulePatch method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="db9ec-107">Plant einen Bereitstellungs Auftrag für Software Updates, mit dem Software Updates auf den virtuellen Computern in einer Sammlung virtueller Desktops installiert werden.</span><span class="sxs-lookup"><span data-stu-id="db9ec-107">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="db9ec-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="db9ec-108">Syntax</span></span>


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a><span data-ttu-id="db9ec-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="db9ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9ec-110">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db9ec-110">*StartTime* \[in\]</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="db9ec-111">Das System meldet die Benutzer der virtuellen Computer erst dann ab, wenn die im *forcelogofftime* -Parameter angegebene Zeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db9ec-111">The system will not log off users of the virtual machines until the time specified in the *ForceLogOffTime* parameter.</span></span>

 

<span data-ttu-id="db9ec-112">Das Datum und die Uhrzeit der Installation der Updates.</span><span class="sxs-lookup"><span data-stu-id="db9ec-112">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="db9ec-113">*Forcelogofftime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db9ec-113">*ForceLogOffTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9ec-114">Das Datum und die Uhrzeit, zu denen das Systembenutzer der virtuellen Maschinen abmeldet.</span><span class="sxs-lookup"><span data-stu-id="db9ec-114">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="db9ec-115">*Jobinputxml* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db9ec-115">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9ec-116">Eine XML-formatierte Zeichenfolge, die die Informationen zum Software Update Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="db9ec-116">An XML formatted string that contains the software update job information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9ec-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db9ec-117">Return value</span></span>

<span data-ttu-id="db9ec-118">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db9ec-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="db9ec-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db9ec-119">Requirements</span></span>



| <span data-ttu-id="db9ec-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db9ec-120">Requirement</span></span> | <span data-ttu-id="db9ec-121">Wert</span><span class="sxs-lookup"><span data-stu-id="db9ec-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="db9ec-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db9ec-122">Minimum supported client</span></span><br/> | <span data-ttu-id="db9ec-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="db9ec-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="db9ec-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db9ec-124">Minimum supported server</span></span><br/> | <span data-ttu-id="db9ec-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db9ec-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="db9ec-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="db9ec-126">Namespace</span></span><br/>                | <span data-ttu-id="db9ec-127">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="db9ec-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="db9ec-128">MOF</span><span class="sxs-lookup"><span data-stu-id="db9ec-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db9ec-129"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="db9ec-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="db9ec-130">DLL</span><span class="sxs-lookup"><span data-stu-id="db9ec-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db9ec-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db9ec-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="db9ec-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db9ec-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db9ec-133">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="db9ec-133">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





