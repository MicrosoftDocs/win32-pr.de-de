---
title: Erstellen eines Domänen-Shader
description: In diesem Thema wird gezeigt, wie ein Domänen-Shader erstellt wird.
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89b7f3d7ec6cf801432a5745520fcbd924d139
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036487"
---
# <a name="how-to-create-a-domain-shader"></a>Vorgehensweise: Erstellen eines Domänen-Shader

Ein Domänen-Shader ist der dritte von drei Phasen, die zusammenarbeiten, um Mosaik Vorgänge [zu implementieren.](direct3d-11-advanced-stages-tessellation.md) Die Eingaben für die Domäne-Shader-Phase stammen aus einem Hull-Shader. In diesem Thema wird gezeigt, wie ein Domänen-Shader erstellt wird.

Ein Domänen-Shader transformiert Oberflächengeometrie (erstellt durch die Mosaik Phase "Fixed-Function") mithilfe von Hull-Shader-Ausgabe Steuerungs Punkten, Hull-Shader-Ausgabe Patch-konstantendaten und einem einzelnen Satz von Mosaik-UV-Koordinaten.

**So erstellen Sie einen Domänen-Shader**

1.  Entwerfen Sie einen Domänen-Shader. Weitere Informationen finden [Sie unter Gewusst wie: Entwerfen eines Domänen Shaders](direct3d-11-advanced-stages-domain-shader-design.md).
2.  Kompilieren Sie den Shader-Code.
3.  Erstellen Sie ein Domänen-Shader-Objekt mit [**ID3D11Device:: kreatedomainshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  Initialisieren Sie die Pipeline Phase mithilfe von [**Verknüpfung id3d11devicecontext aus::D ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
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

 

 




