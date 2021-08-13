---
title: D3DX11_FILTER_FLAG-Enumeration (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Flags für die Texturfilterung.
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- D3DX11_FILTER_FLAG-Enumeration Direct3D 11
- LPD3DX11_FILTER_FLAG-Enumerationszeiger Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_FILTER_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02ddbf1785d1032ab28a990d022950b2f28acc4b032ecdc9a72d5704665c03b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118537001"
---
# <a name="d3dx11_filter_flag-enumeration"></a>D3DX11 \_ FILTER \_ FLAG-Enumeration

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.

 

Flags für die Texturfilterung.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_FILTER_FLAG { 
  D3DX11_FILTER_NONE              = (1 << 0),
  D3DX11_FILTER_POINT             = (2 << 0),
  D3DX11_FILTER_LINEAR            = (3 << 0),
  D3DX11_FILTER_TRIANGLE          = (4 << 0),
  D3DX11_FILTER_BOX               = (5 << 0),
  D3DX11_FILTER_MIRROR_U          = (1 << 16),
  D3DX11_FILTER_MIRROR_V          = (2 << 16),
  D3DX11_FILTER_MIRROR_W          = (4 << 16),
  D3DX11_FILTER_MIRROR            = (7 << 16),
  D3DX11_FILTER_DITHER            = (1 << 19),
  D3DX11_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX11_FILTER_SRGB_IN           = (1 << 21),
  D3DX11_FILTER_SRGB_OUT          = (2 << 21),
  D3DX11_FILTER_SRGB              = (3 << 21)
} D3DX11_FILTER_FLAG, *LPD3DX11_FILTER_FLAG;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**D3DX11 \_ FILTER \_ NONE**
</dt> <dd>

Es erfolgt keine Skalierung oder Filterung. Pixel außerhalb der Grenzen des Quellbilds werden als transparent schwarz angenommen.

</dd> <dt>

<span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**D3DX11-FILTERPUNKT \_ \_**
</dt> <dd>

Jedes Zielpixel wird berechnet, indem das nächste Pixel aus dem Quellbild entnommen wird.

</dd> <dt>

<span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11 \_ FILTER \_ LINEAR**
</dt> <dd>

Jedes Zielpixel wird berechnet, indem die vier nächsten Pixel aus dem Quellbild entnommen werden. Dieser Filter funktioniert am besten, wenn die Skala auf beiden Achsen kleiner als zwei ist.

</dd> <dt>

<span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**D3DX11– \_ \_ FILTERDREIECK**
</dt> <dd>

Jedes Pixel im Quellbild trägt gleichermaßen zum Zielbild bei. Dies ist der langsamste Filter.

</dd> <dt>

<span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**D3DX11-FILTERFELD \_ \_**
</dt> <dd>

Jedes Pixel wird berechnet, indem der Mittelwert eines 2x2(x2)-Felds von Pixeln aus dem Quellbild berechnet wird. Dieser Filter funktioniert nur, wenn die Abmessungen des Ziels halb so sind wie bei Mipmaps.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11 \_ \_ \_ FILTERSPIEGELUNG U**
</dt> <dd>

Pixel am Rand der Textur auf der U-Achse sollten gespiegelt und nicht umschlossen werden.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**D3DX11 \_ FILTER \_ MIRROR \_ V**
</dt> <dd>

Pixel am Rand der Textur auf der V-Achse sollten gespiegelt und nicht umschlossen werden.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**D3DX11 \_ \_ \_ FILTERSPIEGELUNG W**
</dt> <dd>

Pixel am Rand der Textur auf der W-Achse sollten gespiegelt und nicht umschlossen werden.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**D3DX11-FILTERSPIEGEL \_ \_**
</dt> <dd>

Die Angabe dieses Flags entspricht der Angabe der W-Flags D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V und \_ \_ \_ D3DX \_ FILTER \_ \_ MIRROR.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**D3DX11 \_ FILTER \_ DITHER**
</dt> <dd>

Das resultierende Bild muss mithilfe eines 4x4-geordneten Ditheralgorithmus geblendet werden. Dies geschieht beim Konvertieren von einem Format in ein anderes.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**D3DX11 \_ FILTER \_ DITHER \_ WIEDERVERZWEIGT**
</dt> <dd>

Verwenden Sie diffuses Dithering auf dem Bild, wenn Sie von einem Format in ein anderes wechseln.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11 \_ FILTER \_ SRGB \_ IN**
</dt> <dd>

Eingabedaten sind im Standardfarbraum RGB (sRGB) enthalten. Siehe Bemerkungen.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ FILTER \_ SRGB \_ OUT**
</dt> <dd>

Ausgabedaten sind im STANDARD-RGB-Farbraum (sRGB) enthalten. Siehe Bemerkungen.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11 \_ FILTER \_ SRGB**
</dt> <dd>

Entspricht der Angabe von D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT. Siehe Bemerkungen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

D3DX11 führt beim Laden von Texturdaten automatisch eine Gammakorrektur durch (um Farbdaten aus dem RGB-Raum in den RGB-Standardbereich zu konvertieren). Dies erfolgt beispielsweise automatisch, wenn RGB-Daten aus einer .png-Datei in eine sRGB-Textur geladen werden. Verwenden Sie die SRGB-Filterflags, um anzugeben, ob die Daten nicht in sRGB-Speicherplatz konvertiert werden müssen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[D3DX-Enumerationen](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





