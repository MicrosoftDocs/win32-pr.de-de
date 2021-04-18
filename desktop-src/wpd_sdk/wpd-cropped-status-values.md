---
description: Der Enumerationstyp der WPD-zugeschnittenen \_ \_ Status \_ Werte beschreibt den Zustellungs Status eines Bilds.
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: WPD_CROPPED_STATUS_VALUES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361278"
---
# <a name="wpd_cropped_status_values-enumeration"></a><span data-ttu-id="9c078-103">WPD-zugeschnittenen \_ \_ Status \_ Values-Enumeration</span><span class="sxs-lookup"><span data-stu-id="9c078-103">WPD\_CROPPED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="9c078-104">Der Enumerationstyp der WPD-zugeschnittenen **\_ \_ Status \_ Werte** beschreibt den Zustellungs Status eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="9c078-104">The **WPD\_CROPPED\_STATUS\_VALUES** enumeration type describes the cropping status of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c078-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c078-105">Syntax</span></span>


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="9c078-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9c078-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9c078-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**der WPD-zugeschnittenen \_ \_ Status wurde \_ nicht \_ beschnitten.**</span><span class="sxs-lookup"><span data-stu-id="9c078-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**WPD\_CROPPED\_STATUS\_NOT\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="9c078-108">Das Bild wurde nicht abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="9c078-108">The image has not been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="9c078-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**ausgeschnittener WPD- \_ \_ Status \_**</span><span class="sxs-lookup"><span data-stu-id="9c078-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**WPD\_CROPPED\_STATUS\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="9c078-110">Das Bild wurde abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="9c078-110">The image has been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="9c078-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**der WPD-zugeschnittenen \_ \_ Status \_ sollte \_ nicht zugeschnitten \_ werden \_ .**</span><span class="sxs-lookup"><span data-stu-id="9c078-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**WPD\_CROPPED\_STATUS\_SHOULD\_NOT\_BE\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="9c078-112">Das Bild wurde nicht, und sollte nicht, zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="9c078-112">The image has not been, and should not be, cropped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c078-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c078-113">Remarks</span></span>

<span data-ttu-id="9c078-114">Gibt den zugeschnittenen Status eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="9c078-114">Indicates the cropped status of an image.</span></span> <span data-ttu-id="9c078-115">Diese Enumeration wird von der Eigenschaft " [Status des WPD- \_ Bilds \_ \_ ](image-properties.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c078-115">This enumeration is used by the [WPD\_IMAGE\_CROPPED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c078-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c078-116">Requirements</span></span>



| <span data-ttu-id="9c078-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c078-117">Requirement</span></span> | <span data-ttu-id="9c078-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9c078-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c078-119">Header</span><span class="sxs-lookup"><span data-stu-id="9c078-119">Header</span></span><br/> | <dl> <span data-ttu-id="9c078-120"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c078-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c078-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c078-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c078-122">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="9c078-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




