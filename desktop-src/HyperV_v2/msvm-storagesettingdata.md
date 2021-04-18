---
description: Stellt die Speicher spezifischen Einstellungen für ein virtuelles System dar.
ms.assetid: 0b3fcd78-7e9a-4a94-ad18-0ca72b3cfd73
title: Msvm_StorageSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageSettingData
- Msvm_StorageSettingData.VirtualProcessorsPerChannel
- Msvm_StorageSettingData.DisableInterruptBatching
- Msvm_StorageSettingData.ThreadCountPerChannel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db061d048ce45a4d6fa076a5b0367e794cdf16e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352389"
---
# <a name="msvm_storagesettingdata-class"></a><span data-ttu-id="a94b4-103">MSVM \_ storagesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="a94b4-103">Msvm\_StorageSettingData class</span></span>

<span data-ttu-id="a94b4-104">Stellt die Speicher spezifischen Einstellungen für ein virtuelles System dar.</span><span class="sxs-lookup"><span data-stu-id="a94b4-104">Represents the storage-specific settings for a virtual system.</span></span>

<span data-ttu-id="a94b4-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a94b4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a94b4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a94b4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageSettingData : Msvm_SystemComponentSettingData
{
  uint16  VirtualProcessorsPerChannel;
  boolean DisableInterruptBatching;
  uint16  ThreadCountPerChannel;
};
```

## <a name="members"></a><span data-ttu-id="a94b4-107">Member</span><span class="sxs-lookup"><span data-stu-id="a94b4-107">Members</span></span>

<span data-ttu-id="a94b4-108">Die Klasse " **MSVM \_ storagesettingdata** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a94b4-108">The **Msvm\_StorageSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a94b4-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a94b4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a94b4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a94b4-110">Properties</span></span>

<span data-ttu-id="a94b4-111">Die **MSVM \_ storagesettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a94b4-111">The **Msvm\_StorageSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a94b4-112">**Disableinterruptbatching**</span><span class="sxs-lookup"><span data-stu-id="a94b4-112">**DisableInterruptBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a94b4-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a94b4-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a94b4-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a94b4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a94b4-115">Gibt an, ob die Unterbrechung der Batch Verarbeitung deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a94b4-115">Specifies whether interrupt batching should be disabled.</span></span>

<span data-ttu-id="a94b4-116">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifysystemcomponentsettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) -Methode der WMI-Klasse " [**\_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) " geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a94b4-116">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the Wmi [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a94b4-117">**Threadfactperchannel**</span><span class="sxs-lookup"><span data-stu-id="a94b4-117">**ThreadCountPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a94b4-118">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a94b4-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a94b4-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a94b4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a94b4-120">Die Anzahl der Threads pro Speicherkanal für die Verarbeitung von e/a.</span><span class="sxs-lookup"><span data-stu-id="a94b4-120">The number of threads per storage channel to process IO.</span></span>

<span data-ttu-id="a94b4-121">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifysystemcomponentsettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a94b4-121">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="a94b4-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Standard** (0)</span><span class="sxs-lookup"><span data-stu-id="a94b4-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a94b4-123">Standardverhalten</span><span class="sxs-lookup"><span data-stu-id="a94b4-123">Default behavior</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="a94b4-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Niedrig** (1)</span><span class="sxs-lookup"><span data-stu-id="a94b4-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a94b4-125">Geringe Anzahl von Threads pro Speicherkanal.</span><span class="sxs-lookup"><span data-stu-id="a94b4-125">Low number of threads per storage channel.</span></span>

</dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="a94b4-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Mittel** (2)</span><span class="sxs-lookup"><span data-stu-id="a94b4-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a94b4-127">Mittlere Anzahl von Threads pro Speicherkanal.</span><span class="sxs-lookup"><span data-stu-id="a94b4-127">Medium number of threads per storage channel.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="a94b4-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Hoch** (3)</span><span class="sxs-lookup"><span data-stu-id="a94b4-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a94b4-129">Hohe Anzahl von Threads pro Speicherkanal.</span><span class="sxs-lookup"><span data-stu-id="a94b4-129">High number of threads per storage channel.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a94b4-130">**Virtualprocessorsperchannel**</span><span class="sxs-lookup"><span data-stu-id="a94b4-130">**VirtualProcessorsPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a94b4-131">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a94b4-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a94b4-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a94b4-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a94b4-133">Die Anzahl der Prozessoren pro Speicherkanal.</span><span class="sxs-lookup"><span data-stu-id="a94b4-133">The number of processors per storage channel.</span></span> <span data-ttu-id="a94b4-134">Die Anzahl der zu öffnenden Kanäle wird durch angegeben (Anzahl der logischen Prozessoren auf dem Host/**virtualprocessorsperchannel**).</span><span class="sxs-lookup"><span data-stu-id="a94b4-134">The number of channels to be opened is given by (Count of logical processors on the host /**VirtualProcessorsPerChannel**).</span></span>

<span data-ttu-id="a94b4-135">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifysystemcomponentsettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a94b4-135">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a94b4-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a94b4-136">Requirements</span></span>



| <span data-ttu-id="a94b4-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a94b4-137">Requirement</span></span> | <span data-ttu-id="a94b4-138">Wert</span><span class="sxs-lookup"><span data-stu-id="a94b4-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a94b4-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a94b4-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a94b4-140">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a94b4-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a94b4-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a94b4-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a94b4-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a94b4-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a94b4-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="a94b4-143">Namespace</span></span><br/>                | <span data-ttu-id="a94b4-144">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a94b4-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a94b4-145">MOF</span><span class="sxs-lookup"><span data-stu-id="a94b4-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a94b4-146"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a94b4-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a94b4-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a94b4-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a94b4-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a94b4-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a94b4-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a94b4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a94b4-150">**MSVM \_ systemcomponentsettingdata**</span><span class="sxs-lookup"><span data-stu-id="a94b4-150">**Msvm\_SystemComponentSettingData**</span></span>](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




