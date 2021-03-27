---
title: Erstellen eines Hull-Shaders
description: In diesem Thema wird gezeigt, wie ein Hull-Shader erstellt wird.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a1eea7d2e6e70377028976f9576790ce3b64ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708183"
---
# <a name="how-to-create-a-hull-shader"></a>Gewusst wie: Erstellen eines Hull-Shaders

Ein Hull-Shader ist die erste von drei Phasen, die zusammenarbeiten, um Mosaik Vorgänge [zu implementieren.](direct3d-11-advanced-stages-tessellation.md) Die Hull-Shader-Ausgaben steuern die Mosaik Phase sowie die Domäne-Shader-Stufe. In diesem Thema wird gezeigt, wie ein Hull-Shader erstellt wird.

Ein Hull-Shader wandelt eine Reihe von Eingabe Steuerungs Punkten (von einem Vertex-Shader) in einen Satz von Ausgabe Steuerungs Punkten um. Die Anzahl von Eingabe-und Ausgabe Punkten kann in Abhängigkeit von der Transformation (bei einer typischen Transformation eine Basis Transformation) variieren.

Ein Hull-Shader gibt auch patchkonstante Informationen wie Mosaik Faktoren für einen Domänen-Shader und den Mosaik Ausdruck aus. Die Mosaik Stufe Fixed-Function verwendet die Mosaik Faktoren sowie einen anderen Zustand, der in einem Hull-Shader deklariert wurde, um zu bestimmen, wie viel der Mosaik Prozess ist.

**So erstellen Sie einen Hull-Shader**

1.  Entwerfen Sie einen Hull-Shader. Weitere Informationen finden [Sie unter Gewusst wie: Entwerfen eines Hull-Shaders](direct3d-11-advanced-stages-hull-shader-design.md).
2.  Kompilieren des Shader-Codes
3.  Erstellen Sie ein Hull-Shader-Objekt mit [**ID3D11Device:: kreatehullshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  Initialisieren Sie die Pipeline Phase mithilfe von [**Verknüpfung id3d11devicecontext aus:: hssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

Wenn ein Hull-Shader gebunden ist, muss ein Domänen-Shader an die Pipeline gebunden werden. Insbesondere ist es nicht zulässig, Hull-Shader-Steuerungs Punkte direkt mit dem Geometry-Shader zu streamen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Mosaik Übersicht](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




