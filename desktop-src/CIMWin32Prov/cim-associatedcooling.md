---
description: Die CIM \_ associatedcooling-Zuordnung gibt an, wann die Lüfter oder andere Kühlgeräte für ein Gerät spezifisch sind (im Gegensatz zur Bereitstellung von Gehäuse oder CAB-Kühlung).
ms.assetid: 7b20e429-593c-4365-a340-1aef9b0fadf5
ms.tgt_platform: multiple
title: CIM_AssociatedCooling-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedCooling
- CIM_AssociatedCooling.Dependent
- CIM_AssociatedCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb838129226b225f024917e8f8e77ddc92ddf2ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127213"
---
# <a name="cim_associatedcooling-class"></a><span data-ttu-id="13198-103">CIM \_ associatedcooling-Klasse</span><span class="sxs-lookup"><span data-stu-id="13198-103">CIM\_AssociatedCooling class</span></span>

<span data-ttu-id="13198-104">Die **CIM \_ associatedcooling** -Zuordnung gibt an, wann die Lüfter oder andere Kühlgeräte für ein Gerät spezifisch sind (im Gegensatz zur Bereitstellung von Gehäuse oder CAB-Kühlung).</span><span class="sxs-lookup"><span data-stu-id="13198-104">The **CIM\_AssociatedCooling** association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

<span data-ttu-id="13198-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="13198-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="13198-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="13198-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13198-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="13198-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{306F88F2-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedCooling : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_CoolingDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="13198-108">Member</span><span class="sxs-lookup"><span data-stu-id="13198-108">Members</span></span>

<span data-ttu-id="13198-109">Die **CIM \_ associatedcooling** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="13198-109">The **CIM\_AssociatedCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="13198-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13198-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13198-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13198-111">Properties</span></span>

<span data-ttu-id="13198-112">Die **CIM \_ associatedcooling** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="13198-112">The **CIM\_AssociatedCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13198-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="13198-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13198-114">Datentyp: **CIM \_ coolingdevice**</span><span class="sxs-lookup"><span data-stu-id="13198-114">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="13198-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13198-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13198-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="13198-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="13198-117">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das Kühlgerät beschreibt.</span><span class="sxs-lookup"><span data-stu-id="13198-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the cooling device.</span></span>

</dd> <dt>

<span data-ttu-id="13198-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="13198-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13198-119">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="13198-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="13198-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13198-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13198-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="13198-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="13198-122">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das auf das zu kühlende logische Gerät verweist.</span><span class="sxs-lookup"><span data-stu-id="13198-122">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that references the logical device being cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13198-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13198-123">Remarks</span></span>

<span data-ttu-id="13198-124">Die **CIM \_ associatedcooling** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="13198-124">The **CIM\_AssociatedCooling** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="13198-125">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="13198-125">WMI does not implement this class.</span></span>

<span data-ttu-id="13198-126">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="13198-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="13198-127">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="13198-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="13198-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13198-128">Requirements</span></span>



| <span data-ttu-id="13198-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13198-129">Requirement</span></span> | <span data-ttu-id="13198-130">Wert</span><span class="sxs-lookup"><span data-stu-id="13198-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13198-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13198-131">Minimum supported client</span></span><br/> | <span data-ttu-id="13198-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13198-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13198-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13198-133">Minimum supported server</span></span><br/> | <span data-ttu-id="13198-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13198-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13198-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="13198-135">Namespace</span></span><br/>                | <span data-ttu-id="13198-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="13198-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="13198-137">MOF</span><span class="sxs-lookup"><span data-stu-id="13198-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13198-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="13198-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="13198-139">DLL</span><span class="sxs-lookup"><span data-stu-id="13198-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13198-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13198-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13198-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13198-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13198-142">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="13198-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

