---
description: Stellt den konfigurierten Status eines PCI Express-Ports dar.
ms.assetid: adb03dd7-5a47-47e6-a4e4-28224164150c
title: Msvm_PciExpressSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpressSettingData
- Msvm_PciExpressSettingData.VirtualFunctions
- Msvm_PciExpressSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c092cbc119506c4c52bc0565cd969426feffc481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352327"
---
# <a name="msvm_pciexpresssettingdata-class"></a><span data-ttu-id="a497b-103">MSVM \_ PCIExpress SettingData-Klasse</span><span class="sxs-lookup"><span data-stu-id="a497b-103">Msvm\_PciExpressSettingData class</span></span>

<span data-ttu-id="a497b-104">Stellt den konfigurierten Status eines PCI Express-Ports dar.</span><span class="sxs-lookup"><span data-stu-id="a497b-104">Represents the configured state of a PCI Express port.</span></span>

<span data-ttu-id="a497b-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a497b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a497b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a497b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpressSettingData : CIM_ResourceAllocationSettingData
{
  uint16 VirtualFunctions[];
  string VirtualSystemIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="a497b-107">Member</span><span class="sxs-lookup"><span data-stu-id="a497b-107">Members</span></span>

<span data-ttu-id="a497b-108">Die **MSVM \_ PCIExpress SettingData** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a497b-108">The **Msvm\_PciExpressSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a497b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a497b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a497b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a497b-110">Properties</span></span>

<span data-ttu-id="a497b-111">Die **MSVM \_ PCIExpress SettingData** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a497b-111">The **Msvm\_PciExpressSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a497b-112">**Virtualfunctions**</span><span class="sxs-lookup"><span data-stu-id="a497b-112">**VirtualFunctions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a497b-113">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a497b-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a497b-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a497b-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a497b-115">Die Nummer der virtuellen Funktion, die der VM zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a497b-115">The virtual function number to assign to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="a497b-116">**Virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="a497b-116">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a497b-117">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a497b-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a497b-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a497b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a497b-119">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="a497b-119">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a497b-120">Ein frei Handzeichen folgen Array mit Bezeichners dieser Ressource, die dem Betriebssystem des virtuellen Computer Systems präsentiert werden.</span><span class="sxs-lookup"><span data-stu-id="a497b-120">A free-form string array of identifiers of this resource presented to the virtual computer system's operating system.</span></span> <span data-ttu-id="a497b-121">Die Indizes und Werte pro Index werden pro Ressource definiert (d. h. für jeden aufgezählten **ResourceType** -Wert).</span><span class="sxs-lookup"><span data-stu-id="a497b-121">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="a497b-122">Diese Eigenschaft wird auf "GUID" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a497b-122">This property is set to "GUID".</span></span>

<span data-ttu-id="a497b-123">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyvirtualsystemresources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) -Methode der SD-Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a497b-123">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the sd class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a497b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a497b-124">Requirements</span></span>



| <span data-ttu-id="a497b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a497b-125">Requirement</span></span> | <span data-ttu-id="a497b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a497b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a497b-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a497b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a497b-128">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a497b-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a497b-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a497b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a497b-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a497b-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a497b-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="a497b-131">Namespace</span></span><br/>                | <span data-ttu-id="a497b-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a497b-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a497b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="a497b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a497b-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a497b-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a497b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a497b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a497b-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a497b-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a497b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a497b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a497b-138">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="a497b-138">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

