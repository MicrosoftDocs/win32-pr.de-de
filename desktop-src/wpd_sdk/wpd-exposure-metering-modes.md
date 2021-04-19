---
description: Der \_ \_ Enumerationstyp der WPD-aufgabenmessungs- \_ Modi beschreibt den Messungs Modus, der verwendet werden soll, wenn die Verfügbarkeit der Bild Erfassung durch ein Gerät
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: WPD_EXPOSURE_METERING_MODES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370132"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a><span data-ttu-id="907b6-103">Enumeration der WPD- \_ Expositions \_ Messungs \_ Modi</span><span class="sxs-lookup"><span data-stu-id="907b6-103">WPD\_EXPOSURE\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="907b6-104">Der Enumerationstyp der **WPD-aufgabenmessungs- \_ \_ \_ Modi** beschreibt den Messungs Modus, der verwendet werden soll, wenn die Verfügbarkeit der Bild Erfassung durch ein Gerät</span><span class="sxs-lookup"><span data-stu-id="907b6-104">The **WPD\_EXPOSURE\_METERING\_MODES** enumeration type describes the metering mode to use when estimating exposure for still image capture by a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="907b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="907b6-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="907b6-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="907b6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="907b6-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**WPD \_ - \_ \_ aufwirkungs Messungs Modus nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="907b6-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**WPD\_EXPOSURE\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="907b6-108">Der Messungs Modus ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="907b6-108">The metering mode is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="907b6-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**Durchschnitt des WPD- \_ Expositions \_ Messungs \_ Modus \_**</span><span class="sxs-lookup"><span data-stu-id="907b6-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="907b6-110">Verwenden Sie die durchschnittliche Verfügbarkeit im gesamten Image.</span><span class="sxs-lookup"><span data-stu-id="907b6-110">Use averaged exposure across the full image.</span></span>

</dd> <dt>

<span data-ttu-id="907b6-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**mittlere Mittelwert des WPD- \_ Expositions \_ Messungs \_ Modus \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="907b6-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_WEIGHTED\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="907b6-112">Verwenden Sie eine durchschnittliche Verfügbarkeit, bei der der Mittelpunkt des Bilds stärker gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="907b6-112">Use an averaged exposure, with the center of the image given more weight.</span></span>

</dd> <dt>

<span data-ttu-id="907b6-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**multiSpot für den WPD- \_ Expositions \_ Messungs \_ Modus \_ \_**</span><span class="sxs-lookup"><span data-stu-id="907b6-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="907b6-114">Verwenden Sie eine mehrstufige Mittelpunkt Technik.</span><span class="sxs-lookup"><span data-stu-id="907b6-114">Use a multi-spot averaging technique.</span></span>

</dd> <dt>

<span data-ttu-id="907b6-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**Mittelpunkt des WPD- \_ Expositions \_ Messungs \_ Modus \_ \_**</span><span class="sxs-lookup"><span data-stu-id="907b6-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="907b6-116">Verwenden Sie eine Mittelpunkt-Mittelpunkt Technik.</span><span class="sxs-lookup"><span data-stu-id="907b6-116">Use a center-spot averaging technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="907b6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="907b6-117">Remarks</span></span>

<span data-ttu-id="907b6-118">Gibt den Messungs Modus des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="907b6-118">Indicates the metering mode of the device.</span></span> <span data-ttu-id="907b6-119">Diese Enumeration wird von der WPD-Eigenschaft für die Aufzählungs [ \_ \_ \_ \_ \_ Messung des Bilds](still-image-properties.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="907b6-119">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="907b6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="907b6-120">Requirements</span></span>



| <span data-ttu-id="907b6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="907b6-121">Requirement</span></span> | <span data-ttu-id="907b6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="907b6-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="907b6-123">Header</span><span class="sxs-lookup"><span data-stu-id="907b6-123">Header</span></span><br/> | <dl> <span data-ttu-id="907b6-124"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="907b6-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="907b6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="907b6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="907b6-126">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="907b6-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




