---
title: So wird es sein, wie ein Geometry-Shader
description: Die Geometry-Shader-Instanziierung ermöglicht das Ausführen mehrerer Ausführungen desselben Geometry-Shader pro primitiver.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7858de7d8526a9468d3ebd0a07d57777983a66db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992839"
---
# <a name="how-to-instance-a-geometry-shader"></a>Gewusst wie: instanzgeometrie-Shader

Die Geometry-Shader-Instanziierung ermöglicht das Ausführen mehrerer Ausführungen desselben Geometry-Shader pro primitiver. Fügen Sie der Main-shaderfunktion ein Instanzattribut hinzu, und identifizieren Sie im Shader-Funktions Text einen instanzindexparameter, um einen Geometry-Shader zu erhalten.

Zum Instanztyp eines Geometry-Shaders:

1.  Fügen Sie der Main-Funktion das [Instanzattribut](sm5-attributes-instance.md) hinzu.

    ```
    [instance(24)]
    ```

    

    Dadurch wird die Anzahl der Instanzen (maximal 32) definiert, die für die einzelnen primitiven ausgeführt werden.

2.  Fügen Sie den System Wert " [SV \_ gsinstanceid](sv-gsinstanceid.md) " an eine Variable in der Liste der Funktionsparameter an, die zum Nachverfolgen der ID der ausgeführten Instanz verwendet werden kann.
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  Kompilieren Sie den Shader, und erstellen Sie ihn genauso wie jeden anderen Geometry-Shader.

Weitere Details:

-   Die maximale Anzahl von Instanzen beträgt 32.
-   Die maximale Scheitelpunkt Anzahl ist eine maximale Vertex-Anzahl pro Instanz.
-   Jeder instanzaufruf (wie jeder Geometry-Shader-Aufruf) erhöht den Aufruf Zähler und generiert einen impliziten restartstrip ().

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geometry-Shaderfunktionen](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




