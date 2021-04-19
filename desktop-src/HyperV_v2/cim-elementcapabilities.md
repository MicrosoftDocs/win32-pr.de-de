---
description: Stellt eine Zuordnung zwischen einem verwalteten Element und seinen Funktionen dar.
ms.assetid: 0e080042-4a56-40b7-acc5-cf69eb2a0604
title: CIM_ElementCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapabilities
- CIM_ElementCapabilities.ManagedElement
- CIM_ElementCapabilities.Capabilities
- CIM_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c705d0bb4743d4919ca840f51b3324510558078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348823"
---
# <a name="cim_elementcapabilities-class"></a><span data-ttu-id="1b1bf-103">CIM \_ elementfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="1b1bf-103">CIM\_ElementCapabilities class</span></span>

<span data-ttu-id="1b1bf-104">Stellt eine Zuordnung zwischen einem verwalteten Element und seinen Funktionen dar.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-104">Represents an association between a managed element and its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b1bf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b1bf-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="1b1bf-106">Member</span><span class="sxs-lookup"><span data-stu-id="1b1bf-106">Members</span></span>

<span data-ttu-id="1b1bf-107">Die **CIM \_ elementfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1b1bf-107">The **CIM\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="1b1bf-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1b1bf-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b1bf-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1b1bf-109">Properties</span></span>

<span data-ttu-id="1b1bf-110">Die **CIM \_ elementfunktionalitäten** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-110">The **CIM\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b1bf-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="1b1bf-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b1bf-112">Datentyp: **CIM- \_ Funktionen**</span><span class="sxs-lookup"><span data-stu-id="1b1bf-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="1b1bf-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1b1bf-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b1bf-114">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1b1bf-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1b1bf-115">Die dem verwalteten Element zugeordneten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-115">The capabilities associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="1b1bf-116">**Characteristics**</span><span class="sxs-lookup"><span data-stu-id="1b1bf-116">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b1bf-117">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1b1bf-117">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1b1bf-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1b1bf-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b1bf-119">Eine Reihe von beschreibenden Informationen zu den Funktionen.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-119">A set of descriptive information about the capabilities.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="1b1bf-120">**Standard** (2)</span><span class="sxs-lookup"><span data-stu-id="1b1bf-120">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>

<span data-ttu-id="1b1bf-121">**Aktuell** (3)</span><span class="sxs-lookup"><span data-stu-id="1b1bf-121">**Current** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1b1bf-122">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1b1bf-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="1b1bf-123">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="1b1bf-123">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1b1bf-124">**"Managedelement"**</span><span class="sxs-lookup"><span data-stu-id="1b1bf-124">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b1bf-125">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="1b1bf-125">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="1b1bf-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1b1bf-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b1bf-127">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="1b1bf-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1b1bf-128">Das verwaltete Element.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-128">The managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b1bf-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b1bf-129">Requirements</span></span>



| <span data-ttu-id="1b1bf-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b1bf-130">Requirement</span></span> | <span data-ttu-id="1b1bf-131">Wert</span><span class="sxs-lookup"><span data-stu-id="1b1bf-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1bf-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b1bf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1b1bf-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1b1bf-133">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1b1bf-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b1bf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1b1bf-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1b1bf-135">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1b1bf-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b1bf-136">Namespace</span></span><br/>                | <span data-ttu-id="1b1bf-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1b1bf-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1b1bf-138">MOF</span><span class="sxs-lookup"><span data-stu-id="1b1bf-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b1bf-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1b1bf-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b1bf-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1b1bf-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b1bf-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1b1bf-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

