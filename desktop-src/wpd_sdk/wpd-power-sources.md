---
description: Der \_ \_ Enumerationstyp WPD-Power Sources beschreibt die Stromquelle, die von einem Gerät verwendet wird.
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: WPD_POWER_SOURCES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369591"
---
# <a name="wpd_power_sources-enumeration"></a><span data-ttu-id="95a99-103">WPD- \_ Power \_ Sources-Enumeration</span><span class="sxs-lookup"><span data-stu-id="95a99-103">WPD\_POWER\_SOURCES enumeration</span></span>

<span data-ttu-id="95a99-104">Der Enumerationstyp **WPD- \_ Power \_ Sources** beschreibt die Stromquelle, die von einem Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="95a99-104">The **WPD\_POWER\_SOURCES** enumeration type describes the power source that a device is using.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a99-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95a99-105">Syntax</span></span>


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="95a99-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="95a99-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="95a99-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**Akku für WPD- \_ Strom \_ Quelle \_**</span><span class="sxs-lookup"><span data-stu-id="95a99-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**WPD\_POWER\_SOURCE\_BATTERY**</span></span>
</dt> <dd>

<span data-ttu-id="95a99-108">Die Stromquelle des Geräts ist ein Akku.</span><span class="sxs-lookup"><span data-stu-id="95a99-108">The device power source is a battery.</span></span>

</dd> <dt>

<span data-ttu-id="95a99-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**externe WPD- \_ Strom \_ Quelle \_**</span><span class="sxs-lookup"><span data-stu-id="95a99-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**WPD\_POWER\_SOURCE\_EXTERNAL**</span></span>
</dt> <dd>

<span data-ttu-id="95a99-110">Vom Gerät wird eine externe Stromquelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="95a99-110">The device uses an external power source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95a99-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95a99-111">Remarks</span></span>

<span data-ttu-id="95a99-112">Diese Enumeration wird von der [WPD- \_ Geräte \_ Energie \_ Quellen](device-properties.md) -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="95a99-112">This enumeration is used by the [WPD\_DEVICE\_POWER\_SOURCE](device-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="95a99-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95a99-113">Requirements</span></span>



| <span data-ttu-id="95a99-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95a99-114">Requirement</span></span> | <span data-ttu-id="95a99-115">Wert</span><span class="sxs-lookup"><span data-stu-id="95a99-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="95a99-116">Header</span><span class="sxs-lookup"><span data-stu-id="95a99-116">Header</span></span><br/> | <dl> <span data-ttu-id="95a99-117"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="95a99-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95a99-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95a99-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a99-119">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="95a99-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




