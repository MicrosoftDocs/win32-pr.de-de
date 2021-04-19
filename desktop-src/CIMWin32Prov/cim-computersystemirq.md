---
description: Die CIM \_ computersystemirq-Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren Interrupt Request Lines (unqs) dar.
ms.assetid: c2a1f231-1f8e-48b2-9afe-fa798e6a8a1d
ms.tgt_platform: multiple
title: CIM_ComputerSystemIRQ-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemIRQ
- CIM_ComputerSystemIRQ.GroupComponent
- CIM_ComputerSystemIRQ.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490b1f26e8d100f675a6e57a8ddf7a53770d4ea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343177"
---
# <a name="cim_computersystemirq-class"></a><span data-ttu-id="8bb2c-103">CIM \_ computersystemirq-Klasse</span><span class="sxs-lookup"><span data-stu-id="8bb2c-103">CIM\_ComputerSystemIRQ class</span></span>

<span data-ttu-id="8bb2c-104">Die **CIM \_ computersystemirq** -Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren Interrupt Request Lines (unqs) dar.</span><span class="sxs-lookup"><span data-stu-id="8bb2c-104">The **CIM\_ComputerSystemIRQ** class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8bb2c-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8bb2c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8bb2c-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8bb2c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8bb2c-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8bb2c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8bb2c-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8bb2c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb2c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bb2c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC896-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemIRQ : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_IRQ            REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="8bb2c-110">Member</span><span class="sxs-lookup"><span data-stu-id="8bb2c-110">Members</span></span>

<span data-ttu-id="8bb2c-111">Die **CIM \_ computersystemirq** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8bb2c-111">The **CIM\_ComputerSystemIRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="8bb2c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8bb2c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8bb2c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8bb2c-113">Properties</span></span>

<span data-ttu-id="8bb2c-114">Die **CIM \_ computersystemirq** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8bb2c-114">The **CIM\_ComputerSystemIRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bb2c-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8bb2c-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bb2c-116">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="8bb2c-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="8bb2c-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8bb2c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bb2c-118">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span><span class="sxs-lookup"><span data-stu-id="8bb2c-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span></span>
</dt> </dl>

<span data-ttu-id="8bb2c-119">Ein [**CIM- \_ Computersystem**](cim-computersystem.md) , das den dem UNQ zugeordneten Computer beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8bb2c-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer associated with the IRQ.</span></span>

<span data-ttu-id="8bb2c-120">Diese Eigenschaft wird von [ **CIM \_ computersystemresource** geerbt.](cim-computersystemresource.md)</span><span class="sxs-lookup"><span data-stu-id="8bb2c-120">This property is inherited from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md)</span></span>

</dd> <dt>

<span data-ttu-id="8bb2c-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8bb2c-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bb2c-122">Datentyp: **CIM \_ irren**</span><span class="sxs-lookup"><span data-stu-id="8bb2c-122">Data type: **CIM\_IRQ**</span></span>
</dt> <dt>

<span data-ttu-id="8bb2c-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8bb2c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bb2c-124">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("PartComponent"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8bb2c-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8bb2c-125">Eine [**CIM- \_ UNQ**](cim-irq.md) , die eine UNQ des Computer Systems beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8bb2c-125">A [**CIM\_IRQ**](cim-irq.md) describing an IRQ of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8bb2c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8bb2c-126">Remarks</span></span>

<span data-ttu-id="8bb2c-127">Die **CIM \_ computersystemirq** -Klasse wird von [**CIM \_ computersystemresource**](cim-computersystemresource.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8bb2c-127">The **CIM\_ComputerSystemIRQ** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="8bb2c-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8bb2c-128">WMI does not implement this class.</span></span>

<span data-ttu-id="8bb2c-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8bb2c-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8bb2c-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8bb2c-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb2c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bb2c-131">Requirements</span></span>



| <span data-ttu-id="8bb2c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bb2c-132">Requirement</span></span> | <span data-ttu-id="8bb2c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="8bb2c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb2c-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8bb2c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb2c-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bb2c-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8bb2c-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8bb2c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb2c-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bb2c-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8bb2c-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bb2c-138">Namespace</span></span><br/>                | <span data-ttu-id="8bb2c-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8bb2c-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8bb2c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="8bb2c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bb2c-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8bb2c-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bb2c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8bb2c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bb2c-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bb2c-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb2c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bb2c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb2c-145">**CIM \_ computersystemresource**</span><span class="sxs-lookup"><span data-stu-id="8bb2c-145">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

