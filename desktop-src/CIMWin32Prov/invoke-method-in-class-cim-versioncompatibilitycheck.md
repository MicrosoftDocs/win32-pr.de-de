---
description: Die Aufruf Methode der CIM \_ versioncompatibilitycheck-Klasse wertet eine bestimmte Überprüfung aus.
ms.assetid: d1ccc248-340e-4277-9696-063e1e2bf915
ms.tgt_platform: multiple
title: Aufruf Methode der CIM_VersionCompatibilityCheck-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VersionCompatibilityCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bccbb6072ae84a238b60247daf6b81cfaa74e608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860928"
---
# <a name="invoke-method-of-the-cim_versioncompatibilitycheck-class"></a><span data-ttu-id="a9675-103">Aufruf Methode der CIM \_ versioncompatibilitycheck-Klasse</span><span class="sxs-lookup"><span data-stu-id="a9675-103">Invoke method of the CIM\_VersionCompatibilityCheck class</span></span>

<span data-ttu-id="a9675-104">Die **Aufruf** Methode der [**CIM \_ versioncompatibilitycheck**](cim-versioncompatibilitycheck.md) -Klasse wertet eine bestimmte Überprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="a9675-104">The **Invoke** method of the [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="a9675-105">Die Details, wie die Methode eine bestimmte Überprüfung in einem CIM-Kontext auswertet, werden von den nicht abstrakten [**CIM- \_ Check**](cim-check.md) -Unterklassen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a9675-105">The details of how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="a9675-106">Diese Methode wird von der **CIM- \_ Überprüfung** geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9675-106">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9675-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a9675-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a9675-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a9675-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a9675-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9675-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a9675-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a9675-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9675-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9675-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="a9675-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9675-112">Parameters</span></span>

<span data-ttu-id="a9675-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a9675-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9675-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9675-114">Return value</span></span>

<span data-ttu-id="a9675-115">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="a9675-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9675-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9675-116">Remarks</span></span>

<span data-ttu-id="a9675-117">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="a9675-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a9675-118">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="a9675-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a9675-119">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a9675-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a9675-120">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a9675-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9675-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9675-121">Requirements</span></span>



| <span data-ttu-id="a9675-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9675-122">Requirement</span></span> | <span data-ttu-id="a9675-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a9675-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9675-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9675-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9675-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9675-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9675-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9675-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9675-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9675-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9675-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9675-128">Namespace</span></span><br/>                | <span data-ttu-id="a9675-129">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a9675-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a9675-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a9675-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9675-131"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a9675-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9675-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a9675-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9675-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9675-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9675-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9675-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9675-135">CIM \_ versioncompatibilitycheck</span><span class="sxs-lookup"><span data-stu-id="a9675-135">CIM\_VersionCompatibilityCheck</span></span>](invoke-method-in-class-cim-versioncompatibilitycheck.md)
</dt> <dt>

[<span data-ttu-id="a9675-136">**CIM \_ versioncompatibilitycheck**</span><span class="sxs-lookup"><span data-stu-id="a9675-136">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> </dl>

 

