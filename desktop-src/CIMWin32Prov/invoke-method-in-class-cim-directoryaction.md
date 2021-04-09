---
description: Die Aufruf Methode der CIM- \_ directoryaction-Klasse führt eine bestimmte Aktion aus. Details darüber, wie die Methode die Aktion ausführt, sind Implementierungs spezifisch. Diese Methode wird von der CIM- \_ Aktion geerbt.
ms.assetid: e919dfdb-a52d-4bcb-abff-e1273c406226
ms.tgt_platform: multiple
title: Aufruf Methode der CIM_DirectoryAction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f30184fe46cd8e8b9a595545ccba9a7d738af18e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860935"
---
# <a name="invoke-method-of-the-cim_directoryaction-class"></a><span data-ttu-id="eefb1-105">Aufruf Methode der CIM- \_ directoryaction-Klasse</span><span class="sxs-lookup"><span data-stu-id="eefb1-105">Invoke method of the CIM\_DirectoryAction class</span></span>

<span data-ttu-id="eefb1-106">Die **Aufruf** Methode der [**CIM- \_ directoryaction**](cim-directoryaction.md) -Klasse führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="eefb1-106">The **Invoke** method of the [**CIM\_DirectoryAction**](cim-directoryaction.md) class takes a particular action.</span></span> <span data-ttu-id="eefb1-107">Details darüber, wie die Methode die Aktion ausführt, sind Implementierungs spezifisch.</span><span class="sxs-lookup"><span data-stu-id="eefb1-107">Details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="eefb1-108">Diese Methode wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eefb1-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eefb1-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="eefb1-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eefb1-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eefb1-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eefb1-111">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="eefb1-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="eefb1-112">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="eefb1-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="eefb1-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="eefb1-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="eefb1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="eefb1-114">Parameters</span></span>

<span data-ttu-id="eefb1-115">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="eefb1-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eefb1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eefb1-116">Return value</span></span>

<span data-ttu-id="eefb1-117">Gibt bei Erfolg den Wert 0 (null) zurück, 1 (eins), wenn die Methode nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="eefb1-117">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="eefb1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eefb1-118">Remarks</span></span>

<span data-ttu-id="eefb1-119">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="eefb1-119">WMI does not implement this class.</span></span>

<span data-ttu-id="eefb1-120">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="eefb1-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eefb1-121">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="eefb1-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eefb1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eefb1-122">Requirements</span></span>



| <span data-ttu-id="eefb1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eefb1-123">Requirement</span></span> | <span data-ttu-id="eefb1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="eefb1-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eefb1-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eefb1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eefb1-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eefb1-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eefb1-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eefb1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eefb1-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eefb1-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eefb1-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="eefb1-129">Namespace</span></span><br/>                | <span data-ttu-id="eefb1-130">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eefb1-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eefb1-131">MOF</span><span class="sxs-lookup"><span data-stu-id="eefb1-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eefb1-132"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eefb1-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eefb1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="eefb1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eefb1-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eefb1-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eefb1-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eefb1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eefb1-136">CIM \_ Director Action</span><span class="sxs-lookup"><span data-stu-id="eefb1-136">CIM\_DirectoryAction</span></span>](invoke-method-in-class-cim-directoryaction.md)
</dt> <dt>

[<span data-ttu-id="eefb1-137">**CIM \_ Director Action**</span><span class="sxs-lookup"><span data-stu-id="eefb1-137">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> </dl>

 

