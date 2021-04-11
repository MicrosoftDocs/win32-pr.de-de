---
description: Stellt ein Gerät dar, das verwendet wird, um auf die Bereiche einer Anzeige zu zeigen.
ms.assetid: ffc675c3-29bd-4c54-8e54-8b6212daf66d
title: CIM_PointingDevice-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.Resolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57cca8c81a2d363e9e31bfc958a75b71e1b910d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132101"
---
# <a name="cim_pointingdevice-class-hyper-v-management"></a><span data-ttu-id="12046-103">CIM_PointingDevice-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="12046-103">CIM_PointingDevice class (Hyper-V management)</span></span>

<span data-ttu-id="12046-104">Stellt ein Gerät dar, das verwendet wird, um auf die Bereiche einer Anzeige zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="12046-104">Represents a device used to point to regions of a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="12046-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12046-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
{
  uint16 PointingType;
  uint8  NumberOfButtons;
  uint16 Handedness;
  uint32 Resolution;
};
```

## <a name="members"></a><span data-ttu-id="12046-106">Member</span><span class="sxs-lookup"><span data-stu-id="12046-106">Members</span></span>

<span data-ttu-id="12046-107">Die **CIM \_ pointingdevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="12046-107">The **CIM\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="12046-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12046-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12046-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12046-109">Properties</span></span>

<span data-ttu-id="12046-110">Die **CIM \_ pointingdevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="12046-110">The **CIM\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12046-111">**Händigkeit**</span><span class="sxs-lookup"><span data-stu-id="12046-111">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12046-112">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12046-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12046-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12046-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12046-114">Gibt an, ob das Zeigegerät für den rechten oder den überfälligen Vorgang konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="12046-114">Indicates whether the pointing device is configured for right or left handed operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12046-115">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="12046-115">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="12046-116">**Nicht zutreffend** (1)</span><span class="sxs-lookup"><span data-stu-id="12046-116">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="12046-117">**Rechter übergebenen Vorgang** (2)</span><span class="sxs-lookup"><span data-stu-id="12046-117">**Right Handed Operation** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="12046-118">**Linker Vorgang** (3)</span><span class="sxs-lookup"><span data-stu-id="12046-118">**Left Handed Operation** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12046-119">**Anzahl von Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="12046-119">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12046-120">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="12046-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="12046-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12046-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12046-122">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| zeigt Gerät \| 003,4 ")</span><span class="sxs-lookup"><span data-stu-id="12046-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.4")</span></span>
</dt> </dl>

<span data-ttu-id="12046-123">Die Anzahl der Schaltflächen auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="12046-123">The number of buttons on the device.</span></span> <span data-ttu-id="12046-124">Wenn das Zeigegerät keine Schaltflächen hat, sollte dieser Wert auf "0" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="12046-124">If the pointing device has no buttons, this value should be set to "0".</span></span>

</dd> <dt>

<span data-ttu-id="12046-125">**Pointingtype**</span><span class="sxs-lookup"><span data-stu-id="12046-125">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12046-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12046-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12046-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12046-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12046-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| zeigt Gerät \| 003,1 ")</span><span class="sxs-lookup"><span data-stu-id="12046-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.1")</span></span>
</dt> </dl>

<span data-ttu-id="12046-129">Der Typ des Zeige Geräts.</span><span class="sxs-lookup"><span data-stu-id="12046-129">The type of the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12046-130">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="12046-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12046-131">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="12046-131">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="12046-132">**Maus** (3)</span><span class="sxs-lookup"><span data-stu-id="12046-132">**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="12046-133">**Ball verfolgen** (4)</span><span class="sxs-lookup"><span data-stu-id="12046-133">**Track Ball** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="12046-134">Verfolgungs **Punkt** (5)</span><span class="sxs-lookup"><span data-stu-id="12046-134">**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="12046-135">**Gleitspunkt** (6)</span><span class="sxs-lookup"><span data-stu-id="12046-135">**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="12046-136">**Touchpad** (7)</span><span class="sxs-lookup"><span data-stu-id="12046-136">**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="12046-137">**Touchscreen** (8)</span><span class="sxs-lookup"><span data-stu-id="12046-137">**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="12046-138">**Maus optischer Sensor** (9)</span><span class="sxs-lookup"><span data-stu-id="12046-138">**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12046-139">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="12046-139">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12046-140">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12046-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12046-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12046-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12046-142">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zählungen pro Zoll"), **Punit** ("count/inch")</span><span class="sxs-lookup"><span data-stu-id="12046-142">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Counts per Inch"), **PUnit** ("count / inch")</span></span>
</dt> </dl>

<span data-ttu-id="12046-143">Die nach Verfolgungs Auflösung des Zeige Geräts in Zählungen pro Zoll.</span><span class="sxs-lookup"><span data-stu-id="12046-143">The tracking resolution of the pointing device, in counts per inch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12046-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12046-144">Requirements</span></span>



| <span data-ttu-id="12046-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12046-145">Requirement</span></span> | <span data-ttu-id="12046-146">Wert</span><span class="sxs-lookup"><span data-stu-id="12046-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12046-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12046-147">Minimum supported client</span></span><br/> | <span data-ttu-id="12046-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="12046-148">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="12046-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12046-149">Minimum supported server</span></span><br/> | <span data-ttu-id="12046-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12046-150">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="12046-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="12046-151">Namespace</span></span><br/>                | <span data-ttu-id="12046-152">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="12046-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="12046-153">MOF</span><span class="sxs-lookup"><span data-stu-id="12046-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12046-154"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="12046-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12046-155">DLL</span><span class="sxs-lookup"><span data-stu-id="12046-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12046-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12046-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="12046-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12046-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12046-158">**CIM- \_ userdevice**</span><span class="sxs-lookup"><span data-stu-id="12046-158">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

