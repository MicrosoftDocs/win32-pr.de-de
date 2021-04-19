---
description: Die Aufruf Methode der CIM- \_ directoryspecification-Klasse wertet eine bestimmte Überprüfung aus.
ms.assetid: 63289f94-f134-4159-898c-404cdd8f2a5c
ms.tgt_platform: multiple
title: Aufruf Methode der CIM_DirectorySpecification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48e5cb315f7dba6be187280ee6a16d7c4711752f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346633"
---
# <a name="invoke-method-of-the-cim_directoryspecification-class"></a><span data-ttu-id="e662c-103">Aufruf Methode der CIM- \_ directoryspecification-Klasse</span><span class="sxs-lookup"><span data-stu-id="e662c-103">Invoke method of the CIM\_DirectorySpecification class</span></span>

<span data-ttu-id="e662c-104">Die **Aufruf** Methode der [**CIM- \_ directoryspecification**](cim-directoryspecification.md) -Klasse wertet eine bestimmte Überprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="e662c-104">The **Invoke** method of the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class evaluates a particular check.</span></span> <span data-ttu-id="e662c-105">Details dazu, wie die Methode eine bestimmte Überprüfung in einem CIM-Kontext auswertet, wird von den nicht abstrakten [**CIM- \_ Check**](cim-check.md) -Unterklassen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e662c-105">Details about how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="e662c-106">Diese Methode wird von der **CIM- \_ Überprüfung** geerbt.</span><span class="sxs-lookup"><span data-stu-id="e662c-106">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e662c-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e662c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e662c-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e662c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e662c-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e662c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e662c-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e662c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e662c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e662c-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="e662c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e662c-112">Parameters</span></span>

<span data-ttu-id="e662c-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e662c-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e662c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e662c-114">Return value</span></span>

<span data-ttu-id="e662c-115">Gibt bei Erfolg 0 (null) zurück, a 1, wenn die Methode nicht unterstützt wird, und jeder andere Wert gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="e662c-115">Returns a 0 if successful, a 1 if the method is not supported, and any other value indicates an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e662c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e662c-116">Remarks</span></span>

<span data-ttu-id="e662c-117">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="e662c-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e662c-118">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="e662c-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e662c-119">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e662c-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e662c-120">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e662c-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e662c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e662c-121">Requirements</span></span>



| <span data-ttu-id="e662c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e662c-122">Requirement</span></span> | <span data-ttu-id="e662c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e662c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e662c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e662c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e662c-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e662c-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e662c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e662c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e662c-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e662c-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e662c-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="e662c-128">Namespace</span></span><br/>                | <span data-ttu-id="e662c-129">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e662c-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e662c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e662c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e662c-131"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e662c-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e662c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e662c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e662c-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e662c-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e662c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e662c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e662c-135">CIM- \_ directspecification</span><span class="sxs-lookup"><span data-stu-id="e662c-135">CIM\_DirectorySpecification</span></span>](invoke-method-in-class-cim-directoryspecification.md)
</dt> <dt>

[<span data-ttu-id="e662c-136">**CIM- \_ directspecification**</span><span class="sxs-lookup"><span data-stu-id="e662c-136">**CIM\_DirectorySpecification**</span></span>](cim-directoryspecification.md)
</dt> </dl>

 

