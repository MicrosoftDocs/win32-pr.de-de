---
title: Texturkoordinaten Register (HLSL vs-Referenz)
description: Dieses Vertex-Shader-Ausgabe Register enthält pro-Scheitelpunkt-Texturkoordinaten.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102246"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a>Texturkoordinaten Register (HLSL vs-Referenz)

Dieses Vertex-Shader-Ausgabe Register enthält pro-Scheitelpunkt-Texturkoordinaten.

Ein Register besteht aus Eigenschaften, die bestimmen, wie sich die einzelnen Register Verhalten.



| Eigenschaft        | BESCHREIBUNG   |
|-----------------|---------------|
| Name            | oT0 - oT7     |
| Anzahl           | Acht Vektoren |
| E/a-Berechtigungen | Lesegeschützt    |



 

Bei den Ausgabe Texturkoordinaten Register handelt es sich um ein Array von Ausgabedaten Registern. Die Register Daten werden durchlaufen und als Texturkoordinaten durch die Textur-samplingphasen verwendet, um Daten für den Pixelshader bereitzustellen.

Wenn Sie in ein Texturkoordinaten Register schreiben, empfiehlt es sich, nur so viele Gleit Komma Werte wie die Dimension der entsprechenden Textur Zuordnung zu übergeben. Steuern Sie die Werte, die mit einem-Modifizierer übermittelt werden. Verwenden Sie beispielsweise. XY für eine 2D-Textur Zuordnung.

Die [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF COUNT2, D3DTTFF COUNT3, D3DTTFF COUNT4) der Fixed-Funktion der Scheitelpunkt Pipeline \_ \_ \_ muss auf 0 (null) festgelegt werden, wenn Sie einen programmierbaren Scheitelpunkt-Shader verwenden.

Objekt-Vertex-Daten liefern Eingabe Texturkoordinaten. Objekte, die keine Kacheln verwenden, weisen häufig Texturkoordinaten im Bereich von \[ 0 bis 1 auf \] . Objekte, die gekachelte Texturen verwenden (z. b. das Gelände), verfügen in der Regel über Texturkoordinaten, die von \[ -n, + n reichen \]

Die Texturkoordinaten Interpolation wird für Scheitelpunkt Daten für die rasterisierung ausgeführt. Während der rasterisierung werden Texturkoordinaten zwischen Objekt Scheitel Punkten interpoliert, durch Textur Umbrüchen geändert und durch die Textur Größe skaliert (auch die Textur Adressierungs Modi werden berücksichtigt), um einen ganzzahligen Index zu schaffen. Der Index wird dann verwendet, um eine Textur Suche auszuführen. Verwenden Sie den MaxTextureRepeat-Wert in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) , um zu bestimmen, wie oft eine Textur gekachelt werden kann.

## <a name="example"></a>Beispiel

Deklarieren Sie das Texturkoordinaten Register.


```
dcl_texcoord v7
```



Kopieren Sie die Texturkoordinaten pro Scheitelpunkt in das Ausgabe Register.


```
mov oT0, v7
```





| Vertex-Shader-Versionen      | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------------|------|------|-------|------|------|-------|
| Texturkoordinaten Register | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 