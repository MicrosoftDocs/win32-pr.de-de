---
description: Die Aufruf Methode der CIM \_ memorycheck-Klasse wertet eine bestimmte Überprüfung aus. Details darüber, wie die Methode eine bestimmte Überprüfung in einem CIM-Kontext auswertet, wird von den nicht abstrakten CIM- \_ Check-Unterklassen beschrieben. Diese Methode wird von der CIM- \_ Überprüfung geerbt.
ms.assetid: 264a7690-b066-4024-8cb1-d988b829dc72
ms.tgt_platform: multiple
title: Aufruf Methode der CIM_MemoryCheck-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8788b8e910e0a5b7debd9990c18dfb4edef140e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126469"
---
# <a name="invoke-method-of-the-cim_memorycheck-class"></a><span data-ttu-id="944e1-105">Aufruf Methode der CIM \_ memorycheck-Klasse</span><span class="sxs-lookup"><span data-stu-id="944e1-105">Invoke method of the CIM\_MemoryCheck class</span></span>

<span data-ttu-id="944e1-106">Die **Aufruf** Methode der [**CIM \_ memorycheck**](cim-memorycheck.md) -Klasse wertet eine bestimmte Überprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="944e1-106">The **Invoke** method of the [**CIM\_MemoryCheck**](cim-memorycheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="944e1-107">Details darüber, wie die Methode eine bestimmte Überprüfung in einem CIM-Kontext auswertet, wird von den nicht abstrakten [**CIM- \_ Check**](cim-check.md) -Unterklassen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="944e1-107">Details of how the method evaluates a particular check in a CIM context is described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="944e1-108">Diese Methode wird von der **CIM- \_ Überprüfung** geerbt.</span><span class="sxs-lookup"><span data-stu-id="944e1-108">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="944e1-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="944e1-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="944e1-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="944e1-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="944e1-111">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="944e1-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="944e1-112">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="944e1-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="944e1-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="944e1-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="944e1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="944e1-114">Parameters</span></span>

<span data-ttu-id="944e1-115">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="944e1-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="944e1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="944e1-116">Return value</span></span>

<span data-ttu-id="944e1-117">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="944e1-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="944e1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="944e1-118">Remarks</span></span>

<span data-ttu-id="944e1-119">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="944e1-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="944e1-120">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="944e1-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="944e1-121">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="944e1-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="944e1-122">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="944e1-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="944e1-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="944e1-123">Requirements</span></span>



| <span data-ttu-id="944e1-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="944e1-124">Requirement</span></span> | <span data-ttu-id="944e1-125">Wert</span><span class="sxs-lookup"><span data-stu-id="944e1-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="944e1-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="944e1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="944e1-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="944e1-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="944e1-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="944e1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="944e1-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="944e1-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="944e1-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="944e1-130">Namespace</span></span><br/>                | <span data-ttu-id="944e1-131">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="944e1-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="944e1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="944e1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="944e1-133"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="944e1-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="944e1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="944e1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="944e1-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="944e1-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="944e1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="944e1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="944e1-137">CIM- \_ memorycheck</span><span class="sxs-lookup"><span data-stu-id="944e1-137">CIM\_MemoryCheck</span></span>](invoke-method-in-class-cim-memorycheck.md)
</dt> <dt>

[<span data-ttu-id="944e1-138">**CIM- \_ memorycheck**</span><span class="sxs-lookup"><span data-stu-id="944e1-138">**CIM\_MemoryCheck**</span></span>](cim-memorycheck.md)
</dt> </dl>

 

