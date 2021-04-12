---
description: Der durch den D3DTADDRESS \_ Border-Member des D3DTEXTUREADDRESS-Enumerationstyps identifizierte Rahmen Farb Textur-Adress Modus bewirkt, dass Direct3D eine beliebige Farbe, die als Rahmenfarbe bezeichnet wird, für alle Texturkoordinaten außerhalb des Bereichs von 0,0 bis einschließlich 1,0 verwendet.
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: Border Color Texture Address Mode (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42b18d88f3b9305d0602e43a9528357a9397d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393166"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a>Border Color Texture Address Mode (Direct3D 9)

Der durch den D3DTADDRESS \_ Border-Member des [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) -Enumerationstyps identifizierte Rahmen Farb Textur-Adress Modus bewirkt, dass Direct3D eine beliebige Farbe, die als Rahmenfarbe bezeichnet wird, für alle Texturkoordinaten außerhalb des Bereichs von 0,0 bis einschließlich 1,0 verwendet.

In der folgenden Abbildung gibt die Anwendung an, dass die Textur auf die primitive mithilfe eines roten Rahmens angewendet werden soll.

![Abbildung einer Textur und einer Textur mit einem roten Rahmen](images/border.png)

Anwendungen legen die Rahmenfarbe durch Aufrufen von [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)fest. Legen Sie den ersten Parameter für den aufrufswert des gewünschten Textur Stufen Bezeichners, den zweiten Parameter für den D3DSAMP \_ BorderColor Stage State-Wert und den dritten Parameter für die neue RGBA-Rahmenfarbe fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Adressierungs Modi](texture-addressing-modes.md)
</dt> </dl>

 

 
