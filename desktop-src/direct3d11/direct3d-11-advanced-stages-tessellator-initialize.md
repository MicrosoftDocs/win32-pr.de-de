---
title: Initialisieren der Tessellator-Stufe
description: In diesem Thema wird gezeigt, wie die Mosaikstufe initialisiert wird.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f842b1095a4053ad35838864bac6d6677194d85f48e0a78e2fc6975af1e3b8d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096280"
---
# <a name="how-to-initialize-the-tessellator-stage"></a>Vorgehensweise: Initialisieren der Tessellator-Stufe

Im Allgemeinen erweitert das Mosaik das kompakte, benutzerdefinierte Modell eines Patches in geometrie, die eine programmierbare Detailmenge enthält. Die Geometrie ist in der Regel ein Satz von Dreiecken, die eine detaillierte Oberflächengeometrie darstellen. In diesem Thema wird gezeigt, wie die Mosaikstufe initialisiert wird.

Die Mosaikphase ist die zweite von drei Phasen, die zusammenarbeiten, um eine Oberfläche zu mosaikieren oder zu kacheln. Die erste Phase ist die Hüllen-Shader-Stufe. sie funktioniert einmal pro Patch und konfiguriert, wie sich die nächste Phase (der feste Funktionstessellator) verhält. Ein Hüllen-Shader generiert auch benutzerdefinierte Ausgaben, z. B. Ausgabekontrollpunkte und Patchkonstanten, die direkt über den Mosaikator an die dritte Stufe gesendet werden, die Domänen-Shader-Stufe. Ein Domänen-Shader wird einmal pro Mosaikpunkt-Stufe aufgerufen und wertet Oberflächenpositionen aus.

Die Mosaikstufe ist eine feste Funktionsphase, es ist kein shader zu generierender und kein festzulegender Zustand vorhanden. Er empfängt den gesamten Einrichtungsstatus aus der Phase des Hüllen-Shaders. Sobald die Hüllen-Shader-Stufe initialisiert wurde, wird die Mosaikstufe automatisch initialisiert.

**So initialisieren Sie die Mosaikstufe**

-   Initialisieren Sie die Hüllen-Shader-Stufe mit [**ID3D11DeviceContext::HSSetShader.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    *ppClassInstances* ist ein Zeiger auf ein Array von Shaderschnittstellen, dargestellt durch [**ID3D11ClassInstance-Zeiger**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) und die Anzahl der Schnittstellen, dargestellt durch *NumClassInstances.* Wenn diese Parameter nicht verwendet werden, können sie auf **NULL** bzw. 0 festgelegt werden.

Nachdem die Phase des Hüllen-Shaders initialisiert wurde, sollten Sie auch die Domänen-Shader-Stufe initialisieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Übersicht über Mosaik](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




