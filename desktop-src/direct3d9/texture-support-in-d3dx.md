---
description: D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Textur Unterstützung in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9c8d6da498a47d14fe57ca770ba96a6852ae41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339643"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a>Textur Unterstützung in D3DX (Direct3D 9)

D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.

## <a name="textures"></a>Texturen

In den folgenden Themen werden viele verschiedene Texturen unterstützt.

-   Standard mäßige Mipmapping-Textur Unterstützung. Weitere Informationen finden Sie [unter Automatische Generierung von Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).
-   Cubezuordnungs Unterstützung. Siehe [kubische Umgebungs Zuordnung (Direct3D 9)](cubic-environment-mapping.md).
-   Volumetextur-Unterstützung. Weitere Informationen finden Sie unter [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).
-   Unterstützung der Umgebungs Zuordnung. Weitere Informationen finden Sie unter [Umgebungs Zuordnung (Direct3D 9)](environment-mapping.md).
-   Unterstützung der Bump-Zuordnung. Weitere Informationen finden Sie unter [Bump Mapping (Direct3D 9)](bump-mapping.md).

### <a name="texture-color-conversion"></a>Textur Farbkonvertierung

Bei Verwendung einer der Funktionen D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx oder D3DXCreateVolumeTexturexxx muss ggf. eine Farbkonvertierung durchgeführt werden. Eine Oberfläche könnte z. b. den Typ RGBA aufweisen, die andere z. b. uvwq. In Fällen mit unterschiedlichen Formaten lautet die Konvertierungs Sequenz wie folgt:

### <a name="mapping-rgba-to-uvwq"></a>Zuordnung von RGBA zu uvwq

-   R <-> u, der r-Kanal wird dem U-Kanal zugeordnet oder umgekehrt.
-   G <-> v, der g-Kanal dem v-Kanal zugeordnet ist, oder umgekehrt.
-   B <-> w, b-Kanal wird dem W-Kanal zugeordnet oder umgekehrt.
-   Ein < > q/L, ein Kanal ist entweder dem q-oder dem L-Kanal (abhängig davon, welcher im Zielformat verfügbar ist) oder umgekehrt zugeordnet.


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a>Zuordnung von UV zu RGBA

-   U <-> r, u-Kanal wird dem R-Kanal zugeordnet oder umgekehrt.
-   V <-> g, der v-Kanal wird dem G-Kanal zugeordnet oder umgekehrt.
-   1 <-> b, 1 wird dem b-Kanal zugeordnet oder umgekehrt.
-   1 <-> a, 1 wird dem Kanal zugeordnet oder umgekehrt.

Wenn ein Kanal nicht in der Quelle vorhanden ist, wird davon ausgegangen, dass er 1 ist (mit Ausnahme von A8, wobei R, G, B als 0 angenommen wird). Beispiel:


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



