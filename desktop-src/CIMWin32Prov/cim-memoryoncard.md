---
description: Die CIM \_ memoryoncard-Klasse ordnet physischen Speicher zu, der sich auf hostingboards, Adapterkarten usw. befindet. Diese Zuordnung definiert explizit die Beziehung Zwischenspeicher und Karten.
ms.assetid: 0d094cad-c542-4794-b6e1-87cdc8067668
ms.tgt_platform: multiple
title: CIM_MemoryOnCard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryOnCard
- CIM_MemoryOnCard.LocationWithinContainer
- CIM_MemoryOnCard.PartComponent
- CIM_MemoryOnCard.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2094101ab0cbbbc769194793273bf080cfe52818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340124"
---
# <a name="cim_memoryoncard-class"></a><span data-ttu-id="fb320-104">CIM \_ memoryoncard-Klasse</span><span class="sxs-lookup"><span data-stu-id="fb320-104">CIM\_MemoryOnCard class</span></span>

<span data-ttu-id="fb320-105">Die **CIM \_ memoryoncard** -Klasse ordnet physischen Speicher zu, der sich auf hostingboards, Adapterkarten usw. befindet.</span><span class="sxs-lookup"><span data-stu-id="fb320-105">The **CIM\_MemoryOnCard** class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="fb320-106">Diese Zuordnung definiert explizit die Beziehung Zwischenspeicher und Karten.</span><span class="sxs-lookup"><span data-stu-id="fb320-106">This association explicitly defines the relationship of memory to cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb320-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fb320-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fb320-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fb320-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fb320-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="fb320-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fb320-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fb320-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb320-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb320-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryOnCard : CIM_PackagedComponent
{
  string                 LocationWithinContainer;
  CIM_PhysicalMemory REF PartComponent;
  CIM_Card           REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="fb320-112">Member</span><span class="sxs-lookup"><span data-stu-id="fb320-112">Members</span></span>

<span data-ttu-id="fb320-113">Die **CIM \_ memoryoncard** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fb320-113">The **CIM\_MemoryOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="fb320-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb320-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb320-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb320-115">Properties</span></span>

<span data-ttu-id="fb320-116">Die **CIM \_ memoryoncard** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fb320-116">The **CIM\_MemoryOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb320-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="fb320-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb320-118">Datentyp: **CIM- \_ Karte**</span><span class="sxs-lookup"><span data-stu-id="fb320-118">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="fb320-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb320-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb320-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="fb320-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="fb320-121">Eine [**CIM- \_ Karte**](cim-card.md) , die die Karte beschreibt, die den Arbeitsspeicher enthält oder enthält.</span><span class="sxs-lookup"><span data-stu-id="fb320-121">A [**CIM\_Card**](cim-card.md) describing the card that includes or 'contains' memory.</span></span>

</dd> <dt>

<span data-ttu-id="fb320-122">**Locationwithincontainer**</span><span class="sxs-lookup"><span data-stu-id="fb320-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb320-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb320-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb320-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb320-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb320-125">Eine frei Form Zeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb320-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="fb320-126">Informationen in Bezug auf die stationären Elemente im Container (z. b. "Second Drive Bay from the Top"), Winkel, Höhen und andere Daten können in dieser Eigenschaft aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="fb320-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="fb320-127">Diese Zeichenfolge kann anstelle der Instanziierung des [**CIM- \_ Speicherort**](cim-location.md) Objekts ergänzt oder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb320-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="fb320-128">Diese Eigenschaft wird vom [**CIM- \_ Container**](cim-container.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb320-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb320-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="fb320-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb320-130">Datentyp: **CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="fb320-130">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="fb320-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb320-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb320-132">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="fb320-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="fb320-133">Ein [**CIM- \_ PhysicalMemory**](cim-physicalmemory.md) , der den physischen Speicher beschreibt, der sich auf der Karte befindet.</span><span class="sxs-lookup"><span data-stu-id="fb320-133">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) describing the physical memory which is located on the card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb320-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb320-134">Remarks</span></span>

<span data-ttu-id="fb320-135">Die **CIM \_ memoryoncard** -Klasse wird von [**CIM \_ packagedcomponent**](cim-packagedcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fb320-135">The **CIM\_MemoryOnCard** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

<span data-ttu-id="fb320-136">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="fb320-136">WMI does not implement this class.</span></span>

<span data-ttu-id="fb320-137">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fb320-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fb320-138">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fb320-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb320-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb320-139">Requirements</span></span>



| <span data-ttu-id="fb320-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb320-140">Requirement</span></span> | <span data-ttu-id="fb320-141">Wert</span><span class="sxs-lookup"><span data-stu-id="fb320-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb320-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb320-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fb320-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb320-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fb320-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb320-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fb320-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb320-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fb320-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb320-146">Namespace</span></span><br/>                | <span data-ttu-id="fb320-147">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fb320-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fb320-148">MOF</span><span class="sxs-lookup"><span data-stu-id="fb320-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb320-149"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fb320-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb320-150">DLL</span><span class="sxs-lookup"><span data-stu-id="fb320-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb320-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb320-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb320-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb320-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb320-153">**CIM \_ packagedcomponent**</span><span class="sxs-lookup"><span data-stu-id="fb320-153">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> </dl>

 

