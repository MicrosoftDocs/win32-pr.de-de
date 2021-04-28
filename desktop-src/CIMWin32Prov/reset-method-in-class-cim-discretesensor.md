---
description: 'Reset-Methode der CIM_DiscreteSensor-Klasse: Die Reset-Methode fordert eine Zurücksetzung des logischen Geräts an. Diese Methode wird von CIM \_ LogicalDevice geerbt.'
ms.assetid: 4ddbad2a-e586-434a-a33e-7d60dcb67b3a
ms.tgt_platform: multiple
title: Reset-Methode der CIM_DiscreteSensor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiscreteSensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: aecda4b40a70c72679c3edff7b30f6ba548938cf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096908"
---
# <a name="reset-method-of-the-cim_discretesensor-class"></a><span data-ttu-id="6b298-104">Reset-Methode der CIM \_ DiscreteSensor-Klasse</span><span class="sxs-lookup"><span data-stu-id="6b298-104">Reset method of the CIM\_DiscreteSensor class</span></span>

<span data-ttu-id="6b298-105">Die **Reset-Methode** fordert eine Zurücksetzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="6b298-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="6b298-106">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b298-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b298-107">Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6b298-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6b298-108">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="6b298-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6b298-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b298-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="6b298-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b298-110">Parameters</span></span>

<span data-ttu-id="6b298-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6b298-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b298-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b298-112">Return value</span></span>

<span data-ttu-id="6b298-113">Gibt 0 (null) zurück, wenn die Anforderung erfolgreich ausgeführt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6b298-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b298-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b298-114">Remarks</span></span>

<span data-ttu-id="6b298-115">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="6b298-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6b298-116">Um diese Methode verwenden zu können, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="6b298-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6b298-117">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="6b298-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6b298-118">Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6b298-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b298-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b298-119">Requirements</span></span>



| <span data-ttu-id="6b298-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b298-120">Requirement</span></span> | <span data-ttu-id="6b298-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6b298-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b298-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b298-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6b298-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b298-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b298-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b298-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6b298-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b298-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b298-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b298-126">Namespace</span></span><br/>                | <span data-ttu-id="6b298-127">Stamm \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6b298-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b298-128">MOF</span><span class="sxs-lookup"><span data-stu-id="6b298-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b298-129"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b298-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b298-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6b298-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b298-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b298-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b298-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6b298-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b298-133">CIM \_ DiscreteSensor</span><span class="sxs-lookup"><span data-stu-id="6b298-133">CIM\_DiscreteSensor</span></span>](reset-method-in-class-cim-discretesensor.md)
</dt> <dt>

[<span data-ttu-id="6b298-134">**CIM \_ DiscreteSensor**</span><span class="sxs-lookup"><span data-stu-id="6b298-134">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> </dl>

 

 




