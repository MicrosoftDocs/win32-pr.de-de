---
description: Stellt einen zusammenhängenden Bereich logischer Blöcke dar, die von einem Dateisystem über das Feld "DeviceID" (Schlüssel) "Disks" identifiziert werden.
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: CIM_LogicalDisk-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.NameFormat
- CIM_LogicalDisk.NameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7305d0fa6ef45b5a97eb0fb6ab9ea740c98a392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960277"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a><span data-ttu-id="6197b-103">CIM_LogicalDisk-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="6197b-103">CIM_LogicalDisk class (Hyper-V management)</span></span>

<span data-ttu-id="6197b-104">Stellt einen zusammenhängenden Bereich logischer Blöcke dar, die von einem Dateisystem über das **DeviceID** (Key)-Feld des Datenträgers identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6197b-104">Represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="6197b-105">Beispielsweise enthält das Feld " **DeviceID** " in einer Windows-Umgebung einen Laufwerk Buchstaben. in einer UNIX-Umgebung enthält Sie den Zugriffs Pfad. und in einer NetWare-Umgebung enthält Sie den Volumenamen.</span><span class="sxs-lookup"><span data-stu-id="6197b-105">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6197b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6197b-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Device::StorageExtents"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16 NameFormat = 12;
  uint16 NameNamespace = 8;
};
```

## <a name="members"></a><span data-ttu-id="6197b-107">Member</span><span class="sxs-lookup"><span data-stu-id="6197b-107">Members</span></span>

<span data-ttu-id="6197b-108">Die **CIM \_ LogicalDisk** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6197b-108">The **CIM\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="6197b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6197b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6197b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6197b-110">Properties</span></span>

<span data-ttu-id="6197b-111">Die **CIM \_ LogicalDisk** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6197b-111">The **CIM\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6197b-112">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="6197b-112">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6197b-113">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6197b-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6197b-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6197b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6197b-115">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="6197b-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="6197b-116">Gibt an, ob das logische Gerät das Namensformat des Betriebssystems verwendet.</span><span class="sxs-lookup"><span data-stu-id="6197b-116">Indicates whether the logical device uses the name format of the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6197b-117">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6197b-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="6197b-118">**Betriebssystem-Geräte Name** (12)</span><span class="sxs-lookup"><span data-stu-id="6197b-118">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6197b-119">**Namenamespace**</span><span class="sxs-lookup"><span data-stu-id="6197b-119">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6197b-120">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6197b-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6197b-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6197b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6197b-122">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("namenamespace")</span><span class="sxs-lookup"><span data-stu-id="6197b-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")</span></span>
</dt> </dl>

<span data-ttu-id="6197b-123">Gibt an, ob das logische Gerät denselben Namespace aufweist wie das Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="6197b-123">Indicates whether the logical device has the same namespace as the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6197b-124">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6197b-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="6197b-125">**Betriebssystem-Geräte Namespace** (8)</span><span class="sxs-lookup"><span data-stu-id="6197b-125">**OS Device Namespace** (8)</span></span>


<span data-ttu-id="6197b-126"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6197b-126"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="6197b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6197b-127">Requirements</span></span>



| <span data-ttu-id="6197b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6197b-128">Requirement</span></span> | <span data-ttu-id="6197b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="6197b-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6197b-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6197b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6197b-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6197b-131">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6197b-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6197b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6197b-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6197b-133">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6197b-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="6197b-134">Namespace</span></span><br/>                | <span data-ttu-id="6197b-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6197b-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6197b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6197b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6197b-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6197b-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6197b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6197b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6197b-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6197b-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6197b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6197b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6197b-141">**CIM- \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="6197b-141">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

