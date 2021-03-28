---
title: D3DX11_FILTER_FLAG-Enumeration (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Textur Filterflags.
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- D3DX11_FILTER_FLAG-Enumeration Direct3D 11
- LPD3DX11_FILTER_FLAG enumerationszeiger Direct3D 11
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
ms.openlocfilehash: 0f2105970efb7f2ec07464d8a902df49d8f75bc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982573"
---
# <a name="d3dx11_filter_flag-enumeration"></a>Bibliothek d3dx11 \_ - \_ filterflag-Enumeration

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Textur Filterflags.

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

<span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**Bibliothek d3dx11 \_ Filter \_ None**
</dt> <dd>

Es findet keine Skalierung oder Filterung statt. Es wird davon ausgegangen, dass Pixel außerhalb der Begrenzungen des Quell Bilds transparent schwarz sind.

</dd> <dt>

<span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**Bibliothek d3dx11- \_ Filter \_ Punkt**
</dt> <dd>

Jedes Zielpixel wird berechnet, indem das nächste Pixel aus dem Quell Image entnommen wird.

</dd> <dt>

<span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**Bibliothek d3dx11- \_ Filter \_ linear**
</dt> <dd>

Jedes Zielpixel wird berechnet, indem die vier nächsten Pixel aus dem Quell Image entnommen werden. Dieser Filter funktioniert am besten, wenn die Skala auf beiden Achsen kleiner als zwei ist.

</dd> <dt>

<span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**Bibliothek d3dx11 \_ Filter \_ Dreieck**
</dt> <dd>

Jedes Pixel im Quell Image trägt gleichermaßen dem Ziel Image bei. Dies ist der langsamste der Filter.

</dd> <dt>

<span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**Bibliothek d3dx11 \_ Filter \_ Feld**
</dt> <dd>

Jedes Pixel wird berechnet, indem das Feld 2 x 2 (x2) aus dem Quell Abbild durchläuft. Dieser Filter kann nur verwendet werden, wenn die Abmessungen des Ziels die Hälfte der der Quelle sind, wie es bei MipMaps der Fall ist.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**Bibliothek d3dx11 \_ Filter \_ Spiegelung \_ U**
</dt> <dd>

Pixel am Rand der Textur auf der u-Achse sollten gespiegelt, nicht umschließt werden.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**Bibliothek d3dx11 \_ Filter \_ Spiegelung \_ V**
</dt> <dd>

Pixel am Rand der Textur auf der v-Achse sollten gespiegelt und nicht umschließt werden.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**Bibliothek d3dx11 \_ Filter \_ Spiegelung \_**
</dt> <dd>

Pixel am Rand der Textur auf der w-Achse sollten gespiegelt, nicht umschließt werden.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**Bibliothek d3dx11- \_ Filter \_ Spiegelung**
</dt> <dd>

Die Angabe dieses Flags ist identisch mit dem Angeben der D3DX \_ Filter \_ Mirror \_ U, D3DX \_ Filter \_ Spiegel \_ V und D3DX \_ Filter \_ Mirror \_ W-Flags.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**Bibliothek d3dx11 \_ Filter \_ Dither**
</dt> <dd>

Das resultierende Bild muss mit einem 4 x 4-geordneten Dithering-Algorithmus ausgeblendet werden. Dies geschieht bei der Umstellung von einem Format in ein anderes.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**Bibliothek d3dx11 \_ Filter \_ Dither- \_ Verbreitung**
</dt> <dd>

Verwenden Sie beim Wechsel von einem Format in ein anderes diffuses Dithering für das Bild.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**Bibliothek d3dx11 \_ \_ sRGB Filtern \_ in**
</dt> <dd>

Eingabedaten befinden sich im Standard-RGB-Farbraum (sRGB). Siehe Bemerkungen.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**Bibliothek d3dx11 \_ filtert \_ sRGB \_ out**
</dt> <dd>

Ausgabedaten befinden sich im Standard-RGB-Farbraum (sRGB). Siehe Bemerkungen.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**Bibliothek d3dx11 \_ \_ sRGB Filtern**
</dt> <dd>

Identisch \_ \_ mit der Angabe von D3DX Filter sRGB \_ in \| D3DX \_ Filter \_ sRGB \_ out. Siehe Bemerkungen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bibliothek d3dx11 führt beim Laden von Textur Daten automatisch eine Gammakorrektur durch (zum Konvertieren von Farbdaten aus RGB-Raum in Standard-RGB-Speicherplatz). Dies erfolgt automatisch, wenn RGB-Daten aus einer PNG-Datei in eine sRGB-Textur geladen werden. Verwenden Sie die sRGB-Filterflags, um anzugeben, ob die Daten nicht in den sRGB-Speicher konvertiert werden müssen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





