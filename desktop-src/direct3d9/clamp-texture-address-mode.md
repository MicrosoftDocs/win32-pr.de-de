---
description: Der durch den D3DTADDRESS \_ Clamp-Member des D3DTEXTUREADDRESS-Enumerationstyps identifizierte Klemm Textur Adress Modus bewirkt, dass Direct3D die Texturkoordinaten an den \[ Bereich 0,0, 1,0, anklammert \] .
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Einspannen des Textur Adress Modus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153ed1f044bacaec6b87420eb7df22a2557349a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344223"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a><span data-ttu-id="58820-103">Einspannen des Textur Adress Modus (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="58820-103">Clamp Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="58820-104">Der durch den D3DTADDRESS \_ Clamp-Member des [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) -Enumerationstyps identifizierte Klemm Textur Adress Modus bewirkt, dass Direct3D die Texturkoordinaten an den \[ Bereich 0,0, 1,0, anklammert \] .</span><span class="sxs-lookup"><span data-stu-id="58820-104">The clamp texture address mode, identified by the D3DTADDRESS\_CLAMP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to clamp your texture coordinates to the \[0.0, 1.0\] range.</span></span> <span data-ttu-id="58820-105">Das heißt, Sie wendet die Textur einmal an und gibt dann die Farbe der edgepixel aus.</span><span class="sxs-lookup"><span data-stu-id="58820-105">That is, it applies the texture once, then smears the color of edge pixels.</span></span> <span data-ttu-id="58820-106">Nehmen Sie beispielsweise an, dass Ihre Anwendung ein quadratisches primitiv erstellt und die Texturkoordinaten (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) und (3.0, 0,0) den Scheitel Punkten des primitiven zuweist.</span><span class="sxs-lookup"><span data-stu-id="58820-106">For example, suppose that your application creates a square primitive and assigns texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0) to the primitive's vertices.</span></span> <span data-ttu-id="58820-107">Wenn Sie den Textur Adressierungs Modus auf D3DTADDRESS-Klammer festlegen, \_ wird die Textur einmal angewendet.</span><span class="sxs-lookup"><span data-stu-id="58820-107">Setting the texture addressing mode to D3DTADDRESS\_CLAMP results in the texture being applied once.</span></span> <span data-ttu-id="58820-108">Die Pixel Farben am oberen Rand der Spalten und das Ende der Zeilen werden auf den oberen bzw. rechten Rand des primitiven erweitert.</span><span class="sxs-lookup"><span data-stu-id="58820-108">The pixel colors at the top of the columns and the end of the rows are extended to the top and right of the primitive respectively.</span></span>

<span data-ttu-id="58820-109">Die folgende Abbildung zeigt eine geklehte Textur.</span><span class="sxs-lookup"><span data-stu-id="58820-109">The following illustration shows a clamped texture.</span></span>

![Abbildung einer Textur und einer geklamfferten Textur](images/clamp.png)

## <a name="related-topics"></a><span data-ttu-id="58820-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58820-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58820-112">Textur Adressierungs Modi</span><span class="sxs-lookup"><span data-stu-id="58820-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
