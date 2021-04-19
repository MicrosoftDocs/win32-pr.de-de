---
description: Stellt die grundlegenden Anzeigefunktionen eines Computermonitors dar.
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: Wmimonitorbasicdisplaypara-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359425"
---
# <a name="wmimonitorbasicdisplayparams-class"></a><span data-ttu-id="a228c-103">Wmimonitorbasicdisplaypara-Klasse</span><span class="sxs-lookup"><span data-stu-id="a228c-103">WmiMonitorBasicDisplayParams class</span></span>

<span data-ttu-id="a228c-104">Die **wmimonitorbasicdisplayparser** -WMI-Klasse stellt die grundlegenden Anzeigefunktionen eines Computermonitors dar.</span><span class="sxs-lookup"><span data-stu-id="a228c-104">The **WmiMonitorBasicDisplayParams** WMI class represents the basic display features of a computer monitor.</span></span> <span data-ttu-id="a228c-105">Der Wert der **videoinputtype** -Eigenschaft gibt an, ob der Monitor Analog oder Digital ist.</span><span class="sxs-lookup"><span data-stu-id="a228c-105">The value of the **VideoInputType** property indicates whether the monitor is analog or digital.</span></span> <span data-ttu-id="a228c-106">Die Daten in dieser Klasse entsprechen den Daten im grundlegenden Anzeige Parameter/Features-Block des Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) Standard.</span><span class="sxs-lookup"><span data-stu-id="a228c-106">Data in this class corresponds to data in the Basic Display Parameters/Features block of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="a228c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a228c-107">Syntax</span></span>

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a><span data-ttu-id="a228c-108">Member</span><span class="sxs-lookup"><span data-stu-id="a228c-108">Members</span></span>

<span data-ttu-id="a228c-109">Die **wmimonitorbasicdisplayparser** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a228c-109">The **WmiMonitorBasicDisplayParams** class has these types of members:</span></span>

