---
description: Die evictnode-Methode entfernt ein Computersystem aus einem Cluster. Der Knoten, der entfernt werden soll, wird als Parameter für die-Methode angegeben.
ms.assetid: 4691d536-ade3-4a02-bc28-e31ebaf5d9e4
ms.tgt_platform: multiple
title: Evictnode-Methode der CIM_ClusteringService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.EvictNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d68ddc1adc0af335dcf2d4139cf7c1f0a381d986
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748137"
---
# <a name="evictnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="c2ebb-104">Evictnode-Methode der CIM \_ clusteringservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="c2ebb-104">EvictNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="c2ebb-105">Die **evictnode** -Methode entfernt ein Computersystem aus einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="c2ebb-105">The **EvictNode** method removes a computer system from a cluster.</span></span> <span data-ttu-id="c2ebb-106">Der Knoten, der entfernt werden soll, wird als Parameter für die-Methode angegeben.</span><span class="sxs-lookup"><span data-stu-id="c2ebb-106">The node to be evicted is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2ebb-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c2ebb-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c2ebb-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c2ebb-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c2ebb-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2ebb-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c2ebb-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c2ebb-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2ebb-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2ebb-111">Syntax</span></span>


```mof
uint32 EvictNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="c2ebb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2ebb-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2ebb-113">*CS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2ebb-113">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2ebb-114">Verweis auf das Computersystem, das aus dem Cluster entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2ebb-114">Reference to the computer system to remove from the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2ebb-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2ebb-115">Return value</span></span>

<span data-ttu-id="c2ebb-116">Gibt 0 (null) zurück, wenn das Computersystem erfolgreich entfernt wurde, 1 (eins), wenn die Methode nicht unterstützt wird, und eine andere Zahl, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c2ebb-116">Returns 0 (zero) if the computer system is successfully evicted, 1 (one) if the method is not supported, and any other number if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2ebb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2ebb-117">Remarks</span></span>

<span data-ttu-id="c2ebb-118">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c2ebb-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c2ebb-119">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="c2ebb-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c2ebb-120">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c2ebb-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c2ebb-121">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c2ebb-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2ebb-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2ebb-122">Requirements</span></span>



| <span data-ttu-id="c2ebb-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2ebb-123">Requirement</span></span> | <span data-ttu-id="c2ebb-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c2ebb-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ebb-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2ebb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c2ebb-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2ebb-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2ebb-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2ebb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c2ebb-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2ebb-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2ebb-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2ebb-129">Namespace</span></span><br/>                | <span data-ttu-id="c2ebb-130">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c2ebb-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c2ebb-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c2ebb-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2ebb-132"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c2ebb-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2ebb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c2ebb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2ebb-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2ebb-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2ebb-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2ebb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ebb-136">**CIM- \_ clusteringservice**</span><span class="sxs-lookup"><span data-stu-id="c2ebb-136">**CIM\_ClusteringService**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="c2ebb-137">**CIM- \_ clusteringservice**</span><span class="sxs-lookup"><span data-stu-id="c2ebb-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

