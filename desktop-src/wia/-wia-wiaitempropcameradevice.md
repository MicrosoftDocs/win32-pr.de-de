---
description: Für Windows-Abbild Beschaffung (WIA)-Hardware Geräte sind Eigenschaftswerte vorhanden, die in der Windows-Registrierung gespeichert sind. Weitere Informationen finden Sie unter Allgemeine Geräte Eigenschafts Konstanten.
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: Eigenschaften Konstanten für Kamerageräte (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPC_PICTURES_TAKEN
- WIA_DPC_PICTURES_REMAINING
- WIA_DPC_EXPOSURE_MODE
- WIA_DPC_EXPOSURE_COMP
- WIA_DPC_EXPOSURE_TIME
- WIA_DPC_FNUMBER
- WIA_DPC_FLASH_MODE
- WIA_DPC_FOCUS_MODE
- WIA_DPC_FOCUS_MANUAL_DIST
- WIA_DPC_ZOOM_POSITION
- WIA_DPC_PAN_POSITION
- WIA_DPC_TILT_POSITION
- WIA_DPC_TIMER_MODE
- WIA_DPC_TIMER_VALUE
- WIA_DPC_POWER_MODE
- WIA_DPC_BATTERY_STATUS
- WIA_DPC_THUMB_WIDTH
- WIA_DPC_THUMB_HEIGHT
- WIA_DPC_PICT_WIDTH
- WIA_DPC_PICT_HEIGHT
- WIA_DPC_DIMENSION
- WIA_DPC_COMPRESSION_SETTING
- WIA_DPC_FOCUS_METERING
- WIA_DPC_TIMELAPSE_INTERVAL
- WIA_DPC_TIMELAPSE_NUMBER
- WIA_DPC_BURST_INTERVAL
- WIA_DPC_BURST_NUMBER
- WIA_DPC_EFFECT_MODE
- WIA_DPC_DIGITAL_ZOOM
- WIA_DPC_SHARPNESS
- WIA_DPC_CONTRAST
- WIA_DPC_CAPTURE_MODE
- WIA_DPC_CAPTURE_DELAY
- WIA_DPC_EXPOSURE_INDEX
- WIA_DPC_EXPOSURE_METERING_MODE
- WIA_DPC_FOCUS_METERING_MODE
- WIA_DPC_FOCUS_DISTANCE
- WIA_DPC_FOCAL_LENGTH
- WIA_DPC_RGB_GAIN
- WIA_DPC_WHITE_BALANCE
- WIA_DPC_UPLOAD_URL
- WIA_DPC_ARTIST
- WIA_DPC_COPYRIGHT_INFO
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 0114fedd7fd4acf811e71db67376afecc2630cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485043"
---
# <a name="camera-device-property-constants"></a><span data-ttu-id="4b9f6-104">Eigenschaften Konstanten für Kamerageräte</span><span class="sxs-lookup"><span data-stu-id="4b9f6-104">Camera Device Property Constants</span></span>

<span data-ttu-id="4b9f6-105">Für Windows-Abbild Beschaffung (WIA)-Hardware Geräte sind Eigenschaftswerte vorhanden, die in der Windows-Registrierung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-105">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="4b9f6-106">Weitere Informationen finden Sie unter [**Allgemeine Geräte Eigenschafts Konstanten**](-wia-wiaitempropcommondevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b9f6-106">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span>

<span data-ttu-id="4b9f6-107">Die folgenden Geräteeigenschaften Konstanten, mit den zugehörigen Zeichen folgen, sind für digitale Kameras spezifisch.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-107">The following device property constants, with their associated strings, are specific to digital cameras.</span></span> <span data-ttu-id="4b9f6-108">Das Präfix "WIA \_ DPC \_ " gibt eine Geräte Eigenschaft für Kameras an und ist die Benennungs Konvention, die in C/C++ verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-108">The prefix "WIA\_DPC\_" indicates a Device Property for Cameras and is the naming convention used in C/C++.</span></span> <span data-ttu-id="4b9f6-109">Bei der Skripterstellung verwenden diese Konstanten das Präfix "cameradevice" und sind Teil des enumerierten Typs [wiaitempropertyid](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="4b9f6-109">For scripting purposes these constants use the prefix "CameraDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="4b9f6-110">Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-110">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="4b9f6-111">WIA unterstützt keine Kameras in Windows Vista oder höher.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-111">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="4b9f6-112">Verwenden Sie für diese Windows-Versionen die im Windows-Treiber Development Kit (DDK) beschriebene Windows-API für portable Geräte, um Images von Kameras abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-112">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4b9f6-113">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="4b9f6-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4b9f6-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b9f6-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <span data-ttu-id="4b9f6-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>cameradevicepicturestaken</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4b9f6-116">Die Anzahl der Bilder, die die Kamera genommen hat.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-116">The number of pictures that the camera has taken.</span></span> <span data-ttu-id="4b9f6-117">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-117">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="4b9f6-118">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-118">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <span data-ttu-id="4b9f6-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>cameradevicepicturesrest</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4b9f6-120">Die Anzahl von Bildern, die mit den aktuellen Eigenschaften Einstellungen entnommen werden können.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-120">The number of pictures that can be taken, given the current property settings.</span></span> <span data-ttu-id="4b9f6-121">Wenn sich diese Einstellungen ändern und sich die Änderungen auf die Größe der Bilder auswirken, die das Kamera Gerät erzeugt, sollte der WIA-Mini Treiber die Anzahl der verbleibenden Bilder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-121">If these settings change, and the changes affect the size of the images that the camera device produces, the WIA minidriver should update the number of remaining pictures.</span></span> <span data-ttu-id="4b9f6-122">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-122">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="4b9f6-123">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-123">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <span data-ttu-id="4b9f6-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>cameradeviceexposuremode</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4b9f6-125">Gibt den aktuellen Anzeigemodus der Kamera an.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-125">Indicates the camera's current exposure mode.</span></span> <span data-ttu-id="4b9f6-126">Diese Eigenschaft wird von einer Anwendung geändert, um den Anzeigemodus des Kamera Geräts zu steuern.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-126">An application changes this property to control the exposure mode of the camera device.</span></span><br/> <span data-ttu-id="4b9f6-127">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-127">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="4b9f6-128">Die folgende Tabelle enthält die sieben Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-128">The following table has the seven constants that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4b9f6-129">Anzeigemodus</span><span class="sxs-lookup"><span data-stu-id="4b9f6-129">Exposure Mode</span></span></th>
<th><span data-ttu-id="4b9f6-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b9f6-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b9f6-131">EXPOSUREMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="4b9f6-131">EXPOSUREMODE_MANUAL</span></span></td>
<td><span data-ttu-id="4b9f6-132">Die Auslösegeschwindigkeit und-Öffnung werden vom Benutzer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-132">The shutter speed and aperture are set by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-133">EXPOSUREMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="4b9f6-133">EXPOSUREMODE_AUTO</span></span></td>
<td><span data-ttu-id="4b9f6-134">Die Auslösegeschwindigkeit und-Öffnung werden automatisch von der Kamera festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-134">The shutter speed and aperture are automatically set by the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b9f6-135">EXPOSUREMODE_APERTURE_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="4b9f6-135">EXPOSUREMODE_APERTURE_PRIORITY</span></span></td>
<td><span data-ttu-id="4b9f6-136">Die Öffnung wird vom Benutzer festgelegt, und die Kamera legt die Auslösegeschwindigkeit automatisch fest.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-136">The aperture is set by the user, and the camera automatically sets the shutter speed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-137">EXPOSUREMODE_SHUTTER_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="4b9f6-137">EXPOSUREMODE_SHUTTER_PRIORITY</span></span></td>
<td><span data-ttu-id="4b9f6-138">Die Auslösegeschwindigkeit wird vom Benutzer festgelegt, und die Kamera legt automatisch die Öffnung fest.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-138">The shutter speed is set by the user, and the camera automatically sets the aperture.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b9f6-139">EXPOSUREMODE_PROGRAM_CREATIVE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-139">EXPOSUREMODE_PROGRAM_CREATIVE</span></span></td>
<td><span data-ttu-id="4b9f6-140">Die Auslösegeschwindigkeit und die Öffnungs Taste werden automatisch von der Kamera festgelegt, die für eine weitere Gegenfrage optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-140">The shutter speed and aperture are automatically set by the camera, optimized for still subject matter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-141">EXPOSUREMODE_PROGRAM_ACTION</span><span class="sxs-lookup"><span data-stu-id="4b9f6-141">EXPOSUREMODE_PROGRAM_ACTION</span></span></td>
<td><span data-ttu-id="4b9f6-142">Die Auslösegeschwindigkeit und-Öffnung werden automatisch von der Kamera festgelegt, die für Szenen optimiert ist, die schnelles Bewegung enthalten.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-142">The shutter speed and aperture are automatically set by the camera, optimized for scenes containing fast motion.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b9f6-143">EXPOSUREMODE_PORTRAIT</span><span class="sxs-lookup"><span data-stu-id="4b9f6-143">EXPOSUREMODE_PORTRAIT</span></span></td>
<td><span data-ttu-id="4b9f6-144">Die Auslösegeschwindigkeit und die Öffnungs Taste werden automatisch von der Kamera festgelegt, die für hoch Fotografie optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-144">The shutter speed and aperture are automatically set by the camera, optimized for portrait photography.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <span data-ttu-id="4b9f6-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>cameradeviceexposurecomp</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-146">Ermöglicht die Anpassung des festgelegten Punkts der automatischen verfügbar machung des digitalen Kamera-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-146">Allows for the adjustment of the set point of the digital camera's auto-exposure control.</span></span> <span data-ttu-id="4b9f6-147">Beispielsweise wird bei einer Einstellung von 0 (null) die Einstellung für die automatische Festlegung der Werkseinstellungen nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-147">For example, a setting of zero does not change the factory-set auto-exposure level.</span></span> <span data-ttu-id="4b9f6-148">Die Einheiten werden in &quot; Stopps &quot; skaliert, die mit dem Faktor 1000 skaliert werden, um die Stopp Werte in Bruch Zeiten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-148">The units are in &quot;stops&quot; that are scaled by a factor of 1000, to allow for fractional stop values.</span></span> <span data-ttu-id="4b9f6-149">Eine Einstellung von 2000 entspricht zwei nicht mehr Verfügbarkeit (viermal mehr Energie auf dem Sensor) und liefert hellere Bilder.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-149">A setting of 2000 corresponds to two stops more exposure (four times more energy on the sensor), yielding brighter images.</span></span> <span data-ttu-id="4b9f6-150">Eine Einstellung von-1000 entspricht einem ungefährdenden unterlegungs Stand (eine Hälfte der Energie auf dem Sensor) und liefert dunklere Bilder.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-150">A setting of -1000 corresponds to one stop less exposure (one-half the energy on the sensor) yielding darker images.</span></span> <span data-ttu-id="4b9f6-151">Die Einstellungs Werte befinden sich in einem Additiven System von Spitze Einheiten (Photo Exposition).</span><span class="sxs-lookup"><span data-stu-id="4b9f6-151">The setting values are in Additive System of Photographic Exposure (APEX) units.</span></span> <span data-ttu-id="4b9f6-152">Diese Eigenschaft kann entweder als Liste oder als Wertebereich ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-152">This property may be expressed as either a list or a range of values.</span></span> <span data-ttu-id="4b9f6-153">Diese Eigenschaft wird in der Regel nur verwendet, wenn für das Gerät die <strong>WIA_DPC_EXPOSURE_MODE</strong> -Eigenschaft auf EXPOSUREMODE_MANUAL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-153">This property is typically used only when the device has the <strong>WIA_DPC_EXPOSURE_MODE</strong> property set to EXPOSUREMODE_MANUAL.</span></span></p>
<p><span data-ttu-id="4b9f6-154">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> oder WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="4b9f6-154">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <span data-ttu-id="4b9f6-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>cameradeviceexposuretime</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-156">Entspricht der Zeit in Sekunden, die von 10.000 skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-156">Corresponds to the shutter speed, in seconds that are scaled by 10,000.</span></span> <span data-ttu-id="4b9f6-157">In der Regel wird diese Eigenschaft vom Gerät nur verwendet, wenn die <strong>WIA_DPC_EXPOSURE_MODE</strong> -Eigenschaft auf EXPOSUREMODE_MANUAL oder EXPOSUREMODE_SHUTTER_PRIORITY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-157">Typically, the device uses this property only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_SHUTTER_PRIORITY.</span></span></p>
<p><span data-ttu-id="4b9f6-158">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> oder WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="4b9f6-158">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <span data-ttu-id="4b9f6-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>cameradevicefnumber</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-160">Entspricht der Öffnung des Lens in Einheiten der f-Ende-Zahl, die von 100 skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-160">Corresponds to the aperture of the lens, in units of the f-stop number scaled by 100.</span></span> <span data-ttu-id="4b9f6-161">Die Einstellung dieser Eigenschaft ist in der Regel nur gültig, wenn die <strong>WIA_DPC_EXPOSURE_MODE</strong> -Eigenschaft auf EXPOSUREMODE_MANUAL oder EXPOSUREMODE_APERTURE_PRIORITY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-161">The setting of this property is typically valid only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_APERTURE_PRIORITY.</span></span></p>
<p><span data-ttu-id="4b9f6-162">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-162">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <span data-ttu-id="4b9f6-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>cameradeviceflash Mode</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-164">Definiert die aktuelle Einstellung für den Flash Modus für das Kamera Gerät.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-164">Defines the current flash mode setting for the camera device.</span></span> <span data-ttu-id="4b9f6-165">Der Gerätetreiber listet die unterstützten Werte dieser Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-165">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="4b9f6-166">Diese Eigenschaft wird von einer Anwendung geschrieben, um den Flash Modus für das Kamera Gerät festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-166">An application writes this property to set the flash mode for the camera device.</span></span></p>
<p><span data-ttu-id="4b9f6-167">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-167">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="4b9f6-168">Die folgende Tabelle enthält die sechs Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-168">The following table has the six constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4b9f6-169">Flash Modus</span><span class="sxs-lookup"><span data-stu-id="4b9f6-169">Flash Mode</span></span></th>
<th><span data-ttu-id="4b9f6-170">Definition</span><span class="sxs-lookup"><span data-stu-id="4b9f6-170">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b9f6-171">FLASHMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="4b9f6-171">FLASHMODE_AUTO</span></span></td>
<td><span data-ttu-id="4b9f6-172">Das Kamera Gerät legt die richtigen Flash Einstellungen fest.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-172">The camera device determines the proper flash settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-173">FLASHMODE_FILL</span><span class="sxs-lookup"><span data-stu-id="4b9f6-173">FLASHMODE_FILL</span></span></td>
<td><span data-ttu-id="4b9f6-174">Das Kamera Gerät ist so konfiguriert, dass es unabhängig von den aktuellen Beleuchtungsbedingungen blinkt.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-174">The camera device is configured to flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b9f6-175">FLASHMODE_OFF</span><span class="sxs-lookup"><span data-stu-id="4b9f6-175">FLASHMODE_OFF</span></span></td>
<td><span data-ttu-id="4b9f6-176">Das Kamera Gerät ist so konfiguriert, dass es <em>kein</em> Flash für ein Bild erstellt.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-176">The camera device is configured <em>not</em> to flash for any picture taken.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-177">FLASHMODE_REDEYE_AUTO</span><span class="sxs-lookup"><span data-stu-id="4b9f6-177">FLASHMODE_REDEYE_AUTO</span></span></td>
<td><span data-ttu-id="4b9f6-178">Das Kamera Gerät bestimmt die richtigen Flash Einstellungen mithilfe der Red-Eye-Reduzierung, unabhängig von den aktuellen Beleuchtungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-178">The camera device determines the proper flash settings using red-eye reduction, regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b9f6-179">FLASHMODE_REDEYE_FILL</span><span class="sxs-lookup"><span data-stu-id="4b9f6-179">FLASHMODE_REDEYE_FILL</span></span></td>
<td><span data-ttu-id="4b9f6-180">Das Kamera Gerät ist so konfiguriert, dass es unabhängig von den aktuellen Beleuchtungsbedingungen die Red-Eye-Reduzierung und Flash Flash verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-180">The camera device is configured to use red-eye reduction and flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-181">FLASHMODE_EXTERNALSYNC</span><span class="sxs-lookup"><span data-stu-id="4b9f6-181">FLASHMODE_EXTERNALSYNC</span></span></td>
<td><span data-ttu-id="4b9f6-182">Das Kamera Gerät ist für die Synchronisierung mit externen Flash Einheiten konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-182">The camera device is configured to synchronize with external flash units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <span data-ttu-id="4b9f6-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>cameradevicefocemode</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-184">Definiert die aktuelle Fokus Modus-Einstellung für das Kamera Gerät.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-184">Defines the current focus mode setting for the camera device.</span></span> <span data-ttu-id="4b9f6-185">Der Gerätetreiber listet die unterstützten Werte dieser Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-185">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="4b9f6-186">Diese Eigenschaft wird von einer Anwendung geschrieben, um den Fokus Modus für das Kamera Gerät festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-186">An application writes this property to set the focus mode for the camera device.</span></span></p>
<p><span data-ttu-id="4b9f6-187">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-187">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="4b9f6-188">Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-188">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4b9f6-189">Fokusmodus</span><span class="sxs-lookup"><span data-stu-id="4b9f6-189">Focus Mode</span></span></th>
<th><span data-ttu-id="4b9f6-190">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b9f6-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b9f6-191">FOCUSMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="4b9f6-191">FOCUSMODE_MANUAL</span></span></td>
<td><span data-ttu-id="4b9f6-192">Das Kamera Gerät ist so konfiguriert, dass der Benutzer sich manuell fokussieren kann.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-192">The camera device is configured to allow the user to focus manually.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-193">FOCUSMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="4b9f6-193">FOCUSMODE_AUTO</span></span></td>
<td><span data-ttu-id="4b9f6-194">Das Kamera Gerät ist so konfiguriert, dass es automatisch fokussiert wird.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-194">The camera device is configured to focus automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b9f6-195">FOCUSMODE_MACROAUTO</span><span class="sxs-lookup"><span data-stu-id="4b9f6-195">FOCUSMODE_MACROAUTO</span></span></td>
<td><span data-ttu-id="4b9f6-196">Das Kamera Gerät ist so konfiguriert, dass es sich automatisch mithilfe von Makro Einstellungen im kurzen Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-196">The camera device is configured to focus automatically using short-range macro settings.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <span data-ttu-id="4b9f6-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-198">Reserviert, nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-198">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="4b9f6-199">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-199">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <span data-ttu-id="4b9f6-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-201">Reserviert, nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-201">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="4b9f6-202">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-202">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <span data-ttu-id="4b9f6-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>cameradevicepanposition</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-204">Reserviert, nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-204">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="4b9f6-205">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <span data-ttu-id="4b9f6-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>cameradevicetiltposition</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-207">Reserviert, nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-207">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="4b9f6-208">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-208">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <span data-ttu-id="4b9f6-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>cameradevicetimermode</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-210">Reserviert, nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-210">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="4b9f6-211">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-211">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <span data-ttu-id="4b9f6-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>cameradevicetimervalue</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-213">Reserviert, nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-213">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="4b9f6-214">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-214">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <span data-ttu-id="4b9f6-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>cameradevicepowermode</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-216">Definiert die aktuelle Stromquelle für das Kamera Gerät.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-216">Defines the current power source for the camera device.</span></span> <span data-ttu-id="4b9f6-217">Diese Eigenschaft wird von einer Anwendung gelesen, um zu bestimmen, welche Stromquelle von der Kamera verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-217">An application reads this property to determine what power source the camera is using.</span></span></p>
<p><span data-ttu-id="4b9f6-218">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-218">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="4b9f6-219">Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-219">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4b9f6-220">Energiesparmodus</span><span class="sxs-lookup"><span data-stu-id="4b9f6-220">Power Mode</span></span></th>
<th><span data-ttu-id="4b9f6-221">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b9f6-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b9f6-222">POWERMODE_LINE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-222">POWERMODE_LINE</span></span></td>
<td><span data-ttu-id="4b9f6-223">Das Kamera Gerät arbeitet auf einem Strom Adapter.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-223">The camera device is operating on a power adapter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-224">POWERMODE_BATTERY</span><span class="sxs-lookup"><span data-stu-id="4b9f6-224">POWERMODE_BATTERY</span></span></td>
<td><span data-ttu-id="4b9f6-225">Das Kamera Gerät wird mit Akkuleistung betrieben.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-225">The camera device is operating on battery power.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <span data-ttu-id="4b9f6-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>cameradevicebatterystatus</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-227">Der Prozentsatz der Akkukapazität, die für die Arbeit mit dem Kamera Gerät übrig bleibt.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-227">The percentage of battery power that is left to operate the camera device.</span></span> <span data-ttu-id="4b9f6-228">Dieser Wert sollte eine ganze Zahl zwischen 0 und 100 sein.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-228">This value should be an integer from 0 through 100.</span></span> <span data-ttu-id="4b9f6-229">Diese Eigenschaft wird von einer Anwendung gelesen, um die verbleibende Akku Lebensdauer des Kamera Geräts zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-229">An application reads this property to determine the remaining battery life of the camera device.</span></span></p>
<p><span data-ttu-id="4b9f6-230">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-230">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <span data-ttu-id="4b9f6-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>cameradevicethumbwidth</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-232">Die Breite eines Miniatur Bilds, das für neu erfasste Bilder verwendet werden soll, in Pixel.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-232">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="4b9f6-233">Eine Anwendung liest diesen Wert, um eine geschätzte Größe zum Anzeigen von Miniaturansichten in der Benutzeroberfläche zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-233">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="4b9f6-234">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) oder schreibgeschützt (WIA_PROP_NONE), gültige Werte: WIA_PROP_LIST oder WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-234">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <span data-ttu-id="4b9f6-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>cameradevicethumbheight</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-236">Die Breite eines Miniatur Bilds, das für neu erfasste Bilder verwendet werden soll, in Pixel.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-236">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="4b9f6-237">Eine Anwendung liest diesen Wert, um eine geschätzte Größe zum Anzeigen von Miniaturansichten in der Benutzeroberfläche zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-237">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="4b9f6-238">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) oder schreibgeschützt (WIA_PROP_NONE), gültige Werte: WIA_PROP_LIST oder WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-238">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <span data-ttu-id="4b9f6-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>cameradevicepictwidth</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-240">Die Breite in Pixel, die für neu erfasste Bilder verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-240">The width in pixels to use for newly captured images.</span></span> <span data-ttu-id="4b9f6-241">Die Liste gültiger Werte für diese Eigenschaft weist eine eins-zu-eins-Entsprechung zur Liste gültiger Werte für die <strong>WIA_DPC_PICT_HEIGHT</strong> -Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-241">The list of valid values for this property has a one-to-one correspondence to the list of valid values for the <strong>WIA_DPC_PICT_HEIGHT</strong> property.</span></span> <span data-ttu-id="4b9f6-242">Wenn die einzelnen Werte für Breite und Höhe linear feststellbar und orthogonal zueinander stehen, werden Sie möglicherweise als Bereich ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-242">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="4b9f6-243">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-243">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <span data-ttu-id="4b9f6-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>cameradevicepictheight</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-245">Die Höhe in Pixel, die für neu erfasste Bilder verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-245">The height in pixels to use for newly captured images.</span></span> <span data-ttu-id="4b9f6-246">Die Liste gültiger Werte für diese Eigenschaft weist eine eins-zu-eins-Entsprechung mit der Liste gültiger Werte für die <strong>WIA_DPC_PICT_WIDTH</strong> -Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-246">The list of valid values for this property has a one-to-one correspondence with the list of valid values for the <strong>WIA_DPC_PICT_WIDTH</strong> property.</span></span> <span data-ttu-id="4b9f6-247">Wenn die einzelnen Werte für Breite und Höhe linear feststellbar und orthogonal zueinander stehen, werden Sie möglicherweise als Bereich ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-247">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="4b9f6-248">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-248">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <span data-ttu-id="4b9f6-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-250">Reserviert, nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-250">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="4b9f6-251">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-251">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <span data-ttu-id="4b9f6-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>cameradevicecompressionsetting</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-253">Sie sollten in Bezug auf die wahrgenommene Bildqualität für eine breite Palette von Szenen Inhalten ungefähr linear sein, und Sie enthält entweder einen Bereich oder eine Liste mit ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-253">Intended to be approximately linear with respect to perceived image quality over a broad range of scene content, and it contains either a range or a list of integers.</span></span> <span data-ttu-id="4b9f6-254">Kleinere ganze Zahlen werden verwendet, um eine niedrigere Qualität darzustellen (d. h. maximale Komprimierung), wohingegen größere ganze Zahlen verwendet werden, um eine höhere Qualität darzustellen (d. h. minimale Komprimierung).</span><span class="sxs-lookup"><span data-stu-id="4b9f6-254">Smaller integers are used to represent lower quality (that is, maximum compression), whereas larger integers are used to represent higher quality (that is, minimum compression).</span></span> <span data-ttu-id="4b9f6-255">Alle verfügbaren Einstellungen auf einem Gerät sind nur auf dieses Gerät bezogen und sind daher gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-255">Any available settings on a device are relative only to that device and are therefore device specific.</span></span></p>
<p><span data-ttu-id="4b9f6-256">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-256">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <span data-ttu-id="4b9f6-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-258">Reserviert, nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-258">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="4b9f6-259">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-259">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <span data-ttu-id="4b9f6-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>cameradevicetimelapseinterval</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-261">Die Zeitspanne (in Millisekunden) zwischen den Bild Erfassungen in einem Erfassungs Vorgang für einen Zeitablauf.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-261">The time, in milliseconds, between image captures in a time-lapse capture operation.</span></span></p>
<p><span data-ttu-id="4b9f6-262">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-262">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <span data-ttu-id="4b9f6-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>cameradevicetimelapsenum</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-264">Die Anzahl der Images, die das Gerät während einer Zeitverlust Erfassung versucht.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-264">The number of images the device attempts to capture during a time-lapse capture.</span></span></p>
<p><span data-ttu-id="4b9f6-265">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-265">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <span data-ttu-id="4b9f6-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>cameradeviceburstinterval</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-267">Die Zeit (in Millisekunden) zwischen Bild Erfassungen während eines Burst Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-267">The time, in milliseconds, between image captures during a burst operation.</span></span></p>
<p><span data-ttu-id="4b9f6-268">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-268">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <span data-ttu-id="4b9f6-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>cameradeviceburstnumber</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-270">Die Anzahl der Images, die das Gerät während eines Burst Vorgangs erfasst.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-270">The number of images the device attempts to capture during a burst operation.</span></span></p>
<p><span data-ttu-id="4b9f6-271">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-271">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <span data-ttu-id="4b9f6-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>cameradeviceeffectmode</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-273">Gibt den speziellen Bild Erwerbs Modus der Kamera an.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-273">Specifies the special image acquisition mode of the camera.</span></span></p>
<p><span data-ttu-id="4b9f6-274">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-274">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="4b9f6-275">Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-275">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4b9f6-276">Effekt Modus</span><span class="sxs-lookup"><span data-stu-id="4b9f6-276">Effect Mode</span></span></th>
<th><span data-ttu-id="4b9f6-277">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b9f6-277">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b9f6-278">EFFECTMODE_STANDARD</span><span class="sxs-lookup"><span data-stu-id="4b9f6-278">EFFECTMODE_STANDARD</span></span></td>
<td><span data-ttu-id="4b9f6-279">Erfassen eines Bilds im Standardmodus für die Kamera.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-279">Capture an image in the standard mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-280">EFFECTMODE_BW</span><span class="sxs-lookup"><span data-stu-id="4b9f6-280">EFFECTMODE_BW</span></span></td>
<td><span data-ttu-id="4b9f6-281">Erfassen eines Graustufen Bilds.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-281">Capture a grayscale image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b9f6-282">EFFECTMODE_SEPIA</span><span class="sxs-lookup"><span data-stu-id="4b9f6-282">EFFECTMODE_SEPIA</span></span></td>
<td><span data-ttu-id="4b9f6-283">Erfassen Sie ein Image vom Typ "\*".</span><span class="sxs-lookup"><span data-stu-id="4b9f6-283">Capture a sepia image.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <span data-ttu-id="4b9f6-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>cameradevicedigitalzoom</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-285">Das effektive Zoomverhältnis des abgerufenen Images der digitalen Kamera, das um den Faktor 10 skaliert wurde.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-285">The effective zoom ratio of the digital camera's acquired image, scaled by a factor of 10.</span></span> <span data-ttu-id="4b9f6-286">Der Wert 10 entspricht dem Fehlen des digitalen Zoom (1X), der die von der Kamera erfasste Standard Szenengröße ist.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-286">A value of 10 corresponds to the absence of digital zoom (1X), which is the standard scene size captured by the camera.</span></span> <span data-ttu-id="4b9f6-287">Der Wert 20 entspricht einem 2X-Zoom, bei dem ein Viertel der Standard Szenengröße von der Kamera erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-287">A value of 20 corresponds to a 2X zoom, where one-quarter of the standard scene size is captured by the camera.</span></span></p>
<p><span data-ttu-id="4b9f6-288">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-288">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <span data-ttu-id="4b9f6-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>cameradevicesharpness</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-290">Die wahrgenommene Schärfe eines aufgezeichneten Bilds.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-290">The perceived sharpness of a captured image.</span></span> <span data-ttu-id="4b9f6-291">Diese Eigenschaft kann entweder eine Liste von Werten oder einen Wertebereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-291">This property can use either a list of values or a range of values.</span></span> <span data-ttu-id="4b9f6-292">Der minimale Wert stellt die geringste Menge an Schärfe dar, wohingegen der Höchstwert die maximale Schärfe darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-292">The minimum value represents the least amount of sharpness, whereas the maximum value represents the maximum sharpness.</span></span> <span data-ttu-id="4b9f6-293">In der Regel stellt ein Wert in der Mitte des Bereichs normale oder standardmäßige Schärfe dar.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-293">Typically a value in the middle of the range represents normal, or default, sharpness.</span></span></p>
<p><span data-ttu-id="4b9f6-294">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-294">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <span data-ttu-id="4b9f6-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>cameradevicecontrast</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-296">Der erkannte Kontrast eines aufgezeichneten Bilds.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-296">The perceived contrast of a captured image.</span></span> <span data-ttu-id="4b9f6-297">Diese Eigenschaft kann entweder eine Liste mit Werten oder einen Wertebereich enthalten.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-297">This property can contain either a list of values or a range of values.</span></span> <span data-ttu-id="4b9f6-298">Der unterstützte Mindestwert stellt den geringsten Kontrast dar, wohingegen der Höchstwert den meisten Kontrast darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-298">The minimum supported value represents the least amount of contrast, whereas the maximum value represents the most contrast.</span></span> <span data-ttu-id="4b9f6-299">In der Regel stellt ein Wert in der Mitte des Bereichs einen normalen oder einen Standard Kontrast dar.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-299">Typically, a value in the middle of the range represents normal, or default, contrast.</span></span></p>
<p><span data-ttu-id="4b9f6-300">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-300">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <span data-ttu-id="4b9f6-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>cameradevicecapturemode</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-302">Legt den Bild Erfassungs Modus fest.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-302">Sets the image capture mode.</span></span></p>
<p><span data-ttu-id="4b9f6-303">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-303">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="4b9f6-304">Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-304">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4b9f6-305">Aufzeichnungsmodus</span><span class="sxs-lookup"><span data-stu-id="4b9f6-305">Capture Mode</span></span></th>
<th><span data-ttu-id="4b9f6-306">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b9f6-306">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b9f6-307">CAPTUREMODE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="4b9f6-307">CAPTUREMODE_NORMAL</span></span></td>
<td><span data-ttu-id="4b9f6-308">Normaler Modus für die Kamera.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-308">Normal mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-309">CAPTUREMODE_BURST</span><span class="sxs-lookup"><span data-stu-id="4b9f6-309">CAPTUREMODE_BURST</span></span></td>
<td><span data-ttu-id="4b9f6-310">Erfassen Sie mehr als ein Bild in schneller Folge, wie in den Werten der Eigenschaften <strong>WIA_DPC_BURST_NUMBER</strong> und <strong>WIA_DPC_BURST_INTERVAL</strong> definiert.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-310">Capture more than one image in quick succession as defined by the values of the <strong>WIA_DPC_BURST_NUMBER</strong> and <strong>WIA_DPC_BURST_INTERVAL</strong> properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b9f6-311">CAPTUREMODE_TIMELAPSE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-311">CAPTUREMODE_TIMELAPSE</span></span></td>
<td><span data-ttu-id="4b9f6-312">Erfassen Sie mehr als ein Bild nacheinander, wie in den Eigenschaften <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> und <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> definiert.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-312">Capture more than one image in succession as defined by the <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> properties.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <span data-ttu-id="4b9f6-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>cameradevicecapturedelay</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-314">Der-Wert, der die Verzögerung in Millisekunden darstellt, die zwischen dem Erfassungs-und der tatsächlichen Initiierung der Datenerfassung eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-314">The value representing the amount of time delay, in milliseconds, that should be inserted between the capture trigger and the actual initiation of the data capture.</span></span> <span data-ttu-id="4b9f6-315">Diese Eigenschaft ist nicht für die Beschreibung der Zeit zwischen Frames für die Einzel Initiierung gedacht, mehrere Erfassungen, wie z. b. Burst oder Zeitwert, die separate Intervall Eigenschaften <strong>WIA_DPC_BURST_INTERVAL</strong> und <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>haben.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-315">This property is not intended to be used to describe the time between frames for single-initiation, multiple captures such as burst or time lapse, which have separate interval properties <strong>WIA_DPC_BURST_INTERVAL</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>.</span></span> <span data-ttu-id="4b9f6-316">In diesen Fällen dient sie immer noch als anfängliche Verzögerung, bevor das erste Bild in der Reihe unabhängig von der Zeit zwischen Frames erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-316">In those cases, it still serves as an initial delay before the first image in the series is captured, independent of the time between frames.</span></span> <span data-ttu-id="4b9f6-317">Für keine vorab Aufzeichnungs Verzögerung sollte diese Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-317">For no precapture delay, this property should be set to zero.</span></span></p>
<p><span data-ttu-id="4b9f6-318">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-318">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <span data-ttu-id="4b9f6-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>cameradeviceexposureindex</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-320">Ermöglicht die Emulation von Einstellungen für die Filmgeschwindigkeit auf einer digitalen Kamera.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-320">Allows for the emulation of film speed settings on a digital camera.</span></span> <span data-ttu-id="4b9f6-321">Die Einstellungen entsprechen den ISO-Bezeichnungen (ASA/DIN).</span><span class="sxs-lookup"><span data-stu-id="4b9f6-321">The settings correspond to the ISO designations (ASA/DIN).</span></span> <span data-ttu-id="4b9f6-322">In der Regel unterstützt ein Gerät diskrete Enumerationswerte, aber eine kontinuierliche Kontrolle über einen Wertebereich ist möglich.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-322">Typically, a device supports discrete enumerated values, but continuous control over a range of values is possible.</span></span> <span data-ttu-id="4b9f6-323">Der Wert 0xFFFF entspricht der automatischen ISO-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-323">A value of 0xFFFF corresponds to the Automatic ISO setting.</span></span></p>
<p><span data-ttu-id="4b9f6-324">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-324">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <span data-ttu-id="4b9f6-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>cameradeviceexposuremeteringmode</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-326">Gibt den Modus an, den die Kamera zum automatischen Anpassen der Einstellung für die Festlegung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-326">Specifies the mode the camera uses to automatically adjust the exposure setting.</span></span></p>
<p><span data-ttu-id="4b9f6-327">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-327">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4b9f6-328">Expositions Messungs Modus</span><span class="sxs-lookup"><span data-stu-id="4b9f6-328">Exposure Metering Mode</span></span></th>
<th><span data-ttu-id="4b9f6-329">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b9f6-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b9f6-330">EXPOSUREMETERING_AVERAGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-330">EXPOSUREMETERING_AVERAGE</span></span></td>
<td><span data-ttu-id="4b9f6-331">Legen Sie die Festlegung auf Grundlage eines Durchschnitts der gesamten Szene fest.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-331">Set the exposure based on an average of the entire scene.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-332">EXPOSUREMETERING_CENTERWEIGHT</span><span class="sxs-lookup"><span data-stu-id="4b9f6-332">EXPOSUREMETERING_CENTERWEIGHT</span></span></td>
<td><span data-ttu-id="4b9f6-333">Legen Sie die Verfügbarkeit basierend auf einem Mittel gewichteten Durchschnitt fest.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-333">Set the exposure based on a center-weighted average.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b9f6-334">EXPOSUREMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="4b9f6-334">EXPOSUREMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="4b9f6-335">Legen Sie die Verfügbarkeit basierend auf einem multiSpot-Muster fest.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-335">Set the exposure based on a multispot pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-336">EXPOSUREMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="4b9f6-336">EXPOSUREMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="4b9f6-337">Legen Sie die Verfügbarkeit basierend auf einem Mittelpunkt fest.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-337">Set the exposure based on a center spot.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <span data-ttu-id="4b9f6-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>cameradevicefocemeteringmode</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-339">Gibt den Modus an, den die Kamera zum automatischen Anpassen des Fokus verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-339">Specifies the mode the camera uses to automatically adjust the focus.</span></span></p>
<p><span data-ttu-id="4b9f6-340">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-340">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="4b9f6-341">Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-341">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4b9f6-342">Fokus Messungs Modus</span><span class="sxs-lookup"><span data-stu-id="4b9f6-342">Focus Metering Mode</span></span></th>
<th><span data-ttu-id="4b9f6-343">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b9f6-343">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b9f6-344">FOCUSMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="4b9f6-344">FOCUSMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="4b9f6-345">Passen Sie den Fokus auf der Grundlage eines Mittelpunkts an.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-345">Adjust the focus based on a center spot.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-346">FOCUSMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="4b9f6-346">FOCUSMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="4b9f6-347">Passen Sie den Fokus basierend auf einem multiSpot-Muster an.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-347">Adjust the focus based on a multispot pattern.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <span data-ttu-id="4b9f6-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>cameradevicefocudistance</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-349">Der Abstand zwischen der Bild Erfassungs Ebene der digitalen Kamera und dem Punkt des Fokus in Millimeter.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-349">The distance, in millimeters, between the image-capturing plane of the digital camera and the point of focus.</span></span> <span data-ttu-id="4b9f6-350">Der Wert 0xFFFF entspricht einer Einstellung größer als 655 Meter.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-350">A value of 0xFFFF corresponds to a setting greater than 655 meters.</span></span></p>
<p><span data-ttu-id="4b9f6-351">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="4b9f6-351">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <span data-ttu-id="4b9f6-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>cameradevicefocallength</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-353">Die 35-mm-äquivalente Fokuslänge.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-353">The 35mm-equivalent focal length.</span></span> <span data-ttu-id="4b9f6-354">Die Werte dieser Eigenschaft entsprechen der Fokuslänge in Millimeter multipliziert mit 100.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-354">The values of this property correspond to the focal length in millimeters multiplied by 100.</span></span> <span data-ttu-id="4b9f6-355">Die Fokuslänge bestimmt den optischen Zoomfaktor.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-355">The focal length determines the optical zoom.</span></span></p>
<p><span data-ttu-id="4b9f6-356">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-356">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <span data-ttu-id="4b9f6-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>cameradevicergbgewinn</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-358">Eine auf NULL endende Unicode-Zeichenfolge, die den roten, grünen und blauen Gewinn darstellt, der auf Bilddaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-358">A null-terminated Unicode string that represents the red, green, and blue gain applied to image data, respectively.</span></span> <span data-ttu-id="4b9f6-359">&quot;4:25:50 &quot; stellt z. b. einen roten Gewinn von 4, einen grünen Gewinn von 25 und einen blauen Gewinn von 50 dar.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-359">For example, &quot;4:25:50&quot; represents a red gain of 4, a green gain of 25, and a blue gain of 50.</span></span></p>
<p><span data-ttu-id="4b9f6-360">Typ: <strong>VT_BSTR</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-360">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <span data-ttu-id="4b9f6-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>cameradevicewhitebalance</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-362">Gibt an, wie die digitale Kamera Farbkanäle gewichtet.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-362">Specifies how the digital camera weights color channels.</span></span></p>
<p><span data-ttu-id="4b9f6-363">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-363">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="4b9f6-364">Im folgenden finden Sie eine Liste möglicher Werte für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-364">The following is a list of possible values for this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4b9f6-365">Weiß Saldo</span><span class="sxs-lookup"><span data-stu-id="4b9f6-365">White Balance</span></span></th>
<th><span data-ttu-id="4b9f6-366">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b9f6-366">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b9f6-367">WHITEBALANCE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="4b9f6-367">WHITEBALANCE_MANUAL</span></span></td>
<td><span data-ttu-id="4b9f6-368">Der weiße Saldo wird direkt mithilfe der <strong>WIA_DPC_RGB_GAIN</strong> -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-368">The white balance is set directly using the <strong>WIA_DPC_RGB_GAIN</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-369">WHITEBALANCE_AUTO</span><span class="sxs-lookup"><span data-stu-id="4b9f6-369">WHITEBALANCE_AUTO</span></span></td>
<td><span data-ttu-id="4b9f6-370">Die Kamera verwendet einen automatischen Mechanismus, um den weißen Saldo festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-370">The camera uses an automatic mechanism to set the white balance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b9f6-371">WHITEBALANCE_ONEPUSH_AUTO</span><span class="sxs-lookup"><span data-stu-id="4b9f6-371">WHITEBALANCE_ONEPUSH_AUTO</span></span></td>
<td><span data-ttu-id="4b9f6-372">Die Kamera bestimmt die Einstellung für das weiße Gleichgewicht, wenn ein Benutzer die Erfassungs Schaltfläche drückt, während er auf eine weiße Oberfläche zeigt.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-372">The camera determines the white balance setting when a user presses the capture button while pointing the camera at a white surface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-373">WHITEBALANCE_DAYLIGHT</span><span class="sxs-lookup"><span data-stu-id="4b9f6-373">WHITEBALANCE_DAYLIGHT</span></span></td>
<td><span data-ttu-id="4b9f6-374">Die Kamera legt den weißen Saldo auf einen Wert fest, der für die Verwendung in Sommerzeit Bedingungen geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-374">The camera sets the white balance to a value appropriate for use in daylight conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b9f6-375">WHITEBALANCE_FLORESCENT</span><span class="sxs-lookup"><span data-stu-id="4b9f6-375">WHITEBALANCE_FLORESCENT</span></span></td>
<td><span data-ttu-id="4b9f6-376">Die Kamera legt den weißen Saldo auf einen Wert fest, der für die Verwendung mit einer Leuchtstoff Quelle geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-376">The camera sets the white balance to a value appropriate for use with a fluorescent light source.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b9f6-377">WHITEBALANCE_TUNGSTEN</span><span class="sxs-lookup"><span data-stu-id="4b9f6-377">WHITEBALANCE_TUNGSTEN</span></span></td>
<td><span data-ttu-id="4b9f6-378">Die Kamera legt den weißen Saldo auf einen Wert fest, der für die Verwendung mit einer Wolfram-Light-Quelle geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-378">The camera sets the white balance to a value appropriate for use with a tungsten light source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b9f6-379">WHITEBALANCE_FLASH</span><span class="sxs-lookup"><span data-stu-id="4b9f6-379">WHITEBALANCE_FLASH</span></span></td>
<td><span data-ttu-id="4b9f6-380">Die Kamera legt den weißen Saldo auf einen Wert fest, der für die Verwendung mit einem elektronischen Flash geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-380">The camera sets the white balance to a value appropriate for use with an electronic flash.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <span data-ttu-id="4b9f6-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>cameradeviceuploadurl</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-382">Beschreibt eine URL.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-382">Describes a URL.</span></span> <span data-ttu-id="4b9f6-383">Die URL, die von diesem Anteils Operator beschrieben wird, ist eine, die Bilder oder Objekte, nachdem Sie vom Gerät abgerufen wurden, nach einem der folgenden Szenarien in – hochgeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-383">The URL described by this proroperty is one that images or objects, after they are acquired from the device, can be uploaded to—according to one of the following scenarios.</span></span></p>
<ul>
<li><span data-ttu-id="4b9f6-384">Eine WIA-Anwendung liest diese Eigenschaft und ermöglicht dem Benutzer das automatische Hochladen von Bildern in die URL.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-384">A WIA application reads this property and allows the user to automatically upload images to the URL.</span></span></li>
<li><span data-ttu-id="4b9f6-385">Eine Anwendung legt die URL fest, und andere Geräte (Kiosk usw.) verwenden diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-385">An application sets the URL, and other devices (kiosks and so forth) use this property.</span></span></li>
</ul>
<p><span data-ttu-id="4b9f6-386">Microsoft Windows lädt Bilder nicht allein hoch.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-386">Microsoft Windows does not upload images by itself.</span></span></p>
<p><span data-ttu-id="4b9f6-387">Typ: <strong>VT_BSTR</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-387">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <span data-ttu-id="4b9f6-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>cameradeviceartist</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-389">Der Name des Besitzers (der der aktuelle Benutzer ist) des Geräts.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-389">The name of the owner ( which is the current user) of the device.</span></span> <span data-ttu-id="4b9f6-390">Das Gerät verwendet diese Eigenschaft, um das Feld "Artist" in jedem von ihm erfassten EXIF-Bild aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-390">The device uses this property to populate the Artist field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="4b9f6-391">Typ: <strong>VT_BSTR</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-391">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <span data-ttu-id="4b9f6-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>cameradevicecopyrightinfo</dt> </span><span class="sxs-lookup"><span data-stu-id="4b9f6-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4b9f6-393">Die Copyright Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-393">The copyright notification.</span></span> <span data-ttu-id="4b9f6-394">Das Gerät verwendet diese Eigenschaft, um das Feld "Copyright" in jedem von ihm erfassten Exif-Image aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="4b9f6-394">The device uses this property to populate the Copyright field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="4b9f6-395">Typ: <strong>VT_BSTR</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4b9f6-395">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="4b9f6-396">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b9f6-396">Requirements</span></span>



| <span data-ttu-id="4b9f6-397">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b9f6-397">Requirement</span></span> | <span data-ttu-id="4b9f6-398">Wert</span><span class="sxs-lookup"><span data-stu-id="4b9f6-398">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9f6-399">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b9f6-399">Minimum supported client</span></span><br/> | <span data-ttu-id="4b9f6-400">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b9f6-400">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4b9f6-401">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b9f6-401">Minimum supported server</span></span><br/> | <span data-ttu-id="4b9f6-402">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b9f6-402">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4b9f6-403">Header</span><span class="sxs-lookup"><span data-stu-id="4b9f6-403">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b9f6-404"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b9f6-404"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




