---
title: Erstellen eines Hüllen-Shaders
description: In diesem Thema wird gezeigt, wie Sie einen Hüllen-Shader erstellen.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa9fe55a11c68e4cbc247f6509c52b6bac1d01b823d48637ee51073437316f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608990"
---
# <a name="how-to-create-a-hull-shader"></a>Vorgehensweise: Erstellen eines Hüllen-Shaders

Ein Hüllen-Shader ist die erste von drei Phasen, die zusammenarbeiten, um [Mosaik](direct3d-11-advanced-stages-tessellation.md)zu implementieren. Die Ausgaben des Hüllen-Shaders steuern die Mosaikstufe sowie die Domänen-Shader-Stufe. In diesem Thema wird gezeigt, wie Sie einen Hüllen-Shader erstellen.

Ein Hüllen-Shader wandelt einen Satz von Eingabesteuerpunkten (von einem Scheitelpunkt-Shader) in eine Reihe von Ausgabekontrollpunkten um. Die Anzahl der Eingabe- und Ausgabepunkte kann je nach Transformation in Inhalt und Anzahl variieren (eine typische Transformation wäre eine Basistransformation).

Ein Hüllen-Shader gibt auch Patchkonstanteninformationen wie Mosaikfaktoren für einen Domänen-Shader und den Mosaikator aus. Die Tessellatorphase mit fester Funktion verwendet die Mosaikfaktoren sowie einen anderen Zustand, der in einem Hüllen-Shader deklariert ist, um zu bestimmen, wie viel mosaikiert werden soll.

**So erstellen Sie einen Hüllen-Shader**

1.  Entwerfen sie einen Hüllen-Shader. Weitere Informationen finden Sie unter [Vorgehensweise: Entwerfen eines Hüllen-Shaders.](direct3d-11-advanced-stages-hull-shader-design.md)
2.  Kompilieren des Shadercodes
3.  Erstellen Sie mit [**id3D11Device::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)ein Shaderobjekt.
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  Initialisieren Sie die Pipelinephase mit [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

Ein Domänen-Shader muss an die Pipeline gebunden werden, wenn ein Hüllen-Shader gebunden ist. Insbesondere ist es nicht gültig, mit dem geometry-Shader direkt Hüllen-Shader-Kontrollpunkte zu streamen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Übersicht über Mosaik](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




