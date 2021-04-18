---
description: Der \_ Enumerationstyp der WPD-Flash \_ Modi beschreibt einen Flash Modus, der beim Erfassen von Bildern mit einem Gerät verwendet werden soll.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: WPD_FLASH_MODES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372100"
---
# <a name="wpd_flash_modes-enumeration"></a><span data-ttu-id="b005b-103">WPD- \_ Flash \_ Modi-Enumeration</span><span class="sxs-lookup"><span data-stu-id="b005b-103">WPD\_FLASH\_MODES enumeration</span></span>

<span data-ttu-id="b005b-104">Der Enumerationstyp der **WPD- \_ Flash \_ Modi** beschreibt einen Flash Modus, der beim Erfassen von Bildern mit einem Gerät verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b005b-104">The **WPD\_FLASH\_MODES** enumeration type describes a flash mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b005b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b005b-105">Syntax</span></span>


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="b005b-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b005b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b005b-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**WPD- \_ Flash \_ Modus nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="b005b-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**WPD\_FLASH\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="b005b-108">Es wurde kein Flash-Modus angegeben.</span><span class="sxs-lookup"><span data-stu-id="b005b-108">No flash mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="b005b-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**WPD- \_ Flash \_ Modus \_ automatisch**</span><span class="sxs-lookup"><span data-stu-id="b005b-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**WPD\_FLASH\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="b005b-110">Gibt an, dass der Flash im automatischen Modus verwendet werden soll, wie vom Gerät angegeben.</span><span class="sxs-lookup"><span data-stu-id="b005b-110">Specifies that the flash should be used in the automatic mode, as specified by the device.</span></span>

</dd> <dt>

<span data-ttu-id="b005b-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**WPD- \_ Flash \_ Modus \_ Off**</span><span class="sxs-lookup"><span data-stu-id="b005b-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**WPD\_FLASH\_MODE\_OFF**</span></span>
</dt> <dd>

<span data-ttu-id="b005b-112">Gibt an, dass kein Flash verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b005b-112">Specifies that no flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="b005b-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**Füllung des WPD- \_ Flash \_ Modus \_**</span><span class="sxs-lookup"><span data-stu-id="b005b-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**WPD\_FLASH\_MODE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="b005b-114">Gibt einen Flash Füll Typ an.</span><span class="sxs-lookup"><span data-stu-id="b005b-114">Specifies a fill-type flash.</span></span>

</dd> <dt>

<span data-ttu-id="b005b-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD- \_ Flash \_ Modus " \_ Red \_ Eye \_ Auto"**</span><span class="sxs-lookup"><span data-stu-id="b005b-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="b005b-116">Gibt an, dass die rote Augen Reduzierungs-Flash verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b005b-116">Specifies that the red eye reduction flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="b005b-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**\_ \_ \_ Red \_ Eye \_ Fill im WPD-Flash Modus**</span><span class="sxs-lookup"><span data-stu-id="b005b-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="b005b-118">Gibt an, dass der Rote Augen Füll Blitz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b005b-118">Specifies that the red eye fill flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="b005b-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**\_ \_ \_ externe \_ Synchronisierung im WPD-Flash Modus**</span><span class="sxs-lookup"><span data-stu-id="b005b-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**WPD\_FLASH\_MODE\_EXTERNAL\_SYNC**</span></span>
</dt> <dd>

<span data-ttu-id="b005b-120">Gibt an, dass der Flash mit anderen externen Flash Geräten synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b005b-120">Specifies that the flash should be synchronized with other external flash devices.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b005b-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b005b-121">Remarks</span></span>

<span data-ttu-id="b005b-122">Diese Enumeration wird von der [WPD- \_ \_ Image- \_ Flash \_ Mode](still-image-properties.md) -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="b005b-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_FLASH\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b005b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b005b-123">Requirements</span></span>



| <span data-ttu-id="b005b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b005b-124">Requirement</span></span> | <span data-ttu-id="b005b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b005b-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b005b-126">Header</span><span class="sxs-lookup"><span data-stu-id="b005b-126">Header</span></span><br/> | <dl> <span data-ttu-id="b005b-127"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b005b-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b005b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b005b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b005b-129">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="b005b-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




