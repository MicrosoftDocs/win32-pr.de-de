---
description: Definiert den Basis-Typ einer hochwertigen patchoberfläche.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: D3DBASISTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132305"
---
# <a name="d3dbasistype-enumeration"></a>D3DBASISTYPE-Enumeration

Definiert den Basis-Typ einer hochwertigen patchoberfläche.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ Bezier**
</dt> <dd>

Eingabe Vertices werden als eine Reihe von Bézier-Patches behandelt. Die Anzahl der angegebenen Scheitel Punkte muss von 4 unterschieden werden. Teile des Netzes, die über dieses Kriterium hinausgehen, werden nicht gerendert. Die vollständige Kontinuität wird zwischen den Subpatches im Inneren der Oberfläche, die von den einzelnen anrufen gerendert wird, angenommen. Es ist garantiert, dass nur die Scheitel Punkte an den Ecken der einzelnen Subpatches auf der sich ergebenden Oberfläche liegen.

</dd> <dt>

<span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ Bspline**
</dt> <dd>

Eingabe Vertices werden als Steuerungs Punkte einer B-Spline-Oberfläche behandelt. Die Anzahl der gerenderten Blenden ist zwei weniger als die Anzahl der Öffnungen in dieser Richtung. Im Allgemeinen enthält die generierte Oberfläche nicht die angegebenen Steuerelement Scheitel Punkte.

</dd> <dt>

<span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS- \_ Update- \_ Rom**
</dt> <dd>

Eine interinterpolation definiert die Oberfläche, damit die Oberfläche alle angegebenen Eingabe Scheitel Punkte durchläuft. In DirectX 8 war dies D3DBASIS \_ Interpolate.

</dd> <dt>

<span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Member von **D3DBASISTYPE** geben die zu verwendende Formulierung an, die bei der Auswertung der hochwertigen patchoberflächen primitive während des Mosaik Prozesses verwendet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRECTPATCH \_ Info**](d3drectpatch-info.md)
</dt> <dt>

[**D3DTRIPATCH \_ Info**](d3dtripatch-info.md)
</dt> </dl>

 

 