-   [<span data-ttu-id="a228c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a228c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a228c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a228c-111">Properties</span></span>

<span data-ttu-id="a228c-112">Die **wmimonitorbasicdisplayparser** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a228c-112">The **WmiMonitorBasicDisplayParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a228c-113">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="a228c-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a228c-114">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a228c-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a228c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a228c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a228c-116">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="a228c-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="a228c-117">**Display Transfer Merkmal**</span><span class="sxs-lookup"><span data-stu-id="a228c-117">**DisplayTransferCharacteristic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a228c-118">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a228c-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a228c-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a228c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a228c-120">Übertragungs Merkmal anzeigen (100 \* Gamma-100).</span><span class="sxs-lookup"><span data-stu-id="a228c-120">Display transfer characteristic (100\*Gamma-100).</span></span>

</dd> <dt>

<span data-ttu-id="a228c-121">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="a228c-121">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a228c-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a228c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a228c-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a228c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a228c-124">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a228c-124">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a228c-125">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="a228c-125">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="a228c-126">**Maxhorizontalimagesize**</span><span class="sxs-lookup"><span data-stu-id="a228c-126">**MaxHorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a228c-127">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a228c-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a228c-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a228c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a228c-129">Maximale horizontale Bildgröße in Zentimeter.</span><span class="sxs-lookup"><span data-stu-id="a228c-129">Maximum horizontal image size in centimeters.</span></span> <span data-ttu-id="a228c-130">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="a228c-130">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a228c-131">**Maxverticalimagesize**</span><span class="sxs-lookup"><span data-stu-id="a228c-131">**MaxVerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a228c-132">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a228c-132">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a228c-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a228c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a228c-134">Maximale vertikale Bildgröße in Zentimetern.</span><span class="sxs-lookup"><span data-stu-id="a228c-134">Maximum vertical image size in centimeters.</span></span> <span data-ttu-id="a228c-135">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="a228c-135">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a228c-136">**Supporteddisplayfeatures**</span><span class="sxs-lookup"><span data-stu-id="a228c-136">**SupportedDisplayFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a228c-137">Datentyp: **[ **supporteddisplayfeaturesdescriptor**](supporteddisplayfeaturesdescriptor.md)**</span><span class="sxs-lookup"><span data-stu-id="a228c-137">Data type: **[**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a228c-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a228c-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a228c-139">Zeigt die vom Monitor unterstützten Funktionen an.</span><span class="sxs-lookup"><span data-stu-id="a228c-139">Display features supported by the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="a228c-140">**Videoinputtype**</span><span class="sxs-lookup"><span data-stu-id="a228c-140">**VideoInputType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a228c-141">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a228c-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a228c-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a228c-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a228c-143">Video Eingabetyp.</span><span class="sxs-lookup"><span data-stu-id="a228c-143">Video input type.</span></span>



| <span data-ttu-id="a228c-144">Wert</span><span class="sxs-lookup"><span data-stu-id="a228c-144">Value</span></span>                                                                              | <span data-ttu-id="a228c-145">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a228c-145">Meaning</span></span>            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="a228c-146"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a228c-146"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="a228c-147">Ges</span><span class="sxs-lookup"><span data-stu-id="a228c-147">Analog</span></span><br/>  |
| <dl> <span data-ttu-id="a228c-148"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="a228c-148"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="a228c-149">Digital</span><span class="sxs-lookup"><span data-stu-id="a228c-149">Digital</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a228c-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a228c-150">Remarks</span></span>

<span data-ttu-id="a228c-151">**Maxhorizontalimagesize** und **maxverticalimagesize** stellen die maximalen Bild Dimensionen dar, die der Monitor für den gesamten Satz unterstützter Zeitachsen-und Format Kombinationen korrekt anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="a228c-151">**MaxHorizontalImageSize** and **MaxVerticalImageSize** represent the maximum image dimensions that the monitor can correctly display for the entire set of supported timing and format combinations.</span></span> <span data-ttu-id="a228c-152">Die maximale Image Dimension wird durch einen viad-Standard (Video Image Area Definition) definiert und auf den nächsten Zentimeter gerundet.</span><span class="sxs-lookup"><span data-stu-id="a228c-152">The maximum image dimension is defined by VESA Video Image Area Definition (VIAD) Standard and is rounded to the nearest centimeter.</span></span> <span data-ttu-id="a228c-153">Das Host Computersystem kann diese Daten verwenden, um die Abbild Größe und das Seitenverhältnis auszuwählen, das den ordnungsgemäßen skalierten Text zulässt.</span><span class="sxs-lookup"><span data-stu-id="a228c-153">The host computer system can use this data to select the image size and aspect ratio that will allow properly scaled text.</span></span> <span data-ttu-id="a228c-154">Beachten Sie, dass das System keine Annahmen über die Anzeige Größe gibt, wenn eines oder beide Felder NULL sind.</span><span class="sxs-lookup"><span data-stu-id="a228c-154">Be aware that, if either or both of these fields are zero, then the system makes no assumptions about the display size.</span></span> <span data-ttu-id="a228c-155">Beispielsweise kann die Größe einer Projektions Anzeige nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="a228c-155">For example, the size of a projection display may be undetermined.</span></span>

## <a name="requirements"></a><span data-ttu-id="a228c-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a228c-156">Requirements</span></span>



| <span data-ttu-id="a228c-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a228c-157">Requirement</span></span> | <span data-ttu-id="a228c-158">Wert</span><span class="sxs-lookup"><span data-stu-id="a228c-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a228c-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a228c-159">Minimum supported client</span></span><br/> | <span data-ttu-id="a228c-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a228c-160">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a228c-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a228c-161">Minimum supported server</span></span><br/> | <span data-ttu-id="a228c-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a228c-162">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a228c-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="a228c-163">Namespace</span></span><br/>                | <span data-ttu-id="a228c-164">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="a228c-164">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="a228c-165">MOF</span><span class="sxs-lookup"><span data-stu-id="a228c-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a228c-166"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a228c-166"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="a228c-167">DLL</span><span class="sxs-lookup"><span data-stu-id="a228c-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a228c-168"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a228c-168"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a228c-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a228c-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a228c-170">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="a228c-170">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




