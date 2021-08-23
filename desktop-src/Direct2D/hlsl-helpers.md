---
title: HLSL-Hilfsatoren
description: d2d1effecthelpers.hlsli definiert eine Reihe von HLSL-Spracherweiterungen in Form von Hilfsmethoden und Makros, um Autoren beim Schreiben linkbarer Pixel-Shader zu unterstützen.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608ae4b47b96616f8818cd45b466c02a7b09b2171383fbe82ecbe055ed0915b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569560"
---
# <a name="hlsl-helpers"></a>HLSL-Hilfsatoren

d2d1effecthelpers.hlsli definiert eine Reihe von HLSL-Spracherweiterungen in Form von Hilfsmethoden und Makros, um Autoren beim Schreiben linkbarer Pixel-Shader zu unterstützen.

Um "d2d1effecthelpers.hlsli" ihrem Projekt hinzuzufügen, fügen Sie \# der HLSL-Datei eine include-Anweisung hinzu. d2d1effecthelpers.hlsli befindet sich am gleichen Speicherort wie andere Direct2D-Header wie d2d1.h; Sie können auf die Eigenschaftenseite der HLSL-Datei verweisen, indem Sie das Makro $(WindowsSDK \_ IncludePath) zur Eigenschaft Zusätzliche Includeverzeichnisse hinzufügen. Beachten Sie, \# dass die include-Anweisung kommen muss, nachdem präprozessordirektiven wie D2D \_ INPUT COUNT definiert \_ wurden.

``` syntax
#include <d2d1effecthelpers.hlsli>
```

Direct2D unterstützt keine Verknüpfung von Compute- oder Vertex-Shadern. Wenn der Effekt jedoch sowohl einen Vertex-Shader als auch einen Pixel-Shader verwendet, kann die Ausgabe des Pixel-Shaders weiterhin verknüpft werden.

## <a name="preprocessor-directives"></a>Präprozessoranweisungen

Präprozessordirektiven sind erforderlich, um Informationen über den Effekt zu kommunizieren. Dies schließt die Anzahl der Eingaben und den Samplingtyp jeder Eingabe ein. Die folgenden Werte sollten ggf. im Effekt-Shader-Code oberhalb des relevanten Shadereinstiegspunkts definiert werden.

-   `D2D_INPUT_COUNT <N>` : Deklariert die Anzahl der Textureingaben für den Effekt. Wenn der Effekt über eine variable Anzahl von Eingaben verfügt, muss dieser Wert auf jeden Shadereinstiegspunkt entsprechend angepasst werden. Das Definieren dieses Werts ist obligatorisch.
-   `D2D_INPUT<N>_SIMPLE` : Deklariert die N-te Eingabe für die Verwendung einer einfachen Stichprobenentnahme. Wenn sie nicht definiert ist, wird die N-te Eingabe standardmäßig auf komplex festgelegt. Das Definieren dieses Werts ist optional.
-   `D2D_INPUT<N>_COMPLEX` : Deklariert die N-te Eingabe für die Verwendung komplexer Stichproben. Wenn sie nicht definiert ist, wird die N-te Eingabe standardmäßig auf komplex festgelegt. Das Definieren dieses Werts ist optional.
-   `D2D_REQUIRES_SCENE_POSITION`: Gibt an, dass die Shaderfunktion Hilfsmethoden aufruft, die den Szenenpositionswert verwenden (d. h. die [Hilfsfunktion D2DGetScenePosition).](d2dgetsceneposition.md) Dieser Parameter sollte nur bei Bedarf eingeschlossen werden, da nur eine Funktion pro verknüpften Shader diesen Parameter verwenden kann. Das Definieren dieses Werts ist optional.
-   `D2D_CUSTOM_ENTRY` : Gibt an, dass die Pixelsh shader-Funktion die Ausgabe eines benutzerdefinierten Vertex-Shaders verwendet und somit seine Eingabeparameter deklariert. Alle benutzerdefinierten Vertex-Shadereingaben verwenden eine komplexe Stichprobenentnahme und können nicht die Ausgabe einer anderen Shaderfunktion nutzen (d. h., sie sind nur nachverknüpfungsfähig). Das Definieren dieses Werts ist optional.

Beispiel:

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a>Hilfsfunktionen

Hilfsfunktionen werden als Ersatz für einige native systeminterne HLSL-Funktionen verwendet. Zur Kompilierzeit werden diese Hilfsfunktionen von Direct2D je nach Kompilierungszieltyp (vollständiger Shader oder Exportfunktion) in die entsprechende Version neu definiert.

Die Hilfsfunktionen:

<dl>

[D2DGetInput](d2dgetinput.md)  
[D2DSampleInput](d2dsampleinput.md)  
[D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
[D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
[D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
[D2DGetScenePosition](d2dgetsceneposition.md)  
[D2D \_ \_ PS-EINTRAG](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektshader-Verknüpfung](effect-shader-linking.md)
</dt> </dl>

 

 




