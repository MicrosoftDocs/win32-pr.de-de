---
description: Registriert einen Dienst, der globale Ressourcenpool bezogene Objekte bereitstellt.
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Msvm_ResourcePoolRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolRegistration
- Msvm_ResourcePoolRegistration.ResourceType
- Msvm_ResourcePoolRegistration.Component
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6eecfefc8c542eeb3a06c509533060f8036d447e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131840"
---
# <a name="msvm_resourcepoolregistration-class"></a><span data-ttu-id="5d2be-103">MSVM \_ resourcepoolregistration-Klasse</span><span class="sxs-lookup"><span data-stu-id="5d2be-103">Msvm\_ResourcePoolRegistration class</span></span>

<span data-ttu-id="5d2be-104">Registriert einen Dienst, der globale Ressourcenpool bezogene Objekte bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5d2be-104">Registers a service that provides global resource pool-related objects.</span></span>

<span data-ttu-id="5d2be-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5d2be-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d2be-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d2be-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a><span data-ttu-id="5d2be-107">Member</span><span class="sxs-lookup"><span data-stu-id="5d2be-107">Members</span></span>

<span data-ttu-id="5d2be-108">Die **MSVM \_ resourcepoolregistration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5d2be-108">The **Msvm\_ResourcePoolRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="5d2be-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d2be-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d2be-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d2be-110">Properties</span></span>

<span data-ttu-id="5d2be-111">Die **MSVM \_ resourcepoolregistration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5d2be-111">The **Msvm\_ResourcePoolRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d2be-112">**Komponente**</span><span class="sxs-lookup"><span data-stu-id="5d2be-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d2be-113">Datentyp: **[ **MSVM \_ resourcepoolcomponent**](msvm-resourcepoolcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="5d2be-113">Data type: **[**Msvm\_ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="5d2be-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5d2be-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d2be-115">Ein Verweis auf eine-Instanz, die das COM-Objekt beschreibt, das diese Klasse implementiert.</span><span class="sxs-lookup"><span data-stu-id="5d2be-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="5d2be-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="5d2be-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d2be-117">Datentyp: **[ **MSVM \_ resourcetypeer Definition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="5d2be-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="5d2be-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5d2be-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d2be-119">Ein Verweis auf eine-Instanz, die einen vom Dienst unterstützten Ressourcentyp beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5d2be-119">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="5d2be-120">Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponentregistration**](msvm-virtualizationcomponentregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5d2be-120">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d2be-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d2be-121">Remarks</span></span>

<span data-ttu-id="5d2be-122">Der Zugriff auf die **MSVM \_ resourcepoolregistration** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="5d2be-122">Access to the **Msvm\_ResourcePoolRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5d2be-123">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5d2be-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2be-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d2be-124">Requirements</span></span>



| <span data-ttu-id="5d2be-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d2be-125">Requirement</span></span> | <span data-ttu-id="5d2be-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5d2be-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2be-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d2be-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5d2be-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d2be-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5d2be-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d2be-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5d2be-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d2be-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5d2be-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="5d2be-131">End of client support</span></span><br/>    | <span data-ttu-id="5d2be-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5d2be-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5d2be-133">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="5d2be-133">End of server support</span></span><br/>    | <span data-ttu-id="5d2be-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5d2be-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5d2be-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d2be-135">Namespace</span></span><br/>                | <span data-ttu-id="5d2be-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5d2be-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5d2be-137">MOF</span><span class="sxs-lookup"><span data-stu-id="5d2be-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d2be-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5d2be-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d2be-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5d2be-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d2be-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5d2be-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5d2be-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d2be-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2be-142">**MSVM \_ virtualizationcomponentregistration**</span><span class="sxs-lookup"><span data-stu-id="5d2be-142">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="5d2be-143">**MSVM \_ virtualizationcomponentregistration**</span><span class="sxs-lookup"><span data-stu-id="5d2be-143">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

