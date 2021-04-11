---
description: Die Reset-Methode fordert eine zurück setzung des logischen Geräts an. Diese Methode wird von CIM \_ LogicalDevice geerbt.
ms.assetid: 874f8eb4-784a-41ab-9c58-9e48486a7f71
ms.tgt_platform: multiple
title: Reset-Methode der CIM_DiskPartition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskPartition.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 236a8c018b584fbc2d5ef1d13b0429d946b868fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214057"
---
# <a name="reset-method-of-the-cim_diskpartition-class"></a><span data-ttu-id="28c89-104">Reset-Methode der CIM \_ Diskpartition-Klasse</span><span class="sxs-lookup"><span data-stu-id="28c89-104">Reset method of the CIM\_DiskPartition class</span></span>

<span data-ttu-id="28c89-105">Die **Reset** -Methode fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="28c89-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="28c89-106">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="28c89-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28c89-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="28c89-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="28c89-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="28c89-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="28c89-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="28c89-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="28c89-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="28c89-110">Parameters</span></span>

<span data-ttu-id="28c89-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="28c89-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28c89-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28c89-112">Return value</span></span>

<span data-ttu-id="28c89-113">Gibt 0 (null) zurück, wenn die Anforderung erfolgreich ausgeführt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und ein anderer Wert, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="28c89-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="28c89-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28c89-114">Remarks</span></span>

<span data-ttu-id="28c89-115">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="28c89-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="28c89-116">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="28c89-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="28c89-117">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="28c89-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="28c89-118">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="28c89-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="28c89-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28c89-119">Requirements</span></span>



| <span data-ttu-id="28c89-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28c89-120">Requirement</span></span> | <span data-ttu-id="28c89-121">Wert</span><span class="sxs-lookup"><span data-stu-id="28c89-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28c89-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28c89-122">Minimum supported client</span></span><br/> | <span data-ttu-id="28c89-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28c89-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28c89-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28c89-124">Minimum supported server</span></span><br/> | <span data-ttu-id="28c89-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28c89-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28c89-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="28c89-126">Namespace</span></span><br/>                | <span data-ttu-id="28c89-127">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="28c89-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="28c89-128">MOF</span><span class="sxs-lookup"><span data-stu-id="28c89-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28c89-129"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="28c89-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="28c89-130">DLL</span><span class="sxs-lookup"><span data-stu-id="28c89-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28c89-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28c89-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c89-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28c89-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c89-133">CIM \_ Diskpartition</span><span class="sxs-lookup"><span data-stu-id="28c89-133">CIM\_DiskPartition</span></span>](reset-method-in-class-cim-diskpartition.md)
</dt> <dt>

[<span data-ttu-id="28c89-134">**CIM \_ Diskpartition**</span><span class="sxs-lookup"><span data-stu-id="28c89-134">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> </dl>

 

 




