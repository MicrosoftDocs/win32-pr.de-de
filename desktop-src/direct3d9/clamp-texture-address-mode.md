---
description: Der Klammertexturadressmodus, der durch den D3DTADDRESS \_ CLAMP-Member des D3DTEXTUREADDRESS-Enumerationstyps identifiziert wird, bewirkt, dass Direct3D Ihre Texturkoordinaten an den \[ Bereich 0,0, 1,0 \] klammert.
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Klammertexturadressmodus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0602b66c28dfbd48cc7ac3504ff643cd0ffe31769ee8edbeede5b4b870914289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751355"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a>Klammertexturadressmodus (Direct3D 9)

Der Klammertexturadressmodus, der durch den D3DTADDRESS \_ CLAMP-Member des [**D3DTEXTUREADDRESS-Enumerationstyps**](./d3dtextureaddress.md) identifiziert wird, bewirkt, dass Direct3D Ihre Texturkoordinaten an den \[ Bereich 0,0, 1,0 \] klammert. Das heißt, die Textur wird einmal angewendet, und die Farbe der Randpixel wird dann abstrichen. Angenommen, Ihre Anwendung erstellt eine quadratische Primitive und weist den Scheitelpunkten des Primitiven Texturkoordinaten von (0,0,0,0), (0,0,3,0), (3,0,3,0) und (3,0,0,0) zu. Wenn Sie den Texturadressierungsmodus auf D3DTADDRESS CLAMP festlegen, \_ wird die Textur einmal angewendet. Die Pixelfarben am oberen Rand der Spalten und das Ende der Zeilen werden nach oben und rechts des Primitivs erweitert.

Die folgende Abbildung zeigt eine klammerte Textur.

![Abbildung einer Textur und einer klammerten Textur](images/clamp.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturadressierungsmodi](texture-addressing-modes.md)
</dt> </dl>

 

 
