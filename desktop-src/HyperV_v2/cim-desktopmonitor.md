---
description: Stellt einen CRT-Desktop Monitor dar.
ms.assetid: 26a06320-9fd9-434e-87c8-486e9ca4945c
title: CIM_DesktopMonitor-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab152fc10f3fd404744c293d2368039ffcfdb291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357403"
---
# <a name="cim_desktopmonitor-class-hyper-v-management"></a><span data-ttu-id="2c7cd-103">CIM_DesktopMonitor-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="2c7cd-103">CIM_DesktopMonitor class (Hyper-V management)</span></span>

<span data-ttu-id="2c7cd-104">Stellt einen CRT-Desktop Monitor dar.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-104">Represents a CRT desktop monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c7cd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c7cd-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices")]
class CIM_DesktopMonitor : CIM_Display
{
  uint16 DisplayType;
  uint32 Bandwidth;
  uint32 ScreenHeight;
  uint32 ScreenWidth;
};
```

## <a name="members"></a><span data-ttu-id="2c7cd-106">Member</span><span class="sxs-lookup"><span data-stu-id="2c7cd-106">Members</span></span>

<span data-ttu-id="2c7cd-107">Die **CIM \_ Desktopmonitor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2c7cd-107">The **CIM\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="2c7cd-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c7cd-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c7cd-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c7cd-109">Properties</span></span>

<span data-ttu-id="2c7cd-110">Die **CIM \_ Desktopmonitor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-110">The **CIM\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c7cd-111">**Bandwidth**</span><span class="sxs-lookup"><span data-stu-id="2c7cd-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7cd-112">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c7cd-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c7cd-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7cd-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c7cd-114">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Megahertz"), **Punit** ("Hertz \* 10 ^ 6")</span><span class="sxs-lookup"><span data-stu-id="2c7cd-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="2c7cd-115">Die Bandbreite der Anzeige in mhertz.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-115">The bandwidth of the display, in MHertz.</span></span> <span data-ttu-id="2c7cd-116">"0" gibt unbekannt an.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-116">"0" indicates unknown.</span></span>

</dd> <dt>

<span data-ttu-id="2c7cd-117">**Display Type**</span><span class="sxs-lookup"><span data-stu-id="2c7cd-117">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7cd-118">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c7cd-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c7cd-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7cd-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7cd-120">Der Typ des Anzeige Typs des CRT-Monitors.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-120">The type of display type of the CRT monitor.</span></span> <span data-ttu-id="2c7cd-121">Beispielsweise MultiScan-Farbe oder monochrome.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-121">For example, multiscan color, or monochrome.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c7cd-122">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2c7cd-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c7cd-123">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="2c7cd-123">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="2c7cd-124">**MultiScan-Farbe** (2)</span><span class="sxs-lookup"><span data-stu-id="2c7cd-124">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="2c7cd-125">**MultiScan-monochrome** (3)</span><span class="sxs-lookup"><span data-stu-id="2c7cd-125">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="2c7cd-126">**Farbe für fixierte Häufigkeit** (4)</span><span class="sxs-lookup"><span data-stu-id="2c7cd-126">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="2c7cd-127">**Fester Frequenz-Mono** (5)</span><span class="sxs-lookup"><span data-stu-id="2c7cd-127">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c7cd-128">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="2c7cd-128">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7cd-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c7cd-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c7cd-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7cd-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7cd-131">Die logische Höhe der Anzeige in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-131">The logical height of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="2c7cd-132">**Bildschirmbreite**</span><span class="sxs-lookup"><span data-stu-id="2c7cd-132">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7cd-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c7cd-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c7cd-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7cd-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7cd-135">Die logische Breite der Anzeige in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-135">The logical width of the display, in screen coordinates.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c7cd-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c7cd-136">Requirements</span></span>



| <span data-ttu-id="2c7cd-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c7cd-137">Requirement</span></span> | <span data-ttu-id="2c7cd-138">Wert</span><span class="sxs-lookup"><span data-stu-id="2c7cd-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7cd-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c7cd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2c7cd-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2c7cd-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2c7cd-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c7cd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2c7cd-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2c7cd-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2c7cd-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c7cd-143">Namespace</span></span><br/>                | <span data-ttu-id="2c7cd-144">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2c7cd-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2c7cd-145">MOF</span><span class="sxs-lookup"><span data-stu-id="2c7cd-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c7cd-146"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2c7cd-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c7cd-147">DLL</span><span class="sxs-lookup"><span data-stu-id="2c7cd-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c7cd-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c7cd-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2c7cd-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c7cd-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c7cd-150">**CIM- \_ Anzeige**</span><span class="sxs-lookup"><span data-stu-id="2c7cd-150">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

