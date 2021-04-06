---
description: Die WPD-Daten \_ Strom \_ Einheiten-Enumeration gibt die Einheiten Typen an, die für iportabledeviceunitsstream-Vorgänge verwendet werden sollen.
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: WPD_STREAM_UNITS-Enumeration (portabletvicetypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STREAM_UNITS
api_type:
- HeaderDef
api_location:
- PortableDeviceTypes.h
ms.openlocfilehash: 8e70455402a49673b574a0c696b6dda30cc6a884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758838"
---
# <a name="wpd_stream_units-enumeration"></a><span data-ttu-id="75898-103">WPD \_ - \_ streamingeinheiten-Enumeration</span><span class="sxs-lookup"><span data-stu-id="75898-103">WPD\_STREAM\_UNITS enumeration</span></span>

<span data-ttu-id="75898-104">Die **WPD-Daten \_ Strom \_ Einheiten** -Enumeration gibt die Einheiten Typen an, die für [**iportabledeviceunitsstream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) -Vorgänge verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75898-104">The **WPD\_STREAM\_UNITS** enumeration specifies the unit types to be used for [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="75898-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75898-105">Syntax</span></span>


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a><span data-ttu-id="75898-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="75898-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="75898-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**WPD \_ - \_ streameinheiten ( \_ Bytes)**</span><span class="sxs-lookup"><span data-stu-id="75898-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**WPD\_STREAM\_UNITS\_BYTES**</span></span>
</dt> <dd>

<span data-ttu-id="75898-108">Die streameinheiten werden in Bytes angegeben.</span><span class="sxs-lookup"><span data-stu-id="75898-108">The stream units are specified in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="75898-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**Rahmen für WPD- \_ \_ streamingeinheiten \_**</span><span class="sxs-lookup"><span data-stu-id="75898-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**WPD\_STREAM\_UNITS\_FRAMES**</span></span>
</dt> <dd>

<span data-ttu-id="75898-110">Die streameinheiten werden in Frames angegeben.</span><span class="sxs-lookup"><span data-stu-id="75898-110">The stream units are specified in frames.</span></span>

</dd> <dt>

<span data-ttu-id="75898-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**Zeilen für WPD- \_ \_ streameinheiten \_**</span><span class="sxs-lookup"><span data-stu-id="75898-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**WPD\_STREAM\_UNITS\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="75898-112">Die streameinheiten werden in Zeilen angegeben.</span><span class="sxs-lookup"><span data-stu-id="75898-112">The stream units are specified in rows.</span></span>

</dd> <dt>

<span data-ttu-id="75898-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD \_ - \_ streameinheiten ( \_ Millisekunden)**</span><span class="sxs-lookup"><span data-stu-id="75898-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD\_STREAM\_UNITS\_MILLISECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="75898-114">Die streameinheiten werden in Millisekunden angegeben.</span><span class="sxs-lookup"><span data-stu-id="75898-114">The stream units are specified in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="75898-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**WPD \_ - \_ streamingeinheiten ( \_ Mikrosekunden)**</span><span class="sxs-lookup"><span data-stu-id="75898-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**WPD\_STREAM\_UNITS\_MICROSECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="75898-116">Die streameinheiten werden in Mikrosekunden angegeben.</span><span class="sxs-lookup"><span data-stu-id="75898-116">The stream units are specified in microseconds.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75898-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75898-117">Requirements</span></span>



| <span data-ttu-id="75898-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75898-118">Requirement</span></span> | <span data-ttu-id="75898-119">Wert</span><span class="sxs-lookup"><span data-stu-id="75898-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75898-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75898-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75898-121">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75898-121">Windows 8 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="75898-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75898-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75898-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="75898-123">None supported</span></span><br/>                                                                        |
| <span data-ttu-id="75898-124">Header</span><span class="sxs-lookup"><span data-stu-id="75898-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="75898-125"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="75898-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75898-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75898-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75898-127">**Iportabledeviceunitsstream**</span><span class="sxs-lookup"><span data-stu-id="75898-127">**IPortableDeviceUnitsStream**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[<span data-ttu-id="75898-128">**Iportabledeviceunitsstream:: seekinunits**</span><span class="sxs-lookup"><span data-stu-id="75898-128">**IPortableDeviceUnitsStream::SeekInUnits**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




