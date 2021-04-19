---
description: Ordnet dem übergeordneten System ein logisches Gerät zu.
ms.assetid: 2BEAAEC8-F8F2-4CC7-A209-EE3EE3C6FA90
title: Msvm_SystemDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemDevice
- Msvm_SystemDevice.GroupComponent
- Msvm_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be31a51ad4e24bd31785e64400bf5b266624d8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350390"
---
# <a name="msvm_systemdevice-class"></a><span data-ttu-id="3ec26-103">MSVM \_ SystemDevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="3ec26-103">Msvm\_SystemDevice class</span></span>

<span data-ttu-id="3ec26-104">Logische Geräte können von einem System aggregiert werden.</span><span class="sxs-lookup"><span data-stu-id="3ec26-104">Logical devices can be aggregated by a system.</span></span> <span data-ttu-id="3ec26-105">Diese Beziehung wird von der Systemgeräte Zuordnung explizit gemacht.</span><span class="sxs-lookup"><span data-stu-id="3ec26-105">This relationship is made explicit by the system device association.</span></span>

<span data-ttu-id="3ec26-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3ec26-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec26-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ec26-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemDevice : CIM_SystemDevice
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="3ec26-108">Member</span><span class="sxs-lookup"><span data-stu-id="3ec26-108">Members</span></span>

<span data-ttu-id="3ec26-109">Die **MSVM- \_ SystemDevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3ec26-109">The **Msvm\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="3ec26-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3ec26-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ec26-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3ec26-111">Properties</span></span>

<span data-ttu-id="3ec26-112">Die **MSVM- \_ SystemDevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3ec26-112">The **Msvm\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ec26-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3ec26-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec26-114">Datentyp: **[ **CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="3ec26-114">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="3ec26-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ec26-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ec26-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers)setzung, [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="3ec26-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="3ec26-117">Das übergeordnete System in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="3ec26-117">The parent system in the association.</span></span> <span data-ttu-id="3ec26-118">Diese Eigenschaft wird von der [**CIM- \_ Komponente**](/windows/desktop/CIMWin32Prov/cim-component)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ec26-118">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="3ec26-119">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3ec26-119">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec26-120">Datentyp: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="3ec26-120">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="3ec26-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ec26-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec26-122">Das logische Gerät, das ein Element eines Systems ist.</span><span class="sxs-lookup"><span data-stu-id="3ec26-122">The logical device that is an element of a system.</span></span> <span data-ttu-id="3ec26-123">Diese Eigenschaft wird von der [**CIM- \_ Komponente**](/windows/desktop/CIMWin32Prov/cim-component)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ec26-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ec26-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ec26-124">Remarks</span></span>

<span data-ttu-id="3ec26-125">Der Zugriff auf die **MSVM- \_ SystemDevice** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="3ec26-125">Access to the **Msvm\_SystemDevice** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3ec26-126">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3ec26-126">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ec26-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ec26-127">Requirements</span></span>



| <span data-ttu-id="3ec26-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ec26-128">Requirement</span></span> | <span data-ttu-id="3ec26-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3ec26-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec26-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ec26-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec26-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ec26-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3ec26-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ec26-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec26-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ec26-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ec26-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ec26-134">Namespace</span></span><br/>                | <span data-ttu-id="3ec26-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3ec26-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3ec26-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3ec26-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ec26-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3ec26-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ec26-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3ec26-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ec26-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ec26-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ec26-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ec26-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec26-141">**CIM- \_ System Gerät**</span><span class="sxs-lookup"><span data-stu-id="3ec26-141">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="3ec26-142">**CIM- \_ System Gerät**</span><span class="sxs-lookup"><span data-stu-id="3ec26-142">**CIM\_SystemDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-systemdevice)
</dt> <dt>

[<span data-ttu-id="3ec26-143">Klassen des virtuellen Systems</span><span class="sxs-lookup"><span data-stu-id="3ec26-143">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

