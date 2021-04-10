---
description: Beschreibt ein einzelnes Vertex-Element in einer Scheitelpunkt Deklaration.
ms.assetid: efe3e98b-938d-4d4c-b790-2b8c8aab0ded
title: Vertexelement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 049511c89b335c0da31a9f41344082c3b818fa0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124742"
---
# <a name="vertexelement"></a>Vertexelement

Beschreibt ein einzelnes Vertex-Element in einer Scheitelpunkt Deklaration.

``` syntax
template VertexElement 
{ 
    < F752461C-1E23-48f6-B9F8-8350850F336F > 
    DWORD Type; 
    DWORD Method; 
    DWORD Usage; 
    DWORD UsageIndex; 
} 
```

Hierbei gilt:

-   Type-Scheitelpunkt Datentyp. Siehe [**D3DDECLTYPE**](./d3ddecltype.md).
-   Method-Mosaik Verarbeitungsmethode. Siehe [**D3DDECLMETHOD**](./d3ddeclmethod.md).
-   Verwendungs orientierte Verwendung der Vertexdaten. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).
-   "Start": ändert die Verwendungs Daten. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)
</dt> </dl>

 

 
