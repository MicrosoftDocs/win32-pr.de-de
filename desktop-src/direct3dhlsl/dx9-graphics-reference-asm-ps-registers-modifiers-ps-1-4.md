---
title: ps \_ 1 \_ 4 Quellregistermodifizierer für texld, texcrd
description: Anweisungen zur Texturadresse für zwei Pixel-Shader, Version 1 \_ 4, texld – ps \_ 1 4 und \_ texcrd – ps – verfügen über benutzerdefinierte Syntax.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 63a0cfd212767a0219af83d734d3562edacc84901098afcf77c786d8895f32d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512876"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a>ps \_ 1 \_ 4 Quellregistermodifizierer für texld, texcrd

Anweisungen zur Texturadresse für zwei Pixel-Shader, Version 1 \_ 4, [texld – ps \_ 1 \_ 4](texld---ps-1-4.md) und [texcrd – ps](texcrd---ps.md)– verfügen über benutzerdefinierte Syntax. Diese Anweisungen unterstützen ihren eigenen Satz von Quellregistermodifizierern, Quellregister-Selektoren und Zielregister-Schreibmasken, wie hier gezeigt.

## <a name="source-register-modifiers-for-texld-and-texcrd"></a>Quellregistermodifizierer für texld und texcrd

Diese Modifizierer bieten projektive Divisionsfunktionen, indem die x- und y-Werte entweder durch die z- oder w-Werte dividiert werden.



| Quellregistermodifizierer | BESCHREIBUNG                | Syntax       |
|---------------------------|----------------------------|--------------|
| \_( )                      | Dividieren von x,y-Komponenten durch z | Registrieren \_ von "Register" |
| \_db                      | Dividieren von x,y-Komponenten durch z | register \_ db |
| \_Dw                      | Dividieren von x,y-Komponenten durch w | register \_ dw |
| \_da                      | Dividieren von x,y-Komponenten durch w | register \_ da |



 

### <a name="remarks"></a>Hinweise

Der \_ \_ Modifizierer "modifizierer" oder "db" führt Folgendes aus:


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



Der \_ dw- oder \_ da-Modifizierer führt Folgendes aus:


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Modifizierer für Das Pixel-Shader-Quellregister](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




