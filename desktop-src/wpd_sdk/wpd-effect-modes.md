---
description: Der \_ Enumerationstyp der WPD-Effekt \_ Modi beschreibt verschiedene visuelle Effekte, die auf ein Bild angewendet werden können.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: WPD_EFFECT_MODES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360259"
---
# <a name="wpd_effect_modes-enumeration"></a><span data-ttu-id="872bc-103">WPD- \_ Effekt \_ Modi-Enumeration</span><span class="sxs-lookup"><span data-stu-id="872bc-103">WPD\_EFFECT\_MODES enumeration</span></span>

<span data-ttu-id="872bc-104">Der Enumerationstyp der **WPD- \_ Effekt \_ Modi** beschreibt verschiedene visuelle Effekte, die auf ein Bild angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="872bc-104">The **WPD\_EFFECT\_MODES** enumeration type describes various visual effects that can be applied to an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="872bc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="872bc-105">Syntax</span></span>


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="872bc-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="872bc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="872bc-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**WPD- \_ Effekt \_ Modus nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="872bc-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**WPD\_EFFECT\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="872bc-108">Es wurde keine Auswirkung angegeben.</span><span class="sxs-lookup"><span data-stu-id="872bc-108">No effect has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="872bc-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**Farbe für WPD- \_ Effekt \_ Modus \_**</span><span class="sxs-lookup"><span data-stu-id="872bc-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**WPD\_EFFECT\_MODE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="872bc-110">Das Bild sollte "Color" lauten.</span><span class="sxs-lookup"><span data-stu-id="872bc-110">The image should be color.</span></span>

</dd> <dt>

<span data-ttu-id="872bc-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**WPD \_ \_ -Effekt Modus \_ schwarz \_ und \_ weiß**</span><span class="sxs-lookup"><span data-stu-id="872bc-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**WPD\_EFFECT\_MODE\_BLACK\_AND\_WHITE**</span></span>
</dt> <dd>

<span data-ttu-id="872bc-112">Das Bild sollte Schwarz und weiß sein.</span><span class="sxs-lookup"><span data-stu-id="872bc-112">The image should be black and white.</span></span>

</dd> <dt>

<span data-ttu-id="872bc-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**WPD- \_ Effekt Modus (* \_ \_ Pia)*\*</span><span class="sxs-lookup"><span data-stu-id="872bc-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**WPD\_EFFECT\_MODE\_SEPIA**</span></span>
</dt> <dd>

<span data-ttu-id="872bc-114">Das Bild sollte "\* Pia" lauten.</span><span class="sxs-lookup"><span data-stu-id="872bc-114">The image should be sepia.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="872bc-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="872bc-115">Remarks</span></span>

<span data-ttu-id="872bc-116">Diese Enumeration wird von der Eigenschaft " [ \_ immer noch \_ Bild \_ Effekt \_ Modus](still-image-properties.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="872bc-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_EFFECT\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="872bc-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="872bc-117">Requirements</span></span>



| <span data-ttu-id="872bc-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="872bc-118">Requirement</span></span> | <span data-ttu-id="872bc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="872bc-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="872bc-120">Header</span><span class="sxs-lookup"><span data-stu-id="872bc-120">Header</span></span><br/> | <dl> <span data-ttu-id="872bc-121"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="872bc-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="872bc-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="872bc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872bc-123">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="872bc-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




