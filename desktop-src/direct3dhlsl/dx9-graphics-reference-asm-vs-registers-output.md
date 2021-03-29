---
title: Ausgabe Register
description: Ausgabe Register
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4a0b397d17b841877796bd9c33432896208ed6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992751"
---
# <a name="output-registers"></a>Ausgabe Register

-   Vertex-Farb Register
-   Nebelregister
-   Positions \_ Register
-   Punkt \_ Größe \_ registrieren
-   Textur \_ Koordinaten \_ Register

Register Namen wird ein Kleinbuchstabe o vorangestellt, der angibt, dass die Ausgabe Register schreibgeschützt sind.

## <a name="vertex-color-register---od0-od1"></a>Vertex-Farb Register-oD0, oD1

oD0 ist das diffuse Farbregister. oD1 ist das Glanz Farben Register. Der oD0-Wert wird interpoliert und in das Eingabe Farbregister 0 (V0) des Pixel-Shaders geschrieben. Der oD1-Wert wird interpoliert und in das Eingabe Farbregister 1 (v1) des Pixel-Shaders geschrieben. Weitere Informationen zu Pixel-Shader-Farb Registern finden Sie unter Registern.



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Vertex-Farb Register  | x    | x    | x     | x    |      |       |



 

## <a name="fog-register---ofog"></a>Nebelregister-ofog

Der Ausgabe Nebel Wert wird registriert. Der Wert ist der zu interinterdende Nebel Faktor und wird dann an die Tabelle mit den Nebel geroutet. Es wird nur die skalarx-Komponente des Nebels verwendet. Werte werden zwischen null und eins geklammert, bevor Sie an den Rasterizer übergeben werden.



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Nebelregister           | x    | x    | x     | x    |      |       |



 

## <a name="position-register---opos"></a>Positions Register-OPOS

Die Ausgabe Position wird registriert. Der Wert ist die Position im homogenen Clippingbereich. Dieser Wert muss vom Vertex-Shader geschrieben werden.



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Positions Register      | x    | x    | x     | x    |      |       |



 

## <a name="point-size-register---opts"></a>Punktgröße registrieren-OPTS

Die Ausgabepunkt Größen Register. Es wird nur die skalare x-Komponente der Punktgröße verwendet.



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Punktgröße registrieren    | x    | x    | x     | x    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a>Texturkoordinaten Register-oT0 to oT7

Die Ausgabe Texturkoordinaten werden registriert. Dabei handelt es sich hierbei um ein Array von Ausgabedaten Registern, die durchlaufen und als Texturkoordinaten durch die Textur-samplingphasen zum Weiterleiten von Daten an den Pixelshader verwendet werden.



| Vertex-Shader-Versionen      | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------------|------|------|-------|------|------|-------|
| Texturkoordinaten Register | x    | x    | x     | x    |      |       |



 

Beim Schreiben in ein Texturkoordinaten Register wird empfohlen, nur so viele Gleit Komma Werte wie die Dimension der entsprechenden Textur Zuordnung zu übergeben. Steuern der mit einem-Modifizierer bestandenen Werte. Verwenden Sie beispielsweise. XY für eine 2D-Textur Zuordnung.

Wenn die Textur Projektion für eine Textur Phase aktiviert ist, müssen alle vier Gleit Komma Werte in das entsprechende Textur Register geschrieben werden.

Jedes der D3DTTFF \* Textur Transformations Flags sollte NULL sein, wenn die programmierbare Pipeline verwendet wird.

### <a name="texture-coordinate-range"></a>Texturkoordinaten Bereich

Objekt-Vertex-Daten liefern Eingabe Texturkoordinaten. Objekte, die keine gekachelten Texturen verwenden, weisen häufig Texturkoordinaten im Bereich von \[ 0 bis 1 auf \] . Objekte mit Kacheln, wie z. b. Terrain, haben in der Regel Texturkoordinaten, die von \[ -?, +? ab liegen \] ? kann eine große Gleit Komma Zahl sein.

Die Texturkoordinaten Interpolation wird für Scheitelpunkt Daten für die rasterisierung ausgeführt. Während der rasterisierung werden Texturkoordinaten zwischen Objekt Scheitel Punkten interpoliert, durch Textur Umbrüchen geändert und durch die Textur Größe (auch durch Berücksichtigung des Textur Adress Modus) skaliert, sodass ein ganzzahliger Index erzeugt wird. Der Index wird dann verwendet, um eine Textur Suche auszuführen. Mit MaxTextureRepeat kann bestimmt werden, wie oft eine Textur gekachelt werden kann.

Wenn Texturkoordinaten direkt in einem Pixelshader (mit texcoord oder texcrd) gelesen werden, hängt der Bereich der Textur Koordinate von der Anweisung und der Pixel-Shader-Version ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




