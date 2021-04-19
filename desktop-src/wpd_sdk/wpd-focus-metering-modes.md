---
description: Der \_ Enumerationstyp "WPD-Fokus \_ Messungs \_ Modi" beschreibt, wie ein Gerät entscheiden soll, welcher Teil eines Frames zum Festlegen des Fokus verwendet werden soll.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: WPD_FOCUS_METERING_MODES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f59d6a2f1cabbbe7b072a87caa3e5d74d012fc49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355918"
---
# <a name="wpd_focus_metering_modes-enumeration"></a><span data-ttu-id="be68a-103">WPD- \_ Fokus \_ Messungs Modi- \_ Enumeration</span><span class="sxs-lookup"><span data-stu-id="be68a-103">WPD\_FOCUS\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="be68a-104">Der Enumerationstyp " **WPD- \_ Fokus \_ Messungs \_ Modi** " beschreibt, wie ein Gerät entscheiden soll, welcher Teil eines Frames zum Festlegen des Fokus verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="be68a-104">The **WPD\_FOCUS\_METERING\_MODES** enumeration type describes how a device should decide what part of a frame to use to set focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="be68a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be68a-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="be68a-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="be68a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="be68a-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**WPD- \_ Fokus \_ Messungs Modus nicht \_ \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="be68a-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**WPD\_FOCUS\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="be68a-108">Gibt an, dass kein Fokus Modus angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="be68a-108">Indicates that no focusing mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="be68a-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**Mittelpunkt des WPD- \_ Fokus \_ Messungs \_ Modus \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be68a-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="be68a-110">Konzentriert sich auf den Mittelpunkt des eingerahmten Bereichs.</span><span class="sxs-lookup"><span data-stu-id="be68a-110">Focuses on the center of the framed area.</span></span>

</dd> <dt>

<span data-ttu-id="be68a-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**multiSpot des WPD- \_ Fokus \_ Messungs \_ Modus \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be68a-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="be68a-112">Bestimmen Sie den Fokus, indem Sie mehrere Teile des eingerahmten Bereichs analysieren.</span><span class="sxs-lookup"><span data-stu-id="be68a-112">Determine focus by analyzing multiple parts of the framed area.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be68a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be68a-113">Remarks</span></span>

<span data-ttu-id="be68a-114">Diese Enumeration wird von der Eigenschaft für den [ \_ \_ \_ Fokus \_ Messungs \_ Modus der WPD-Bild Größe](still-image-properties.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="be68a-114">This enumeration is specified by the [WPD\_STILL\_IMAGE\_FOCUS\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="be68a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be68a-115">Requirements</span></span>



| <span data-ttu-id="be68a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be68a-116">Requirement</span></span> | <span data-ttu-id="be68a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="be68a-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="be68a-118">Header</span><span class="sxs-lookup"><span data-stu-id="be68a-118">Header</span></span><br/> | <dl> <span data-ttu-id="be68a-119"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="be68a-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be68a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be68a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be68a-121">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="be68a-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




