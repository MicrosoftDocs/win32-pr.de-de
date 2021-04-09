---
description: Die Reset-Methode der CIM- \_ aggregatepsextent-Klasse fordert das Zurücksetzen des logischen Geräts an.
ms.assetid: 6669126f-ceab-4e34-81e5-5cfe1abf5b98
ms.tgt_platform: multiple
title: Reset-Methode der CIM_AggregatePSExtent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePSExtent.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 376ac4f0180e92f1b67a13e4fbf98a2912ee4ade
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861740"
---
# <a name="reset-method-of-the-cim_aggregatepsextent-class"></a><span data-ttu-id="e8d5a-103">Reset-Methode der CIM- \_ aggregatepsextent-Klasse</span><span class="sxs-lookup"><span data-stu-id="e8d5a-103">Reset method of the CIM\_AggregatePSExtent class</span></span>

<span data-ttu-id="e8d5a-104">Die **Reset** -Methode der CIM- \_ aggregatepsextent-Klasse fordert das Zurücksetzen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="e8d5a-104">The **Reset** method of the CIM\_AggregatePSExtent class requests a reset of the logical device.</span></span> <span data-ttu-id="e8d5a-105">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e8d5a-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8d5a-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e8d5a-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e8d5a-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e8d5a-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e8d5a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8d5a-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="e8d5a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8d5a-109">Parameters</span></span>

<span data-ttu-id="e8d5a-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e8d5a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8d5a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8d5a-111">Return value</span></span>

<span data-ttu-id="e8d5a-112">Gibt 0 (null) zurück, wenn die Anforderung erfolgreich ausgeführt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und ein anderer Wert, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e8d5a-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8d5a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8d5a-113">Remarks</span></span>

<span data-ttu-id="e8d5a-114">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="e8d5a-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e8d5a-115">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="e8d5a-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e8d5a-116">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e8d5a-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e8d5a-117">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e8d5a-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8d5a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8d5a-118">Requirements</span></span>



| <span data-ttu-id="e8d5a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8d5a-119">Requirement</span></span> | <span data-ttu-id="e8d5a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e8d5a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d5a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8d5a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e8d5a-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8d5a-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e8d5a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8d5a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e8d5a-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8d5a-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e8d5a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8d5a-125">Namespace</span></span><br/>                | <span data-ttu-id="e8d5a-126">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e8d5a-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e8d5a-127">MOF</span><span class="sxs-lookup"><span data-stu-id="e8d5a-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8d5a-128"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e8d5a-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8d5a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e8d5a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8d5a-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8d5a-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8d5a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8d5a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8d5a-132">CIM \_ aggregatepsextent</span><span class="sxs-lookup"><span data-stu-id="e8d5a-132">CIM\_AggregatePSExtent</span></span>](reset-method-in-class-cim-aggregatepsextent.md)
</dt> <dt>

[<span data-ttu-id="e8d5a-133">**CIM \_ aggregatepsextent**</span><span class="sxs-lookup"><span data-stu-id="e8d5a-133">**CIM\_AggregatePSExtent**</span></span>](cim-aggregatepsextent.md)
</dt> </dl>

 

 




