---
title: Ausgaberegister
description: Ausgaberegister
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cfa17c09315f4cdca98f5c5fc10f7ab15541eb8b774835963b06169c4afe225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457770"
---
# <a name="output-registers"></a>Ausgaberegister

-   Vertexfarbregister
-   Register "Register"
-   \_Positionsregister
-   \_ \_ Punktgrößenregister
-   \_Texturkoordinatenregister \_

Registernamen wird ein Kleinbuchstabe o vorangestellt, der angibt, dass die Ausgaberegister schreibgeschränkt sind.

## <a name="vertex-color-register---od0-od1"></a>Vertexfarbregister – oD0, oD1

oD0 ist das diffuse Farbregister. oD1 ist das Specular Color Register. Der oD0-Wert wird interpoliert und in das Eingabefarbregister 0 (v0) des Pixel-Shaders geschrieben. Der oD1-Wert wird interpoliert und in das Eingabefarbregister 1 (v1) des Pixelshader geschrieben. Weitere Informationen zu Farbregistern für Pixelshader finden Sie unter Register.



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Vertexfarbregister  | x    | x    | x     | x    |      |       |



 

## <a name="fog-register---ofog"></a>Register "Register" für Register : oFog

Der Ausgabewert wird registriert. Der Wert ist der Faktor, der interpoliert und dann an die Tabellentabelle weitergeleitet werden soll. Es wird nur die skalare x-Komponente des Skalars verwendet. Werte werden vor der Übergabe an den Rasterizer zwischen 0 und 1 klammern.



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Register "Register"           | x    | x    | x     | x    |      |       |



 

## <a name="position-register---opos"></a>Positionsregister – oPos

Die Ausgabeposition wird registriert. Der Wert ist die Position im homogenen Clippingbereich. Dieser Wert muss vom Vertex-Shader geschrieben werden.



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Positionsregister      | x    | x    | x     | x    |      |       |



 

## <a name="point-size-register---opts"></a>Punktgrößenregister – oPts

Die Ausgabepunktgröße wird registriert. Es wird nur die skalare x-Komponente der Punktgröße verwendet.



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Punktgrößenregister    | x    | x    | x     | x    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a>Texturkoordinatenregister – oT0 zu oT7

Die Ausgabetexturkoordinaten registrieren sich. Dabei handelt es sich insbesondere um ein Array von Ausgabedatenregistern, die durchlaufen und von den Textursamplingstufen als Texturkoordinaten verwendet werden, die Daten an den Pixelshader weiterleiten.



| Vertex-Shaderversionen      | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------------|------|------|-------|------|------|-------|
| Texturkoordinatenregister | x    | x    | x     | x    |      |       |



 

Beim Schreiben in ein Texturkoordinatenregister wird empfohlen, nur so viele Gleitkommawerte wie die Dimension der entsprechenden Texturkarte zu übergeben. Steuern Sie die werte, die mit einem Modifizierer übergeben werden. Verwenden Sie beispielsweise XY für eine 2D-Texturkarte.

Wenn die Texturprojektion für eine Texturphase aktiviert ist, müssen alle vier Gleitkommawerte in das entsprechende Texturregister geschrieben werden.

Jedes der \* D3DTTFF-Texturtransformationsflags sollte null sein, wenn die programmierbare Pipeline verwendet wird.

### <a name="texture-coordinate-range"></a>Texturkoordinatenbereich

Objektvertexdaten liefern Eingabetexturkoordinaten. Objekte, die keine gekachelten Texturen verwenden, weisen häufig Texturkoordinaten im Bereich \[ von 0,1 \] auf. Objekte, die kachelte Texturen verwenden, z. B. Gelände, weisen in der Regel Texturkoordinaten auf, die von \[ -?,+? wo \] ? kann eine große Gleitkommazahl sein.

Die Texturkoordinateninterpolation wird für Scheitelpunktdaten für die Rasterung durchgeführt. Während der Rasterung werden Texturkoordinaten zwischen Objektvertices interpoliert, durch Texturumbruch geändert und durch die Texturgröße skaliert (auch unter Berücksichtigung des Texturadressmodus), um einen ganzzahligen Index zu erzeugen. Der Index wird dann verwendet, um eine Textursuche durchzuführen. MaxTextureRepeat kann verwendet werden, um zu bestimmen, wie oft eine Textur gekachelt werden kann.

Wenn Texturkoordinaten direkt in einen Pixel-Shader gelesen werden (mithilfe von Texcoord oder Texcrd), hängt der Texturkoordinatenbereich von der Anweisung und der Pixelshaderversion ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




