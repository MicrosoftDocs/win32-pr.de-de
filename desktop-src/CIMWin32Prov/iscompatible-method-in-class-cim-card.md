---
description: Die iscompatible-Methode überprüft, ob das physische-Element, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.
ms.assetid: 809a1871-dfa2-499b-9adf-118dec71586b
ms.tgt_platform: multiple
title: Iscompatible-Methode der CIM_Card-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Card.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0573cc9902826d2a283e549414cf31aae98cc331
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126457"
---
# <a name="iscompatible-method-of-the-cim_card-class"></a><span data-ttu-id="f33d1-103">Iscompatible-Methode der CIM- \_ Karten Klasse</span><span class="sxs-lookup"><span data-stu-id="f33d1-103">IsCompatible method of the CIM\_Card class</span></span>

<span data-ttu-id="f33d1-104">Die **iscompatible** -Methode überprüft, ob das physische-Element, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f33d1-104">The **IsCompatible** method verifies whether the referenced physical element may be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="f33d1-105">In einer Unterklasse kann der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f33d1-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="f33d1-106">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, können auch in der Unterklasse als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f33d1-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="f33d1-107">Diese Methode wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f33d1-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f33d1-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f33d1-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f33d1-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f33d1-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f33d1-110">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f33d1-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f33d1-111">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f33d1-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f33d1-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="f33d1-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="f33d1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f33d1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f33d1-114">*Elementto-Check* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f33d1-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f33d1-115">Verweis auf das physische Element, für das die **iscompatible** -Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f33d1-115">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f33d1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f33d1-116">Return value</span></span>

<span data-ttu-id="f33d1-117">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="f33d1-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f33d1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f33d1-118">Remarks</span></span>

<span data-ttu-id="f33d1-119">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="f33d1-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f33d1-120">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="f33d1-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f33d1-121">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f33d1-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f33d1-122">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f33d1-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f33d1-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f33d1-123">Requirements</span></span>



| <span data-ttu-id="f33d1-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f33d1-124">Requirement</span></span> | <span data-ttu-id="f33d1-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f33d1-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f33d1-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f33d1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f33d1-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f33d1-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f33d1-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f33d1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f33d1-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f33d1-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f33d1-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="f33d1-130">Namespace</span></span><br/>                | <span data-ttu-id="f33d1-131">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f33d1-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f33d1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f33d1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f33d1-133"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f33d1-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f33d1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f33d1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f33d1-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f33d1-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f33d1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f33d1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33d1-137">CIM- \_ Karte</span><span class="sxs-lookup"><span data-stu-id="f33d1-137">CIM\_Card</span></span>](iscompatible-method-in-class-cim-card.md)
</dt> <dt>

[<span data-ttu-id="f33d1-138">**CIM- \_ Karte**</span><span class="sxs-lookup"><span data-stu-id="f33d1-138">**CIM\_Card**</span></span>](cim-card.md)
</dt> </dl>

 

