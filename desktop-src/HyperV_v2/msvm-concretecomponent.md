---
description: Eine generische Zuordnung, die verwendet wird, um einen Teil der Beziehungen zwischen verwalteten Elementen herzustellen.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Msvm_ConcreteComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2ef9e286f4c7ca296ee6b3638ffb9511ccea4115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347464"
---
# <a name="msvm_concretecomponent-class"></a><span data-ttu-id="c4ccb-103">MSVM- \_ Klasse "concretecomponent"</span><span class="sxs-lookup"><span data-stu-id="c4ccb-103">Msvm\_ConcreteComponent class</span></span>

<span data-ttu-id="c4ccb-104">Eine generische Zuordnung, die verwendet wird, um Beziehungen zwischen verwalteten Elementen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-104">A generic association used to establish 'part of' relationships between managed elements.</span></span> <span data-ttu-id="c4ccb-105">[**CIM \_ "Concretecomponent**](/previous-versions//cc150665(v=vs.85)) " ist als konkrete Unterklasse der abstrakten [**CIM- \_ Komponenten**](/windows/desktop/CIMWin32Prov/cim-component) Klasse definiert und kann anstelle vieler spezifischer Unterklassen von Komponenten verwendet werden, die keine Semantik hinzufügen (d. h. Unterklassen, die den Typ der Komposition nicht verdeutlichen, Kardinalitäten aktualisieren oder Qualifizierer hinzufügen oder entfernen).</span><span class="sxs-lookup"><span data-stu-id="c4ccb-105">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) is defined as a concrete subclass of the abstract [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component) class, to be used in place of many specific subclasses of component that add no semantics (that is subclasses that do not clarify the type of composition, update cardinalities, or add or remove qualifiers.)</span></span>

<span data-ttu-id="c4ccb-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4ccb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4ccb-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="c4ccb-108">Member</span><span class="sxs-lookup"><span data-stu-id="c4ccb-108">Members</span></span>

<span data-ttu-id="c4ccb-109">Die **MSVM-Klasse " \_ concretecomponent** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c4ccb-109">The **Msvm\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="c4ccb-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4ccb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4ccb-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4ccb-111">Properties</span></span>

<span data-ttu-id="c4ccb-112">Die **MSVM-Klasse " \_ concretecomponent** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-112">The **Msvm\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4ccb-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4ccb-114">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="c4ccb-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4ccb-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4ccb-116">Das übergeordnete Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-116">The parent element in the association.</span></span> <span data-ttu-id="c4ccb-117">Diese Eigenschaft wird von [**CIM " \_ concretecomponent**](/previous-versions//cc150665(v=vs.85))" geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-117">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4ccb-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4ccb-119">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-119">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="c4ccb-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4ccb-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4ccb-121">Das untergeordnete-Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-121">The child element in the association.</span></span> <span data-ttu-id="c4ccb-122">Diese Eigenschaft wird von [**CIM " \_ concretecomponent**](/previous-versions//cc150665(v=vs.85))" geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-122">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4ccb-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4ccb-123">Remarks</span></span>

<span data-ttu-id="c4ccb-124">Der Zugriff auf die **MSVM-Klasse " \_ concretecomponent** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-124">Access to the **Msvm\_ConcreteComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c4ccb-125">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c4ccb-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ccb-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4ccb-126">Requirements</span></span>



| <span data-ttu-id="c4ccb-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4ccb-127">Requirement</span></span> | <span data-ttu-id="c4ccb-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c4ccb-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ccb-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4ccb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c4ccb-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4ccb-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c4ccb-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4ccb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c4ccb-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4ccb-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4ccb-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4ccb-133">Namespace</span></span><br/>                | <span data-ttu-id="c4ccb-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c4ccb-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c4ccb-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c4ccb-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4ccb-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c4ccb-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4ccb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c4ccb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4ccb-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4ccb-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c4ccb-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4ccb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ccb-140">**CIM- \_ concretecomponent**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-140">**CIM\_ConcreteComponent**</span></span>](cim-concretecomponent.md)
</dt> <dt>

<span data-ttu-id="c4ccb-141">[**CIM- \_ concretecomponent**](/previous-versions//cc150665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4ccb-141">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c4ccb-142">Klassen des virtuellen Systems</span><span class="sxs-lookup"><span data-stu-id="c4ccb-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

