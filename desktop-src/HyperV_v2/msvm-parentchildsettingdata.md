---
description: Eine Zuordnung zwischen einer Instanz von MSVM \_ virtualsystemsettingdata und der MSVM \_ virtualsystemsettingdata-Instanz, die die aktuelle Momentaufnahme darstellt, auf der dieses Objekt basiert.
ms.assetid: F779775B-9AB3-4495-B6FF-9985FCDF63E4
title: Msvm_ParentChildSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentChildSettingData
- Msvm_ParentChildSettingData.Antecedent
- Msvm_ParentChildSettingData.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 083de5f5d162f32fc9499a67b2ec991c6d3b398a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349683"
---
# <a name="msvm_parentchildsettingdata-class"></a><span data-ttu-id="2291a-103">MSVM-Klasse von " \_ parametrichildsettingdata"</span><span class="sxs-lookup"><span data-stu-id="2291a-103">Msvm\_ParentChildSettingData class</span></span>

<span data-ttu-id="2291a-104">Eine Zuordnung zwischen einer Instanz von [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) und der **MSVM \_ virtualsystemsettingdata** -Instanz, die die aktuelle Momentaufnahme darstellt, auf der dieses Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="2291a-104">An association between an instance of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) and the **Msvm\_VirtualSystemSettingData** instance that represents the most recent snapshot upon which this object is based.</span></span>

<span data-ttu-id="2291a-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2291a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2291a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2291a-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentChildSettingData : CIM_Dependency
{
  Msvm_VirtualSystemSettingData REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2291a-107">Member</span><span class="sxs-lookup"><span data-stu-id="2291a-107">Members</span></span>

<span data-ttu-id="2291a-108">Die **MSVM-Klasse " \_ parametrichildsettingdata** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2291a-108">The **Msvm\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2291a-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2291a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2291a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2291a-110">Properties</span></span>

<span data-ttu-id="2291a-111">Die **MSVM-Klasse " \_ parametrichildsettingdata** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2291a-111">The **Msvm\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2291a-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="2291a-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2291a-113">Datentyp: **[ **MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="2291a-113">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2291a-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2291a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2291a-115">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="2291a-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2291a-116">Die Momentaufnahme Einstellungsdaten, auf denen die Daten der untergeordneten Einstellung basieren.</span><span class="sxs-lookup"><span data-stu-id="2291a-116">The snapshot setting data upon which the child setting data is based.</span></span>

</dd> <dt>

<span data-ttu-id="2291a-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="2291a-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2291a-118">Datentyp: **[ **MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="2291a-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2291a-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2291a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2291a-120">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. abhängig")</span><span class="sxs-lookup"><span data-stu-id="2291a-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2291a-121">Die Einstellungsdaten für den virtuellen Computer, der das untergeordnete Element des übergeordneten Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="2291a-121">The setting data for the virtual machine that represents the child of the parent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2291a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2291a-122">Remarks</span></span>

<span data-ttu-id="2291a-123">Der Zugriff auf die **MSVM-Klasse "parameterchildsettingdata \_** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="2291a-123">Access to the **Msvm\_ParentChildSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2291a-124">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2291a-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2291a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2291a-125">Requirements</span></span>



| <span data-ttu-id="2291a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2291a-126">Requirement</span></span> | <span data-ttu-id="2291a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2291a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2291a-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2291a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2291a-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2291a-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2291a-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2291a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2291a-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2291a-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2291a-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="2291a-132">Namespace</span></span><br/>                | <span data-ttu-id="2291a-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2291a-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2291a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2291a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2291a-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2291a-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2291a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2291a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2291a-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2291a-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2291a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2291a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2291a-139">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="2291a-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="2291a-140">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="2291a-140">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> <dt>

[<span data-ttu-id="2291a-141">Klassen des virtuellen Systems</span><span class="sxs-lookup"><span data-stu-id="2291a-141">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

