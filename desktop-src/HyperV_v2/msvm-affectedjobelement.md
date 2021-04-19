---
description: Stellt eine Zuordnung zwischen einem Auftrag und dem verwalteten Element dar, das von seiner Ausführung betroffen sein kann.
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Msvm_AffectedJobElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bef667872a7afa4c726ee1b2c77a36c29649114d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356947"
---
# <a name="msvm_affectedjobelement-class"></a><span data-ttu-id="37cc4-103">MSVM \_ affectedjobelements-Klasse</span><span class="sxs-lookup"><span data-stu-id="37cc4-103">Msvm\_AffectedJobElement class</span></span>

<span data-ttu-id="37cc4-104">Stellt eine Zuordnung zwischen einem Auftrag und dem verwalteten Element dar, das von seiner Ausführung betroffen sein kann.</span><span class="sxs-lookup"><span data-stu-id="37cc4-104">Represents an association between a job and the managed element that may be affected by its execution.</span></span>

<span data-ttu-id="37cc4-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="37cc4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37cc4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="37cc4-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="37cc4-107">Member</span><span class="sxs-lookup"><span data-stu-id="37cc4-107">Members</span></span>

<span data-ttu-id="37cc4-108">Die **MSVM \_ affectedjobelements** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="37cc4-108">The **Msvm\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="37cc4-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37cc4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37cc4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37cc4-110">Properties</span></span>

<span data-ttu-id="37cc4-111">Die **MSVM \_ affectedjobelements** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="37cc4-111">The **Msvm\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37cc4-112">**Affectedelta-Element**</span><span class="sxs-lookup"><span data-stu-id="37cc4-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37cc4-113">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="37cc4-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="37cc4-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37cc4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37cc4-115">Das verwaltete Element, das von der Ausführung des Auftrags betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="37cc4-115">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="37cc4-116">Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="37cc4-116">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="37cc4-117">**Affectingelement**</span><span class="sxs-lookup"><span data-stu-id="37cc4-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37cc4-118">Datentyp: **[ **MSVM \_ concretejob**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="37cc4-118">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="37cc4-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37cc4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37cc4-120">Der Auftrag, der sich auf das verwaltete Element auswirkt.</span><span class="sxs-lookup"><span data-stu-id="37cc4-120">The job that is affecting the managed element.</span></span> <span data-ttu-id="37cc4-121">Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="37cc4-121">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="37cc4-122">**Elementeffects**</span><span class="sxs-lookup"><span data-stu-id="37cc4-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37cc4-123">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="37cc4-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="37cc4-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37cc4-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37cc4-125">Eine Enumeration, die den Effekt auf das verwaltete Element beschreibt.</span><span class="sxs-lookup"><span data-stu-id="37cc4-125">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="37cc4-126">Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="37cc4-126">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="37cc4-127">**Otherelementeffect-Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="37cc4-127">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37cc4-128">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="37cc4-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="37cc4-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37cc4-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37cc4-130">Stellt Details für den Effekt an der entsprechenden Array Position in **elementeffects** bereit.</span><span class="sxs-lookup"><span data-stu-id="37cc4-130">Provides details for the effect at the corresponding array position in **ElementEffects**.</span></span> <span data-ttu-id="37cc4-131">Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="37cc4-131">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37cc4-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37cc4-132">Remarks</span></span>

<span data-ttu-id="37cc4-133">Der Zugriff auf die **MSVM- \_ affectedjobelements** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="37cc4-133">Access to the **Msvm\_AffectedJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="37cc4-134">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="37cc4-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="37cc4-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37cc4-135">Requirements</span></span>



| <span data-ttu-id="37cc4-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37cc4-136">Requirement</span></span> | <span data-ttu-id="37cc4-137">Wert</span><span class="sxs-lookup"><span data-stu-id="37cc4-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37cc4-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37cc4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="37cc4-139">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37cc4-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="37cc4-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37cc4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="37cc4-141">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37cc4-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37cc4-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="37cc4-142">Namespace</span></span><br/>                | <span data-ttu-id="37cc4-143">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="37cc4-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="37cc4-144">MOF</span><span class="sxs-lookup"><span data-stu-id="37cc4-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37cc4-145"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="37cc4-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37cc4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="37cc4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37cc4-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37cc4-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37cc4-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37cc4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37cc4-149">**CIM- \_ affectedjobelements**</span><span class="sxs-lookup"><span data-stu-id="37cc4-149">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="37cc4-150">[**CIM- \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="37cc4-150">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="37cc4-151">Verwaltungs Klassen für virtuelle Systeme</span><span class="sxs-lookup"><span data-stu-id="37cc4-151">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

