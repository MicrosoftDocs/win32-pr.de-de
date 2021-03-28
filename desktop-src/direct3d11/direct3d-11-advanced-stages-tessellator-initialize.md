---
title: Initialisieren der Mosaik Phase
description: In diesem Thema wird gezeigt, wie die Mosaik Stufe initialisiert wird.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cfe00a4d59396f0dc1b0157f84e57e9cabc4a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992742"
---
# <a name="how-to-initialize-the-tessellator-stage"></a>Gewusst wie: Initialisieren der Mosaik Phase

Im Allgemeinen erweitert das Mosaik Modell das kompakte, benutzerdefinierte Modell eines Patches in Geometry, das eine programmierbare Menge von Details enthält. Die Geometrie ist in der Regel eine Gruppe von Dreiecken, die eine detaillierte Oberflächengeometrie darstellt. In diesem Thema wird gezeigt, wie die Mosaik Stufe initialisiert wird.

Die Mosaik Phase ist die zweite von drei Phasen, die zusammenarbeiten, um eine Oberfläche zu Mosaik oder zu Kacheln. Die erste Phase ist die Hull-Shader-Stufe. Es wird einmal pro Patch betrieben und konfiguriert, wie sich die nächste Stufe (der Mosaik-Mosaik Prozess) verhält. Ein Hull-Shader generiert auch benutzerdefinierte Ausgaben, wie z. b. Ausgabe Steuerungs Punkte und Patch-Konstanten, die über den Mosaik Prozess direkt an die dritte Phase gesendet werden, die Domäne-Shader-Stufe. Ein Domänen-Shader wird einmal pro Mosaik-Stagingpunkt aufgerufen und wertet Oberflächen Positionen aus.

Die Mosaik Phase ist eine fixierte Funktions Phase, es ist kein Shader vorhanden, der generiert werden kann, und es kann kein Zustand festgelegt werden. Er empfängt seinen gesamten Setup Status aus der Hull-Shader-Stufe. Nachdem die Hülle-Shader-Stufe initialisiert wurde, wird die Mosaik Phase automatisch initialisiert.

**So initialisieren Sie die Mosaik Phase**

-   Initialisieren Sie die Hull-Shader-Phase mit [**Verknüpfung id3d11devicecontext aus:: hssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    *ppclassinhaltungen* ist ein Zeiger auf ein Array von shaderschnittstellen, dargestellt durch [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) -Zeiger und die Anzahl der Schnittstellen, die durch *numclassinhaltungen* dargestellt werden. Wenn Sie nicht verwendet werden, können diese Parameter auf **null** bzw. 0 festgelegt werden.

Nachdem die Hull-Shader-Stufe initialisiert wurde, sollten Sie auch die Domäne-Shader-Stufe initialisieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Mosaik Übersicht](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




