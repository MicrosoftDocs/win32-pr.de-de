---
description: Ordnet eine Instanz einer zugeordneten Ressource dem physischen NUMA-Knoten zu, von dem Sie zugeordnet wurde.
ms.assetid: 811ed19f-9084-4e30-8604-860d2bf722c7
title: Msvm_ElementAllocatedFromNumaNode-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromNumaNode
- Msvm_ElementAllocatedFromNumaNode.Antecedent
- Msvm_ElementAllocatedFromNumaNode.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98940306f25d46c6af1be31133ee336765f8f1a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866407"
---
# <a name="msvm_elementallocatedfromnumanode-class"></a><span data-ttu-id="6f203-103">MSVM \_ elementzuweisung-Klasse</span><span class="sxs-lookup"><span data-stu-id="6f203-103">Msvm\_ElementAllocatedFromNumaNode class</span></span>

<span data-ttu-id="6f203-104">Ordnet eine Instanz einer zugeordneten Ressource dem physischen NUMA-Knoten zu, von dem Sie zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="6f203-104">Associates an instance of an allocated resource with the physical NUMA node from which it was allocated.</span></span>

<span data-ttu-id="6f203-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6f203-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f203-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f203-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromNumaNode : CIM_Dependency
{
  Msvm_NumaNode      REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6f203-107">Member</span><span class="sxs-lookup"><span data-stu-id="6f203-107">Members</span></span>

<span data-ttu-id="6f203-108">Die **MSVM- \_ elementdepingedfromnumanode** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6f203-108">The **Msvm\_ElementAllocatedFromNumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="6f203-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6f203-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f203-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6f203-110">Properties</span></span>

<span data-ttu-id="6f203-111">Die **MSVM \_ elementdepaseedfromnumanode** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6f203-111">The **Msvm\_ElementAllocatedFromNumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f203-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="6f203-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f203-113">Datentyp: **[ **MSVM \_ numanode**](msvm-numanode.md)**</span><span class="sxs-lookup"><span data-stu-id="6f203-113">Data type: **[**Msvm\_NumaNode**](msvm-numanode.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6f203-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6f203-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f203-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6f203-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6f203-116">Der physische NUMA-Knoten.</span><span class="sxs-lookup"><span data-stu-id="6f203-116">The physical NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="6f203-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="6f203-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f203-118">Datentyp: **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="6f203-118">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="6f203-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6f203-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f203-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="6f203-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6f203-121">Die zugeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="6f203-121">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f203-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f203-122">Requirements</span></span>



| <span data-ttu-id="6f203-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f203-123">Requirement</span></span> | <span data-ttu-id="6f203-124">Wert</span><span class="sxs-lookup"><span data-stu-id="6f203-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f203-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f203-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6f203-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f203-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6f203-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f203-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6f203-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f203-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f203-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f203-129">Namespace</span></span><br/>                | <span data-ttu-id="6f203-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6f203-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6f203-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6f203-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f203-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6f203-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f203-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6f203-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f203-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f203-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

