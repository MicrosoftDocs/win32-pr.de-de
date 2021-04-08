---
description: Beschreibt die Funktionen der zugeordneten MSVM \_ resourcepoolconfigurationservice-Klasse.
ms.assetid: 3e6857f9-62a0-420b-8f1d-8aad685a7ff7
title: Msvm_ResourcePoolConfigurationCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationCapabilities
- Msvm_ResourcePoolConfigurationCapabilities.InstanceID
- Msvm_ResourcePoolConfigurationCapabilities.Caption
- Msvm_ResourcePoolConfigurationCapabilities.Description
- Msvm_ResourcePoolConfigurationCapabilities.ElementName
- Msvm_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- Msvm_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b70d9e84e2c85d4c5b702a638982df0b47d62193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866111"
---
# <a name="msvm_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="09257-103">MSVM \_ resourcepoolconfigurationfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="09257-103">Msvm\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="09257-104">Beschreibt die Funktionen der zugeordneten [**MSVM \_ resourcepoolconfigurationservice**](msvm-resourcepoolconfigurationservice.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="09257-104">Describes the capabilities of the associated [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class.</span></span> <span data-ttu-id="09257-105">Clients können Instanzen dieser Klasse verwenden, um zu bestimmen, welche Methoden synchron oder asynchron unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="09257-105">Clients can use instances of this class to determine which methods are supported synchronously or asynchronously.</span></span> <span data-ttu-id="09257-106">Dieselbe Methode darf nicht in beiden Listen aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="09257-106">The same method must not be in both lists.</span></span> <span data-ttu-id="09257-107">Methoden Implementierungen müssen entweder synchron oder asynchron sein.</span><span class="sxs-lookup"><span data-stu-id="09257-107">Method implementations must either be synchronous or asynchronous.</span></span>

<span data-ttu-id="09257-108">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="09257-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="09257-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="09257-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = "Resource Pool Configuration Capabilities";
  string Description = "Microsoft Resource Pool Configuration Capabilities";
  string ElementName = "Resource Pool Configuration Capabilities";
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="09257-110">Member</span><span class="sxs-lookup"><span data-stu-id="09257-110">Members</span></span>

<span data-ttu-id="09257-111">Die **MSVM \_ resourcepoolconfigurationfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="09257-111">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="09257-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="09257-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09257-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="09257-113">Properties</span></span>

<span data-ttu-id="09257-114">Die **MSVM \_ resourcepoolconfigurationfunktionalitäten** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="09257-114">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09257-115">**Asynchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="09257-115">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09257-116">Datentyp: **UInt32** Array</span><span class="sxs-lookup"><span data-stu-id="09257-116">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="09257-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="09257-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09257-118">Ein Array von Methoden bezeichgern, von denen jedes eine Methode der [**MSVM \_ resourcepoolconfigurationservice**](msvm-resourcepoolconfigurationservice.md) -Klasse identifiziert, die asynchron von der-Implementierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="09257-118">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="09257-119">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="09257-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="09257-120">" **Kreatepool" wird unterstützt** (32768).</span><span class="sxs-lookup"><span data-stu-id="09257-120">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="09257-121">**Changepoolresources wird unterstützt** (32769).</span><span class="sxs-lookup"><span data-stu-id="09257-121">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="09257-122">**Changepoolsettings wird unterstützt** (32770).</span><span class="sxs-lookup"><span data-stu-id="09257-122">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="09257-123">**Deletepool wird unterstützt** (32771).</span><span class="sxs-lookup"><span data-stu-id="09257-123">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="09257-124">**Anbieter reserviert** (32772.65535)</span><span class="sxs-lookup"><span data-stu-id="09257-124">**Vendor Reserved** (32772..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="09257-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="09257-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09257-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="09257-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09257-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="09257-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09257-128">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="09257-128">A short description of the object.</span></span> <span data-ttu-id="09257-129">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ressourcen Pool-Konfigurationsfunktionen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="09257-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="09257-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="09257-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09257-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="09257-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09257-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="09257-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09257-133">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="09257-133">A description of the object.</span></span> <span data-ttu-id="09257-134">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft-Ressourcen Pool-Konfigurationsfunktionen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="09257-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="09257-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="09257-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09257-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="09257-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09257-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="09257-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09257-138">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="09257-138">A display name for the object.</span></span> <span data-ttu-id="09257-139">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ressourcen Pool-Konfigurationsfunktionen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="09257-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="09257-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="09257-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09257-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="09257-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09257-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="09257-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09257-143">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="09257-143">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="09257-144">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="09257-144">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="09257-145">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="09257-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="09257-146">**Synchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="09257-146">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09257-147">Datentyp: **UInt32** Array</span><span class="sxs-lookup"><span data-stu-id="09257-147">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="09257-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="09257-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09257-149">Ein Array von Methoden bezeichgern, von denen jedes eine Methode der [**MSVM \_ resourcepoolconfigurationservice**](msvm-resourcepoolconfigurationservice.md) -Klasse identifiziert, die von der-Implementierung synchron unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="09257-149">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="09257-150">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="09257-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="09257-151">" **Kreatepool" wird unterstützt** (32768).</span><span class="sxs-lookup"><span data-stu-id="09257-151">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="09257-152">**Changepoolresources wird unterstützt** (32769).</span><span class="sxs-lookup"><span data-stu-id="09257-152">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="09257-153">**Changepoolsettings wird unterstützt** (32770).</span><span class="sxs-lookup"><span data-stu-id="09257-153">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="09257-154">**Deletepool wird unterstützt** (32771).</span><span class="sxs-lookup"><span data-stu-id="09257-154">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="09257-155">**Anbieter reserviert** (32772.65535)</span><span class="sxs-lookup"><span data-stu-id="09257-155">**Vendor Reserved** (32772..65535)</span></span>


<span data-ttu-id="09257-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="09257-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="09257-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09257-157">Requirements</span></span>



| <span data-ttu-id="09257-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09257-158">Requirement</span></span> | <span data-ttu-id="09257-159">Wert</span><span class="sxs-lookup"><span data-stu-id="09257-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09257-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09257-160">Minimum supported client</span></span><br/> | <span data-ttu-id="09257-161">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="09257-161">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="09257-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09257-162">Minimum supported server</span></span><br/> | <span data-ttu-id="09257-163">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09257-163">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="09257-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="09257-164">Namespace</span></span><br/>                | <span data-ttu-id="09257-165">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="09257-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="09257-166">MOF</span><span class="sxs-lookup"><span data-stu-id="09257-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09257-167"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="09257-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09257-168">DLL</span><span class="sxs-lookup"><span data-stu-id="09257-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09257-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09257-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

