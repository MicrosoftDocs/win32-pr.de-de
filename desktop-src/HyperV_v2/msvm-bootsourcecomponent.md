---
description: Ordnet die MSVM- \_ bootsourcesettingdata der allgemeinen MSVM \_ virtualsystemsettingdata zu.
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Msvm_BootSourceComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dfe86fa7882b1b20e5b5abbbdaa9d4f37f231f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349058"
---
# <a name="msvm_bootsourcecomponent-class"></a><span data-ttu-id="9418c-103">MSVM \_ bootsourcecomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="9418c-103">Msvm\_BootSourceComponent class</span></span>

<span data-ttu-id="9418c-104">Ordnet die [**MSVM- \_ bootsourcesettingdata**](msvm-bootsourcesettingdata.md) der allgemeinen [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)zu.</span><span class="sxs-lookup"><span data-stu-id="9418c-104">Associates the [**Msvm\_BootSourceSettingData**](msvm-bootsourcesettingdata.md) to the overall [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).</span></span> <span data-ttu-id="9418c-105">Diese Klasse wird von der [**CIM- \_ Komponente**](/windows/desktop/CIMWin32Prov/cim-component)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9418c-105">This class derives from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

<span data-ttu-id="9418c-106">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="9418c-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9418c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9418c-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9418c-108">Member</span><span class="sxs-lookup"><span data-stu-id="9418c-108">Members</span></span>

<span data-ttu-id="9418c-109">Die **MSVM \_ bootsourcecomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9418c-109">The **Msvm\_BootSourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="9418c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9418c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9418c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9418c-111">Properties</span></span>

<span data-ttu-id="9418c-112">Die **MSVM \_ bootsourcecomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9418c-112">The **Msvm\_BootSourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9418c-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9418c-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9418c-114">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="9418c-114">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="9418c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9418c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9418c-116">Verweis auf das übergeordnete Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="9418c-116">Reference to the parent element in the association.</span></span> <span data-ttu-id="9418c-117">Diese Eigenschaft wird von der [**CIM- \_ Komponente**](cim-component.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9418c-117">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="9418c-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9418c-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9418c-119">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="9418c-119">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="9418c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9418c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9418c-121">Verweis auf das untergeordnete Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="9418c-121">Reference to the child element in the association.</span></span> <span data-ttu-id="9418c-122">Diese Eigenschaft wird von der [**CIM- \_ Komponente**](cim-component.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9418c-122">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9418c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9418c-123">Requirements</span></span>



| <span data-ttu-id="9418c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9418c-124">Requirement</span></span> | <span data-ttu-id="9418c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9418c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9418c-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9418c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9418c-127">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="9418c-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9418c-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9418c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9418c-129">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9418c-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9418c-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="9418c-130">Namespace</span></span><br/>                | <span data-ttu-id="9418c-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9418c-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9418c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="9418c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9418c-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9418c-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9418c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9418c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9418c-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9418c-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9418c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9418c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9418c-137">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="9418c-137">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="9418c-138">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="9418c-138">**CIM\_Component**</span></span>](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[<span data-ttu-id="9418c-139">**MSVM \_ bootsourcesettingdata**</span><span class="sxs-lookup"><span data-stu-id="9418c-139">**Msvm\_BootSourceSettingData**</span></span>](msvm-bootsourcesettingdata.md)
</dt> <dt>

[<span data-ttu-id="9418c-140">**MSVM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="9418c-140">**Msvm\_VirtualSystemSettingData**</span></span>](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 

