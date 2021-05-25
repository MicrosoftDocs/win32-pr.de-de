---
description: Definiert den unterstützten Überblendmodus.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: D3DBLEND-Enumeration (D3D9Types.h)
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
ms.openlocfilehash: 55edb432913720f58860d4f5cb87d8da9b9a8681
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343385"
---
# <a name="d3dblend-enumeration"></a>D3DBLEND-Enumeration

Definiert den unterstützten Überblendmodus.

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

<span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ ZERO**
</dt> <dd>

Der Überblendfaktor ist (0, 0, 0, 0).

</dd> <dt>

<span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ ONE**
</dt> <dd>

Der Überblendfaktor ist (1, 1, 1, 1).

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ SRCCOLOR**
</dt> <dd>

Der Überblendfaktor ist (Rs, Gs, Bs, As).

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND \_ INVSRCCOLOR**
</dt> <dd>

Der Überblendfaktor ist (1 – Rs, 1 – Gs, 1 – Bs, 1 – As).

</dd> <dt>

<span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ SRCALPHA**
</dt> <dd>

Der Überblendfaktor ist (As, As, As, As).

</dd> <dt>

<span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND \_ INVSRCALPHA**
</dt> <dd>

Der Überblendfaktor ist ( 1 - As, 1 - As, 1 - As, 1 - As).

</dd> <dt>

<span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ DESTALPHA**
</dt> <dd>

Der Überblendfaktor ist (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND \_ INVDESTALPHA**
</dt> <dd>

Der Überblendfaktor ist (1 – A<sub>d</sub> 1 – A<sub>d</sub> 1 – A<sub>d</sub> 1 – A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ DESTCOLOR**
</dt> <dd>

Der Blend-Faktor ist (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ INVDESTCOLOR**
</dt> <dd>

Der Blend-Faktor ist (1 – R<sub>d</sub>, 1 – G<sub>d</sub>, 1 – B<sub>d</sub>, 1 – A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ SRCALPHASAT**
</dt> <dd>

Der Blend-Faktor ist (f, f, f, 1); where f = min(As, 1 - A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ BOTHSRCALPHA**
</dt> <dd>

**Veraltete**. Ab DirectX 6 können Sie den gleichen Effekt erzielen, indem Sie die Quellen- und Zielmischungsfaktoren in separaten Aufrufen auf D3DBLEND \_ SRCALPHA und D3DBLEND \_ INVSRCALPHA festlegen.

</dd> <dt>

<span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ BOTHINVSRCALPHA**
</dt> <dd>

**Veraltete**. Der Quellmischungsfaktor ist (1 – As, 1 – As, 1 – As, 1 – As), und der Zielmischungsfaktor ist (As, As, As, As); Die Zielmischungsauswahl wird überschrieben. Dieser Blendmodus wird nur für den D3DRS \_ SRCBLEND-Renderzustand unterstützt.

</dd> <dt>

<span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ BLENDFACTOR**
</dt> <dd>

Konstanter Farbmischungsfaktor, der vom Framepufferblender verwendet wird. Dieser Blendmodus wird nur unterstützt, wenn D3DPBLENDCAPS \_ BLENDFACTOR in den **Membern SrcBlendCaps** oder **DestBlendCaps** von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)festgelegt ist.

</dd> <dt>

<span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND \_ INVBLENDFACTOR**
</dt> <dd>

Invertierter konstanter Farbmischungsfaktor, der vom Framepufferblender verwendet wird. Dieser Blendmodus wird nur unterstützt, wenn das D3DPBLENDCAPS \_ BLENDFACTOR-Bit in den **Membern SrcBlendCaps** oder **DestBlendCaps** von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)festgelegt ist.

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**
</dt> <dd>

Der Überblendfaktor ist (PSOutColor \[ 1 \] <sub>r,</sub>PSOutColor \[ 1 \] <sub>g,</sub>PSOutColor \[ 1 \] <sub>b,</sub>nicht verwendet). Weitere Informationen finden [Sie unter Renderzielmischung.](#render-target-blending)

Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:

- Dieses Flag ist nur in Direct3D 9Ex verfügbar.



 

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**
</dt> <dd>

Der Überblendfaktor ist (1 - PSOutColor \[ 1 \] <sub>r</sub>, 1 - PSOutColor \[ 1 \] <sub>g</sub>, 1 - PSOutColor \[ 1 \] <sub>b</sub>, nicht verwendet)). Weitere Informationen finden [Sie unter Renderzielmischung.](#render-target-blending)


Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:

- Dieses Flag ist nur in Direct3D 9Ex verfügbar.



 

</dd> <dt>

<span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

In den obigen Memberbeschreibungen werden die RGBA-Werte der Quelle und des Ziels durch die Inskripts s und d angegeben.

Die Werte in diesem aufzählten Typ werden von den folgenden Renderzuständen verwendet:

-   D3DRS \_ DESTBLEND
-   D3DRS \_ SRCBLEND
-   D3DRS \_ DESTBLENDALPHA
-   D3DRS \_ SRCBLENDALPHA

Siehe [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

### <a name="render-target-blending"></a>Renderzielblending

Direct3D 9Ex verfügt über verbesserte Funktionen zum Rendern von Text. Für das Rendern von Schriftarten vom Typ "Klartext" sind normalerweise zwei Durchläufe erforderlich. Um den zweiten Durchlauf zu vermeiden, kann ein Pixel-Shader verwendet werden, um zwei Farben auszugeben, die wir ALS PSOutColor \[ 0 \] und PSOutColor 1 bezeichnen \[ \] können. Die erste Farbe würde die standardmäßigen drei Farbkomponenten (RGB) enthalten. Die zweite Farbe enthält drei Alphakomponenten (eine für jede Komponente der ersten Farbe).

Diese neuen Mischungsmodi werden nur für das Textrendering auf dem ersten Renderziel verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
