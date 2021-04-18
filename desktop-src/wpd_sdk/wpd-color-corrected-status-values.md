---
description: Der \_ \_ Enumerationstyp "korrigierte WPD-Farben" \_ beschreibt den Status der \_ Farbkorrektur eines Bilds oder einer Videodatei.
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: WPD_COLOR_CORRECTED_STATUS_VALUES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371231"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a><span data-ttu-id="e8d70-103">Mit der WPD- \_ Farbe \_ korrigierte \_ Status \_ Werte Enumeration</span><span class="sxs-lookup"><span data-stu-id="e8d70-103">WPD\_COLOR\_CORRECTED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="e8d70-104">Der Enumerationstyp " **korrigierte WPD- \_ Farben \_ \_ \_** " beschreibt den Status der Farbkorrektur eines Bilds oder einer Videodatei.</span><span class="sxs-lookup"><span data-stu-id="e8d70-104">The **WPD\_COLOR\_CORRECTED\_STATUS\_VALUES** enumeration type describes the color correction status of an image or video file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8d70-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8d70-105">Syntax</span></span>


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="e8d70-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e8d70-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e8d70-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**Status der \_ korrigierten WPD-Farbe \_ \_ \_ nicht \_ korrigiert**</span><span class="sxs-lookup"><span data-stu-id="e8d70-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_NOT\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="e8d70-108">Das Bild wurde nicht farblich korrigiert.</span><span class="sxs-lookup"><span data-stu-id="e8d70-108">The image has not been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="e8d70-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**korrigierter Status der WPD- \_ Farbe \_ \_ \_ korrigiert**</span><span class="sxs-lookup"><span data-stu-id="e8d70-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="e8d70-110">Das Bild wurde farblich korrigiert.</span><span class="sxs-lookup"><span data-stu-id="e8d70-110">The image has been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="e8d70-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**der Status der korrigierten WPD- \_ Farbe \_ \_ \_ sollte \_ nicht \_ \_ korrigiert werden.**</span><span class="sxs-lookup"><span data-stu-id="e8d70-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_SHOULD\_NOT\_BE\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="e8d70-112">Das Bild wurde nicht, und sollte nicht sein, dass die Farbe korrigiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e8d70-112">The image has not been, and should not be, color corrected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8d70-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8d70-113">Remarks</span></span>

<span data-ttu-id="e8d70-114">Gibt den Status der Farbkorrektur eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="e8d70-114">Indicates the color corrected status of an image.</span></span> <span data-ttu-id="e8d70-115">Diese Enumeration wird von der Eigenschaft " [Status der WPD- \_ Image \_ Farbe \_ korrigiert \_ ](image-properties.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8d70-115">This enumeration is used by the [WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8d70-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8d70-116">Requirements</span></span>



| <span data-ttu-id="e8d70-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8d70-117">Requirement</span></span> | <span data-ttu-id="e8d70-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e8d70-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d70-119">Header</span><span class="sxs-lookup"><span data-stu-id="e8d70-119">Header</span></span><br/> | <dl> <span data-ttu-id="e8d70-120"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8d70-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8d70-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8d70-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8d70-122">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="e8d70-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




