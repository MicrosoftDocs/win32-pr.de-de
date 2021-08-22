---
description: Der Texturadressmodus der Rahmenfarbe, der durch den D3DTADDRESS \_ BORDER-Member des D3DTEXTUREADDRESS-Enumerationstyps identifiziert wird, bewirkt, dass Direct3D eine beliebige Farbe, die als Rahmenfarbe bezeichnet wird, für alle Texturkoordinaten außerhalb des Bereichs von 0,0 bis 1,0 einschließlich verwendet.
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: Texturadressmodus für Rahmenfarbe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e0685359227f80a847174157117e90116cffe8e61a48e172451a83aa8ec5fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496315"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a>Texturadressmodus für Rahmenfarbe (Direct3D 9)

Der Texturadressmodus der Rahmenfarbe, der durch den D3DTADDRESS \_ BORDER-Member des [**D3DTEXTUREADDRESS-Enumerationstyps**](./d3dtextureaddress.md) identifiziert wird, bewirkt, dass Direct3D eine beliebige Farbe, die als Rahmenfarbe bezeichnet wird, für alle Texturkoordinaten außerhalb des Bereichs von 0,0 bis 1,0 einschließlich verwendet.

In der folgenden Abbildung gibt die Anwendung an, dass die Textur mithilfe eines roten Rahmens auf den Primitiven angewendet werden soll.

![Abbildung einer Textur und einer Textur mit einem roten Rahmen](images/border.png)

Anwendungen legen die Rahmenfarbe fest, indem [**sie IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)aufrufen. Legen Sie den ersten Parameter für den Aufruf des gewünschten Texturstufenbezeichners, den zweiten Parameter auf den D3DSAMP \_ BORDERCOLOR-Stufenzustandswert und den dritten Parameter auf die neue RGBA-Rahmenfarbe fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturadressierungsmodi](texture-addressing-modes.md)
</dt> </dl>

 

 
