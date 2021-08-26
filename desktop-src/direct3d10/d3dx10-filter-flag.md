---
description: Flags für die Texturfilterung.
ms.assetid: bc73d916-fe18-4b15-b507-7954e157ab9a
title: D3DX10_FILTER_FLAG-Enumeration (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FILTER_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 400347efde28133055b97016d877b1bd4148624387ddd7086f4ff185ab87cca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989530"
---
# <a name="d3dx10_filter_flag-enumeration"></a>D3DX10 \_ FILTER \_ FLAG-Enumeration

Flags für die Texturfilterung.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_FILTER_FLAG { 
  D3DX10_FILTER_NONE              = (1 << 0),
  D3DX10_FILTER_POINT             = (2 << 0),
  D3DX10_FILTER_LINEAR            = (3 << 0),
  D3DX10_FILTER_TRIANGLE          = (4 << 0),
  D3DX10_FILTER_BOX               = (5 << 0),
  D3DX10_FILTER_MIRROR_U          = (1 << 16),
  D3DX10_FILTER_MIRROR_V          = (2 << 16),
  D3DX10_FILTER_MIRROR_W          = (4 << 16),
  D3DX10_FILTER_MIRROR            = (7 << 16),
  D3DX10_FILTER_DITHER            = (1 << 19),
  D3DX10_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX10_FILTER_SRGB_IN           = (1 << 21),
  D3DX10_FILTER_SRGB_OUT          = (2 << 21),
  D3DX10_FILTER_SRGB              = (3 << 21)
} D3DX10_FILTER_FLAG, *LPD3DX10_FILTER_FLAG;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**D3DX10 \_ FILTER \_ NONE**
</dt> <dd>

Es erfolgt keine Skalierung oder Filterung. Pixel außerhalb der Grenzen des Quellbilds werden als transparent schwarz angenommen.

</dd> <dt>

<span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**D3DX10-FILTERPUNKT \_ \_**
</dt> <dd>

Jedes Zielpixel wird berechnet, indem das nächste Pixel aus dem Quellbild entnommen wird.

</dd> <dt>

<span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**D3DX10 \_ FILTER \_ LINEAR**
</dt> <dd>

Jedes Zielpixel wird berechnet, indem die vier nächsten Pixel aus dem Quellbild entnommen werden. Dieser Filter funktioniert am besten, wenn die Skala auf beiden Achsen kleiner als zwei ist.

</dd> <dt>

<span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**\_D3DX10-FILTERDREIECK \_**
</dt> <dd>

Jedes Pixel im Quellbild trägt gleichermaßen zum Zielbild bei. Dies ist der langsamste Filter.

</dd> <dt>

<span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**D3DX10-FILTERFELD \_ \_**
</dt> <dd>

Jedes Pixel wird berechnet, indem der Mittelwert eines 2x2(x2)-Felds von Pixeln aus dem Quellbild berechnet wird. Dieser Filter funktioniert nur, wenn die Abmessungen des Ziels halb so sind wie bei Mipmaps.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**D3DX10 \_ \_ \_ FILTERSPIEGELUNG U**
</dt> <dd>

Pixel am Rand der Textur auf der U-Achse sollten gespiegelt und nicht umschlossen werden.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**D3DX10 \_ FILTER \_ MIRROR \_ V**
</dt> <dd>

Pixel am Rand der Textur auf der V-Achse sollten gespiegelt und nicht umschlossen werden.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**D3DX10 \_ \_ \_ FILTERSPIEGELUNG W**
</dt> <dd>

Pixel am Rand der Textur auf der W-Achse sollten gespiegelt und nicht umschlossen werden.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**D3DX10-FILTERSPIEGEL \_ \_**
</dt> <dd>

Die Angabe dieses Flags entspricht der Angabe der W-Flags D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V und \_ \_ \_ D3DX \_ FILTER \_ \_ MIRROR.

</dd> <dt>

<span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**D3DX10 \_ FILTER \_ DITHER**
</dt> <dd>

Das resultierende Bild muss mithilfe eines 4x4-geordneten Ditheralgorithmus geblendet werden. Dies geschieht beim Konvertieren von einem Format in ein anderes.

</dd> <dt>

<span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**D3DX10 \_ FILTER \_ DITHER \_ FEE**
</dt> <dd>

Verwenden Sie diffuses Dithering auf dem Bild, wenn Sie von einem Format in ein anderes wechseln.

</dd> <dt>

<span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10 \_ FILTER \_ SRGB \_ IN**
</dt> <dd>

Eingabedaten sind im Standardfarbraum RGB (sRGB) enthalten. Siehe Bemerkungen.

</dd> <dt>

<span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10 \_ FILTER \_ SRGB \_ OUT**
</dt> <dd>

Ausgabedaten sind im STANDARD-RGB-Farbraum (sRGB) enthalten. Siehe Bemerkungen.

</dd> <dt>

<span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3DX10 \_ FILTER \_ SRGB**
</dt> <dd>

Entspricht der Angabe von D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT. Siehe Bemerkungen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

D3DX10 führt beim Laden von Texturdaten automatisch eine Gammakorrektur durch (um Farbdaten aus dem RGB-Raum in den RGB-Standardbereich zu konvertieren). Dies geschieht beispielsweise automatisch, wenn RGB-Daten aus einer .png-Datei in eine sRGB-Textur geladen werden. Verwenden Sie die SRGB-Filterflags, um anzugeben, ob die Daten nicht in sRGB-Speicherplatz konvertiert werden müssen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




