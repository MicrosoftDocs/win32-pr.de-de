---
description: Texturphasenzustände definieren Texturvorgänge mit mehreren Blendern.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: D3DTEXTURESTAGESTATETYPE-Enumeration (D3D9Types.h)
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
ms.openlocfilehash: 4879009f603a6943302f0595f37176ec5edf8e1a1d3212efedb66c923d775104
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894150"
---
# <a name="d3dtexturestagestatetype-enumeration"></a>D3DTEXTURESTAGESTATETYPE-Enumeration

Texturphasenzustände definieren Texturvorgänge mit mehreren Blendern. Einige Samplerzustände richten die Scheitelpunktverarbeitung ein, und einige richten die Pixelverarbeitung ein. Zustandszustände der Texturphase können mithilfe von Zustandsblöcken gespeichert und wiederhergestellt werden (siehe [Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9)](state-blocks-save-and-restore-state.md)).

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

<span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ COLOROP**
</dt> <dd>

Der Texturphasenzustand ist ein Texturfarbmischungsvorgang, der von einem Member des [**D3DTEXTUREOP-Enumerationstyps**](./d3dtextureop.md) identifiziert wird. Der Standardwert für die erste Texturphase (Stufe 0) ist D3DTOP \_ MODULATE. Für alle anderen Phasen ist der Standardwert D3DTOP \_ DISABLE.

</dd> <dt>

<span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**
</dt> <dd>

Der Texturphasenzustand ist das erste Farbargument für die Stufe, das durch einen der [D3DTA](d3dta.md)identifiziert wird. Das Standardargument ist D3DTA \_ TEXTURE.

Geben Sie D3DTA \_ TEMP an, um eine temporäre Registerfarbe für Lese- oder Schreibzugriff auszuwählen. D3DTA \_ TEMP wird unterstützt, wenn die D3DPMISCCAPS \_ TSSARGTEMP-Gerätefunktion vorhanden ist. Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**
</dt> <dd>

Der Texturphasenzustand ist das zweite Farbargument für die Stufe, das durch [D3DTA](d3dta.md)identifiziert wird. Das Standardargument ist D3DTA \_ CURRENT. Geben Sie D3DTA \_ TEMP an, um eine temporäre Registerfarbe für Lese- oder Schreibzugriff auszuwählen. D3DTA \_ TEMP wird unterstützt, wenn die D3DPMISCCAPS \_ TSSARGTEMP-Gerätefunktion vorhanden ist. Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ ALPHAOP**
</dt> <dd>

Der Texturphasenzustand ist ein Textur-Alphablendingvorgang, der von einem Member des [**D3DTEXTUREOP-Enumerationstyps**](./d3dtextureop.md) identifiziert wird. Der Standardwert für die erste Texturphase (Stufe 0) ist D3DTOP \_ SELECTARG1, und für alle anderen Phasen ist der Standardwert D3DTOP \_ DISABLE.

</dd> <dt>

<span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**
</dt> <dd>

Der Texturphasenzustand ist das erste Alphaargument für die Stufe, das durch [D3DTA](d3dta.md)identifiziert wird. Das Standardargument ist D3DTA \_ TEXTURE. Wenn für diese Phase keine Textur festgelegt ist, ist das Standardargument D3DTA \_ DIFFUSE. Geben Sie D3DTA \_ TEMP an, um eine temporäre Registerfarbe für Lese- oder Schreibzugriff auszuwählen. D3DTA \_ TEMP wird unterstützt, wenn die D3DPMISCCAPS \_ TSSARGTEMP-Gerätefunktion vorhanden ist. Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**
</dt> <dd>

Der Texturphasenzustand ist das zweite Alphaargument für die Phase, das durch [D3DTA](d3dta.md)identifiziert wird. Das Standardargument ist D3DTA \_ CURRENT. Geben Sie D3DTA \_ TEMP an, um eine temporäre Registerfarbe für Lese- oder Schreibzugriff auszuwählen. D3DTA \_ TEMP wird unterstützt, wenn die D3DPMISCCAPS \_ TSSARGTEMP-Gerätefunktion vorhanden ist. Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**
</dt> <dd>

Der Texturphasenzustand ist ein Gleitkommawert für den \[ \] \[ Koeffizienten 0 0 \] in einer Bumpmappingmatrix. Der Standardwert ist 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**
</dt> <dd>

Der Texturphasenzustand ist ein Gleitkommawert für den \[ \] \[ Koeffizienten 0 1 \] in einer Bump-Mapping-Matrix. Der Standardwert ist 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**
</dt> <dd>

Der Texturphasenzustand ist ein Gleitkommawert für den \[ \] \[ Koeffizienten 1 0 \] in einer Bumpmappingmatrix. Der Standardwert ist 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**
</dt> <dd>

Der Texturphasenzustand ist ein Gleitkommawert für den \[ \] \[ Koeffizienten 1 1 \] in einer Bump-Mapping-Matrix. Der Standardwert ist 0,0.

</dd> <dt>

<span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ TEXCOORDINDEX**
</dt> <dd>

Index des Texturkoordinatensatzes, der mit dieser Texturphase verwendet werden soll. Sie können bis zu acht Sätze von Texturkoordinaten pro Scheitelpunkt angeben. Wenn ein Scheitelpunkt keinen Satz von Texturkoordinaten am angegebenen Index enthält, verwendet das System standardmäßig die Sie- und v-Koordinaten (0,0).

