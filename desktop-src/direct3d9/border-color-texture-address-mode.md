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
# <a name="border-color-texture-address-mode-direct3d-9"></a><span data-ttu-id="d1e77-103">Border Color Texture Address Mode (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d1e77-103">Border Color Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="d1e77-104">Der durch den D3DTADDRESS \_ Border-Member des [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) -Enumerationstyps identifizierte Rahmen Farb Textur-Adress Modus bewirkt, dass Direct3D eine beliebige Farbe, die als Rahmenfarbe bezeichnet wird, für alle Texturkoordinaten außerhalb des Bereichs von 0,0 bis einschließlich 1,0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1e77-104">The border color texture address mode, identified by the D3DTADDRESS\_BORDER member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to use an arbitrary color, known as the border color, for any texture coordinates outside the range of 0.0 through 1.0, inclusive.</span></span>

<span data-ttu-id="d1e77-105">In der folgenden Abbildung gibt die Anwendung an, dass die Textur auf die primitive mithilfe eines roten Rahmens angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1e77-105">In the following illustration, the application specifies that the texture be applied to the primitive using a red border.</span></span>

![Abbildung einer Textur und einer Textur mit einem roten Rahmen](images/border.png)

<span data-ttu-id="d1e77-107">Anwendungen legen die Rahmenfarbe durch Aufrufen von [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)fest.</span><span class="sxs-lookup"><span data-stu-id="d1e77-107">Applications set the border color by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="d1e77-108">Legen Sie den ersten Parameter für den aufrufswert des gewünschten Textur Stufen Bezeichners, den zweiten Parameter für den D3DSAMP \_ BorderColor Stage State-Wert und den dritten Parameter für die neue RGBA-Rahmenfarbe fest.</span><span class="sxs-lookup"><span data-stu-id="d1e77-108">Set the first parameter for the call to the desired texture stage identifier, the second parameter to the D3DSAMP\_BORDERCOLOR stage state value, and the third parameter to the new RGBA border color.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1e77-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d1e77-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1e77-110">Textur Adressierungs Modi</span><span class="sxs-lookup"><span data-stu-id="d1e77-110">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
