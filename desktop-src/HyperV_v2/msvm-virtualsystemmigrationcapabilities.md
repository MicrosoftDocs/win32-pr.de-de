---
description: Definiert die Möglichkeiten, mit denen ein Client die vom Migrationsdienst bereitgestellten Methoden und den gültigen Bereich der Einstellungsdaten für die virtuelle System Migration ermitteln kann.
ms.assetid: 704fa81d-54a4-4d12-9b85-8836581d2784
title: Msvm_VirtualSystemMigrationCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationCapabilities
- Msvm_VirtualSystemMigrationCapabilities.InstanceID
- Msvm_VirtualSystemMigrationCapabilities.Caption
- Msvm_VirtualSystemMigrationCapabilities.Description
- Msvm_VirtualSystemMigrationCapabilities.ElementName
- Msvm_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c89e898cbf861d2bc3643e43a8bd9089062a2d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525193"
---
# <a name="msvm_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="b5db1-103">MSVM \_ virtualsystemmigrationfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="b5db1-103">Msvm\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="b5db1-104">Definiert die Möglichkeiten, mit denen ein Client die vom Migrationsdienst bereitgestellten Methoden und den gültigen Bereich der Einstellungsdaten für die virtuelle System Migration ermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="b5db1-104">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span> <span data-ttu-id="b5db1-105">Das **MSVM \_ virtualsystemmigrationfunktionalitäten** -Objekt ist [**MSVM \_ virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md) -Objekten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b5db1-105">The **Msvm\_VirtualSystemMigrationCapabilities** object is associated with [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) objects.</span></span> <span data-ttu-id="b5db1-106">Diese Zuordnungen definieren den gültigen Bereich von verfügbaren Migrationsdiensten.</span><span class="sxs-lookup"><span data-stu-id="b5db1-106">These associations define the valid range of migration services available.</span></span>

