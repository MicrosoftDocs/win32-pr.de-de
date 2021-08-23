---
description: Der WPD \_ VIDEO \_ SCAN \_ TYPES-Enumerationstyp beschreibt, wie die Felder in einer Videodatei codiert werden.
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: WPD_VIDEO_SCAN_TYPES Enumeration (PortableDevice.h)
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
ms.openlocfilehash: 5f2c6f8a5707780bae6c8a135e3ca940fb4a77408c3df835b321b5b190644fcc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703720"
---
# <a name="wpd_video_scan_types-enumeration"></a>WPD \_ VIDEO \_ SCAN \_ TYPES-Enumeration

Der **WPD \_ VIDEO SCAN \_ TYPES-Enumerationstyp \_** beschreibt, wie die Felder in einer Videodatei codiert werden.

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

<span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**\_WPD-VIDEOSCANTYP \_ \_ NICHT \_ VERWENDET**
</dt> <dd>

Der Scantyp wurde für diese Videodatei nicht definiert oder ist nicht anwendbar.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**\_WPD-VIDEOSCANTYP \_ \_ \_ PROGRESSIVE**
</dt> <dd>

Eine Progressive Scan-Videodatei.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**WPD \_ VIDEO \_ SCAN \_ TYPE \_ FIELD \_ INTERLEAVED \_ UPPER \_ FIRST**
</dt> <dd>

Eine überlappte Videodatei, in der die Felder wechseln und das obere Feld (mit Zeile 1) zuerst gezeichnet wird. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**WPD \_ VIDEO \_ SCAN \_ TYPE \_ FIELD \_ INTERLEAVED \_ LOWER \_ FIRST**
</dt> <dd>

Eine überlappte Videodatei, in der die Felder wechseln und das untere Feld (mit Zeile 2) zuerst gezeichnet wird. Weitere Informationen finden Sie in den Anmerkungen in diesem Abschnitt.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**WPD \_ VIDEO \_ SCAN \_ TYPE \_ FIELD \_ SINGLE \_ UPPER \_ FIRST**
</dt> <dd>

Eine überlappte Videodatei, an die die Felder als zusammenhängende Stichproben gesendet werden und das obere Feld (mit Zeile 1) zuerst gezeichnet wird. Weitere Informationen finden Sie in den Anmerkungen in diesem Abschnitt.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**WPD \_ VIDEO \_ SCAN \_ TYPE \_ FIELD \_ SINGLE \_ LOWER \_ FIRST**
</dt> <dd>

Eine überlappte Videodatei, an die die Felder als zusammenhängende Stichproben gesendet werden, und das untere Feld (mit Zeile 2) wird zuerst gesendet.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**WPD \_ VIDEO \_ SCAN \_ TYPE \_ MIXED \_ INTERLACE**
</dt> <dd>

Eine Videodatei mit einer Mischung aus Interlacingmodi.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD \_ VIDEO \_ SCAN \_ TYPE \_ MIXED \_ INTERLACE \_ AND \_ PROGRESSIVE**
</dt> <dd>

Eine Videodatei mit einer Mischung aus Interlacing- und progressiven Modi.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird von der [WPD \_ VIDEO SCAN \_ \_ TYPE-Eigenschaft](properties-and-attributes.md) verwendet.

Es gibt zwei Typen von überlappten Dateiformaten, die von dieser Enumeration angegeben werden. **WPD \_ VIDEO \_ SCAN TYPE FIELD \_ \_ \_ INTERLEAVED** bezieht sich auf ein Dateiformat, in dem Frames übermittelt werden, während sie als alternative Gescannte Felder verwendet wurden, und Daten zeilenweise übermittelt werden, wie hier gezeigt:

**Frame 1**

Feld 1: Zeile 1

Feld 2: Zeile 1

Feld 1: Zeile 2

Feld 2: Zeile 2

Feld 1: Zeile 3

Feld 2: Zeile 3

...

**WPD \_ VIDEO \_ SCAN TYPE FIELD \_ \_ \_ SINGLE** bezieht sich auf ein Dateiformat, in dem jedes Feld in einem einzelnen Block von Scanzeilen gespeichert und Felder sequenziell gespeichert werden, wie hier gezeigt:

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
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




