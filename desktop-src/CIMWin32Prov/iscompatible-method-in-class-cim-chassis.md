---
description: Überprüft, ob das physische Chassis, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.
ms.assetid: 9a1aa1b7-2b95-4887-9d14-e416ff69f9df
ms.tgt_platform: multiple
title: Iscompatible-Methode der CIM_Chassis-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8796582b153a7283429715569eeed91e4dd38fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343163"
---
# <a name="iscompatible-method-of-the-cim_chassis-class"></a><span data-ttu-id="42e68-103">Iscompatible-Methode der CIM- \_ Chassis-Klasse</span><span class="sxs-lookup"><span data-stu-id="42e68-103">IsCompatible method of the CIM\_Chassis class</span></span>

<span data-ttu-id="42e68-104">Die **iscompatible** -Methode überprüft, ob das physische Chassis, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="42e68-104">The **IsCompatible** method verifies whether the referenced physical chassis can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="42e68-105">In einer Unterklasse kann der Satz möglicher Rückgabecodes mit einem [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="42e68-105">In a subclass, the set of possible return codes can be specified by using a [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) qualifier on the method.</span></span> <span data-ttu-id="42e68-106">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, können auch in der Unterklasse als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="42e68-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="42e68-107">Diese Methode wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42e68-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="42e68-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="42e68-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="42e68-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="42e68-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="42e68-110">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="42e68-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="42e68-111">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="42e68-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="42e68-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="42e68-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="42e68-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="42e68-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42e68-114">*Elementto-Check* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42e68-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e68-115">Verweis auf das physische Element, für das die Kompatibilität überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="42e68-115">Reference to the physical element for which to check compatibility.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42e68-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42e68-116">Return value</span></span>

<span data-ttu-id="42e68-117">Gibt bei Erfolg den Wert 0 (null) zurück, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="42e68-117">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="42e68-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42e68-118">Remarks</span></span>

<span data-ttu-id="42e68-119">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="42e68-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="42e68-120">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="42e68-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="42e68-121">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="42e68-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="42e68-122">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="42e68-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="42e68-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42e68-123">Requirements</span></span>



| <span data-ttu-id="42e68-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42e68-124">Requirement</span></span> | <span data-ttu-id="42e68-125">Wert</span><span class="sxs-lookup"><span data-stu-id="42e68-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42e68-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42e68-126">Minimum supported client</span></span><br/> | <span data-ttu-id="42e68-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42e68-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42e68-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42e68-128">Minimum supported server</span></span><br/> | <span data-ttu-id="42e68-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42e68-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42e68-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="42e68-130">Namespace</span></span><br/>                | <span data-ttu-id="42e68-131">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="42e68-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="42e68-132">MOF</span><span class="sxs-lookup"><span data-stu-id="42e68-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42e68-133"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="42e68-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="42e68-134">DLL</span><span class="sxs-lookup"><span data-stu-id="42e68-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42e68-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42e68-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42e68-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42e68-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e68-137">**CIM- \_ Chassis**</span><span class="sxs-lookup"><span data-stu-id="42e68-137">**CIM\_Chassis**</span></span>](iscompatible-method-in-class-cim-chassis.md)
</dt> <dt>

[<span data-ttu-id="42e68-138">**CIM- \_ Chassis**</span><span class="sxs-lookup"><span data-stu-id="42e68-138">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> </dl>

 

