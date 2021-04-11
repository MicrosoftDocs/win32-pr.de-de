---
description: Die \_ WMI-Klasse für die Win32 programgroupcontent Association verknüpft eine Programm Gruppen Reihenfolge und eine einzelne darin enthaltene Programmgruppe bzw. ein bestimmtes Element.
ms.assetid: 687794d1-acc1-498a-9886-0c9ac762ebf4
ms.tgt_platform: multiple
title: Win32_ProgramGroupContents-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupContents
- Win32_ProgramGroupContents.GroupComponent
- Win32_ProgramGroupContents.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f77a61052357f7c67009ee7a89da018abeadda8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041362"
---
# <a name="win32_programgroupcontents-class"></a><span data-ttu-id="1dc5c-103">Win32 \_ programgroupcontents-Klasse</span><span class="sxs-lookup"><span data-stu-id="1dc5c-103">Win32\_ProgramGroupContents class</span></span>

<span data-ttu-id="1dc5c-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32 \_ programgroupcontent** Association verknüpft eine Programm Gruppen Reihenfolge und eine einzelne darin enthaltene Programmgruppe bzw. ein bestimmtes Element.</span><span class="sxs-lookup"><span data-stu-id="1dc5c-104">The **Win32\_ProgramGroupContents** association [WMI class](../wmisdk/retrieving-a-class.md) relates a program group order and an individual program group or item contained in it.</span></span>

<span data-ttu-id="1dc5c-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1dc5c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1dc5c-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="1dc5c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc5c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dc5c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{86E30E83-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupContents : CIM_Component
{
  Win32_LogicalProgramGroup REF GroupComponent;
  Win32_ProgramGroupOrItem  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="1dc5c-108">Member</span><span class="sxs-lookup"><span data-stu-id="1dc5c-108">Members</span></span>

<span data-ttu-id="1dc5c-109">Die **Win32 \_ programgroupcontents** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1dc5c-109">The **Win32\_ProgramGroupContents** class has these types of members:</span></span>

-   [<span data-ttu-id="1dc5c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1dc5c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1dc5c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1dc5c-111">Properties</span></span>

<span data-ttu-id="1dc5c-112">Die **Win32 \_ programgroupcontents** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1dc5c-112">The **Win32\_ProgramGroupContents** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1dc5c-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="1dc5c-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dc5c-114">Datentyp: **Win32 \_ logicalprogramgroup**</span><span class="sxs-lookup"><span data-stu-id="1dc5c-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="1dc5c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1dc5c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dc5c-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ logicalprogram Group")</span><span class="sxs-lookup"><span data-stu-id="1dc5c-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="1dc5c-117">Verweis auf die-Instanz, die die logische Programmgruppe für diese Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1dc5c-117">Reference to the instance representing the logical program group for this association.</span></span>

</dd> <dt>

<span data-ttu-id="1dc5c-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1dc5c-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dc5c-119">Datentyp: **Win32 \_ programgrouporitem**</span><span class="sxs-lookup"><span data-stu-id="1dc5c-119">Data type: **Win32\_ProgramGroupOrItem**</span></span>
</dt> <dt>

<span data-ttu-id="1dc5c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1dc5c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dc5c-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ programgrouporitem")</span><span class="sxs-lookup"><span data-stu-id="1dc5c-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ProgramGroupOrItem")</span></span>
</dt> </dl>

<span data-ttu-id="1dc5c-122">Verweis auf die-Instanz, die die **Start** Menü Gruppe bzw. das Element für diese Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1dc5c-122">Reference to the instance representing the **Start** menu group or item for this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1dc5c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dc5c-123">Remarks</span></span>

<span data-ttu-id="1dc5c-124">Die **Win32 \_ programgroupcontents** -Klasse wird von der [**CIM- \_ Komponente**](cim-component.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1dc5c-124">The **Win32\_ProgramGroupContents** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1dc5c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1dc5c-125">Requirements</span></span>



| <span data-ttu-id="1dc5c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1dc5c-126">Requirement</span></span> | <span data-ttu-id="1dc5c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1dc5c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc5c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1dc5c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc5c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1dc5c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1dc5c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1dc5c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc5c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1dc5c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1dc5c-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="1dc5c-132">Namespace</span></span><br/>                | <span data-ttu-id="1dc5c-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1dc5c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1dc5c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1dc5c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1dc5c-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1dc5c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1dc5c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1dc5c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dc5c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dc5c-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dc5c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dc5c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc5c-139">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="1dc5c-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="1dc5c-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="1dc5c-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
