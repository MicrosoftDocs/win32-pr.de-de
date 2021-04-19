---
description: Bringt ein neues Computersystem in einen Cluster.
ms.assetid: 26d9428e-99de-4dcb-96ed-d773f28e015a
ms.tgt_platform: multiple
title: AddNode-Methode der CIM_ClusteringService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.AddNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1769ebb876fd2ae99c800a61b80d339a850ab232
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344604"
---
# <a name="addnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="4693f-103">AddNode-Methode der CIM \_ clusteringservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="4693f-103">AddNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="4693f-104">Mit der **AddNode** -Methode wird ein neues Computersystem in einen Cluster integriert.</span><span class="sxs-lookup"><span data-stu-id="4693f-104">The **AddNode** method brings a new computer system into a cluster.</span></span> <span data-ttu-id="4693f-105">Der hinzu zufügende Knoten wird als Parameter für die-Methode angegeben.</span><span class="sxs-lookup"><span data-stu-id="4693f-105">The node to be added is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4693f-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4693f-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4693f-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4693f-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4693f-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="4693f-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4693f-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4693f-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4693f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4693f-110">Syntax</span></span>


```mof
uint32 AddNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="4693f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4693f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4693f-112">*CS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4693f-112">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4693f-113">Verweis auf das Computersystem, das dem Cluster hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4693f-113">Reference to the computer system to add to the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4693f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4693f-114">Return value</span></span>

<span data-ttu-id="4693f-115">Gibt bei Erfolg den Wert 0 (null) zurück, 1 (eins), wenn der Vorgang nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="4693f-115">Returns a value of 0 (zero) on success, 1 (one) if the operation is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4693f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4693f-116">Remarks</span></span>

<span data-ttu-id="4693f-117">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4693f-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4693f-118">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="4693f-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4693f-119">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4693f-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4693f-120">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4693f-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4693f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4693f-121">Requirements</span></span>



| <span data-ttu-id="4693f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4693f-122">Requirement</span></span> | <span data-ttu-id="4693f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4693f-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4693f-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4693f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4693f-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4693f-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4693f-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4693f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4693f-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4693f-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4693f-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="4693f-128">Namespace</span></span><br/>                | <span data-ttu-id="4693f-129">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4693f-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4693f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4693f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4693f-131"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4693f-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4693f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4693f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4693f-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4693f-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4693f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4693f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4693f-135">**CIM- \_ clusteringservice**</span><span class="sxs-lookup"><span data-stu-id="4693f-135">**CIM\_ClusteringService**</span></span>](addnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="4693f-136">**CIM- \_ clusteringservice**</span><span class="sxs-lookup"><span data-stu-id="4693f-136">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

