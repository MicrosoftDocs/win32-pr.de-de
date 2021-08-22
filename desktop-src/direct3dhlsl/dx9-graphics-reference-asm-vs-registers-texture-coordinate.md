---
title: Texturkoordinatenregister (HLSL VS-Referenz)
description: Dieses Vertex-Shader-Ausgaberegister enthält Texturkoordinaten pro Scheitelpunkt.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e695765d57c7e74c94fe0605ca7ec7b96705d7b37d1dc24cad068a5aed6a2ca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457760"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a>Texturkoordinatenregister (HLSL VS-Referenz)

Dieses Vertex-Shader-Ausgaberegister enthält Texturkoordinaten pro Scheitelpunkt.

Ein Register besteht aus Eigenschaften, die bestimmen, wie sich die einzelnen Register verhalten.



| Eigenschaft        | Beschreibung   |
|-----------------|---------------|
| Name            | oT0 – oT7     |
| Anzahl           | Acht Vektoren |
| E/A-Berechtigungen | Lesegeschützt    |



 

Die Ausgabetexturkoordinatenregister sind ein Array von Ausgabedatenregistern. Die Registerdaten werden durchlaufen und von den Textursamplingstufen als Texturkoordinaten verwendet, um Daten an den Pixelshader zu liefern.

Beim Schreiben in ein Texturkoordinatenregister wird empfohlen, nur so viele Gleitkommawerte wie die Dimension der entsprechenden Texturkarte zu übergeben. Steuern Sie die Werte, die mit einem Modifizierer übergeben werden. Verwenden Sie beispielsweise XY für eine 2D-Texturkarte.

Die Vertexpipelineflags der festen Funktion [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3, D3DTTFF \_ COUNT4) sollten bei Verwendung eines programmierbaren Vertex-Shaders auf 0 festgelegt werden.

Objektvertexdaten liefern Eingabetexturkoordinaten. Objekte, die keine gekachelten Texturen verwenden, weisen häufig Texturkoordinaten im Bereich \[ von 0,1 \] auf. Objekte, die kachelte Texturen verwenden, z. B. Gelände, verfügen in der Regel über Texturkoordinaten zwischen \[ -n und +n, \] wobei n eine beliebige Gleitkommazahl sein kann.

Die Texturkoordinateninterpolation wird für Scheitelpunktdaten für die Rasterung durchgeführt. Während der Rasterung werden Texturkoordinaten zwischen Objektvertices interpoliert, durch Texturumbruch geändert und anhand der Texturgröße skaliert (auch unter Berücksichtigung der Texturadressierungsmodi), um einen ganzzahligen Index zu erzeugen. Der Index wird dann verwendet, um eine Textursuche durchzuführen. Verwenden Sie den MaxTextureRepeat-Wert in [**D3DCAPS9,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) um zu bestimmen, wie oft eine Textur gekachelt werden kann.

## <a name="example"></a>Beispiel

Deklarieren Sie das Texturkoordinatenregister.


```
dcl_texcoord v7
```



Kopieren Sie die Texturkoordinaten pro Scheitelpunkt in das Ausgaberegister.


```
mov oT0, v7
```





| Vertex-Shaderversionen      | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------------|------|------|-------|------|------|-------|
| Texturkoordinatenregister | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 