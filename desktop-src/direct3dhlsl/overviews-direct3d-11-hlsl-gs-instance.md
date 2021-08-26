---
title: Instanz eines Geometrie-Shaders
description: Die Geometry-Shader-Instancing ermöglicht die Ausführung mehrerer Ausführungen desselben Geometrie-Shaders pro Primitiv.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 866b0cedb4de0fe2f8bf9087df6637d3a6340505289b4b773eaccd380fa4b367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067920"
---
# <a name="how-to-instance-a-geometry-shader"></a>How To: Instanz eines Geometrie-Shaders

Die Geometry-Shader-Instancing ermöglicht die Ausführung mehrerer Ausführungen desselben Geometrie-Shaders pro Primitiv. Um einen Geometrie-Shader zu instanziieren, fügen Sie der Haupt-Shaderfunktion ein Instanzattribut hinzu, und identifizieren Sie einen Instanzindexparameter im Shaderfunktionskörper.

So instanzindiert man einen Geometrie-Shader:

1.  Fügen Sie [der main-Funktion](sm5-attributes-instance.md) das Instanzattribut hinzu.

    ```
    [instance(24)]
    ```

    

    Dadurch wird die Anzahl der Instanzen (maximal 32) definiert, die für jede Primitive ausgeführt werden sollen.

2.  Fügen Sie [den SV \_ GSInstanceID-Systemwert](sv-gsinstanceid.md) an eine Variable in der Funktionsparameterliste an, die zum Nachverfolgen der ID der ausgeführten Instanz verwendet werden kann.
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  Kompilieren und erstellen Sie den Shader wie jeden anderen Geometrie-Shader.

Weitere Details:

-   Die maximale Anzahl von Instanzen beträgt 32.
-   Die maximale Scheitelpunktanzahl ist eine maximale Scheitelpunktanzahl pro Instanz.
-   Jeder Instanzaufruf (wie jeder Geometry-Shaderaufruf) erhöht die Aufrufanzahl und generiert einen impliziten RestartStrip().

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geometrie-Shaderfeatures](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