<span data-ttu-id="b5db1-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b5db1-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5db1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5db1-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationCapabilities : CIM_VirtualSystemMigrationCapabilities
{
  string InstanceID;
  string Caption = "Migration Capabilities";
  string Description = "Virtual System Migration Capabilities";
  string ElementName;
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="b5db1-109">Member</span><span class="sxs-lookup"><span data-stu-id="b5db1-109">Members</span></span>

<span data-ttu-id="b5db1-110">Die **MSVM \_ virtualsystemmigrationfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b5db1-110">The **Msvm\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="b5db1-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5db1-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5db1-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5db1-112">Properties</span></span>

<span data-ttu-id="b5db1-113">Die **MSVM \_ virtualsystemmigrationfunktionalitäten** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b5db1-113">The **Msvm\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5db1-114">**Asynchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="b5db1-114">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5db1-115">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="b5db1-115">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5db1-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-117">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("asynchronousmethodssupported")</span><span class="sxs-lookup"><span data-stu-id="b5db1-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="b5db1-118">Identifiziert die Methoden, deren Implementierung möglicherweise asynchron ist. Das heißt, der Vorgang wird nicht sofort abgeschlossen, und es wird ein Auftrag zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5db1-118">Identifies the methods whose implementation may be asynchronous; that is, the operation will not be completed immediately and will return a job.</span></span> <span data-ttu-id="b5db1-119">Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationfunktionen** geerbt.</span><span class="sxs-lookup"><span data-stu-id="b5db1-119">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="b5db1-120">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="b5db1-120">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="b5db1-121">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="b5db1-121">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableSupported"></span><span id="checkvirtualsystemismigratablesupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLESUPPORTED"></span>

<span data-ttu-id="b5db1-122">**CheckVirtualSystemIsMigratableSupported** (32768)</span><span class="sxs-lookup"><span data-stu-id="b5db1-122">**CheckVirtualSystemIsMigratableSupported** (32768)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b5db1-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b5db1-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5db1-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b5db1-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5db1-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5db1-126">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b5db1-126">A short description of the object.</span></span> <span data-ttu-id="b5db1-127">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Migrations Funktionen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b5db1-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="b5db1-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b5db1-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5db1-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b5db1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5db1-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5db1-131">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b5db1-131">A description of the object.</span></span> <span data-ttu-id="b5db1-132">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Virtual System Migration-Funktionen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b5db1-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual System Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="b5db1-133">**Destinationhostformatssupported**</span><span class="sxs-lookup"><span data-stu-id="b5db1-133">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5db1-134">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="b5db1-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5db1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5db1-136">Ein Array von namens Formaten, die für den *destinationhost* -Parameter der [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) -Methode und der [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) -Methode unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b5db1-136">An array of name formats that are supported for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) and [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) methods.</span></span> <span data-ttu-id="b5db1-137">Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationfunktionen** geerbt.</span><span class="sxs-lookup"><span data-stu-id="b5db1-137">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>



| <span data-ttu-id="b5db1-138">Wert</span><span class="sxs-lookup"><span data-stu-id="b5db1-138">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="b5db1-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b5db1-139">Meaning</span></span>                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span><dl> <span data-ttu-id="b5db1-140"><dt>**Domainnameformatsupported**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b5db1-140"><dt>**DomainNameFormatSupported**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="b5db1-141">Unterstützung des Domänen Namen Formats gemäß RFC 10353.</span><span class="sxs-lookup"><span data-stu-id="b5db1-141">Support of the domain name format according to RFC 10353.</span></span><br/>         |
| <span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span><dl> <span data-ttu-id="b5db1-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b5db1-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="b5db1-143">Unterstützung des IPv4-gepunkteten Dezimal Formats gemäß RFC 12084.</span><span class="sxs-lookup"><span data-stu-id="b5db1-143">Support of the IPv4 dotted decimal format according to RFC 12084.</span></span><br/> |
| <span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span><dl> <span data-ttu-id="b5db1-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b5db1-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="b5db1-145">Unterstützung des IPv6-Text Formats gemäß RFC 4291.</span><span class="sxs-lookup"><span data-stu-id="b5db1-145">Support of the IPv6 text format according to RFC 4291.</span></span><br/>            |



 

</dd> <dt>

<span data-ttu-id="b5db1-146">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b5db1-146">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5db1-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b5db1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5db1-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5db1-149">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b5db1-149">A display name for the object.</span></span> <span data-ttu-id="b5db1-150">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b5db1-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5db1-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b5db1-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5db1-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b5db1-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5db1-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-154">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="b5db1-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b5db1-155">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b5db1-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b5db1-156">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b5db1-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5db1-157">**Synchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="b5db1-157">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5db1-158">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="b5db1-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5db1-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5db1-160">Identifiziert die Methoden, deren Implementierung synchron sein kann. Das heißt, der Vorgang wird sofort abgeschlossen, und es wird kein Auftrag zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5db1-160">Identifies the methods whose implementation may be synchronous; that is, the operation will be completed immediately and will not return a job.</span></span> <span data-ttu-id="b5db1-161">Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationfunktionen** geerbt.</span><span class="sxs-lookup"><span data-stu-id="b5db1-161">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="b5db1-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="b5db1-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="b5db1-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="b5db1-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="b5db1-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b5db1-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="b5db1-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="b5db1-167">)</span><span class="sxs-lookup"><span data-stu-id="b5db1-167">)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5db1-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5db1-168">Requirements</span></span>



| <span data-ttu-id="b5db1-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5db1-169">Requirement</span></span> | <span data-ttu-id="b5db1-170">Wert</span><span class="sxs-lookup"><span data-stu-id="b5db1-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5db1-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5db1-171">Minimum supported client</span></span><br/> | <span data-ttu-id="b5db1-172">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5db1-172">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b5db1-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5db1-173">Minimum supported server</span></span><br/> | <span data-ttu-id="b5db1-174">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5db1-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5db1-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5db1-175">Namespace</span></span><br/>                | <span data-ttu-id="b5db1-176">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b5db1-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b5db1-177">MOF</span><span class="sxs-lookup"><span data-stu-id="b5db1-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5db1-178"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b5db1-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5db1-179">DLL</span><span class="sxs-lookup"><span data-stu-id="b5db1-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5db1-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5db1-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

