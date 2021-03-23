---
title: Direkte Verwendung von Konstanten in der Stamm Signatur
description: Anwendungen können Stamm Konstanten in der Stamm Signatur definieren, jeweils als Satz von 32-Bit-Werten. Sie werden in High Level Shading Language (HLSL) als konstanter Puffer angezeigt. Beachten Sie, dass Konstante Puffer aus historischen Gründen als Sätze von 4x32-Bit-Werten angezeigt werden.
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104058"
---
# <a name="using-constants-directly-in-the-root-signature"></a>Direkte Verwendung von Konstanten in der Stamm Signatur

Anwendungen können Stamm Konstanten in der Stamm Signatur definieren, jeweils als Satz von 32-Bit-Werten. Sie werden in High Level Shading Language (HLSL) als konstanter Puffer angezeigt. Beachten Sie, dass Konstante Puffer aus historischen Gründen als Sätze von 4x32-Bit-Werten angezeigt werden.

Jeder Satz von Benutzer Konstanten wird als skalares Array von 32-Bit-Werten behandelt, das dynamisch indizierbar und schreibgeschützt vom Shader ist. Out-of-Bounds-Indizierung eine bestimmte Gruppe von Stamm Konstanten erzeugt nicht definierte Ergebnisse. In HLSL können Datenstruktur Definitionen bereitgestellt werden, damit die Benutzer Konstanten Typen erhalten. Wenn die Stamm Signatur beispielsweise einen Satz von vier Stamm Konstanten definiert, kann HLSL die folgende Struktur überlagern.

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

Arrays sind in konstanten Puffern, die auf Stamm Konstanten zugeordnet werden, nicht zulässig, da die dynamische Indizierung im Stamm Signatur Bereich nicht unterstützt wird. Beispielsweise ist es ungültig, einen Eintrag im Konstanten Puffer wie zu haben `float myArray[2];` . Ein konstanter Puffer, der Stamm Konstanten zugeordnet ist, kann kein Array sein. Daher ist es ungültig, Stamm `cbuffer myCBArray[2]` Konstanten zuzuordnen.

Konstanten können teilweise festgelegt werden. Wenn die Stamm Signatur z. b. 4 32-Bit-Werte in *roottablebindslot* 2 definiert, kann jede Teilmenge der vier Konstanten gleichzeitig festgelegt werden (die anderen verbleiben unverändert). Dies kann in Paketen nützlich sein, die den Stamm Signatur Zustand erben und teilweise ändern können.

Beim Festlegen von Konstanten muss das Konstante Puffer Layout, das vom Shader erwartet wird, vorsichtig sein. Es ist möglich, dass Konstanten `vec4` z. b. an Grenzen aufgefüllt werden. Überprüfen Sie die Reflektionsinformationen aus dem HLSL-Shader, um das erwartete Layout zu überprüfen.

Die folgenden APIs (von der [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) -Schnittstelle) dienen dem direkten Festlegen von Konstanten auf der Stamm Signatur:

-   [**SetGraphicsRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [**SetComputeRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

Weitere Informationen finden Sie auch in der Struktur der D3D12-Stamm [**\_ \_ Konstanten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Stamm Signaturen](root-signatures.md)
</dt> </dl>

 

 




