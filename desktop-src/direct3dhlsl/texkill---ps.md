---
title: texkill-PS
description: Bricht das Rendering des aktuellen Pixels ab, wenn eine der ersten drei Komponenten (UVW) der Texturkoordinaten kleiner als 0 (null) ist.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da9c6b59a3c16eeecb8755f2f19542df6ee8a7b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313614"
---
# <a name="texkill---ps"></a>texkill-PS

Bricht das Rendering des aktuellen Pixels ab, wenn eine der ersten drei Komponenten (UVW) der Texturkoordinaten kleiner als 0 (null) ist.

## <a name="syntax"></a>Syntax



| texkill DST |
|-------------|



 

where

-   DST ist ein Ziel Register

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texkill               | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Diese Anweisung entspricht der " [**Clip**](dx-graphics-hlsl-clip.md) "-Funktion von HLSL.

texkill führt keine Stichprobe für eine Textur aus. Er arbeitet auf den ersten drei Komponenten der Texturkoordinaten, die von der Ziel Registernummer angegeben werden. Für PS \_ 1 \_ 4 arbeitet texkill mit den Daten in den ersten drei Komponenten des Ziel Registers.

Sie können diese Anweisung verwenden, um beliebige Clip-Ebenen im Rasterizer zu implementieren.

Bei der Verwendung von Vertex-Shadern ist die Anwendung für das Anwenden der Perspektiven Transformation verantwortlich. Dies kann Probleme für die willkürlichen clippingflächen verursachen, denn wenn Sie anfügende Skalierungsfaktoren enthält, müssen auch die Clip-Ebenen transformiert werden. Daher ist es am besten, eine nicht projizierte Scheitelpunkt Position für die Verwendung im beliebigen clipperdienst bereitzustellen. dabei handelt es sich um den durch den texkill-Operator identifizierten Texturkoordinaten Satz.

Diese Anweisung wird wie folgt verwendet:

<dl> texkill TN  
Die Pixel Maskierung wird wie folgt durchgeführt:  
if (x, y, z Komponenten von TextureCoordinates (Stufe n)<sub>uvwq</sub>< 0)  
Pixel Rendering Abbrechen
</dl>

Für den Pixelshader 1 \_ 1, 1 \_ 2 und 1 \_ 3 arbeitet texkill mit dem Texturkoordinaten Satz, der von der Ziel Registernummer angegeben wird. In Version 1 \_ 4 arbeitet texkill jedoch mit den Daten, die im [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) oder in dem temporären Register (RN) enthalten sind, das als Ziel angegeben wurde.

Wenn die multisamplinggrad-Funktion aktiviert ist, werden alle Antialiasing-Effekte, die aufgrund von multisamplinggrad auf Polygon Kanten erzielt wurden, nicht an einem von texkill generierten Edge erreicht. Der Pixelshader wird einmal pro Pixel ausgeführt.

Dieses Beispiel dient nur zur Veranschaulichung.

In diesem Beispiel werden Pixel mit negativen Texturkoordinaten maskiert. Die Pixel Farben werden aus Scheitelpunkt Farben interpoliert, die in den Scheitelpunkt Daten bereitgestellt werden.


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



Die Texturkoordinaten reichen von-0,5 bis 0,5 in u und 0,0 bis 1,0 in v. Diese Anweisung bewirkt, dass die negativen u-Werte maskiert werden. Die erste Abbildung unten zeigt die Vertexfarbe, die auf das Vierfache angewendet wird, ohne dass die texkill-Anweisung angewendet wurde. Die zweite Abbildung unten zeigt das Ergebnis der texkill-Anweisung. Die Pixel Farben aus den Texturkoordinaten unterhalb von 0 (wobei x von-0,5 bis 0,0 reicht) werden maskiert. Die Hintergrundfarbe (weiß) wird verwendet, wenn die Pixelfarbe maskiert ist.

![Abbildung der Ausgabe mit der auf das Vierfache angewendeten Vertexfarbe ohne die texkill-Anweisung](images/pstexkill-in.jpg)![Darstellung der Ausgabe mit angewendeter texkill-Anweisung](images/pstexkill-out.jpg)

Die Texturkoordinaten Daten werden in diesem Beispiel in der Vertex-Daten Deklaration deklariert.


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

 

 




