---
description: Der Spiegeltextur-Adressmodus, der vom D3DTADDRESS MIRROR-Member des \_ aufzählten D3DTEXTUREADDRESS-Typs identifiziert wird, bewirkt, dass Direct3D die Textur an jeder ganzzahligen Grenze spiegelt.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Spiegeltextur-Adressmodus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ef8731c060e95c470bbf8d34222b9ee66e7f9da2c7a6f03a09c2989986ca3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728366"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a>Spiegeltextur-Adressmodus (Direct3D 9)

Der Spiegeltextur-Adressmodus, der vom D3DTADDRESS MIRROR-Member des \_ [**aufzählten D3DTEXTUREADDRESS-Typs**](./d3dtextureaddress.md) identifiziert wird, bewirkt, dass Direct3D die Textur an jeder ganzzahligen Grenze spiegelt. Angenommen, Ihre Anwendung erstellt eine quadratische Primitive und gibt Texturkoordinaten von (0,0,0,0), (0,0, 3,0), (3,0, 3,0) und (3,0,0,0) an. Wenn Sie den Texturadrierungsmodus auf D3DTADDRESS MIRROR festlegen, wird die Textur dreimal in u- und \_ v-Richtung angewendet. Jede andere Zeile und Spalte, auf die sie angewendet wird, ist ein Spiegelbild der vorangehenden Zeile oder Spalte, wie in der folgenden Abbildung dargestellt.

![Abbildung von Spiegelbildern in einem 3x3-Raster](images/mirror.png)

Die Auswirkungen dieses Texturadressenmodus ähneln denen des Wrap-Modus, unterscheiden sich jedoch von diesen. Weitere Informationen finden Sie unter [Umschließen des Texturadressenmodus (Direct3D 9).](wrap-texture-address-mode.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur adressierungsmodi](texture-addressing-modes.md)
</dt> </dl>

 

 
