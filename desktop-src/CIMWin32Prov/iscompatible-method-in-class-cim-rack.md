---
description: Überprüft, ob das Rack, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.
ms.assetid: 03276c6a-ca48-48bc-adbe-e53e02107abb
ms.tgt_platform: multiple
title: Iscompatible-Methode der CIM_Rack-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6855b797e8941882aac1dc25d77b2ef7e3bc11c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346438"
---
# <a name="iscompatible-method-of-the-cim_rack-class"></a><span data-ttu-id="7895f-103">Iscompatible-Methode der CIM- \_ Rack-Klasse</span><span class="sxs-lookup"><span data-stu-id="7895f-103">IsCompatible method of the CIM\_Rack class</span></span>

<span data-ttu-id="7895f-104">Die **iscompatible** -Methode überprüft, ob das Rack, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7895f-104">The **IsCompatible** method verifies whether the referenced rack can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="7895f-105">In einer Unterklasse kann der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7895f-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="7895f-106">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, können auch in der Unterklasse als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7895f-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="7895f-107">Diese Methode wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7895f-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7895f-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7895f-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7895f-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7895f-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7895f-110">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="7895f-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7895f-111">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7895f-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7895f-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="7895f-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="7895f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7895f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7895f-114">*Elementto-Check* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7895f-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7895f-115">Verweis auf das physische Element, für das diese Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7895f-115">Reference to the physical element that this method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7895f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7895f-116">Return value</span></span>

<span data-ttu-id="7895f-117">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="7895f-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7895f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7895f-118">Remarks</span></span>

<span data-ttu-id="7895f-119">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="7895f-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7895f-120">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="7895f-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="7895f-121">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7895f-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7895f-122">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7895f-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7895f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7895f-123">Requirements</span></span>



| <span data-ttu-id="7895f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7895f-124">Requirement</span></span> | <span data-ttu-id="7895f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7895f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7895f-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7895f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7895f-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7895f-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7895f-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7895f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7895f-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7895f-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7895f-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="7895f-130">Namespace</span></span><br/>                | <span data-ttu-id="7895f-131">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7895f-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7895f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7895f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7895f-133"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7895f-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7895f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7895f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7895f-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7895f-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7895f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7895f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7895f-137">**CIM- \_ Rack**</span><span class="sxs-lookup"><span data-stu-id="7895f-137">**CIM\_Rack**</span></span>](iscompatible-method-in-class-cim-rack.md)
</dt> <dt>

[<span data-ttu-id="7895f-138">**CIM- \_ Rack**</span><span class="sxs-lookup"><span data-stu-id="7895f-138">**CIM\_Rack**</span></span>](cim-rack.md)
</dt> </dl>

 

