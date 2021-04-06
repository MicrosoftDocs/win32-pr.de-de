---
title: HLSL-Hilfsprogramme
description: Zur Unterstützung von Autoren beim Schreiben von Verknüpf bares-Pixel-Shadern definiert d2d1effecthelpers. hlsli einen Satz von HLSL-Spracherweiterungen in Form von Hilfsmethoden und-Makros.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8f43447c16d93ef9e1839ac319c761b975222a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947482"
---
# <a name="hlsl-helpers"></a>HLSL-Hilfsprogramme

Zur Unterstützung von Autoren beim Schreiben von Verknüpf bares-Pixel-Shadern definiert d2d1effecthelpers. hlsli einen Satz von HLSL-Spracherweiterungen in Form von Hilfsmethoden und-Makros.

Fügen Sie der HLSL-Datei eine include-Anweisung hinzu, um d2d1effecthelpers. hlsli dem Projekt hinzuzufügen \# . d2d1effecthelpers. hlsli befindet sich am gleichen Speicherort wie andere Direct2D-Header, z. b. d2d1. h; Sie können auf die Eigenschaften Seite der HLSL-Datei verweisen, indem Sie das Makro $ (windowssdk \_ INCLUDEPATH) der zusätzlichen include-Verzeichnisse-Eigenschaft hinzufügen. Beachten Sie, dass die \# include-Anweisung vorhanden sein muss, nachdem alle Präprozessordirektiven wie D2D \_ input \_ count definiert wurden.

``` syntax
#include <d2d1effecthelpers.hlsli>
```

Direct2D bietet keine Unterstützung für das Verknüpfen von COMPUTE-oder Vertex-Shadern. Wenn Ihre Wirkung jedoch sowohl einen Vertex-Shader als auch einen PixelShader verwendet, kann die Ausgabe des Pixelshaders weiterhin verknüpft werden.

## <a name="preprocessor-directives"></a>Präprozessoranweisungen

Präprozessordirektiven sind erforderlich, um Informationen über den Effekt zu übermitteln. Dies schließt die Anzahl der Eingaben und den Samplings der einzelnen Eingaben ein. Die folgenden Werte sollten ggf. im Effekt-Shader-Code oberhalb des relevanten Shader-Einstiegs Punkts definiert werden.

-   `D2D_INPUT_COUNT <N>` : Deklariert die Anzahl der Textur Eingaben für den Effekt. Wenn der Effekt eine Variable Anzahl von Eingaben hat, muss dieser Wert ordnungsgemäß auf jeden Shader-Einstiegspunkt festgelegt werden. Die Definition dieses Werts ist obligatorisch.
-   `D2D_INPUT<N>_SIMPLE` : Deklariert die n-te Eingabe für die Verwendung der einfachen Stichprobenentnahme. Wenn Sie nicht definiert ist, wird die n-te Eingabe standardmäßig auf Complex festgelegt Die Definition dieses Werts ist optional.
-   `D2D_INPUT<N>_COMPLEX` : Deklariert die n-te Eingabe für die Verwendung komplexer Stichproben. Wenn Sie nicht definiert ist, wird die n-te Eingabe standardmäßig auf Complex festgelegt Die Definition dieses Werts ist optional.
-   `D2D_REQUIRES_SCENE_POSITION` : Gibt an, dass die shaderfunktion Hilfsmethoden aufruft, die den Positionswert der Szene verwenden (nämlich die [D2DGetScenePosition](d2dgetsceneposition.md) Helper-Funktion). Dieser Parameter sollte nur bei Bedarf eingeschlossen werden, da dieser Parameter nur von einer Funktion pro verknüpftem Shader verwendet werden kann. Die Definition dieses Werts ist optional.
-   `D2D_CUSTOM_ENTRY` : Gibt an, dass die pixelshaderfunktion die Ausgabe eines benutzerdefinierten Vertex-Shaders verarbeitet und somit seine Eingabeparameter deklariert. Alle benutzerdefinierten Vertex-shadereingaben verwenden eine komplexe Stichprobenentnahme und können die Ausgabe einer anderen shaderfunktion nicht verwenden (d. h., Sie sind nur nach dem ablaufbar). Die Definition dieses Werts ist optional.

Beispiel:

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a>Hilfsfunktionen

Hilfsfunktionen werden als Ersatz für einige systeminterne HLSL-Funktionen verwendet. Zur Kompilierzeit werden diese Hilfsfunktionen von Direct2D in der entsprechenden Version neu definiert, abhängig vom Typ der Kompilierungs Methode (Full Shader oder Export Function).

Die Hilfsfunktionen:

<dl>

[D2DGetInput](d2dgetinput.md)  
[D2DSampleInput](d2dsampleinput.md)  
[D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
[D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
[D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
[D2DGetScenePosition](d2dgetsceneposition.md)  
[D2D \_ PS- \_ Eintrag](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektshader-Verknüpfung](effect-shader-linking.md)
</dt> </dl>

 

 




