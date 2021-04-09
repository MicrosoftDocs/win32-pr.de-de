---
description: Ordnet dem Verwaltungsdienst eine Instanz des virtuellen Computers zu, der den Zustand steuert.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Msvm_ServiceAffectsElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130000"
---
# <a name="msvm_serviceaffectselement-class"></a><span data-ttu-id="0de43-103">MSVM \_ serviceaffectselements-Klasse</span><span class="sxs-lookup"><span data-stu-id="0de43-103">Msvm\_ServiceAffectsElement class</span></span>

<span data-ttu-id="0de43-104">Ordnet dem Verwaltungsdienst eine Instanz des virtuellen Computers zu, der den Zustand steuert.</span><span class="sxs-lookup"><span data-stu-id="0de43-104">Associates a virtual machine instance with the management service that controls its state.</span></span>

<span data-ttu-id="0de43-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0de43-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0de43-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0de43-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="0de43-107">Member</span><span class="sxs-lookup"><span data-stu-id="0de43-107">Members</span></span>

<span data-ttu-id="0de43-108">Die **MSVM \_ serviceaffectselements** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0de43-108">The **Msvm\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="0de43-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0de43-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0de43-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0de43-110">Properties</span></span>

<span data-ttu-id="0de43-111">Die **MSVM \_ serviceaffectselements** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0de43-111">The **Msvm\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0de43-112">**Affectedelta-Element**</span><span class="sxs-lookup"><span data-stu-id="0de43-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de43-113">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="0de43-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="0de43-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0de43-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0de43-115">Ein Verweis auf den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0de43-115">A reference to the virtual machine.</span></span> <span data-ttu-id="0de43-116">Diese Eigenschaft wird von [**CIM \_ serviceaffectselements**](/previous-versions//cc136907(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0de43-116">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0de43-117">**Affectingelement**</span><span class="sxs-lookup"><span data-stu-id="0de43-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de43-118">Datentyp: **[ **CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="0de43-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="0de43-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0de43-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0de43-120">Ein Verweis auf den Dienst, der den virtuellen Computer steuert.</span><span class="sxs-lookup"><span data-stu-id="0de43-120">A reference to the service that controls the virtual machine.</span></span> <span data-ttu-id="0de43-121">Diese Eigenschaft wird von [**CIM \_ serviceaffectselements**](/previous-versions//cc136907(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0de43-121">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0de43-122">**Elementeffects**</span><span class="sxs-lookup"><span data-stu-id="0de43-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de43-123">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0de43-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0de43-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0de43-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0de43-125">Gibt den Typ des Steuer Elements an, das die Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="0de43-125">Specifies the type of control that the association represents.</span></span> <span data-ttu-id="0de43-126">Diese Eigenschaft wird von [**CIM \_ serviceaffectselements**](/previous-versions//cc136907(v=vs.85))geerbt und ist immer auf den folgenden Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0de43-126">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to the following value.</span></span>



| <span data-ttu-id="0de43-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0de43-127">Value</span></span>                                                                        | <span data-ttu-id="0de43-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0de43-128">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="0de43-129"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0de43-129"><dt>5</dt></span></span> </dl> | <span data-ttu-id="0de43-130">Verwaltet</span><span class="sxs-lookup"><span data-stu-id="0de43-130">Manages</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0de43-131">**Otherelementeffect-Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="0de43-131">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de43-132">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="0de43-132">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0de43-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0de43-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0de43-134">Die Details für den Typ der Zuordnung an der entsprechenden Array Position in der **Element beeinflusst** das Eigenschafts Array.</span><span class="sxs-lookup"><span data-stu-id="0de43-134">The details for the type of association at the corresponding array position in the **ElementAffects** property array.</span></span> <span data-ttu-id="0de43-135">Diese Informationen sind erforderlich, wenn **Element Affekte** auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0de43-135">This information is required if **ElementAffects** is set to 1 (Other).</span></span> <span data-ttu-id="0de43-136">Diese Eigenschaft wird von [**CIM \_ serviceaffectselements**](/previous-versions//cc136907(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0de43-136">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0de43-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0de43-137">Remarks</span></span>

<span data-ttu-id="0de43-138">Der Zugriff auf die **MSVM \_ serviceaffectselements** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="0de43-138">Access to the **Msvm\_ServiceAffectsElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0de43-139">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0de43-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0de43-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0de43-140">Requirements</span></span>



| <span data-ttu-id="0de43-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0de43-141">Requirement</span></span> | <span data-ttu-id="0de43-142">Wert</span><span class="sxs-lookup"><span data-stu-id="0de43-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0de43-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0de43-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0de43-144">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0de43-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0de43-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0de43-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0de43-146">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0de43-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0de43-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="0de43-147">Namespace</span></span><br/>                | <span data-ttu-id="0de43-148">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0de43-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0de43-149">MOF</span><span class="sxs-lookup"><span data-stu-id="0de43-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0de43-150"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0de43-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0de43-151">DLL</span><span class="sxs-lookup"><span data-stu-id="0de43-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0de43-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0de43-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0de43-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0de43-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0de43-154">**CIM \_ serviceaffectselements**</span><span class="sxs-lookup"><span data-stu-id="0de43-154">**CIM\_ServiceAffectsElement**</span></span>](cim-serviceaffectselement.md)
</dt> <dt>

<span data-ttu-id="0de43-155">[**CIM \_ serviceaffectselements**](/previous-versions//cc136907(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0de43-155">[**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))</span></span>
</dt> </dl>

 

