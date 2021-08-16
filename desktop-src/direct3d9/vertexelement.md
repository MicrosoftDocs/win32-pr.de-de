---
description: Beschreibt ein einzelnes Scheitelpunktelement in einer Scheitelpunktdeklaration.
ms.assetid: efe3e98b-938d-4d4c-b790-2b8c8aab0ded
title: VertexElement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2ecef6cfa8c522532599acef1b83343c64edd2b5eca93fe461d8bf8419ada8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518852"
---
# <a name="vertexelement"></a>VertexElement

Beschreibt ein einzelnes Scheitelpunktelement in einer Scheitelpunktdeklaration.

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

-   Typ: Vertexdatentyp. Siehe [**D3DDECLTYPE**](./d3ddecltype.md).
-   Methode: Tessellator-Verarbeitungsmethode. Siehe [**D3DDECLMETHOD**](./d3ddeclmethod.md).
-   Verwendung: Beabsichtigte Verwendung der Scheitelpunktdaten. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).
-   UsageIndex: Ändert die Nutzungsdaten. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)
</dt> </dl>

 

 
