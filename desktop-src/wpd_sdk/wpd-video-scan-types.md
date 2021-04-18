---
description: Der \_ Enumerationstyp der WPD-Video Überprüfung \_ beschreibt, \_ wie die Felder in einer Video Datei codiert werden.
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: WPD_VIDEO_SCAN_TYPES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a636bc95fd3d25de20c2df413576a504c4fa1b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352845"
---
# <a name="wpd_video_scan_types-enumeration"></a><span data-ttu-id="07efb-103">WPD \_ - \_ \_ videoscantypen-Enumeration</span><span class="sxs-lookup"><span data-stu-id="07efb-103">WPD\_VIDEO\_SCAN\_TYPES enumeration</span></span>

<span data-ttu-id="07efb-104">Der Enumerationstyp der **WPD- \_ Video \_ \_** Überprüfung beschreibt, wie die Felder in einer Video Datei codiert werden.</span><span class="sxs-lookup"><span data-stu-id="07efb-104">The **WPD\_VIDEO\_SCAN\_TYPES** enumeration type describes how the fields in a video file are encoded.</span></span>

## <a name="syntax"></a><span data-ttu-id="07efb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07efb-105">Syntax</span></span>


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="07efb-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="07efb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="07efb-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**WPD \_ - \_ \_ videoscantyp nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="07efb-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**WPD\_VIDEO\_SCAN\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="07efb-108">Der Überprüfungstyp wurde für diese Videodatei nicht definiert oder ist nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="07efb-108">The scan type has not been defined for this video file, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="07efb-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**WPD \_ - \_ \_ videoscantyp \_ progressiv**</span><span class="sxs-lookup"><span data-stu-id="07efb-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="07efb-110">Eine Progressive Scan Videodatei.</span><span class="sxs-lookup"><span data-stu-id="07efb-110">A progressive scan video file.</span></span>

</dd> <dt>

<span data-ttu-id="07efb-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**Feld "WPD- \_ \_ videoscantyp" überlappend \_ \_ \_ \_ \_ zuerst**</span><span class="sxs-lookup"><span data-stu-id="07efb-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="07efb-112">Eine verschachtelte Videodatei, in der die Felder Alternativen und das obere Feld (mit Zeile 1) zuerst gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="07efb-112">An interleaved video file where the fields alternate and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="07efb-113">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="07efb-113">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="07efb-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**das Feld "WPD- \_ \_ \_ videoscantyp" \_ \_ interleaved \_ Lower \_ First**</span><span class="sxs-lookup"><span data-stu-id="07efb-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="07efb-115">Eine verschachtelte Videodatei, in der die Felder alternativem Feld und das untere Feld (mit Zeile 2) zuerst gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="07efb-115">An interleaved video file where the fields alternate and the lower field (with line 2) is drawn first.</span></span> <span data-ttu-id="07efb-116">Weitere Informationen finden Sie unter Hinweise in diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="07efb-116">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="07efb-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**Feld "WPD- \_ \_ \_ videoscantyp" \_ \_ Single \_ Upper \_ First**</span><span class="sxs-lookup"><span data-stu-id="07efb-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="07efb-118">Eine verschachtelte Videodatei, in der die Felder als zusammenhängende Beispiele gesendet werden und das obere Feld (mit Zeile 1) zuerst gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="07efb-118">An interleaved video file where the fields are sent as contiguous samples and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="07efb-119">Weitere Informationen finden Sie unter Hinweise in diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="07efb-119">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="07efb-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**Feld "WPD- \_ \_ VideoScan \_ Type" \_ \_ Single \_ Lower \_ First**</span><span class="sxs-lookup"><span data-stu-id="07efb-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="07efb-121">Eine verschachtelte Videodatei, in der die Felder als zusammenhängende Beispiele gesendet werden und das untere Feld (mit Zeile 2) zuerst gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="07efb-121">An interleaved video file where the fields are sent as contiguous samples and the lower field (with line 2) is sent first.</span></span>

</dd> <dt>

<span data-ttu-id="07efb-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**WPD \_ - \_ \_ videoscantyp \_ gemischte \_ Interlace**</span><span class="sxs-lookup"><span data-stu-id="07efb-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE**</span></span>
</dt> <dd>

<span data-ttu-id="07efb-123">Eine Videodatei mit einer Mischung aus interschnür Modi.</span><span class="sxs-lookup"><span data-stu-id="07efb-123">A video file with a mix of interlacing modes.</span></span>

</dd> <dt>

<span data-ttu-id="07efb-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD \_ \_ \_ -videoscantyp \_ gemischte \_ Interlace \_ und \_ progressiv**</span><span class="sxs-lookup"><span data-stu-id="07efb-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE\_AND\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="07efb-125">Eine Videodatei mit einer Mischung aus Zeilen Sprung und progressivem Modus.</span><span class="sxs-lookup"><span data-stu-id="07efb-125">A video file with a mix of interlaced and progressive modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07efb-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07efb-126">Remarks</span></span>

