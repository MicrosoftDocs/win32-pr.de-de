---
description: Ordnet zwei verwaltete Elemente zu, die unterschiedliche Aspekte der gleichen zugrunde liegenden Entität darstellen.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Msvm_LogicalIdentity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2f8d2ee522fde3769c08bcbb78611b99eed8e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529048"
---
# <a name="msvm_logicalidentity-class"></a><span data-ttu-id="d55a2-103">MSVM \_ logicalidentity-Klasse</span><span class="sxs-lookup"><span data-stu-id="d55a2-103">Msvm\_LogicalIdentity class</span></span>

<span data-ttu-id="d55a2-104">Ordnet zwei verwaltete Elemente zu, die unterschiedliche Aspekte der gleichen zugrunde liegenden Entität darstellen.</span><span class="sxs-lookup"><span data-stu-id="d55a2-104">Associates two managed elements that represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="d55a2-105">Diese Klasse wird von [**CIM \_ logicalidentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d55a2-105">This class derives from [**CIM\_LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).</span></span>

<span data-ttu-id="d55a2-106">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d55a2-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d55a2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d55a2-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="d55a2-108">Member</span><span class="sxs-lookup"><span data-stu-id="d55a2-108">Members</span></span>

<span data-ttu-id="d55a2-109">Die **MSVM \_ logicalidentity** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d55a2-109">The **Msvm\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="d55a2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d55a2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d55a2-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d55a2-111">Properties</span></span>

<span data-ttu-id="d55a2-112">Die **MSVM \_ logicalidentity** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d55a2-112">The **Msvm\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d55a2-113">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="d55a2-113">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55a2-114">Datentyp: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="d55a2-114">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="d55a2-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d55a2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d55a2-116">Verweis auf einen alternativen Aspekt der System Entität.</span><span class="sxs-lookup"><span data-stu-id="d55a2-116">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="d55a2-117">**Systemelement**</span><span class="sxs-lookup"><span data-stu-id="d55a2-117">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55a2-118">Datentyp: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="d55a2-118">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="d55a2-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d55a2-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d55a2-120">Verweis auf einen Aspekt des logischen Elements.</span><span class="sxs-lookup"><span data-stu-id="d55a2-120">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d55a2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d55a2-121">Requirements</span></span>



| <span data-ttu-id="d55a2-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d55a2-122">Requirement</span></span> | <span data-ttu-id="d55a2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d55a2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d55a2-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d55a2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d55a2-125">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="d55a2-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d55a2-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d55a2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d55a2-127">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d55a2-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d55a2-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="d55a2-128">Namespace</span></span><br/>                | <span data-ttu-id="d55a2-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d55a2-129">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d55a2-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d55a2-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d55a2-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d55a2-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d55a2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d55a2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d55a2-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d55a2-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d55a2-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d55a2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55a2-135">**CIM- \_ logikalidentität**</span><span class="sxs-lookup"><span data-stu-id="d55a2-135">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dt>

[<span data-ttu-id="d55a2-136">**CIM- \_ logikalidentität**</span><span class="sxs-lookup"><span data-stu-id="d55a2-136">**CIM\_LogicalIdentity**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

