---
description: Der Adressmodus der Wraptextur, der durch den D3DTADDRESS \_ WRAP-Member des D3DTEXTUREADDRESS-Enumerationstyps identifiziert wird, bewirkt, dass Direct3D die Textur auf jeder ganzzahligen Verbindung wiederholt.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Wrap Texture Address Mode (Direct3D 9) (Textur-Adressmodus umschließen (Direct3D 9))
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820273a68754c11f17f4f2762c7e824562b8e52bfc0b2b097c21e82789ce4168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627824"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a>Wrap Texture Address Mode (Direct3D 9) (Textur-Adressmodus umschließen (Direct3D 9))

Der Adressmodus der Wraptextur, der durch den D3DTADDRESS \_ WRAP-Member des [**D3DTEXTUREADDRESS-Enumerationstyps**](./d3dtextureaddress.md) identifiziert wird, bewirkt, dass Direct3D die Textur auf jeder ganzzahligen Verbindung wiederholt. Angenommen, Ihre Anwendung erstellt eine quadratische Primitive und gibt Texturkoordinaten von (0,0,0,0), (0,0,3,0), (3,0,3,0) und (3,0,0,0) an. Wenn Sie den Texturadressierungsmodus auf D3DTADDRESS \_ WRAP festlegen, wird die Textur dreimal in u- und v-Richtung angewendet, wie in der folgenden Abbildung dargestellt.

![Abbildung einer Gesichtstextur, die in u-Richtung und v-Richtung umschlossen ist](images/wrap.png)

Die Auswirkungen dieses Texturadressmodus ähneln denen des Spiegelmodus, unterscheiden sich jedoch von diesen. Weitere Informationen finden Sie unter [Spiegeltexturadressmodus (Direct3D 9).](mirror-texture-address-mode.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturadressierungsmodi](texture-addressing-modes.md)
</dt> </dl>

 

 
