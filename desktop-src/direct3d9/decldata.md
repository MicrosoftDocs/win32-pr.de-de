---
description: Beschreibt eine Scheitelpunkt Deklaration.
ms.assetid: 6a95bdf6-8767-4ad3-bcec-b32858d25571
title: Decldata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a26d667f853db3044db3155c55eb4a6d941c6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481115"
---
# <a name="decldata"></a>Decldata

Beschreibt eine Scheitelpunkt Deklaration.

``` syntax
template DeclData
{
    < BF22E553-292C-4781-9FEA-62BD554BDD93 >
    DWORD nElements;
    array VertexElement Elements[nElements];
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

Hierbei gilt:

-   nelements: Anzahl der Scheitelpunkt Deklarations Elemente.
-   Elemente \[ nelements \] -Array von Vertex-Deklarations Elementen.
-   ndwords: Anzahl der DWORDs.
-   Data \[ ndwords \] : Array von DWords, die die Daten in jedem Scheitelpunkt Element enthalten.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



