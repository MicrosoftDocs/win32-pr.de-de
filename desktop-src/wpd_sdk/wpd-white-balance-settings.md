---
description: Der \_ Enumerationstyp für WPD-White \_ Balance- \_ Einstellungen beschreibt, wie ein Video-oder Bild-Gerät Farbkanäle gewichtet, um einen geeigneten weißen Saldo zu erzielen
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: WPD_WHITE_BALANCE_SETTINGS-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 06e607acc06ed00cc9fe91670650caee44c30430
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372344"
---
# <a name="wpd_white_balance_settings-enumeration"></a><span data-ttu-id="635aa-103">WPD \_ - \_ Enumeration für weiß Balance- \_ Einstellungen</span><span class="sxs-lookup"><span data-stu-id="635aa-103">WPD\_WHITE\_BALANCE\_SETTINGS enumeration</span></span>

<span data-ttu-id="635aa-104">Der Enumerationstyp für **WPD- \_ White \_ Balance- \_ Einstellungen** beschreibt, wie ein Video-oder Bild-Gerät Farbkanäle gewichtet, um einen geeigneten weißen Saldo zu erzielen</span><span class="sxs-lookup"><span data-stu-id="635aa-104">The **WPD\_WHITE\_BALANCE\_SETTINGS** enumeration type describes how a video or image device weights color channels to achieve a proper white balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="635aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="635aa-105">Syntax</span></span>


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="635aa-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="635aa-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="635aa-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**WPD- \_ weißen \_ Saldo nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="635aa-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**WPD\_WHITE\_BALANCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="635aa-108">Dieser Wert wurde nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="635aa-108">This value has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="635aa-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD \_ - \_ WhiteBalance \_ manuell**</span><span class="sxs-lookup"><span data-stu-id="635aa-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD\_WHITE\_BALANCE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="635aa-110">Der weiße Saldo wird explizit mit der-Eigenschaft für den Bild-und Bild-Wert von WPD festgelegt und wird nicht selbst geändert. [ \_ \_ \_ \_ ](still-image-properties.md)</span><span class="sxs-lookup"><span data-stu-id="635aa-110">The white balance is set explicitly by using the [WPD\_STILL\_IMAGE\_RGB\_GAIN](still-image-properties.md) property and will not change by itself.</span></span>

</dd> <dt>

<span data-ttu-id="635aa-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**WPD- \_ weiß- \_ Ausgleich \_ automatisch**</span><span class="sxs-lookup"><span data-stu-id="635aa-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**WPD\_WHITE\_BALANCE\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="635aa-112">Das Gerät legt den weißen Saldo fest.</span><span class="sxs-lookup"><span data-stu-id="635aa-112">The device will set the white balance.</span></span>

</dd> <dt>

<span data-ttu-id="635aa-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD- \_ weiß- \_ Ausgleich \_ 1 \_ Push \_ automatisch**</span><span class="sxs-lookup"><span data-stu-id="635aa-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD\_WHITE\_BALANCE\_ONE\_PUSH\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="635aa-114">Das Gerät legt den weißen Saldo fest, aber nur, wenn der Benutzer die Erfassungs Schaltfläche des Geräts drückt, während er das Gerät in einem weißen Feld anzielt.</span><span class="sxs-lookup"><span data-stu-id="635aa-114">The device will set the white balance, but only when the user pushes the device's capture button while aiming the device at a white field.</span></span>

</dd> <dt>

<span data-ttu-id="635aa-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD \_ weiß \_ Balance- \_ Sommerzeit**</span><span class="sxs-lookup"><span data-stu-id="635aa-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD\_WHITE\_BALANCE\_DAYLIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="635aa-116">Auf dem Gerät werden die in den meisten Sommerzeit Einstellungen geeigneten weißen Ausgleichs Nummern verwendet.</span><span class="sxs-lookup"><span data-stu-id="635aa-116">The device will use white balance numbers appropriate for use in most daylight settings.</span></span>

</dd> <dt>

<span data-ttu-id="635aa-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD- \_ weiß \_ Balance- \_ Wolfram**</span><span class="sxs-lookup"><span data-stu-id="635aa-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD\_WHITE\_BALANCE\_TUNGSTEN**</span></span>
</dt> <dd>

<span data-ttu-id="635aa-118">Auf dem Gerät werden die in den meisten Umgebungen für das Incandescent-Beleuchtungs Verfahren verwendeten weißen Ausgleichs Nummern verwendet.</span><span class="sxs-lookup"><span data-stu-id="635aa-118">The device will use white balance numbers appropriate for use in most indoor, incandescent lighting settings.</span></span>

</dd> <dt>

<span data-ttu-id="635aa-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD- \_ weiß \_ Balance \_ Flash**</span><span class="sxs-lookup"><span data-stu-id="635aa-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD\_WHITE\_BALANCE\_FLASH**</span></span>
</dt> <dd>

<span data-ttu-id="635aa-120">Auf dem Gerät werden die für die Verwendung mit einem Flash geeigneten weißen Ausgleichs Nummern verwendet.</span><span class="sxs-lookup"><span data-stu-id="635aa-120">The device will use white balance numbers appropriate for use with a flash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="635aa-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="635aa-121">Remarks</span></span>

<span data-ttu-id="635aa-122">Diese Enumeration wird von der WPD-Eigenschaft für den [ \_ \_ \_ weißen \_ Saldo weiterhin](still-image-properties.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="635aa-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_WHITE\_BALANCE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="635aa-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="635aa-123">Requirements</span></span>



| <span data-ttu-id="635aa-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="635aa-124">Requirement</span></span> | <span data-ttu-id="635aa-125">Wert</span><span class="sxs-lookup"><span data-stu-id="635aa-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="635aa-126">Header</span><span class="sxs-lookup"><span data-stu-id="635aa-126">Header</span></span><br/> | <dl> <span data-ttu-id="635aa-127"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="635aa-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="635aa-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="635aa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="635aa-129">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="635aa-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




