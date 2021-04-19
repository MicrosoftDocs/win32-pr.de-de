---
description: Der \_ Enumerationstyp des WPD-Fokus \_ Modus beschreibt den Fokus Modus, der von einem Bild Erfassungsgerät verwendet wird.
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: WPD_FOCUS_MODES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370155"
---
# <a name="wpd_focus_modes-enumeration"></a><span data-ttu-id="764aa-103">WPD- \_ Fokus \_ Modi-Enumeration</span><span class="sxs-lookup"><span data-stu-id="764aa-103">WPD\_FOCUS\_MODES enumeration</span></span>

<span data-ttu-id="764aa-104">Der Enumerationstyp des **WPD- \_ Fokus \_** Modus beschreibt den Fokus Modus, der von einem Bild Erfassungsgerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="764aa-104">The **WPD\_FOCUS\_MODES** enumeration type describes the focus mode used by a still image capture device.</span></span>

## <a name="syntax"></a><span data-ttu-id="764aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="764aa-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="764aa-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="764aa-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="764aa-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**WPD- \_ Fokus nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="764aa-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**WPD\_FOCUS\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="764aa-108">Der Fokus Modus wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="764aa-108">The focus mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="764aa-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**WPD- \_ Fokus \_ manuell**</span><span class="sxs-lookup"><span data-stu-id="764aa-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**WPD\_FOCUS\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="764aa-110">Gibt den manuellen Fokus an.</span><span class="sxs-lookup"><span data-stu-id="764aa-110">Specifies manual focus.</span></span>

</dd> <dt>

<span data-ttu-id="764aa-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD- \_ Fokus \_ automatisch**</span><span class="sxs-lookup"><span data-stu-id="764aa-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD\_FOCUS\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="764aa-112">Gibt den automatischen Fokus an, der vom Gerät gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="764aa-112">Specifies automatic focus, controlled by the device.</span></span>

</dd> <dt>

<span data-ttu-id="764aa-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**Automatisches WPD- \_ Fokus- \_ \_ Makro**</span><span class="sxs-lookup"><span data-stu-id="764aa-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**WPD\_FOCUS\_AUTOMATIC\_MACRO**</span></span>
</dt> <dd>

<span data-ttu-id="764aa-114">Gibt an, dass das Gerät nach Bedarf automatisch zwischen Makro und normalem Fokus wechseln soll.</span><span class="sxs-lookup"><span data-stu-id="764aa-114">Specifies that the device should automatically switch between macro and normal focus, as required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="764aa-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="764aa-115">Remarks</span></span>

<span data-ttu-id="764aa-116">Diese Enumeration wird von der Eigenschaft für den [ \_ \_ \_ Fokus \_ Modus des WPD-Bilds](still-image-properties.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="764aa-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_FOCUS\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="764aa-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="764aa-117">Requirements</span></span>



| <span data-ttu-id="764aa-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="764aa-118">Requirement</span></span> | <span data-ttu-id="764aa-119">Wert</span><span class="sxs-lookup"><span data-stu-id="764aa-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="764aa-120">Header</span><span class="sxs-lookup"><span data-stu-id="764aa-120">Header</span></span><br/> | <dl> <span data-ttu-id="764aa-121"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="764aa-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="764aa-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="764aa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="764aa-123">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="764aa-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




