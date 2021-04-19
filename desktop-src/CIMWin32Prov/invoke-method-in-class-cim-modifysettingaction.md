---
description: Die Aufruf Methode der CIM \_ modifysettingaction-Klasse führt eine bestimmte Aktion aus. Details darüber, wie die Methode die Aktion ausführt, sind Implementierungs spezifisch. Diese Methode wird von der CIM- \_ Aktion geerbt.
ms.assetid: 360e3e00-1c09-495a-8fc0-ce2e9d1f9e77
ms.tgt_platform: multiple
title: Aufruf Methode der CIM_ModifySettingAction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ModifySettingAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4e4c5dc08f4e9ad27d7f4578ca5c82543253b57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344600"
---
# <a name="invoke-method-of-the-cim_modifysettingaction-class"></a><span data-ttu-id="1c225-105">Aufruf Methode der CIM \_ modifysettingaction-Klasse</span><span class="sxs-lookup"><span data-stu-id="1c225-105">Invoke method of the CIM\_ModifySettingAction class</span></span>

<span data-ttu-id="1c225-106">Die **Aufruf** Methode der [**CIM \_ modifysettingaction**](cim-modifysettingaction.md) -Klasse führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="1c225-106">The **Invoke** method of the [**CIM\_ModifySettingAction**](cim-modifysettingaction.md) class takes a particular action.</span></span> <span data-ttu-id="1c225-107">Details darüber, wie die Methode die Aktion ausführt, sind Implementierungs spezifisch.</span><span class="sxs-lookup"><span data-stu-id="1c225-107">Details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="1c225-108">Diese Methode wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c225-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c225-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1c225-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1c225-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1c225-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1c225-111">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c225-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1c225-112">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1c225-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1c225-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c225-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="1c225-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c225-114">Parameters</span></span>

<span data-ttu-id="1c225-115">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1c225-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c225-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c225-116">Return value</span></span>

<span data-ttu-id="1c225-117">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="1c225-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c225-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c225-118">Remarks</span></span>

<span data-ttu-id="1c225-119">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="1c225-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1c225-120">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="1c225-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1c225-121">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1c225-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1c225-122">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1c225-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c225-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c225-123">Requirements</span></span>



| <span data-ttu-id="1c225-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c225-124">Requirement</span></span> | <span data-ttu-id="1c225-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1c225-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c225-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c225-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1c225-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c225-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c225-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c225-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1c225-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c225-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c225-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c225-130">Namespace</span></span><br/>                | <span data-ttu-id="1c225-131">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1c225-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c225-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1c225-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c225-133"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1c225-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c225-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1c225-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c225-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c225-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c225-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c225-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c225-137">CIM \_ modifysettingaction</span><span class="sxs-lookup"><span data-stu-id="1c225-137">CIM\_ModifySettingAction</span></span>](invoke-method-in-class-cim-modifysettingaction.md)
</dt> <dt>

[<span data-ttu-id="1c225-138">**CIM \_ modifysettingaction**</span><span class="sxs-lookup"><span data-stu-id="1c225-138">**CIM\_ModifySettingAction**</span></span>](cim-modifysettingaction.md)
</dt> </dl>

 

