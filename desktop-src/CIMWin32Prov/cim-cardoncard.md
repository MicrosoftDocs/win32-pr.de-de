---
description: Die CIM \_ cardoncard-Zuordnung beschreibt die Beziehungen zu Karten, die an den über Ladungen/Baseboards, daughtercards eines Adapters oder Karten mit speziellen Karten ähnlichen Modulen angeschlossen werden können.
ms.assetid: a500b29d-d836-4755-b5df-b296e3cbd2ab
ms.tgt_platform: multiple
title: CIM_CardOnCard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardOnCard
- CIM_CardOnCard.LocationWithinContainer
- CIM_CardOnCard.PartComponent
- CIM_CardOnCard.GroupComponent
- CIM_CardOnCard.MountOrSlotDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15f94bb8d0f159e71cac44f069f9d8e7d9453509
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393118"
---
# <a name="cim_cardoncard-class"></a><span data-ttu-id="faa1b-103">CIM \_ cardoncard-Klasse</span><span class="sxs-lookup"><span data-stu-id="faa1b-103">CIM\_CardOnCard class</span></span>

<span data-ttu-id="faa1b-104">Die **CIM \_ cardoncard** -Zuordnung beschreibt die Beziehungen zu Karten, die an den über Ladungen/Baseboards, daughtercards eines Adapters oder Karten mit speziellen Karten ähnlichen Modulen angeschlossen werden können.</span><span class="sxs-lookup"><span data-stu-id="faa1b-104">The **CIM\_CardOnCard** association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="faa1b-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="faa1b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="faa1b-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="faa1b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="faa1b-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="faa1b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="faa1b-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="faa1b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="faa1b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="faa1b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B77-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardOnCard : CIM_Container
{
  string       LocationWithinContainer;
  CIM_Card REF PartComponent;
  CIM_Card REF GroupComponent;
  string       MountOrSlotDescription;
};
```

## <a name="members"></a><span data-ttu-id="faa1b-110">Member</span><span class="sxs-lookup"><span data-stu-id="faa1b-110">Members</span></span>

<span data-ttu-id="faa1b-111">Die **CIM \_ cardoncard** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="faa1b-111">The **CIM\_CardOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="faa1b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="faa1b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="faa1b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="faa1b-113">Properties</span></span>

<span data-ttu-id="faa1b-114">Die **CIM \_ cardoncard** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="faa1b-114">The **CIM\_CardOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="faa1b-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="faa1b-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faa1b-116">Datentyp: **CIM- \_ Karte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-116">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="faa1b-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="faa1b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="faa1b-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="faa1b-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="faa1b-119">Eine [**CIM- \_ Karte**](cim-card.md) , die die Karte beschreibt, die eine andere Karte hostet.</span><span class="sxs-lookup"><span data-stu-id="faa1b-119">A [**CIM\_Card**](cim-card.md) that describes the card that hosts another card.</span></span>

</dd> <dt>

<span data-ttu-id="faa1b-120">**Locationwithincontainer**</span><span class="sxs-lookup"><span data-stu-id="faa1b-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faa1b-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="faa1b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="faa1b-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="faa1b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="faa1b-123">Eine frei Form Zeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt.</span><span class="sxs-lookup"><span data-stu-id="faa1b-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="faa1b-124">Informationen in Bezug auf die stationären Elemente im Container (z. b. "Second Drive Bay from the Top"), Winkel, Höhen und andere Daten können in dieser Eigenschaft aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="faa1b-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="faa1b-125">Diese Zeichenfolge kann anstelle der Instanziierung des [**CIM- \_ Speicherort**](cim-location.md) Objekts ergänzt oder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="faa1b-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="faa1b-126">Diese Eigenschaft wird vom [**CIM- \_ Container**](cim-container.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="faa1b-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="faa1b-127">**Mountor slotdescription**</span><span class="sxs-lookup"><span data-stu-id="faa1b-127">**MountOrSlotDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faa1b-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="faa1b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="faa1b-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="faa1b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="faa1b-130">Hier wird beschrieben, wie die Karte an der Karte "Other" eingebunden oder an diese angeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="faa1b-130">Describes and identifies how the card is mounted on or plugged into the "other" card.</span></span> <span data-ttu-id="faa1b-131">Slotinformationen können in dieses Feld eingeschlossen werden und sind möglicherweise für bestimmte Verwaltungszwecke ausreichend. Dadurch wird das Erstellen von Instanziierungen von Connector/Slot-Objekten vermieden, um die Beziehung von Karten zu hostingboards oder anderen Adaptern zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="faa1b-131">Slot information can be included in this field and may be sufficient for certain management purposes, which avoids creating instantiations of connector/slot objects just to model the relationship of cards to hosting boards or other adapters.</span></span> <span data-ttu-id="faa1b-132">Wenn die Informationen zum Slot und zum Connector verfügbar sind, können Sie dieses Feld verwenden, um ausführliche Einfügungs-oder einfügeeinfügedaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="faa1b-132">On the other hand, if slot and connector information is available, this field can be used to provide detailed mounting or slot insertion data.</span></span>

</dd> <dt>

<span data-ttu-id="faa1b-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="faa1b-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faa1b-134">Datentyp: **CIM- \_ Karte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-134">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="faa1b-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="faa1b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="faa1b-136">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="faa1b-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="faa1b-137">Eine [**CIM- \_ Karte**](cim-card.md) , die die Karte beschreibt, die an eine andere Karte angeschlossen ist oder anderweitig bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="faa1b-137">A [**CIM\_Card**](cim-card.md) that describes the card that is plugged into or otherwise mounted on another card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="faa1b-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="faa1b-138">Remarks</span></span>

<span data-ttu-id="faa1b-139">Die **CIM \_ cardoncard** -Klasse wird vom [**CIM- \_ Container**](cim-container.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="faa1b-139">The **CIM\_CardOnCard** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="faa1b-140">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="faa1b-140">WMI does not implement this class.</span></span>

<span data-ttu-id="faa1b-141">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="faa1b-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="faa1b-142">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="faa1b-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="faa1b-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faa1b-143">Requirements</span></span>



| <span data-ttu-id="faa1b-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="faa1b-144">Requirement</span></span> | <span data-ttu-id="faa1b-145">Wert</span><span class="sxs-lookup"><span data-stu-id="faa1b-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="faa1b-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="faa1b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="faa1b-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="faa1b-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="faa1b-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="faa1b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="faa1b-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="faa1b-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="faa1b-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="faa1b-150">Namespace</span></span><br/>                | <span data-ttu-id="faa1b-151">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="faa1b-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="faa1b-152">MOF</span><span class="sxs-lookup"><span data-stu-id="faa1b-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faa1b-153"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="faa1b-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="faa1b-154">DLL</span><span class="sxs-lookup"><span data-stu-id="faa1b-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="faa1b-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faa1b-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faa1b-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faa1b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faa1b-157">**CIM- \_ Container**</span><span class="sxs-lookup"><span data-stu-id="faa1b-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

