---
description: Stellt eine Auflistung von virtuellen System Referenzpunkten dar.
ms.assetid: dc293f94-a683-468f-af05-ba99824d773e
title: Msvm_ReferencePointCollection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointCollection
- Msvm_ReferencePointCollection.CollectionID
- Msvm_ReferencePointCollection.ElementName
- Msvm_ReferencePointCollection.ReferencePointType
- Msvm_ReferencePointCollection.ConsistencyLevel
- Msvm_ReferencePointCollection.VirtualSystemCollectionId
- Msvm_ReferencePointCollection.HasAssociatedLog
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 570590221ee8568d78e150fec3c359365c8434cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865524"
---
# <a name="msvm_referencepointcollection-class"></a><span data-ttu-id="5e788-103">MSVM \_ referencepointcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="5e788-103">Msvm\_ReferencePointCollection class</span></span>

<span data-ttu-id="5e788-104">Stellt eine Auflistung von virtuellen System Referenzpunkten dar.</span><span class="sxs-lookup"><span data-stu-id="5e788-104">Represents a collection of virtual system reference points.</span></span>

<span data-ttu-id="5e788-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5e788-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e788-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e788-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointCollection : CIM_Collection
{
  string  CollectionID;
  string  ElementName;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemCollectionId;
  boolean HasAssociatedLog;
};
```

## <a name="members"></a><span data-ttu-id="5e788-107">Member</span><span class="sxs-lookup"><span data-stu-id="5e788-107">Members</span></span>

<span data-ttu-id="5e788-108">Die **MSVM \_ referencepointcollection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5e788-108">The **Msvm\_ReferencePointCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="5e788-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e788-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e788-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e788-110">Properties</span></span>

<span data-ttu-id="5e788-111">Die **MSVM \_ referencepointcollection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5e788-111">The **Msvm\_ReferencePointCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e788-112">**Sammlungs**</span><span class="sxs-lookup"><span data-stu-id="5e788-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e788-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5e788-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e788-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5e788-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e788-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5e788-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e788-116">Die eindeutige Identifikation des Auflistungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="5e788-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="5e788-117">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="5e788-117">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e788-118">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e788-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e788-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5e788-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5e788-120">Konsistenz Ebene des Bezugspunkts.</span><span class="sxs-lookup"><span data-stu-id="5e788-120">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e788-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="5e788-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="5e788-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Absturz konsistent** (1)</span><span class="sxs-lookup"><span data-stu-id="5e788-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5e788-123">Der Bezugspunkt gibt einen Zeitpunkt an, an dem sich das virtuelle System in einem Absturz konsistenten Zustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="5e788-123">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="5e788-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Anwendungs konsistent** (2)</span><span class="sxs-lookup"><span data-stu-id="5e788-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5e788-125">Der Bezugspunkt gibt einen Zeitpunkt an, an dem sich das virtuelle System in einem Anwendungs konsistenten Zustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="5e788-125">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5e788-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5e788-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e788-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5e788-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e788-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5e788-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e788-129">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Elementname")</span><span class="sxs-lookup"><span data-stu-id="5e788-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="5e788-130">Ein benutzerdefinierter Name für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="5e788-130">An user-defined name for the collection.</span></span> <span data-ttu-id="5e788-131">Beachten Sie, dass dies nicht unbedingt eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="5e788-131">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="5e788-132">**Hasassociatedlog**</span><span class="sxs-lookup"><span data-stu-id="5e788-132">**HasAssociatedLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e788-133">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5e788-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e788-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5e788-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5e788-135">**true** , wenn allen Mitglieds Verweis Punkten Protokolle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5e788-135">**true** if all the member reference points have associated logs.</span></span> <span data-ttu-id="5e788-136">Dies gilt nur für Protokoll basierte Referenzpunkte.</span><span class="sxs-lookup"><span data-stu-id="5e788-136">This is valid only for log based reference points.</span></span> <span data-ttu-id="5e788-137">Bei RCT-basierten Referenzpunkten wird **hasassociatedlog** auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5e788-137">For RCT based reference points, **HasAssociatedLog** is set to **false**.</span></span> <span data-ttu-id="5e788-138">Bei Protokoll basierten Referenzpunkten wird **hasassociatedlog** , sobald das Protokoll verworfen wird, **false**.</span><span class="sxs-lookup"><span data-stu-id="5e788-138">For log based reference points, once the log is discarded **HasAssociatedLog** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="5e788-139">**Referencepointtype**</span><span class="sxs-lookup"><span data-stu-id="5e788-139">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e788-140">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e788-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e788-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5e788-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e788-142">Qualifizierer: [ **in**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5e788-142">Qualifiers: [**In**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5e788-143">Gibt den Typ des Bezugspunkts an.</span><span class="sxs-lookup"><span data-stu-id="5e788-143">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e788-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="5e788-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="5e788-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Protokoll basiert** (1)</span><span class="sxs-lookup"><span data-stu-id="5e788-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5e788-146">Protokoll Nachverfolgung für Hyper-V-Replikate.</span><span class="sxs-lookup"><span data-stu-id="5e788-146">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="5e788-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT basiert** (2)</span><span class="sxs-lookup"><span data-stu-id="5e788-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5e788-148">Basierend auf robusten Änderungsnachverfolgung von virtuellen Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="5e788-148">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5e788-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="5e788-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="5e788-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="5e788-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5e788-151">**Virtualsystemcollectionid**</span><span class="sxs-lookup"><span data-stu-id="5e788-151">**VirtualSystemCollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e788-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5e788-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e788-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5e788-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e788-154">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ virtualsystemcollection**](msvm-virtualsystemcollection.md).**CollectionId**")</span><span class="sxs-lookup"><span data-stu-id="5e788-154">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md).**CollectionID**")</span></span>
</dt> </dl>

<span data-ttu-id="5e788-155">Der Bezeichner der [**MSVM \_ virtualsystemcollection**](msvm-virtualsystemcollection.md) , zu der dieser Verweis Punkt gehört.</span><span class="sxs-lookup"><span data-stu-id="5e788-155">The identifier of the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to which this reference point belongs.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e788-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e788-156">Requirements</span></span>



| <span data-ttu-id="5e788-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e788-157">Requirement</span></span> | <span data-ttu-id="5e788-158">Wert</span><span class="sxs-lookup"><span data-stu-id="5e788-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e788-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e788-159">Minimum supported client</span></span><br/> | <span data-ttu-id="5e788-160">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e788-160">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5e788-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e788-161">Minimum supported server</span></span><br/> | <span data-ttu-id="5e788-162">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5e788-162">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5e788-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e788-163">Namespace</span></span><br/>                | <span data-ttu-id="5e788-164">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5e788-164">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5e788-165">MOF</span><span class="sxs-lookup"><span data-stu-id="5e788-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e788-166"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5e788-166"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e788-167">DLL</span><span class="sxs-lookup"><span data-stu-id="5e788-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e788-168"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e788-168"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5e788-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e788-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e788-170">**CIM \_ -Auflistung**</span><span class="sxs-lookup"><span data-stu-id="5e788-170">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

