---
description: Die Aufruf Methode der CIM \_ removefileaction-Klasse führt eine bestimmte Aktion aus. Die Details, wie die Methode die Aktion ausführt, sind Implementierungs spezifisch. Diese Methode wird von der CIM- \_ Aktion geerbt.
ms.assetid: 7fc33654-a51b-41cf-a5b4-ef08fd6e40ac
ms.tgt_platform: multiple
title: Aufruf Methode der CIM_RemoveFileAction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveFileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a371ad1f7b1da874b6a049b04d5f50ec694cf181
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344950"
---
# <a name="invoke-method-of-the-cim_removefileaction-class"></a><span data-ttu-id="56691-105">Aufruf Methode der CIM \_ removefileaction-Klasse</span><span class="sxs-lookup"><span data-stu-id="56691-105">Invoke method of the CIM\_RemoveFileAction class</span></span>

<span data-ttu-id="56691-106">Die **Aufruf** Methode der [**CIM \_ removefileaction**](cim-removefileaction.md) -Klasse führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="56691-106">The **Invoke** method of the [**CIM\_RemoveFileAction**](cim-removefileaction.md) class takes a particular action.</span></span> <span data-ttu-id="56691-107">Die Details, wie die Methode die Aktion ausführt, sind Implementierungs spezifisch.</span><span class="sxs-lookup"><span data-stu-id="56691-107">The details of how the method performs the action is implementation specific.</span></span> <span data-ttu-id="56691-108">Diese Methode wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="56691-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56691-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="56691-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="56691-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="56691-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="56691-111">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="56691-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="56691-112">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="56691-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="56691-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="56691-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="56691-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="56691-114">Parameters</span></span>

<span data-ttu-id="56691-115">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="56691-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56691-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56691-116">Return value</span></span>

<span data-ttu-id="56691-117">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="56691-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="56691-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56691-118">Remarks</span></span>

<span data-ttu-id="56691-119">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="56691-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="56691-120">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="56691-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="56691-121">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="56691-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="56691-122">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="56691-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="56691-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56691-123">Requirements</span></span>



| <span data-ttu-id="56691-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56691-124">Requirement</span></span> | <span data-ttu-id="56691-125">Wert</span><span class="sxs-lookup"><span data-stu-id="56691-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56691-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56691-126">Minimum supported client</span></span><br/> | <span data-ttu-id="56691-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56691-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="56691-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56691-128">Minimum supported server</span></span><br/> | <span data-ttu-id="56691-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56691-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="56691-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="56691-130">Namespace</span></span><br/>                | <span data-ttu-id="56691-131">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="56691-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="56691-132">MOF</span><span class="sxs-lookup"><span data-stu-id="56691-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56691-133"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="56691-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="56691-134">DLL</span><span class="sxs-lookup"><span data-stu-id="56691-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56691-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56691-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56691-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56691-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56691-137">CIM- \_ removefileaction</span><span class="sxs-lookup"><span data-stu-id="56691-137">CIM\_RemoveFileAction</span></span>](invoke-method-in-class-cim-removefileaction.md)
</dt> <dt>

[<span data-ttu-id="56691-138">**CIM- \_ removefileaction**</span><span class="sxs-lookup"><span data-stu-id="56691-138">**CIM\_RemoveFileAction**</span></span>](cim-removefileaction.md)
</dt> </dl>

 

