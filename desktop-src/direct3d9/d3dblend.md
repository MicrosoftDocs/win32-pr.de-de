---
description: Definiert den unterstützten Blend-Modus.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: D3DBLEND-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d8d779ad714e396f9c9a82bbbc42ddd09b76e2ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961568"
---
# <a name="d3dblend-enumeration"></a>D3DBLEND-Enumeration

Definiert den unterstützten Blend-Modus.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ 0**
</dt> <dd>

Der Blend-Faktor ist (0, 0, 0, 0).

</dd> <dt>

<span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_**
</dt> <dd>

Der Blend-Faktor ist (1, 1, 1, 1).

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ srccolor**
</dt> <dd>

Der Blend-Faktor ist (RS, GS, SB, as).

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND- \_ invsrccolor**
</dt> <dd>

Der Blend-Faktor ist (1-RS, 1-GS, 1-SB, 1-AS).

</dd> <dt>

<span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ srcalpha**
</dt> <dd>

Der Blend-Faktor ist (AS, as, as).

</dd> <dt>

<span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND- \_ invsrcalpha**
</dt> <dd>

Der Blend-Faktor ist (1-AS, 1-AS, 1-AS, 1-AS).

</dd> <dt>

<span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ -Debug**
</dt> <dd>

Der<sub>Blend-Faktor</sub>ist<sub>(a d a d</sub> <sub>a d</sub> <sub>a d</sub> ).

</dd> <dt>

<span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND- \_ invwastalpha**
</dt> <dd>

Der Blend-Faktor ist (1-a<sub>d</sub> 1<sub>-a d 1-</sub> a<sub>d 1-</sub> <sub>a).</sub>

</dd> <dt>

<span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ destcolor**
</dt> <dd>

Der Blend-Faktor ist (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, a<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ invdestcolor**
</dt> <dd>

Der Blend-Faktor ist (1-R<sub>d</sub>, 1-G<sub>d</sub>, 1-B<sub>d</sub>, 1-A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ srcalphasat**
</dt> <dd>

Blend-Faktor ist (f, f, f, 1); Where f = min (AS, 1-A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ bothsrcalpha**
</dt> <dd>

**Veraltet**. Ab DirectX 6 können Sie denselben Effekt erzielen, indem Sie die Quell-und Ziel-Blend-Faktoren auf D3DBLEND \_ srcalpha und D3DBLEND \_ invsrcalpha in separaten Aufrufen festlegen.

</dd> <dt>

<span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ bothinvsrcalpha**
</dt> <dd>

**Veraltet**. Der Quell Blend Faktor ist (1-AS, 1-AS, 1-AS, 1-AS), und der Ziel-Blend-Faktor ist (AS, as, as); die Ziel-Blend-Auswahl wird überschrieben. Dieser Blend-Modus wird nur für den \_ renderzustand D3DRS srcblend unterstützt.

</dd> <dt>

<span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ blendfactor**
</dt> <dd>

Konstanter Farb Mischungs Faktor, der vom Frame Puffer-Blender verwendet wird. Dieser Blend-Modus wird nur unterstützt, wenn D3DPBLENDCAPS \_ blendfactor in den **srcblendcaps** -oder **destblendcaps** -Membern von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)festgelegt ist.

</dd> <dt>

<span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND- \_ invblendfactor**
</dt> <dd>

Der invertierte konstante Farb Mischungs Faktor, der vom Frame Puffer-Blender verwendet wird. Dieser Blend-Modus wird nur unterstützt, wenn das D3DPBLENDCAPS \_ blendfactor-Bit in den **srcblendcaps** -oder **destblendcaps** -Membern von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)festgelegt ist.

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**
</dt> <dd>

Der Blend-Faktor ist (psoutcolor \[ 1 \] <sub>r</sub>, psoutcolor \[ 1 \] <sub>g</sub>, psoutcolor \[ 1 \] <sub>b</sub>, nicht verwendet). Siehe [renderzielmischungs](#render-target-blending).



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/> |



 

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**
</dt> <dd>

Der Blend-Faktor ist (1-psoutcolor \[ 1 \] <sub>r</sub>, 1-psoutcolor \[ 1 \] <sub>g</sub>, 1-psoutcolor \[ 1 \] <sub>b</sub>, nicht verwendet)). Siehe [renderzielmischungs](#render-target-blending).



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/> |



 

</dd> <dt>

<span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

In den vorstehenden Element Beschreibungen werden die RGBA-Werte der Quelle und des Ziels durch die e-und d-Indizes angegeben.

Die Werte in diesem enumerierten Typ werden von den folgenden Rendering-Zuständen verwendet:

-   D3DRS \_ destblend
-   D3DRS \_ srcblend
-   D3DRS \_ destblendalpha
-   D3DRS \_ srcblendalpha

Siehe [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

### <a name="render-target-blending"></a>Mischung für Renderziel

Direct3D 9Ex hat verbesserte textrenderingfunktionen. Das Rendern von Schriftarten mit Klartext erfordert normalerweise zwei Durchgänge. Um den zweiten Durchlauf auszuschließen, kann ein Pixelshader verwendet werden, um zwei Farben auszugeben, die wir psoutcolor \[ 0 \] und psoutcolor \[ 1 \] aufrufen können. Die erste Farbe enthält die Standard-drei Farbkomponenten (RGB). Die zweite Farbe würde 3 Alpha Komponenten enthalten (eine für jede Komponente der ersten Farbe).

Diese neuen Mischungs Modi werden nur zum Rendern von Text auf dem ersten Renderziel verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
