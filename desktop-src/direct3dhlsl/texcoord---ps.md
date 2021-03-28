---
title: texcoord-PS
description: Interpretiert Texturkoordinaten Daten (UVW1) als Farbdaten (RGBA).
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728057"
---
# <a name="texcoord---ps"></a>texcoord-PS

Interpretiert Texturkoordinaten Daten (UVW1) als Farbdaten (RGBA).

## <a name="syntax"></a>Syntax



| texcoord-DST |
|--------------|



 

where

-   DST ist das Ziel Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcoord              | x    | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung interpretiert den Texturkoordinaten Satz (UVW1), der der Ziel Registernummer als Farbdaten (RGBA) entspricht. Wenn der Texturkoordinaten Satz weniger als drei Komponenten enthält, werden die fehlenden Komponenten auf 0 festgelegt. Die vierte Komponente ist immer auf 1 festgelegt. Alle Werte werden zwischen 0 und 1 geklammert.

Der Vorteil von texcoord besteht darin, dass es eine Möglichkeit bietet, Scheitelpunkt Daten mit hoher Genauigkeit direkt in den Pixelshader zu übergeben. Wenn die Daten jedoch in das Ziel Register geschrieben werden, gehen einige Genauigkeit verloren, abhängig von der Anzahl der Bits, die von der Hardware für Register verwendet werden.

Von dieser Anweisung wird keine Textur entnommen. Nur für diese Textur Stufe festgelegte Texturkoordinaten sind relevant.

Alle Textur Daten (z. b. Position, normal und Lichtquellen Richtung) können von einem Vertexshader in eine Textur Koordinate zugeordnet werden. Dies erfolgt durch Zuordnen einer Textur zu einem Textur Register mithilfe von [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) und durch Angeben der Art und Weise, wie die Textur Stichprobe mithilfe von [**settexturestagestate**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)durchgeführt wird. Wenn die Pipeline für eine fixierte Funktion verwendet wird, stellen Sie sicher, dass Sie das TSS \_ texcoordindex-Flag angeben.

Diese Anweisung wird wie folgt verwendet:


```
texcoord tn
```



Ein [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) enthält vier Farbwerte (RGBA). Die Daten können auch als Vektordaten (xyzw) betrachtet werden. texcoord ruft drei dieser Werte (XYZ) aus dem Texturkoordinaten Satz x ab, und die vierte Komponente (w) wird auf 1 festgelegt. Die Textur Adresse wird aus dem Texturkoordinaten Satz n kopiert. Das Ergebnis wird zwischen 0 und 1 geklammert.

Dieses Beispiel dient nur zur Veranschaulichung. Der C-Code, der den Shader begleitet, wurde nicht für die Leistung optimiert.

Hier ist ein Beispiel-Shader, der texcoord verwendet.


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



Die gerenderte Ausgabe des Pixelshaders wird in der folgenden Abbildung dargestellt. Die Koordinaten Werte (u, v, w, 1) werden den Kanälen (RGB) zugeordnet. Der Alphakanal ist auf 1 festgelegt. In den Ecken der Abbildung wird Koordinate (0, 0, 0, 1) als schwarz interpretiert. (1, 0, 0, 1) ist rot. (0, 1, 0, 1) ist grün. und (1, 1, 0, 1) enthält grün und rot, wodurch gelb erzeugt wird.

![Abbildung der gerenderten Ausgabe des Pixelshaders example](images/pstexcoord.jpg)

Zusätzlicher Code ist erforderlich, um diesen Shader zu verwenden, und ein Beispielszenario ist unten dargestellt.


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 