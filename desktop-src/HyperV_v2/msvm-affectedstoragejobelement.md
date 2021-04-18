---
description: Stellt die Zuordnung zwischen einem Auftrag und den verwalteten Elementen dar, die von seiner Ausführung betroffen sein können.
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Msvm_AffectedStorageJobElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d900f42e5022301a08ebeee0036400be3a2f1bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344646"
---
# <a name="msvm_affectedstoragejobelement-class"></a><span data-ttu-id="9fdfc-103">MSVM \_ affectedstoragejobelements-Klasse</span><span class="sxs-lookup"><span data-stu-id="9fdfc-103">Msvm\_AffectedStorageJobElement class</span></span>

<span data-ttu-id="9fdfc-104">Stellt die Zuordnung zwischen einem Auftrag und den verwalteten Elementen dar, die von seiner Ausführung betroffen sein können.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-104">Represents the association between a job and the managed elements that may be affected by its execution.</span></span>

<span data-ttu-id="9fdfc-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fdfc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fdfc-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="9fdfc-107">Member</span><span class="sxs-lookup"><span data-stu-id="9fdfc-107">Members</span></span>

<span data-ttu-id="9fdfc-108">Die **MSVM \_ affectedstoragejobelements** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9fdfc-108">The **Msvm\_AffectedStorageJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="9fdfc-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9fdfc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9fdfc-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9fdfc-110">Properties</span></span>

<span data-ttu-id="9fdfc-111">Die **MSVM \_ affectedstoragejobelements** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-111">The **Msvm\_AffectedStorageJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9fdfc-112">**Affectedelta-Element**</span><span class="sxs-lookup"><span data-stu-id="9fdfc-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fdfc-113">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="9fdfc-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="9fdfc-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9fdfc-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fdfc-115">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="9fdfc-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9fdfc-116">Das verwaltete Element, das von der Ausführung des Auftrags betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-116">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="9fdfc-117">Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-117">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9fdfc-118">**Affectingelement**</span><span class="sxs-lookup"><span data-stu-id="9fdfc-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fdfc-119">Datentyp: **[ **MSVM \_ storagejob**](msvm-storagejob.md)**</span><span class="sxs-lookup"><span data-stu-id="9fdfc-119">Data type: **[**Msvm\_StorageJob**](msvm-storagejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="9fdfc-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9fdfc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fdfc-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ affectedjobelement. affectingelement")</span><span class="sxs-lookup"><span data-stu-id="9fdfc-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_AffectedJobElement.AffectingElement")</span></span>
</dt> </dl>

<span data-ttu-id="9fdfc-122">Der Auftrag, der sich auf das betroffene Element auswirkt.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-122">The job that is affecting the affected element.</span></span> <span data-ttu-id="9fdfc-123">Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-123">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9fdfc-124">**Elementeffects**</span><span class="sxs-lookup"><span data-stu-id="9fdfc-124">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fdfc-125">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9fdfc-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9fdfc-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9fdfc-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fdfc-127">Eine Enumeration, die den Effekt auf das verwaltete Element beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-127">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="9fdfc-128">Dieses Array entspricht dem **otherelementeffectbeschreigenschaftenarray** , bei dem letztere Details zu den von dieser Eigenschaft aufgelisteten Grund Effekten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-128">This array corresponds to the **OtherElementEffectsDescriptions** property array, where the latter provides details related to the high-level effects enumerated by this property.</span></span> <span data-ttu-id="9fdfc-129">Weitere Details sind erforderlich, wenn das **elementeffects** -Eigenschafts Array den Wert 1 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-129">Additional detail is required if the **ElementEffects** property array contains the value 1, (Other).</span></span> <span data-ttu-id="9fdfc-130">Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-130">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9fdfc-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9fdfc-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9fdfc-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9fdfc-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9fdfc-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Exklusive Verwendung** (2)</span><span class="sxs-lookup"><span data-stu-id="9fdfc-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Exclusive Use** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9fdfc-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Leistungs Beeinträchtigung** (3)</span><span class="sxs-lookup"><span data-stu-id="9fdfc-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Performance Impact** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9fdfc-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Element Integrität** (4)</span><span class="sxs-lookup"><span data-stu-id="9fdfc-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Element Integrity** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9fdfc-136">**Otherelementeffect-Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="9fdfc-136">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fdfc-137">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="9fdfc-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9fdfc-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9fdfc-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fdfc-139">Stellt Details für den Effekt an der entsprechenden Array Position im **elementeffects** -Eigenschafts Array bereit.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-139">Provides details for the effect at the corresponding array position in the **ElementEffects** property array.</span></span> <span data-ttu-id="9fdfc-140">Diese Informationen sind immer dann erforderlich, wenn das entsprechende Element im **elementeffects** -Eigenschafts Array den Wert 1 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-140">This information is required whenever the corresponding element in the **ElementEffects** property array contains the value 1 (Other).</span></span> <span data-ttu-id="9fdfc-141">Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-141">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fdfc-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fdfc-142">Remarks</span></span>

<span data-ttu-id="9fdfc-143">Der Zugriff auf die **MSVM \_ affectedstoragejobelements** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-143">Access to the **Msvm\_AffectedStorageJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9fdfc-144">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9fdfc-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fdfc-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fdfc-145">Requirements</span></span>



| <span data-ttu-id="9fdfc-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fdfc-146">Requirement</span></span> | <span data-ttu-id="9fdfc-147">Wert</span><span class="sxs-lookup"><span data-stu-id="9fdfc-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fdfc-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fdfc-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9fdfc-149">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fdfc-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9fdfc-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fdfc-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9fdfc-151">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fdfc-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9fdfc-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fdfc-152">Namespace</span></span><br/>                | <span data-ttu-id="9fdfc-153">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9fdfc-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9fdfc-154">MOF</span><span class="sxs-lookup"><span data-stu-id="9fdfc-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fdfc-155"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9fdfc-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fdfc-156">DLL</span><span class="sxs-lookup"><span data-stu-id="9fdfc-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fdfc-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9fdfc-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9fdfc-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fdfc-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fdfc-159">**CIM- \_ affectedjobelements**</span><span class="sxs-lookup"><span data-stu-id="9fdfc-159">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="9fdfc-160">[**CIM- \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9fdfc-160">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9fdfc-161">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="9fdfc-161">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

