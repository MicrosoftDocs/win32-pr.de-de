---
description: Die Reset-Methode der CIM \_ cdromdrive-Klasse fordert das Zurücksetzen des logischen Geräts an.
ms.assetid: 9d422fb3-8332-4be5-8e90-0e782640748a
ms.tgt_platform: multiple
title: Reset-Methode der CIM_CDROMDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CDROMDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 307d866c22a1ba414913a3115be9d355a3138d6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523731"
---
# <a name="reset-method-of-the-cim_cdromdrive-class"></a><span data-ttu-id="64f59-103">Reset-Methode der CIM \_ cdromdrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="64f59-103">Reset method of the CIM\_CDROMDrive class</span></span>

<span data-ttu-id="64f59-104">Die **Reset** -Methode der CIM \_ cdromdrive-Klasse fordert das Zurücksetzen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="64f59-104">The **Reset** method of the CIM\_CDROMDrive class requests a reset of the logical device.</span></span> <span data-ttu-id="64f59-105">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="64f59-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64f59-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="64f59-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="64f59-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="64f59-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="64f59-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="64f59-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="64f59-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="64f59-109">Parameters</span></span>

<span data-ttu-id="64f59-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="64f59-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64f59-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64f59-111">Return value</span></span>

<span data-ttu-id="64f59-112">Gibt 0 (null) zurück, wenn die Anforderung erfolgreich ausgeführt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und ein anderer Wert, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="64f59-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="64f59-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64f59-113">Remarks</span></span>

<span data-ttu-id="64f59-114">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="64f59-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="64f59-115">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="64f59-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="64f59-116">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="64f59-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="64f59-117">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="64f59-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="64f59-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64f59-118">Requirements</span></span>



| <span data-ttu-id="64f59-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64f59-119">Requirement</span></span> | <span data-ttu-id="64f59-120">Wert</span><span class="sxs-lookup"><span data-stu-id="64f59-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64f59-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64f59-121">Minimum supported client</span></span><br/> | <span data-ttu-id="64f59-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64f59-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64f59-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64f59-123">Minimum supported server</span></span><br/> | <span data-ttu-id="64f59-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64f59-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64f59-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="64f59-125">Namespace</span></span><br/>                | <span data-ttu-id="64f59-126">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="64f59-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="64f59-127">MOF</span><span class="sxs-lookup"><span data-stu-id="64f59-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64f59-128"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="64f59-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="64f59-129">DLL</span><span class="sxs-lookup"><span data-stu-id="64f59-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64f59-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64f59-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64f59-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64f59-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64f59-132">CIM- \_ cdromdrive</span><span class="sxs-lookup"><span data-stu-id="64f59-132">CIM\_CDROMDrive</span></span>](reset-method-in-class-cim-cdromdrive.md)
</dt> <dt>

[<span data-ttu-id="64f59-133">**CIM- \_ cdromdrive**</span><span class="sxs-lookup"><span data-stu-id="64f59-133">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> </dl>

 

 




