---
title: texkill - ps
description: Bricht das Rendering des aktuellen Pixels ab, wenn eine der ersten drei Komponenten (UVW) der Texturkoordinaten kleiner als 0 (null) ist.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 462549a9caba9b4b49ca5b5ac088e41320b3d6f731a78a0251d5191cc601a2e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284028"
---
# <a name="texkill---ps"></a>texkill - ps

Bricht das Rendering des aktuellen Pixels ab, wenn eine der ersten drei Komponenten (UVW) der Texturkoordinaten kleiner als 0 (null) ist.

## <a name="syntax"></a>Syntax



| texkill dst |
|-------------|



 

where

-   dst ist ein Zielregister.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texkill               | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Diese Anweisung entspricht der [**Clipfunktion**](dx-graphics-hlsl-clip.md) von HLSL.

texkill führt keine Stichprobenentnahme für eine Textur durch. Er arbeitet mit den ersten drei Komponenten der Texturkoordinaten, die von der Zielregisternummer angegeben werden. Für ps \_ 1 \_ 4 verarbeitet texkill die Daten in den ersten drei Komponenten des Zielregisters.

Sie können diese Anweisung verwenden, um beliebige Clipebenen im Rasterizer zu implementieren.

Bei Verwendung von Vertex-Shadern ist die Anwendung für die Anwendung der Perspektiventransformation verantwortlich. Dies kann Probleme für die beliebigen Clippingebenen verursachen, da die Clipebenen ebenfalls transformiert werden müssen, wenn sie anisomorphe Skalierungsfaktoren enthalten. Daher ist es am besten, eine nicht projizierte Scheitelpunktposition bereitzustellen, die im beliebigen Clipper verwendet werden kann. Dabei handelt es sich um den Texturkoordinatensatz, der vom Texkill-Operator identifiziert wird.

Diese Anweisung wird wie folgt verwendet:

<dl> texkill tn  
Die Pixelmaskierung wird wie folgt durchgeführt:  
if ( die x,y,z-Komponenten von TextureCoordinates(stage n)<sub>UVWQ</sub>< 0 )  
Abbrechen des Pixelrenderings
</dl>

Für den Pixelshader 1 \_ 1, 1 \_ 2 und 1 \_ 3 arbeitet texkill mit der Texturkoordinatenmenge, die von der Zielregisternummer angegeben wird. In Version 1 \_ 4 arbeitet texkill jedoch mit den Daten, die im [Texturkoordinatenregister (tn)](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) oder im temporären Register (rn) enthalten sind, das als Ziel angegeben wurde.

Wenn Multisampling aktiviert ist, werden alle Antialiasingeffekte, die aufgrund von Multisampling an Polygonrändern erzielt werden, nicht entlang eines Edges erreicht, der von texkill generiert wurde. Der Pixelshader wird einmal pro Pixel ausgeführt.

Dieses Beispiel dient nur zur Veranschaulichung.

In diesem Beispiel werden Pixel mit negativen Texturkoordinaten maskiert. Die Pixelfarben werden aus scheitelpunktfarben interpoliert, die in den Scheitelpunktdaten bereitgestellt werden.


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



Die Texturkoordinaten reichen von -0,5 bis 0,5 in u und 0,0 bis 1,0 in v. Diese Anweisung bewirkt, dass die negativen u-Werte maskiert werden. Die erste Abbildung unten zeigt die Scheitelpunktfarbe, die auf das Quad angewendet wird, ohne dass die Texkill-Anweisung angewendet wurde. Die zweite Abbildung unten zeigt das Ergebnis der Texkill-Anweisung. Die Pixelfarben der Texturkoordinaten unter 0 (wobei x von -0,5 bis 0,0 verläuft) werden maskiert. Die Hintergrundfarbe (weiß) wird verwendet, wenn die Pixelfarbe maskiert ist.

![Abbildung der Ausgabe mit der Vertexfarbe, die ohne die Texkill-Anweisung auf das Quad angewendet wird](images/pstexkill-in.jpg)![Abbildung der Ausgabe mit angewendeter Texkill-Anweisung](images/pstexkill-out.jpg)

Die Texturkoordinatendaten werden in diesem Beispiel in der Vertexdatendeklaration deklariert.


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




