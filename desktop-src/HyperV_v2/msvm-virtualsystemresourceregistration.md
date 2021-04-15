---
description: Registriert einen Dienst, der Virtual Machine-spezifische ressourcenbezogene Objekte bereitstellt.
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Msvm_VirtualSystemResourceRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525187"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a><span data-ttu-id="4bbda-103">MSVM \_ virtualsystemresourceregistration-Klasse</span><span class="sxs-lookup"><span data-stu-id="4bbda-103">Msvm\_VirtualSystemResourceRegistration class</span></span>

<span data-ttu-id="4bbda-104">Registriert einen Dienst, der Virtual Machine-spezifische ressourcenbezogene Objekte bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4bbda-104">Registers a service that provides virtual machine-specific resource-related objects.</span></span>

<span data-ttu-id="4bbda-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4bbda-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bbda-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bbda-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a><span data-ttu-id="4bbda-107">Member</span><span class="sxs-lookup"><span data-stu-id="4bbda-107">Members</span></span>

<span data-ttu-id="4bbda-108">Die **MSVM \_ virtualsystemresourceregistration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4bbda-108">The **Msvm\_VirtualSystemResourceRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="4bbda-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4bbda-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4bbda-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4bbda-110">Properties</span></span>

<span data-ttu-id="4bbda-111">Die **MSVM \_ virtualsystemresourceregistration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4bbda-111">The **Msvm\_VirtualSystemResourceRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4bbda-112">**Komponente**</span><span class="sxs-lookup"><span data-stu-id="4bbda-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bbda-113">Datentyp: **[ **MSVM \_ virtualsystemresourcecomponent**](msvm-virtualsystemresourcecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="4bbda-113">Data type: **[**Msvm\_VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4bbda-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4bbda-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bbda-115">Ein Verweis auf eine-Instanz, die das COM-Objekt beschreibt, das diese Klasse implementiert.</span><span class="sxs-lookup"><span data-stu-id="4bbda-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="4bbda-116">**Isrootdevice**</span><span class="sxs-lookup"><span data-stu-id="4bbda-116">**IsRootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bbda-117">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4bbda-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bbda-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4bbda-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bbda-119">**True** , wenn diese Registrierung angibt, ob der angegebene Ressourcentyp das Stamm Gerät (oder das übergeordnete oder übergeordnete) Gerät für diesen Dienst ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="4bbda-119">**True** if this registration indicates whether the specified resource type is the root (or parent-less) device for this service; otherwise, **False**.</span></span> <span data-ttu-id="4bbda-120">Wenn **isrootdevice** auf **true** festgelegt ist, kann nur eine Registrierung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4bbda-120">Only one registration can exist when **IsRootDevice** is set to **True**.</span></span> <span data-ttu-id="4bbda-121">Andernfalls stellt diese Registrierung eine Zuordnung zu einem untergeordneten Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="4bbda-121">Otherwise, this registration represents a mapping to a sub-device.</span></span> <span data-ttu-id="4bbda-122">Diese Eigenschaft ist immer auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4bbda-122">This property is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="4bbda-123">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="4bbda-123">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bbda-124">Datentyp: **[ **MSVM \_ resourcetypeer Definition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="4bbda-124">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4bbda-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4bbda-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bbda-126">Ein Verweis auf eine-Instanz, die einen vom Dienst unterstützten Ressourcentyp beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4bbda-126">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="4bbda-127">Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponentregistration**](msvm-virtualizationcomponentregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4bbda-127">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4bbda-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bbda-128">Remarks</span></span>

<span data-ttu-id="4bbda-129">Der Zugriff auf die **MSVM \_ virtualsystemresourceregistration** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="4bbda-129">Access to the **Msvm\_VirtualSystemResourceRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4bbda-130">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4bbda-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bbda-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bbda-131">Requirements</span></span>



| <span data-ttu-id="4bbda-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bbda-132">Requirement</span></span> | <span data-ttu-id="4bbda-133">Wert</span><span class="sxs-lookup"><span data-stu-id="4bbda-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bbda-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4bbda-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4bbda-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bbda-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4bbda-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4bbda-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4bbda-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bbda-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4bbda-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4bbda-138">End of client support</span></span><br/>    | <span data-ttu-id="4bbda-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4bbda-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4bbda-140">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="4bbda-140">End of server support</span></span><br/>    | <span data-ttu-id="4bbda-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4bbda-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4bbda-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="4bbda-142">Namespace</span></span><br/>                | <span data-ttu-id="4bbda-143">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4bbda-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4bbda-144">MOF</span><span class="sxs-lookup"><span data-stu-id="4bbda-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bbda-145"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4bbda-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bbda-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4bbda-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bbda-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4bbda-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4bbda-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bbda-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bbda-149">**MSVM \_ virtualizationcomponentregistration**</span><span class="sxs-lookup"><span data-stu-id="4bbda-149">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="4bbda-150">**MSVM \_ virtualizationcomponentregistration**</span><span class="sxs-lookup"><span data-stu-id="4bbda-150">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

