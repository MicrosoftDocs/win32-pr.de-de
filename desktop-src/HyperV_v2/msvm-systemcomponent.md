---
description: Richtet einen &\# 0034; Teil&\# 0034; Beziehung zwischen einem System und einem beliebigen verwalteten System Element ein, von dem es zusammengesetzt wird.
ms.assetid: 6BF72E36-9B6C-4853-A553-DDAF65991C86
title: Msvm_SystemComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemComponent
- Msvm_SystemComponent.GroupComponent
- Msvm_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee150793143b549c90d280eef287ee6a5afb66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393426"
---
# <a name="msvm_systemcomponent-class"></a><span data-ttu-id="29982-103">MSVM \_ SystemComponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="29982-103">Msvm\_SystemComponent class</span></span>

<span data-ttu-id="29982-104">Richtet einen "Teil" der Beziehung zwischen einem System und einem beliebigen verwalteten System Element ein, von dem es zusammengesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="29982-104">Establishes a "part of" relationship between a system and any managed system element of which it is composed.</span></span>

<span data-ttu-id="29982-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="29982-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="29982-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="29982-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), Association, Aggregation]
class Msvm_SystemComponent : CIM_SystemComponent
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="29982-107">Member</span><span class="sxs-lookup"><span data-stu-id="29982-107">Members</span></span>

<span data-ttu-id="29982-108">Die **MSVM \_ SystemComponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="29982-108">The **Msvm\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="29982-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29982-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29982-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29982-110">Properties</span></span>

<span data-ttu-id="29982-111">Die **MSVM \_ SystemComponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="29982-111">The **Msvm\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29982-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="29982-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29982-113">Datentyp: **[ **CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="29982-113">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="29982-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="29982-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29982-115">Das übergeordnete Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="29982-115">The parent element in the association.</span></span> <span data-ttu-id="29982-116">Diese Eigenschaft wird von [**CIM \_ SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="29982-116">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> <dt>

<span data-ttu-id="29982-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="29982-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29982-118">Datentyp: **[ **CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span><span class="sxs-lookup"><span data-stu-id="29982-118">Data type: **[**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span></span>
</dt> <dt>

<span data-ttu-id="29982-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="29982-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29982-120">Das untergeordnete-Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="29982-120">The child element in the association.</span></span> <span data-ttu-id="29982-121">Diese Eigenschaft wird von [**CIM \_ SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="29982-121">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29982-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29982-122">Requirements</span></span>



| <span data-ttu-id="29982-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29982-123">Requirement</span></span> | <span data-ttu-id="29982-124">Wert</span><span class="sxs-lookup"><span data-stu-id="29982-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29982-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29982-125">Minimum supported client</span></span><br/> | <span data-ttu-id="29982-126">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="29982-126">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="29982-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29982-127">Minimum supported server</span></span><br/> | <span data-ttu-id="29982-128">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29982-128">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="29982-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="29982-129">Namespace</span></span><br/>                | <span data-ttu-id="29982-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="29982-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="29982-131">MOF</span><span class="sxs-lookup"><span data-stu-id="29982-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29982-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="29982-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="29982-133">DLL</span><span class="sxs-lookup"><span data-stu-id="29982-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29982-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="29982-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

