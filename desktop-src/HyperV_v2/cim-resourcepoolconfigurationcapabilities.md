---
description: Verwaltet die Funktionen der CIM \_ resourcepoolconfigurationservice-Instanz für ein CIM- \_ resourcepool-Objekt.
ms.assetid: bd2eb4da-8ecd-4adb-b657-837c8da4dcdc
title: CIM_ResourcePoolConfigurationCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationCapabilities
- CIM_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- CIM_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 967b307049fa9c5f81b8deb6da96bcaa3be9acc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353113"
---
# <a name="cim_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="ecb0a-103">CIM \_ resourcepoolconfigurationfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="ecb0a-103">CIM\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="ecb0a-104">Verwaltet die Funktionen der [**CIM \_ resourcepoolconfigurationservice**](cim-resourcepoolconfigurationservice.md) -Instanz für ein [**CIM- \_ resourcepool**](cim-resourcepool.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-104">Manages the capabilities of the [**CIM\_ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md) instance for a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb0a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecb0a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="ecb0a-106">Member</span><span class="sxs-lookup"><span data-stu-id="ecb0a-106">Members</span></span>

<span data-ttu-id="ecb0a-107">Die **CIM \_ resourcepoolconfigurationfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ecb0a-107">The **CIM\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="ecb0a-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ecb0a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ecb0a-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ecb0a-109">Properties</span></span>

<span data-ttu-id="ecb0a-110">Die **CIM \_ resourcepoolconfigurationfunktionalitäten** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-110">The **CIM\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ecb0a-111">**Asynchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="ecb0a-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb0a-112">Datentyp: **UInt32** Array</span><span class="sxs-lookup"><span data-stu-id="ecb0a-112">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="ecb0a-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ecb0a-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecb0a-114">Die Methoden des Konfigurations Dienstanbieter, die für asynchrone Vorgänge unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-114">The methods of the configuration service that are supported for asynchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ecb0a-115">" **Kreateresourcepool" wird unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-115">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ecb0a-116">" **Kreatechild resourcepool" wird unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-116">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ecb0a-117">**Deleteresourcepool wird unterstützt** (4)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-117">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ecb0a-118">**Adresssourcestoresourcepool wird unterstützt** (5)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-118">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ecb0a-119">**Removeresourcesfromresourcepool wird unterstützt** (6)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-119">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangeParentResourcePool_is_supported"></span><span id="changeparentresourcepool_is_supported"></span><span id="CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ecb0a-120">**Changeparser-sourcepool wird unterstützt** (7)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-120">**ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ecb0a-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ecb0a-122">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ecb0a-123">**Synchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="ecb0a-123">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb0a-124">Datentyp: **UInt32** Array</span><span class="sxs-lookup"><span data-stu-id="ecb0a-124">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="ecb0a-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ecb0a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecb0a-126">Die Methoden des Konfigurations Dienstanbieter, die für synchrone Vorgänge unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-126">The methods of the configuration service that are supported for synchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ecb0a-127">" **Kreateresourcepool" wird unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-127">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ecb0a-128">" **Kreatechild resourcepool" wird unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-128">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ecb0a-129">**Deleteresourcepool wird unterstützt** (4)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-129">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ecb0a-130">**Adresssourcestoresourcepool wird unterstützt** (5)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-130">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ecb0a-131">**Removeresourcesfromresourcepool wird unterstützt** (6)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-131">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CIM_ChangeParentResourcePool_is_supported"></span><span id="cim_changeparentresourcepool_is_supported"></span><span id="CIM_CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ecb0a-132">**CIM \_ Changeparser-sourcepool wird unterstützt** (7)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-132">**CIM\_ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ecb0a-133">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ecb0a-134">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-134">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="ecb0a-135"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ecb0a-135"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ecb0a-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecb0a-136">Requirements</span></span>



| <span data-ttu-id="ecb0a-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ecb0a-137">Requirement</span></span> | <span data-ttu-id="ecb0a-138">Wert</span><span class="sxs-lookup"><span data-stu-id="ecb0a-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb0a-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb0a-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ecb0a-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ecb0a-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ecb0a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb0a-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ecb0a-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ecb0a-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="ecb0a-143">Namespace</span></span><br/>                | <span data-ttu-id="ecb0a-144">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ecb0a-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ecb0a-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ecb0a-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecb0a-146"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ecb0a-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecb0a-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ecb0a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecb0a-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ecb0a-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ecb0a-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecb0a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb0a-150">**CIM- \_ Funktionen**</span><span class="sxs-lookup"><span data-stu-id="ecb0a-150">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

 




