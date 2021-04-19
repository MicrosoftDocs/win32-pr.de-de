---
description: Stellt die Registrierung eines Dienstanbieter in der Microsoft Hyper-V Plattform dar.
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Msvm_VirtualizationComponentRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e9704dcade0474a10ca60383280941ec2e3591b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342828"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a><span data-ttu-id="eb78e-103">MSVM- \_ virtualizationcomponentregistration-Klasse</span><span class="sxs-lookup"><span data-stu-id="eb78e-103">Msvm\_VirtualizationComponentRegistration class</span></span>

<span data-ttu-id="eb78e-104">Stellt die Registrierung eines Dienstanbieter in der Microsoft Hyper-V Plattform dar.</span><span class="sxs-lookup"><span data-stu-id="eb78e-104">Represents the registration of a service in the Microsoft Hyper-V platform.</span></span>

<span data-ttu-id="eb78e-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="eb78e-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb78e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb78e-106">Syntax</span></span>

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a><span data-ttu-id="eb78e-107">Member</span><span class="sxs-lookup"><span data-stu-id="eb78e-107">Members</span></span>

<span data-ttu-id="eb78e-108">Die **MSVM- \_ virtualizationcomponentregistration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eb78e-108">The **Msvm\_VirtualizationComponentRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="eb78e-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb78e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb78e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb78e-110">Properties</span></span>

<span data-ttu-id="eb78e-111">Die **MSVM- \_ virtualizationcomponentregistration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eb78e-111">The **Msvm\_VirtualizationComponentRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb78e-112">**Komponente**</span><span class="sxs-lookup"><span data-stu-id="eb78e-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb78e-113">Datentyp: **[ **MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="eb78e-113">Data type: **[**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="eb78e-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb78e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb78e-115">Ein Verweis auf eine-Instanz, die das COM-Objekt beschreibt, das diese Klasse implementiert.</span><span class="sxs-lookup"><span data-stu-id="eb78e-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="eb78e-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="eb78e-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb78e-117">Datentyp: **[ **MSVM \_ resourcetypeer Definition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="eb78e-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="eb78e-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb78e-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb78e-119">Ein Verweis auf eine-Instanz, die einen vom Dienst unterstützten Ressourcentyp beschreibt.</span><span class="sxs-lookup"><span data-stu-id="eb78e-119">A reference to an instance that describes a resource type supported by the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb78e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb78e-120">Remarks</span></span>

<span data-ttu-id="eb78e-121">Der Zugriff auf die **MSVM- \_ virtualizationcomponentregistration** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="eb78e-121">Access to the **Msvm\_VirtualizationComponentRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="eb78e-122">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="eb78e-122">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb78e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb78e-123">Requirements</span></span>



| <span data-ttu-id="eb78e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb78e-124">Requirement</span></span> | <span data-ttu-id="eb78e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="eb78e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb78e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb78e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eb78e-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb78e-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="eb78e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb78e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eb78e-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb78e-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb78e-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="eb78e-130">End of client support</span></span><br/>    | <span data-ttu-id="eb78e-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="eb78e-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="eb78e-132">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="eb78e-132">End of server support</span></span><br/>    | <span data-ttu-id="eb78e-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="eb78e-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="eb78e-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb78e-134">Namespace</span></span><br/>                | <span data-ttu-id="eb78e-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="eb78e-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eb78e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="eb78e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb78e-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eb78e-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb78e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="eb78e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb78e-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb78e-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