<span data-ttu-id="07efb-127">Diese Enumeration wird von der Eigenschaft [WPD \_ - \_ \_ videoscantyp](properties-and-attributes.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="07efb-127">This enumeration is used by the [WPD\_VIDEO\_SCAN\_TYPE](properties-and-attributes.md) property.</span></span>

<span data-ttu-id="07efb-128">Es gibt zwei Arten von verschachtelten Dateiformaten, die von dieser Enumeration angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="07efb-128">There are two types of interleaved file formats that are specified by this enumeration.</span></span> <span data-ttu-id="07efb-129">**WPD \_ Das überlappende \_ Feld " \_ videoscantyp \_ \_** " bezieht sich auf ein Dateiformat, in dem Frames übermittelt werden, weil Sie als Felder abgescannt werden, und die Daten werden zeilenweise angezeigt, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="07efb-129">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED** refers to a file format where frames are delivered as they were scanned fields alternate and data goes line by line, as shown here:</span></span>

<span data-ttu-id="07efb-130">**Frame 1**</span><span class="sxs-lookup"><span data-stu-id="07efb-130">**Frame 1**</span></span>

<span data-ttu-id="07efb-131">Feld 1: Zeile 1</span><span class="sxs-lookup"><span data-stu-id="07efb-131">Field 1: Line 1</span></span>

<span data-ttu-id="07efb-132">Feld 2: Zeile 1</span><span class="sxs-lookup"><span data-stu-id="07efb-132">Field 2: Line 1</span></span>

<span data-ttu-id="07efb-133">Feld 1: Zeile 2</span><span class="sxs-lookup"><span data-stu-id="07efb-133">Field 1: Line 2</span></span>

<span data-ttu-id="07efb-134">Feld 2: Zeile 2</span><span class="sxs-lookup"><span data-stu-id="07efb-134">Field 2: Line 2</span></span>

<span data-ttu-id="07efb-135">Feld 1: Zeile 3</span><span class="sxs-lookup"><span data-stu-id="07efb-135">Field 1: Line 3</span></span>

<span data-ttu-id="07efb-136">Feld 2: Zeile 3</span><span class="sxs-lookup"><span data-stu-id="07efb-136">Field 2: Line 3</span></span>

<span data-ttu-id="07efb-137">...</span><span class="sxs-lookup"><span data-stu-id="07efb-137">...</span></span>

<span data-ttu-id="07efb-138">**WPD \_ Der Video \_ Scan \_ Type \_ Field \_ Single** bezieht sich auf ein Dateiformat, in dem jedes Feld in einem einzelnen Block von Scan Zeilen gespeichert wird, und Felder werden sequenziell gespeichert, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="07efb-138">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE** refers to a file format where each field is stored in a single block of scan lines, and fields are stored sequentially, as shown here:</span></span>

<span data-ttu-id="07efb-139">**Frame 1**</span><span class="sxs-lookup"><span data-stu-id="07efb-139">**Frame 1**</span></span>

<span data-ttu-id="07efb-140">Feld 1: Zeile 1</span><span class="sxs-lookup"><span data-stu-id="07efb-140">Field 1: Line 1</span></span>

<span data-ttu-id="07efb-141">Feld 1: Zeile 2</span><span class="sxs-lookup"><span data-stu-id="07efb-141">Field 1: Line 2</span></span>

<span data-ttu-id="07efb-142">Feld 1: Zeile 3</span><span class="sxs-lookup"><span data-stu-id="07efb-142">Field 1: Line 3</span></span>

<span data-ttu-id="07efb-143">...</span><span class="sxs-lookup"><span data-stu-id="07efb-143">...</span></span>

<span data-ttu-id="07efb-144">Gefolgt von</span><span class="sxs-lookup"><span data-stu-id="07efb-144">Followed by</span></span>

<span data-ttu-id="07efb-145">Feld 2: Zeile 1</span><span class="sxs-lookup"><span data-stu-id="07efb-145">Field 2: Line 1</span></span>

<span data-ttu-id="07efb-146">Feld 2: Zeile 2</span><span class="sxs-lookup"><span data-stu-id="07efb-146">Field 2: Line 2</span></span>

<span data-ttu-id="07efb-147">Feld 2: Zeile 3</span><span class="sxs-lookup"><span data-stu-id="07efb-147">Field 2: Line 3</span></span>

<span data-ttu-id="07efb-148">...</span><span class="sxs-lookup"><span data-stu-id="07efb-148">...</span></span>

## <a name="requirements"></a><span data-ttu-id="07efb-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07efb-149">Requirements</span></span>



| <span data-ttu-id="07efb-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07efb-150">Requirement</span></span> | <span data-ttu-id="07efb-151">Wert</span><span class="sxs-lookup"><span data-stu-id="07efb-151">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="07efb-152">Header</span><span class="sxs-lookup"><span data-stu-id="07efb-152">Header</span></span><br/> | <dl> <span data-ttu-id="07efb-153"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="07efb-153"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07efb-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07efb-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07efb-155">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="07efb-155">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




