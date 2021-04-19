---
description: Stellt den Zustand des PCI Express-Ports dar.
ms.assetid: 15d670ee-940a-4737-b2cd-e89dd8a63a5c
title: Msvm_PciExpress-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpress
- Msvm_PciExpress.DeviceInstancePath
- Msvm_PciExpress.LocationPath
- Msvm_PciExpress.FunctionNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7534d09c9c0f3825ca462c342747caa17c8de9c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362962"
---
# <a name="msvm_pciexpress-class"></a><span data-ttu-id="1eb0c-103">MSVM \_ PCIExpress-Klasse</span><span class="sxs-lookup"><span data-stu-id="1eb0c-103">Msvm\_PciExpress class</span></span>

<span data-ttu-id="1eb0c-104">Stellt den Zustand des PCI Express-Ports dar.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-104">Represents the state of the PCI Express port.</span></span>

<span data-ttu-id="1eb0c-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb0c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1eb0c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpress : CIM_LogicalDevice
{
  string DeviceInstancePath;
  string LocationPath;
  uint16 FunctionNumber;
};
```

## <a name="members"></a><span data-ttu-id="1eb0c-107">Member</span><span class="sxs-lookup"><span data-stu-id="1eb0c-107">Members</span></span>

<span data-ttu-id="1eb0c-108">Die **MSVM \_ PCIExpress** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1eb0c-108">The **Msvm\_PciExpress** class has these types of members:</span></span>

-   [<span data-ttu-id="1eb0c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1eb0c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1eb0c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1eb0c-110">Properties</span></span>

<span data-ttu-id="1eb0c-111">Die **MSVM \_ PCIExpress** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-111">The **Msvm\_PciExpress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1eb0c-112">**Gerätepfad**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb0c-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb0c-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1eb0c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb0c-115">Eine Zeichenfolge mit dem geräteinstanzpfad zur Identifizierung des virtuellen PCI Express-Geräts.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-115">A string containing the device instance path that identifies the device virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="1eb0c-116">**Functionnumber**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-116">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb0c-117">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1eb0c-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1eb0c-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb0c-119">Die Funktions Nummer des virtuellen PCI Express-Geräts.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-119">The function number of the virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="1eb0c-120">**LocationPath**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-120">**LocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb0c-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb0c-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1eb0c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb0c-123">Eine Zeichenfolge mit dem Speicherort Pfad des Geräts, der das virtuelle PCI Express-Gerät identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-123">A string containing the device location path that identifies the device virtual PCI Express device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1eb0c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1eb0c-124">Requirements</span></span>



| <span data-ttu-id="1eb0c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1eb0c-125">Requirement</span></span> | <span data-ttu-id="1eb0c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1eb0c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb0c-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1eb0c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1eb0c-128">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1eb0c-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1eb0c-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1eb0c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1eb0c-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1eb0c-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1eb0c-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="1eb0c-131">Namespace</span></span><br/>                | <span data-ttu-id="1eb0c-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1eb0c-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1eb0c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="1eb0c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1eb0c-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1eb0c-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1eb0c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1eb0c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eb0c-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1eb0c-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1eb0c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1eb0c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb0c-138">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




