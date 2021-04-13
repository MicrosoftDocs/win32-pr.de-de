---
description: Textur Stufen Zustände definieren MULTIMIXER-Textur Vorgänge.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: D3DTEXTURESTAGESTATETYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0530f428c9ebf89607fa89509c65ddd336fee293
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219479"
---
# <a name="d3dtexturestagestatetype-enumeration"></a>D3DTEXTURESTAGESTATETYPE-Enumeration

Textur Stufen Zustände definieren MULTIMIXER-Textur Vorgänge. Einige samplerzustände richten die Vertexverarbeitung ein, und einige richten die Pixel Verarbeitung ein. Textur Stufen Zustände können mithilfe von stateblocks gespeichert und wieder hergestellt werden (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ colorop**
</dt> <dd>

Der Textur Zustand ist ein Textur Farb Mischungs Vorgang, der durch einen Member des [**D3DTEXTUREOP**](./d3dtextureop.md) -Enumerationstyps identifiziert wird. Der Standardwert für die erste Textur Phase (Phase 0) ist D3DTOP \_ modulate; für alle anderen Stufen lautet der Standardwert D3DTOP \_ deaktivieren.

</dd> <dt>

<span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**
</dt> <dd>

Der Textur Stufen Status ist das erste Farb Argument für die Stufe, das durch eine der [D3DTA](d3dta.md)identifiziert wird. Das Standardargument ist D3DTA \_ Texture.

Geben \_ Sie D3DTA Temp an, um eine temporäre Register Farbe für Lese-oder Schreibvorgänge auszuwählen. D3DTA \_ Temp wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist. Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**
</dt> <dd>

Der Textur Zustand ist das zweite Farb Argument für die Stufe, das durch [D3DTA](d3dta.md)identifiziert wird. Das Standardargument ist D3DTA \_ Current. Geben \_ Sie D3DTA Temp an, um eine temporäre Register Farbe für Lese-oder Schreibvorgänge auszuwählen. D3DTA \_ Temp wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist. Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ alphaop**
</dt> <dd>

Der Textur Zustand ist ein Textur Alpha-Mischungs Vorgang, der durch einen Member des [**D3DTEXTUREOP**](./d3dtextureop.md) -Enumerationstyps identifiziert wird. Der Standardwert für die erste Textur Phase (Phase 0) ist D3DTOP \_ SELECTARG1, und für alle anderen Stufen lautet der Standardwert D3DTOP \_ deaktivieren.

</dd> <dt>

<span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**
</dt> <dd>

Der Textur Zustand ist das erste Alpha Argument für die Stufe, das durch [D3DTA](d3dta.md)identifiziert wird. Das Standardargument ist D3DTA \_ Texture. Wenn für diese Stufe keine Textur festgelegt ist, ist das Standardargument D3DTA \_ diffus. Geben \_ Sie D3DTA Temp an, um eine temporäre Register Farbe für Lese-oder Schreibvorgänge auszuwählen. D3DTA \_ Temp wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist. Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**
</dt> <dd>

Der Textur Zustand ist das zweite Alpha Argument für die Stufe, das durch [D3DTA](d3dta.md)identifiziert wird. Das Standardargument ist D3DTA \_ Current. Geben \_ Sie D3DTA Temp an, um eine temporäre Register Farbe für Lese-oder Schreibvorgänge auszuwählen. D3DTA \_ Temp wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist. Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**
</dt> <dd>

Der Textur Zustand ist ein Gleit Komma Wert für den \[ \] \[ Koeffizienten 0 0 \] in einer Bump-mappingmatrix. Der Standardwert ist 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**
</dt> <dd>

Der Textur Zustand ist ein Gleit Komma Wert für den \[ \] \[ Koeffizienten 0 1 \] in einer Bump-mappingmatrix. Der Standardwert ist 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**
</dt> <dd>

Der Textur Zustand ist ein Gleit Komma Wert für den \[ 1 \] \[ 0 \] -Koeffizienten in einer Bump-mappingmatrix. Der Standardwert ist 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**
</dt> <dd>

Der Textur Zustand ist ein Gleit Komma Wert für den \[ 1 1- \] \[ \] Koeffizienten in einer Bump-mappingmatrix. Der Standardwert ist 0,0.

</dd> <dt>

<span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ texcoordindex**
</dt> <dd>

Der Index der Texturkoordinaten Menge, die mit dieser Textur Phase verwendet werden soll. Sie können bis zu acht Sätze von Texturkoordinaten pro Scheitelpunkt angeben. Wenn ein Scheitelpunkt keinen Satz von Texturkoordinaten am angegebenen Index enthält, werden standardmäßig die Koordinaten "You" und "v" (0, 0) verwendet.

Beim Rendering mithilfe von Vertex-Shadern muss der Texturkoordinaten Index jeder Phase auf den Standardwert festgelegt werden. Der Standard Index für jede Stufe ist gleich dem Phasen Index. Legen Sie diesen Status auf den NULL basierten Index des Koordinaten Satzes für jeden Scheitelpunkt fest, den diese Textur Phase verwendet.

Darüber hinaus können Anwendungen, als logisch oder mit dem Index festgelegt werden, eine der Konstanten, die Direct3D automatisch die Eingabe Texturkoordinaten für eine Textur Transformation generieren. Eine Liste aller Konstanten finden Sie unter [D3DTSS \_ TCI](d3dtss-tci.md).

Mit Ausnahme von D3DTSS \_ TCI \_ passthru, das in NULL aufgelöst wird, verwendet das System den Index streng, um den Textur umschließmodus zu bestimmen, wenn einer der folgenden Werte im festgelegten Index enthalten ist. Diese Flags sind besonders nützlich, wenn Sie die Umgebungs Zuordnung durchführen.

</dd> <dt>

<span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ bumpendvlscale**
</dt> <dd>

Gleit Komma-Skalierungs Wert für die Bump-Map-Beleuchtung. Der Standardwert ist 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ bumpenvloffset**
</dt> <dd>

Gleit Komma Offset Wert für die Bild-und Bild Lauf Beleuchtung. Der Standardwert ist 0,0.

</dd> <dt>

<span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ texturetransformflags**
</dt> <dd>

Member des [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) -Enumerationstyps, der die Transformation von Texturkoordinaten für diese Textur Phase steuert. Der Standardwert ist D3DTTFF \_ deaktivieren.

</dd> <dt>

<span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**
</dt> <dd>

Einstellungen für den dritten Farb Operanden für die Ausführung von Vorgängen (multiplizieren, addieren und Linear Interpolate), die durch [D3DTA](d3dta.md)identifiziert werden. Diese Einstellung wird unterstützt, wenn die \_ Gerätefunktionen D3DTEXOPCAPS MultiplyAdd oder D3DTEXOPCAPS \_ Lerp vorhanden sind. Das Standardargument ist D3DTA \_ Current. Geben \_ Sie D3DTA Temp an, um eine temporäre Register Farbe für Lese-oder Schreibvorgänge auszuwählen. D3DTA \_ Temp wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist. Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**
</dt> <dd>

Einstellungen für den Alphakanal Auswahl-Operanden für Selektor-Vorgänge (multiplizieren, addieren und Linear Interpolate), die durch [D3DTA](d3dta.md)identifiziert werden. Diese Einstellung wird unterstützt, wenn die \_ Gerätefunktionen D3DTEXOPCAPS MultiplyAdd oder D3DTEXOPCAPS \_ Lerp vorhanden sind. Das Standardargument ist D3DTA \_ Current. Geben \_ Sie D3DTA Temp an, um eine temporäre Register Farbe für Lese-oder Schreibvorgänge auszuwählen. D3DTA \_ Temp wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist. Das Standardargument ist (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ resultarg**
</dt> <dd>

Die Einstellung zum Auswählen des Ziels für das Ergebnis dieser Phase wird durch [D3DTA](d3dta.md)identifiziert. Dieser Wert kann auf D3DTA \_ Current (Standardwert) oder auf D3DTA Temp festgelegt werden. dabei handelt es sich um \_ ein einzelnes temporäres Register, das als Eingabe Argument in nachfolgende Stufen gelesen werden kann. Die endgültige Farbe, die an den nebelmixer und den Frame Puffer übertragen wird, wird von D3DTA \_ Current übernommen, sodass der letzte aktive Textur Phasen Zustand auf den aktuellen Wert festgelegt werden muss. Diese Einstellung wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist.

</dd> <dt>

<span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS- \_ Konstante**
</dt> <dd>

Einstufige Konstante Farbe. Informationen dazu, ob ein Gerät eine einstufige Konstante Konstante unterstützt, finden Sie \_ in der D3DPMISCCAPS perstageconstant-Konstante in [D3DPMISCCAPS](d3dpmisccaps.md). D3DTSS- \_ Konstante wird von D3DTA- \_ Konstanten verwendet. Siehe [D3DTA](d3dta.md).

</dd> <dt>

<span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Member dieses Enumerationstyps werden mit den Methoden [**IDirect3DDevice9:: gettexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) und [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) verwendet, um Textur Zustands Werte abzurufen und festzulegen.

Der gültige Wertebereich für die \_ Matrizen der D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 und D3DTSS \_ BUMPENVMAT11 Bump-Mapping-Matrix ist größer als oder gleich-8,0 und kleiner als 8,0. Dieser Bereich wird in mathematischer Notation ausgedrückt (-8.0, 8.0).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: gettexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
