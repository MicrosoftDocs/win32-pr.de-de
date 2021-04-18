---
description: Der \_ \_ \_ Enumerationstyp der WPD-aufgabenprogrammebeschreibt einen Bereitstellungs Modus, der beim Erfassen von Bildern mit einem Gerät verwendet werden
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: WPD_EXPOSURE_PROGRAM_MODES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a88ce90bb9e776cd45245b32a363635c2ccf0560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372101"
---
# <a name="wpd_exposure_program_modes-enumeration"></a><span data-ttu-id="29235-103">WPD \_ - \_ \_ Aufzählungs Programmmodi-Enumeration</span><span class="sxs-lookup"><span data-stu-id="29235-103">WPD\_EXPOSURE\_PROGRAM\_MODES enumeration</span></span>

<span data-ttu-id="29235-104">Der Enumerationstyp der WPD-aufgabenprogrammebeschreibt einen Bereitstellungs Modus, der beim Erfassen von Bildern mit einem Gerät verwendet werden **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="29235-104">The **WPD\_EXPOSURE\_PROGRAM\_MODES** enumeration type describes an exposure mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="29235-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="29235-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="29235-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="29235-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="29235-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**WPD \_ - \_ renderingprogrammmodus nicht \_ \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="29235-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="29235-108">Der Anzeigemodus wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="29235-108">The exposure mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="29235-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**WPD \_ - \_ \_ aufstellungsprogrammmodus \_ manuell**</span><span class="sxs-lookup"><span data-stu-id="29235-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="29235-110">Die Anwendung sollte alle Einstellungen für das verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="29235-110">The application should specify all exposure settings.</span></span>

</dd> <dt>

<span data-ttu-id="29235-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**WPD \_ - \_ \_ aufwirkungs Programmmodus \_ automatisch**</span><span class="sxs-lookup"><span data-stu-id="29235-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="29235-112">Verwenden Sie einen Geräte definierten automatischen Funktionsmodus.</span><span class="sxs-lookup"><span data-stu-id="29235-112">Use a device-defined automatic exposure mode.</span></span>

</dd> <dt>

<span data-ttu-id="29235-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**Öffnungs Priorität des WPD- \_ \_ renderingprogrammmodus \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="29235-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_APERTURE\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="29235-114">Ein automatisierter Anzeigemodus, der angibt, dass der Wert für die lichtöffnung festgelegt bleiben soll, aber die Auswertungs Geschwindigkeit vom Gerät bestimmt werden soll.</span><span class="sxs-lookup"><span data-stu-id="29235-114">An automated exposure mode that indicates that the lens aperture value should remain fixed, but shutter speed should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="29235-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**Auslöse Priorität für den WPD- \_ \_ auflockprogrammmodus \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="29235-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_SHUTTER\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="29235-116">Ein automatisierter Anzeigemodus, der angibt, dass die Auslösegeschwindigkeit korrigiert bleiben soll, diese aber vom Gerät bestimmt werden soll.</span><span class="sxs-lookup"><span data-stu-id="29235-116">An automated exposure mode that indicates that the shutter speed should remain fixed, but that lens aperture should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="29235-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD \_ - \_ renderingprogrammmodus- \_ \_ kreativ**</span><span class="sxs-lookup"><span data-stu-id="29235-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_CREATIVE**</span></span>
</dt> <dd>

<span data-ttu-id="29235-118">Ein automatisierter Anzeigemodus, der versucht, die Tiefe des Felds zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="29235-118">An automated exposure mode that tries to maximize the depth of field.</span></span>

</dd> <dt>

<span data-ttu-id="29235-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**Aktion für den WPD-aufwirkungs \_ \_ Programm \_ Modus \_**</span><span class="sxs-lookup"><span data-stu-id="29235-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_ACTION**</span></span>
</dt> <dd>

<span data-ttu-id="29235-120">Ein automatisierter Anzeigemodus, der versucht, die Auslösegeschwindigkeit zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="29235-120">An automated exposure mode that tries to maximize the shutter speed.</span></span>

</dd> <dt>

<span data-ttu-id="29235-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**Hochformat des WPD- \_ \_ \_ aufwirkungs Programms \_**</span><span class="sxs-lookup"><span data-stu-id="29235-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_PORTRAIT**</span></span>
</dt> <dd>

<span data-ttu-id="29235-122">Ein automatisierter Anzeigemodus, der eine relativ flache Tiefe von Feldern angibt.</span><span class="sxs-lookup"><span data-stu-id="29235-122">An automated exposure mode that specifies a relatively shallow depth of field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29235-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29235-123">Remarks</span></span>

<span data-ttu-id="29235-124">Gibt den aufgeräteregistrierungs Modus des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="29235-124">Indicates the exposure program mode of the device.</span></span> <span data-ttu-id="29235-125">Diese Enumeration wird von der WPD-Eigenschaft zum [ \_ \_ \_ \_ renderingprogrammmodus \_ weiterhin](still-image-properties.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="29235-125">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_PROGRAM\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="29235-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29235-126">Requirements</span></span>



| <span data-ttu-id="29235-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29235-127">Requirement</span></span> | <span data-ttu-id="29235-128">Wert</span><span class="sxs-lookup"><span data-stu-id="29235-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="29235-129">Header</span><span class="sxs-lookup"><span data-stu-id="29235-129">Header</span></span><br/> | <dl> <span data-ttu-id="29235-130"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="29235-130"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29235-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29235-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29235-132">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="29235-132">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




