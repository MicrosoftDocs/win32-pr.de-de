---
description: Die Aufruf Methode der CIM- \_ Check-Klasse wertet eine bestimmte Überprüfung aus.
ms.assetid: cf1adeb2-f8a2-4f84-978f-e801bce104ac
ms.tgt_platform: multiple
title: Aufruf Methode der CIM_Check-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7774fcd1b3ef451fffb34ce9ad10d404e8ea95b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343164"
---
# <a name="invoke-method-of-the-cim_check-class"></a><span data-ttu-id="8f656-103">Aufruf Methode der CIM- \_ Check-Klasse</span><span class="sxs-lookup"><span data-stu-id="8f656-103">Invoke method of the CIM\_Check class</span></span>

<span data-ttu-id="8f656-104">Die **Aufruf** Methode der [**CIM- \_ Check**](cim-check.md) -Klasse wertet eine bestimmte Überprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="8f656-104">The **Invoke** method of the [**CIM\_Check**](cim-check.md) class evaluates a particular check.</span></span>

<span data-ttu-id="8f656-105">Weitere Informationen dazu, wie die-Methode eine bestimmte Überprüfung in einem CIM-Kontext auswertet, finden Sie Unterklassen der nicht abstrakten [**CIM- \_ Überprüfung**](cim-check.md) .</span><span class="sxs-lookup"><span data-stu-id="8f656-105">For more information about how the method evaluates a particular check in a CIM context, see the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f656-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8f656-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8f656-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8f656-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8f656-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8f656-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8f656-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8f656-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f656-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f656-110">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="8f656-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f656-111">Parameters</span></span>

<span data-ttu-id="8f656-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8f656-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f656-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f656-113">Return value</span></span>

<span data-ttu-id="8f656-114">Gibt bei Erfolg den Wert 0 (null) zurück, 1 (eins), wenn die Methode nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="8f656-114">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f656-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f656-115">Remarks</span></span>

<span data-ttu-id="8f656-116">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="8f656-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8f656-117">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="8f656-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8f656-118">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8f656-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8f656-119">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8f656-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f656-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f656-120">Requirements</span></span>



| <span data-ttu-id="8f656-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f656-121">Requirement</span></span> | <span data-ttu-id="8f656-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8f656-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f656-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f656-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8f656-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f656-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f656-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f656-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8f656-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f656-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f656-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f656-127">Namespace</span></span><br/>                | <span data-ttu-id="8f656-128">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8f656-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f656-129">MOF</span><span class="sxs-lookup"><span data-stu-id="8f656-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f656-130"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8f656-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f656-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8f656-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f656-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f656-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f656-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f656-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f656-134">**CIM- \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="8f656-134">**CIM\_Check**</span></span>](invoke-method-in-class-cim-check.md)
</dt> <dt>

[<span data-ttu-id="8f656-135">**CIM- \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="8f656-135">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

