---
description: Überprüft, ob das physische-Element, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.
ms.assetid: 406aaa75-b48c-4377-adb5-e900676b6e36
ms.tgt_platform: multiple
title: Iscompatible-Methode der CIM_PhysicalPackage-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1957b8d0c1929ff6f7b4ef8c69fa55ea4ccc83b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343598"
---
# <a name="iscompatible-method-of-the-cim_physicalpackage-class"></a><span data-ttu-id="a4d63-103">Iscompatible-Methode der CIM \_ physicalpackage-Klasse</span><span class="sxs-lookup"><span data-stu-id="a4d63-103">IsCompatible method of the CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="a4d63-104">Die **iscompatible** -Methode überprüft, ob das physische-Element, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a4d63-104">The **IsCompatible** method verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="a4d63-105">In einer Unterklasse kann der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a4d63-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="a4d63-106">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, können auch in der Unterklasse als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a4d63-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a4d63-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a4d63-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a4d63-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a4d63-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a4d63-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4d63-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a4d63-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a4d63-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d63-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4d63-111">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="a4d63-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4d63-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4d63-113">*Elementto-Check* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4d63-113">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d63-114">Verweis auf das physische Element, für das die **iscompatible** -Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4d63-114">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4d63-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4d63-115">Return value</span></span>

<span data-ttu-id="a4d63-116">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="a4d63-116">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4d63-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4d63-117">Remarks</span></span>

<span data-ttu-id="a4d63-118">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="a4d63-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a4d63-119">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="a4d63-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a4d63-120">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a4d63-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a4d63-121">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a4d63-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4d63-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4d63-122">Requirements</span></span>



| <span data-ttu-id="a4d63-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4d63-123">Requirement</span></span> | <span data-ttu-id="a4d63-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a4d63-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d63-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4d63-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a4d63-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4d63-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4d63-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4d63-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a4d63-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4d63-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4d63-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4d63-129">Namespace</span></span><br/>                | <span data-ttu-id="a4d63-130">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a4d63-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a4d63-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a4d63-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4d63-132"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a4d63-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4d63-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a4d63-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4d63-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4d63-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4d63-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4d63-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d63-136">**CIM- \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="a4d63-136">**CIM\_PhysicalPackage**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="a4d63-137">**CIM- \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="a4d63-137">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