Beim Rendern mit Vertex-Shadern muss der Texturkoordinatenindex jeder Phase auf den Standardwert festgelegt werden. Der Standardindex für jede Phase ist gleich dem Phasenindex. Legen Sie diesen Zustand auf den nullbasierten Index des Koordinatensatzes für jeden Scheitelpunkt fest, der von dieser Texturphase verwendet wird.

Darüber hinaus können Anwendungen als logisches OR mit dem festgelegten Index eine der Konstanten enthalten, die anfordern, dass Direct3D automatisch die Eingabetexturkoordinaten für eine Texturtransformation generiert. Eine Liste aller Konstanten finden Sie unter [D3DTSS \_ TCI](d3dtss-tci.md).

Mit Ausnahme von D3DTSS \_ TCI \_ PASSTHRU, das in 0 (null) aufgelöst wird, verwendet das System den Index ausschließlich, um den Texturumbruchmodus zu bestimmen, wenn einer der folgenden Werte in den festzulegenden Index eingeschlossen wird. Diese Flags sind besonders nützlich beim Durchführen der Umgebungszuordnung.

</dd> <dt>

<span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ BUMPENVLSCALE**
</dt> <dd>

Gleitkomma-Skalierungswert für die Leuchtdichte von Bumpmaps. Der Standardwert ist 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ BUMPENVLOFFSET**
</dt> <dd>

Gleitkommaoffsetwert für die Leuchtdichte von Bumpmaps. Der Standardwert ist 0,0.

</dd> <dt>

<span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ TEXTURETRANSFORMFLAGS**
</dt> <dd>

Member des [**D3DTEXTURETRANSFORMFLAGS-Enumerationstyps,**](./d3dtexturetransformflags.md) der die Transformation von Texturkoordinaten für diese Texturphase steuert. Der Standardwert ist D3DTTFF \_ DISABLE.

</dd> <dt>

<span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**
</dt> <dd>

Einstellungen für den dritten Farbopernden für trikoische Operationen (Multiplizieren, Hinzufügen und lineares Interpolieren), die durch [D3DTA](d3dta.md)identifiziert werden. Diese Einstellung wird unterstützt, wenn die LERP-Gerätefunktionen D3DTEXOPCAPS \_ MULTIPLYADD oder D3DTEXOPCAPS \_ vorhanden sind. Das Standardargument ist D3DTA \_ CURRENT. Geben Sie D3DTA \_ TEMP an, um eine temporäre Registerfarbe für Lese- oder Schreibzugriff auszuwählen. D3DTA \_ TEMP wird unterstützt, wenn die D3DPMISCCAPS \_ TSSARGTEMP-Gerätefunktion vorhanden ist. Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**
</dt> <dd>

Einstellungen für den Alphakanalselektoropernden für trikoische Vorgänge (Multiplizieren, Hinzufügen und lineares Interpolieren), die durch [D3DTA](d3dta.md)identifiziert werden. Diese Einstellung wird unterstützt, wenn die LERP-Gerätefunktionen D3DTEXOPCAPS \_ MULTIPLYADD oder D3DTEXOPCAPS \_ vorhanden sind. Das Standardargument ist D3DTA \_ CURRENT. Geben Sie D3DTA \_ TEMP an, um eine temporäre Registerfarbe für Lese- oder Schreibzugriff auszuwählen. D3DTA \_ TEMP wird unterstützt, wenn die D3DPMISCCAPS \_ TSSARGTEMP-Gerätefunktion vorhanden ist. Das Standardargument ist (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ RESULTARG**
</dt> <dd>

Einstellung zum Auswählen des Zielregisters für das Ergebnis dieser Phase, identifiziert durch [D3DTA.](d3dta.md) Dieser Wert kann auf D3DTA CURRENT (Standardwert) oder auf D3DTA TEMP festgelegt werden. Dabei handelt es sich \_ um ein \_ einzelnes temporäres Register, das als Eingabeargument in nachfolgende Phasen eingelesen werden kann. Die endgültige Farbe, die an den Blender und den Framepuffer übergeben wird, wird von D3DTA \_ CURRENT übernommen, sodass der Zustand der letzten aktiven Texturphase auf "Aktuell" festgelegt werden muss. Diese Einstellung wird unterstützt, wenn die D3DPMISCCAPS \_ TSSARGTEMP-Gerätefunktion vorhanden ist.

</dd> <dt>

<span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS-KONSTANTE \_**
</dt> <dd>

Konstante Farbe pro Stufe. Um festzustellen, ob ein Gerät eine stufenspezifische Konstante unterstützt, lesen Sie die D3DPMISCCAPS \_ PERSTAGECONSTANT-Konstante in [D3DPMISCCAPS.](d3dpmisccaps.md) D3DTSS \_ CONSTANT wird von D3DTA CONSTANT \_ verwendet. Siehe [D3DTA](d3dta.md).

</dd> <dt>

<span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Member dieses Enumerationstyps werden mit den [**Methoden IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) und [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) verwendet, um Texturzustandswerte abzurufen und festzulegen.

Der gültige Wertebereich für die Matrixkoeffizienten D3DTSS \_ BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 und D3DTSS \_ BUMPENVMAT11 ist größer oder gleich -8,0 und kleiner als 8,0. Dieser In mathematischer Notation ausgedrückte Bereich ist (-8,0,8,0).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
