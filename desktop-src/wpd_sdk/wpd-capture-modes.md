---
description: Der \_ Enumerationstyp des WPD-Erfassungs \_ Modus beschreibt den Erfassungs Zeit Steuerungs Modus einer immer noch Abbild Erfassung.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: WPD_CAPTURE_MODES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356406"
---
# <a name="wpd_capture_modes-enumeration"></a><span data-ttu-id="7a560-103">WPD- \_ Erfassungs \_ Modi-Enumeration</span><span class="sxs-lookup"><span data-stu-id="7a560-103">WPD\_CAPTURE\_MODES enumeration</span></span>

<span data-ttu-id="7a560-104">Der Enumerationstyp des **WPD- \_ Erfassungs \_** Modus beschreibt den Erfassungs Zeit Steuerungs Modus einer immer noch Abbild Erfassung.</span><span class="sxs-lookup"><span data-stu-id="7a560-104">The **WPD\_CAPTURE\_MODES** enumeration type describes the capture timing mode of a still image capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a560-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a560-105">Syntax</span></span>


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="7a560-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="7a560-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7a560-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**WPD- \_ Erfassungs \_ Modus nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="7a560-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**WPD\_CAPTURE\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="7a560-108">Der Erfassungs Modus wurde nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="7a560-108">The capture mode has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="7a560-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**WPD- \_ Erfassungs \_ Modus \_ Normal**</span><span class="sxs-lookup"><span data-stu-id="7a560-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**WPD\_CAPTURE\_MODE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="7a560-110">Es sollte keine Verzögerung oder kein Burst Modus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a560-110">No delay or burst mode should be used.</span></span>

</dd> <dt>

<span data-ttu-id="7a560-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**Burst für WPD- \_ Erfassungs \_ Modus \_**</span><span class="sxs-lookup"><span data-stu-id="7a560-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**WPD\_CAPTURE\_MODE\_BURST**</span></span>
</dt> <dd>

<span data-ttu-id="7a560-112">Gibt an, dass eine definierte Anzahl von Bildern mit einem definierten Intervall zwischen Ihnen aufgezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a560-112">Specifies that a defined number of images should be captured with a defined interval between them.</span></span> <span data-ttu-id="7a560-113">Die Anzahl der zu erfassenden Abbilder und die Zeitverzögerung zwischen Ihnen werden von der [WPD- \_ Image- \_ \_ Burst \_ Nummer](still-image-properties.md) und der WPD-Eigenschaft für das [ \_ \_ \_ Burst \_ Intervall](still-image-properties.md) für Images angegeben.</span><span class="sxs-lookup"><span data-stu-id="7a560-113">The number of images to capture and time delay between them are specified by the [WPD\_STILL\_IMAGE\_BURST\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_BURST\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="7a560-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**WPD- \_ Erfassungs \_ Modus ( \_ Timelapse)**</span><span class="sxs-lookup"><span data-stu-id="7a560-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**WPD\_CAPTURE\_MODE\_TIMELAPSE**</span></span>
</dt> <dd>

<span data-ttu-id="7a560-115">Die Abbild Erfassung sollte Zeitverlaufs Fotos verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a560-115">Image capture should use time lapse photography.</span></span> <span data-ttu-id="7a560-116">Die Anzahl der Abbilder und des Intervalls zwischen Ihnen wird von der [WPD- \_ Anzahl der nach wie vor \_ Abbild- \_ \_ Timelapse](still-image-properties.md) und von WPD-Eigenschaften für das Zeit [ \_ \_ \_ \_ Intervall Image](still-image-properties.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7a560-116">The number of images and interval between them are described by the [WPD\_STILL\_IMAGE\_TIMELAPSE\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_TIMELAPSE\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a560-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a560-117">Remarks</span></span>

<span data-ttu-id="7a560-118">Diese Enumeration wird von der WPD-Eigenschaft für die [ \_ \_ Image \_ Erfassungs \_ Modus](still-image-properties.md) -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a560-118">This enumeration is used by the [WPD\_STILL\_IMAGE\_CAPTURE\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a560-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a560-119">Requirements</span></span>



| <span data-ttu-id="7a560-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a560-120">Requirement</span></span> | <span data-ttu-id="7a560-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7a560-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a560-122">Header</span><span class="sxs-lookup"><span data-stu-id="7a560-122">Header</span></span><br/> | <dl> <span data-ttu-id="7a560-123"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a560-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a560-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a560-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a560-125">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="7a560-125">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="7a560-126">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="7a560-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




