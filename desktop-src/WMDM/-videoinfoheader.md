---
title: _VIDEOINFOHEADER-Struktur
description: Die VIDEOINFOHEADER-Struktur enthält Informationen zu einem Videostream und eine \_ BITMAPINFOHEADER-Struktur, die das \_ Format eines einzelnen Frames definiert.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- _VIDEOINFOHEADER Struktur von Windows Media Geräte-Manager
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
ms.openlocfilehash: 5b00c641f0fb9a9f68217de8a21a732b4b45a8e4417104be981ffd90161f7340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586800"
---
# <a name="_videoinfoheader-structure"></a>\_VIDEOINFOHEADER-Struktur

Die **\_ VIDEOINFOHEADER-Struktur** enthält Informationen zu einem Videostream und eine **\_ BITMAPINFOHEADER-Struktur,** die das Format eines einzelnen Frames definiert.

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

**RECT-Struktur,** die das Quellvideofenster angibt.

</dd> <dt>

**rcTarget**
</dt> <dd>

**RECT-Struktur,** die das Zielvideofenster angibt.

</dd> <dt>

**dwBitRate**
</dt> <dd>

**DWORD-Wert,** der die ungefähre Datenrate des Videostreams in Bits pro Sekunde angibt.

</dd> <dt>

**dwBitErrorRate**
</dt> <dd>

**DWORD-Wert,** der die Datenfehlerrate des Videostreams in Bitfehlern pro Sekunde angibt.

</dd> <dt>

**AvgTimePerFrame**
</dt> <dd>

**REFERENZ \_ TIME-Wert,** der die durchschnittliche Anzeigezeit des Videoframes in Einheiten von 100 Nanosekunden angibt.

</dd> <dt>

**bmiHeader**
</dt> <dd>

Win32 **\_ BITMAPINFOHEADER-Struktur,** die Farb- und Dimensionsinformationen für die Videobildbitmap enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





