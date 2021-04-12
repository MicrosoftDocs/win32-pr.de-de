---
description: Beschreibt die Einstellungsdaten für einen virtuellen synthetischen Anzeige Controller.
ms.assetid: cea79b24-4175-49db-a8b4-a9efb1fd0b96
title: Msvm_SyntheticDisplayControllerSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayControllerSettingData
- Msvm_SyntheticDisplayControllerSettingData.ResolutionType
- Msvm_SyntheticDisplayControllerSettingData.HorizontalResolution
- Msvm_SyntheticDisplayControllerSettingData.VerticalResolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 52935800eda641eb9015247e9320f33f22b40251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215372"
---
# <a name="msvm_syntheticdisplaycontrollersettingdata-class"></a><span data-ttu-id="18554-103">MSVM \_ syntheticdisplaycontrollersettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="18554-103">Msvm\_SyntheticDisplayControllerSettingData class</span></span>

<span data-ttu-id="18554-104">Beschreibt die Einstellungsdaten für einen virtuellen synthetischen Anzeige Controller.</span><span class="sxs-lookup"><span data-stu-id="18554-104">Describes the setting data for a virtual synthetic display controller.</span></span>

<span data-ttu-id="18554-105">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="18554-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18554-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="18554-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  uint8  ResolutionType;
  uint16 HorizontalResolution;
  uint16 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="18554-107">Member</span><span class="sxs-lookup"><span data-stu-id="18554-107">Members</span></span>

<span data-ttu-id="18554-108">Die **MSVM \_ syntheticdisplaycontrollersettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="18554-108">The **Msvm\_SyntheticDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="18554-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18554-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18554-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18554-110">Properties</span></span>

<span data-ttu-id="18554-111">Die **MSVM \_ syntheticdisplaycontrollersettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="18554-111">The **Msvm\_SyntheticDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18554-112">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="18554-112">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18554-113">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18554-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18554-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="18554-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18554-115">Die horizontale Auflösung.</span><span class="sxs-lookup"><span data-stu-id="18554-115">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="18554-116">**ResolutionType**</span><span class="sxs-lookup"><span data-stu-id="18554-116">**ResolutionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18554-117">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="18554-117">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="18554-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18554-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18554-119">Der Lösungstyp.</span><span class="sxs-lookup"><span data-stu-id="18554-119">The resolution type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18554-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="18554-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18554-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="18554-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="18554-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span><span class="sxs-lookup"><span data-stu-id="18554-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Single"></span><span id="single"></span><span id="SINGLE"></span>

<span data-ttu-id="18554-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Single** (3)</span><span class="sxs-lookup"><span data-stu-id="18554-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Single** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="18554-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Standard** (4)</span><span class="sxs-lookup"><span data-stu-id="18554-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="18554-125">Hinzugefügt in Windows 10, Version 1703.</span><span class="sxs-lookup"><span data-stu-id="18554-125">Added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18554-126">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="18554-126">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18554-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18554-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18554-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="18554-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18554-129">Die vertikale Auflösung.</span><span class="sxs-lookup"><span data-stu-id="18554-129">The vertical resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18554-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18554-130">Requirements</span></span>



| <span data-ttu-id="18554-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18554-131">Requirement</span></span> | <span data-ttu-id="18554-132">Wert</span><span class="sxs-lookup"><span data-stu-id="18554-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18554-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18554-133">Minimum supported client</span></span><br/> | <span data-ttu-id="18554-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18554-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="18554-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18554-135">Minimum supported server</span></span><br/> | <span data-ttu-id="18554-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="18554-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="18554-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="18554-137">Namespace</span></span><br/>                | <span data-ttu-id="18554-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="18554-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="18554-139">MOF</span><span class="sxs-lookup"><span data-stu-id="18554-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18554-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="18554-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18554-141">DLL</span><span class="sxs-lookup"><span data-stu-id="18554-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18554-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18554-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18554-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18554-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18554-144">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="18554-144">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




