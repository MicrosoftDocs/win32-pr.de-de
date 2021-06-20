---
description: Erfahren Sie mehr über die Texturunterstützung in D3DX. D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bietet. Es handelt sich um eine Ebene über der Direct3D-Komponente.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Texturunterstützung in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f31a597ddcab317477d31e0d833c9da96f71ed4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404603"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a>Texturunterstützung in D3DX (Direct3D 9)

D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bietet. Es handelt sich um eine Ebene über der Direct3D-Komponente.

## <a name="textures"></a>Texturen

In den folgenden Themen werden viele verschiedene Texturen unterstützt.

-   Standardmäßige mipmapped-Texturunterstützung. Weitere [Informationen finden Sie unter Automatische Generierung von Mipmaps (Direct3D 9).](automatic-generation-of-mipmaps.md)
-   Cubezuordnungsunterstützung. Weitere Informationen [finden Sie unter Kubische Umgebungszuordnung (Direct3D 9).](cubic-environment-mapping.md)
-   Volumentexturunterstützung. Siehe [Volumetexturressourcen (Direct3D 9).](volume-texture-resources.md)
-   Unterstützung der Umgebungszuordnung. Weitere Informationen [finden Sie unter Umgebungszuordnung (Direct3D 9).](environment-mapping.md)
-   Unterstützung für die Bumpzuordnung. Weitere Informationen [finden Sie unter Bump Mapping (Direct3D 9) (Bumpzuordnung (Direct3D 9)).](bump-mapping.md)

### <a name="texture-color-conversion"></a>Texturfarbkonvertierung

Wenn Sie eine der Funktionen D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx oder D3DXCreateVolumeTexturexxx verwenden, muss möglicherweise eine Farbkonvertierung durchgeführt werden. Beispielsweise kann eine Oberfläche den Typ RGBA und die andere UVWQ haben. Bei unterschiedlichen Formaten lautet die Konvertierungssequenz wie folgt:

### <a name="mapping-rgba-to-uvwq"></a>Zuordnen von RGBA zu UVWQ

-   R <-> U, R-Kanal wird dem U-Kanal zugeordnet (oder umgekehrt).
-   G <-> V, G-Kanal wird dem V-Kanal zugeordnet (oder umgekehrt).
-   B <-> W, der B-Kanal wird dem W-Kanal zugeordnet (oder umgekehrt).
-   Ein <-> Q/L, ein Kanal wird entweder dem Q- oder dem L-Kanal zugeordnet (je nachdem, welcher kanal im Zielformat verfügbar ist) oder umgekehrt.


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a>Zuordnen von UV zu RGBA

-   U <-> R, U-Kanal wird dem R-Kanal zugeordnet (oder umgekehrt).
-   V <-> G, V-Kanal wird dem G-Kanal zugeordnet (oder umgekehrt).
-   1 <-> B, 1 wird dem B-Kanal zugeordnet (oder umgekehrt).
-   1 <-> A, 1 wird dem A-Kanal zugeordnet (oder umgekehrt).

Wenn ein Kanal in der Quelle nicht vorhanden ist, wird davon ausgegangen, dass er 1 ist (mit Ausnahme von A8, wobei R, G, B als 0 angenommen wird). Beispiel:


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3dx](d3dx.md)
</dt> </dl>

 

 



