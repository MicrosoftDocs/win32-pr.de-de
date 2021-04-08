---
description: Die Aufruf Methode der CIM- \_ Klasse "kreatedirectoryaction" führt eine bestimmte Aktion aus. Details dazu, wie die Methode die Aktion ausführt, sind Implementierungs spezifisch. Diese Methode wird von der CIM- \_ Aktion geerbt.
ms.assetid: f14e215d-31f2-46c5-b45e-3de64ce46bf2
ms.tgt_platform: multiple
title: Aufruf Methode der CIM_CreateDirectoryAction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CreateDirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 690a29ae0ea85e0b965d2a426703eea87aee9184
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748113"
---
# <a name="invoke-method-of-the-cim_createdirectoryaction-class"></a><span data-ttu-id="8e095-105">Aufrufen-Methode der CIM- \_ Klasse "kreatedirectoryaction"</span><span class="sxs-lookup"><span data-stu-id="8e095-105">Invoke method of the CIM\_CreateDirectoryAction class</span></span>

<span data-ttu-id="8e095-106">Die **Aufruf** Methode der CIM-Klasse " [**\_ kreatedirectoryaction**](cim-createdirectoryaction.md) " führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="8e095-106">The **Invoke** method of the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class takes a particular action.</span></span> <span data-ttu-id="8e095-107">Details dazu, wie die Methode die Aktion ausführt, sind Implementierungs spezifisch.</span><span class="sxs-lookup"><span data-stu-id="8e095-107">Details about how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="8e095-108">Diese Methode wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8e095-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e095-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8e095-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8e095-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8e095-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8e095-111">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e095-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8e095-112">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8e095-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e095-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e095-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="8e095-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e095-114">Parameters</span></span>

<span data-ttu-id="8e095-115">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8e095-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e095-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e095-116">Return value</span></span>

<span data-ttu-id="8e095-117">Gibt bei Erfolg den Wert 0 zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="8e095-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e095-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e095-118">Remarks</span></span>

<span data-ttu-id="8e095-119">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="8e095-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8e095-120">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="8e095-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8e095-121">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8e095-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8e095-122">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8e095-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e095-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e095-123">Requirements</span></span>



| <span data-ttu-id="8e095-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e095-124">Requirement</span></span> | <span data-ttu-id="8e095-125">Wert</span><span class="sxs-lookup"><span data-stu-id="8e095-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e095-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e095-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8e095-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e095-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e095-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e095-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8e095-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e095-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e095-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e095-130">Namespace</span></span><br/>                | <span data-ttu-id="8e095-131">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8e095-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e095-132">MOF</span><span class="sxs-lookup"><span data-stu-id="8e095-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e095-133"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8e095-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e095-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8e095-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e095-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e095-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e095-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e095-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e095-137">**CIM- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="8e095-137">**CIM\_CreateDirectoryAction**</span></span>](invoke-method-in-class-cim-createdirectoryaction.md)
</dt> <dt>

[<span data-ttu-id="8e095-138">**CIM- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="8e095-138">**CIM\_CreateDirectoryAction**</span></span>](cim-createdirectoryaction.md)
</dt> </dl>

 

