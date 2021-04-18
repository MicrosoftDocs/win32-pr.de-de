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
# <a name="wpd_video_scan_types-enumeration"></a>WPD \_ - \_ \_ videoscantypen-Enumeration

Der Enumerationstyp der **WPD- \_ Video \_ \_** Überprüfung beschreibt, wie die Felder in einer Video Datei codiert werden.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**WPD \_ - \_ \_ videoscantyp nicht \_ verwendet**
</dt> <dd>

Der Überprüfungstyp wurde für diese Videodatei nicht definiert oder ist nicht anwendbar.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**WPD \_ - \_ \_ videoscantyp \_ progressiv**
</dt> <dd>

Eine Progressive Scan Videodatei.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**Feld "WPD- \_ \_ videoscantyp" überlappend \_ \_ \_ \_ \_ zuerst**
</dt> <dd>

Eine verschachtelte Videodatei, in der die Felder Alternativen und das obere Feld (mit Zeile 1) zuerst gezeichnet werden. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**das Feld "WPD- \_ \_ \_ videoscantyp" \_ \_ interleaved \_ Lower \_ First**
</dt> <dd>

Eine verschachtelte Videodatei, in der die Felder alternativem Feld und das untere Feld (mit Zeile 2) zuerst gezeichnet werden. Weitere Informationen finden Sie unter Hinweise in diesem Abschnitt.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**Feld "WPD- \_ \_ \_ videoscantyp" \_ \_ Single \_ Upper \_ First**
</dt> <dd>

Eine verschachtelte Videodatei, in der die Felder als zusammenhängende Beispiele gesendet werden und das obere Feld (mit Zeile 1) zuerst gezeichnet wird. Weitere Informationen finden Sie unter Hinweise in diesem Abschnitt.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**Feld "WPD- \_ \_ VideoScan \_ Type" \_ \_ Single \_ Lower \_ First**
</dt> <dd>

Eine verschachtelte Videodatei, in der die Felder als zusammenhängende Beispiele gesendet werden und das untere Feld (mit Zeile 2) zuerst gesendet wird.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**WPD \_ - \_ \_ videoscantyp \_ gemischte \_ Interlace**
</dt> <dd>

Eine Videodatei mit einer Mischung aus interschnür Modi.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD \_ \_ \_ -videoscantyp \_ gemischte \_ Interlace \_ und \_ progressiv**
</dt> <dd>

Eine Videodatei mit einer Mischung aus Zeilen Sprung und progressivem Modus.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von der Eigenschaft [WPD \_ - \_ \_ videoscantyp](properties-and-attributes.md) verwendet.

Es gibt zwei Arten von verschachtelten Dateiformaten, die von dieser Enumeration angegeben werden. **WPD \_ Das überlappende \_ Feld " \_ videoscantyp \_ \_** " bezieht sich auf ein Dateiformat, in dem Frames übermittelt werden, weil Sie als Felder abgescannt werden, und die Daten werden zeilenweise angezeigt, wie hier gezeigt:

**Frame 1**

Feld 1: Zeile 1

Feld 2: Zeile 1

Feld 1: Zeile 2

Feld 2: Zeile 2

Feld 1: Zeile 3

Feld 2: Zeile 3

...

**WPD \_ Der Video \_ Scan \_ Type \_ Field \_ Single** bezieht sich auf ein Dateiformat, in dem jedes Feld in einem einzelnen Block von Scan Zeilen gespeichert wird, und Felder werden sequenziell gespeichert, wie hier gezeigt:

**Frame 1**

Feld 1: Zeile 1

Feld 1: Zeile 2

Feld 1: Zeile 3

...

Gefolgt von

Feld 2: Zeile 1

Feld 2: Zeile 2

Feld 2: Zeile 3

...

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




