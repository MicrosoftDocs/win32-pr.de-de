---
title: _VIDEOINFOHEADER Struktur
description: Die \_ videoinfoheader-Struktur enthält Informationen zu einem Videostream und enthält eine \_ BITMAPINFOHEADER-Struktur, die das Format eines einzelnen Frames definiert.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- _VIDEOINFOHEADER Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b389c5c82296e95ecfb3900518af4a2c7ddd7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365892"
---
# <a name="_videoinfoheader-structure"></a>\_Videoinfoheader-Struktur

Die **\_ videoinfoheader** -Struktur enthält Informationen zu einem Videostream und enthält eine **\_ BITMAPINFOHEADER** -Struktur, die das Format eines einzelnen Frames definiert.

## <a name="syntax"></a>Syntax


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**rcSource**
</dt> <dd>

**Rect** -Struktur, die das Quellvideo Fenster angibt.

</dd> <dt>

**rctarget**
</dt> <dd>

**Rect** -Struktur, die das Ziel Videofenster angibt.

</dd> <dt>

**dwbitrate**
</dt> <dd>

**DWORD** -Wert, der die ungefähre Datenrate des Videostreams in Bits pro Sekunde angibt.

</dd> <dt>

**dwbiterrorrate**
</dt> <dd>

**DWORD** -Wert, der die Datenfehler Rate des Videostreams in Bitfehlern pro Sekunde angibt.

</dd> <dt>

**Avgtimeperframe**
</dt> <dd>

**Verweis \_ Der Zeitwert** , der die durchschnittliche Anzeigezeit des Video Frames in 100-Nanosecond-Einheiten angibt.

</dd> <dt>

**bmiheader**
</dt> <dd>

Win32- **\_ BITMAPINFOHEADER** -Struktur, die Farb-und Dimensions Informationen für die Video Bild-Bitmap enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





