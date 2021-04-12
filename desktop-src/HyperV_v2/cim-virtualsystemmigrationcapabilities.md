---
description: Stellt die Funktionen eines CIM \_ virtualsystemmigrationservice-Objekts dar.
ms.assetid: 5fe3a10b-c075-4c45-838d-0b5c2e491584
title: CIM_VirtualSystemMigrationCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationCapabilities
- CIM_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a9a9a0a0f8e9ea344c7a37ad1168dcb5e059093
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528895"
---
# <a name="cim_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="18c76-103">CIM \_ virtualsystemmigrationfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="18c76-103">CIM\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="18c76-104">Stellt die Funktionen eines [**CIM \_ virtualsystemmigrationservice**](cim-virtualsystemmigrationservice.md) -Objekts dar.</span><span class="sxs-lookup"><span data-stu-id="18c76-104">Represents the capabilities of a [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="18c76-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18c76-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationCapabilities : CIM_Capabilities
{
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="18c76-106">Member</span><span class="sxs-lookup"><span data-stu-id="18c76-106">Members</span></span>

<span data-ttu-id="18c76-107">Die **CIM \_ virtualsystemmigrationfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="18c76-107">The **CIM\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="18c76-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18c76-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18c76-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18c76-109">Properties</span></span>

<span data-ttu-id="18c76-110">Die **CIM \_ virtualsystemmigrationfunktionalitäten** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="18c76-110">The **CIM\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18c76-111">**Asynchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="18c76-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c76-112">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="18c76-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18c76-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c76-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18c76-114">Ein Array, das die [**CIM \_ virtualsystemmigrationservice**](cim-virtualsystemmigrationservice.md) -Methoden angibt, die für asynchrone Vorgänge unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="18c76-114">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="18c76-115">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="18c76-115">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="18c76-116">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="18c76-116">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="18c76-117">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="18c76-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18c76-118">**Destinationhostformatssupported**</span><span class="sxs-lookup"><span data-stu-id="18c76-118">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c76-119">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="18c76-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18c76-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c76-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c76-121">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ virtualsystemmigrationservice**](cim-virtualsystemmigrationservice.md)".**MigrateVirtualSystemToHost (destinationhost)**","**CIM \_ virtualsystemmigrationservice**.**CheckVirtualSystemIsMigratableToHost (destinationhost)**")</span><span class="sxs-lookup"><span data-stu-id="18c76-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md).**MigrateVirtualSystemToHost(DestinationHost)**", "**CIM\_VirtualSystemMigrationService**.**CheckVirtualSystemIsMigratableToHost(DestinationHost)**")</span></span>
</dt> </dl>

<span data-ttu-id="18c76-122">Ein Array, das die unterstützten Formate für den *destinationhost* -Parameter der [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) -Methode und der [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) -Methode für das [**CIM \_ virtualsystemmigrationservice**](cim-virtualsystemmigrationservice.md) -Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="18c76-122">An array that contains the supported formats for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) and [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) methods for the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

<dt>

<span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>

<span data-ttu-id="18c76-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**Domainnameformatsupported** (2)</span><span class="sxs-lookup"><span data-stu-id="18c76-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**DomainNameFormatSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18c76-124">Unterstützung des Domänen Namen-Text Formats gemäß RFC 1035.</span><span class="sxs-lookup"><span data-stu-id="18c76-124">Support of the Domain Name text format according to RFC 1035.</span></span>

</dd> <dt>

<span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>

<span data-ttu-id="18c76-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="18c76-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18c76-126">Unterstützung des IPv4-gepunkteten Dezimal Formats gemäß RFC 1208.</span><span class="sxs-lookup"><span data-stu-id="18c76-126">Support of the IPv4 dotted decimal format according to RFC 1208.</span></span>

</dd> <dt>

<span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>

<span data-ttu-id="18c76-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="18c76-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="18c76-128">Unterstützung des IPv6-Text Formats gemäß RFC 4291</span><span class="sxs-lookup"><span data-stu-id="18c76-128">Support of the IPv6 text format according to RFC 4291</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="18c76-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="18c76-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18c76-130">**Synchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="18c76-130">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c76-131">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="18c76-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18c76-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c76-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18c76-133">Ein Array, das die [**CIM \_ virtualsystemmigrationservice**](cim-virtualsystemmigrationservice.md) -Methoden angibt, die für synchrone Vorgänge unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="18c76-133">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for synchronous operations.</span></span>

<span data-ttu-id="18c76-134">Enumeration von Methoden bezeichlern, deren Implementierung synchron sein kann; Das heißt, der Vorgang kann sofort durchgeführt werden. Daher gibt die Methode möglicherweise keinen Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="18c76-134">Enumeration of method identifiers whose implementation may be synchronous; that is, the operation may complete immediately and therefore the method may not return a job.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="18c76-135">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="18c76-135">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="18c76-136">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="18c76-136">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>

<span data-ttu-id="18c76-137">**CheckVirtualSystemIsMigratableToHostSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="18c76-137">**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>

<span data-ttu-id="18c76-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="18c76-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="18c76-139">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="18c76-139">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="18c76-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="18c76-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="18c76-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18c76-141">Requirements</span></span>



| <span data-ttu-id="18c76-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18c76-142">Requirement</span></span> | <span data-ttu-id="18c76-143">Wert</span><span class="sxs-lookup"><span data-stu-id="18c76-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18c76-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18c76-144">Minimum supported client</span></span><br/> | <span data-ttu-id="18c76-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="18c76-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="18c76-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18c76-146">Minimum supported server</span></span><br/> | <span data-ttu-id="18c76-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18c76-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="18c76-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="18c76-148">Namespace</span></span><br/>                | <span data-ttu-id="18c76-149">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="18c76-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="18c76-150">MOF</span><span class="sxs-lookup"><span data-stu-id="18c76-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18c76-151"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="18c76-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18c76-152">DLL</span><span class="sxs-lookup"><span data-stu-id="18c76-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18c76-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18c76-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18c76-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18c76-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18c76-155">**CIM- \_ Funktionen**</span><span class="sxs-lookup"><span data-stu-id="18c76-155">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

