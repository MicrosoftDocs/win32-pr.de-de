---
title: Quellen Register-Bias
description: Subtrahieren Sie 0,5 von allen Komponenten.
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948087"
---
# <a name="source-register-bias"></a>Quellen Register-Bias

Subtrahieren Sie 0,5 von allen Komponenten.

## <a name="registers"></a>Register

Quell Register. Weitere Informationen zu Register Typen finden Sie unter [PS \_ 1 1 PS 1 \_ \_ \_ \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Bemerkungen

Der Inhalt des Registers wird nicht geändert. Der-Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet. Der Bias wird wie folgt auf alle vier Farbkanäle (RGBA) angewendet:


```
output = (input - 0.5)
```



Der Effekt besteht darin, die Daten im Bereich von 0 bis 1 im Bereich von-0,5 bis 0,5 zu ändern. Das Anwenden von Bias auf Daten außerhalb dieses Bereichs kann zu undefinierten Ergebnissen führen.

> [!Note]  
> Dieser Modifizierer schließt sich mit dem [Quell Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)gegenseitig aus und kann daher nicht auf dasselbe Register angewendet werden.

 

Dieser Modifizierer ist für die Verwendung mit arithmetischen Anweisungen vorgesehen.

## <a name="example"></a>Beispiel

In diesem Beispiel wird der gleiche Vorgang wie D3DTOP \_ AddSigned in DirectX 6,0 und 7,0 multiple texture-Syntax durchführt.


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader-quellregistrierungs Modifizierern](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




