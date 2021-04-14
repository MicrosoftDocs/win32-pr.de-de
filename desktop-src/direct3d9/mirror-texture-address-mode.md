---
description: Der vom D3DTADDRESS- \_ Spiegelungs Member des D3DTEXTUREADDRESS-Enumerationstyps identifizierte Spiegel Textur Adress Modus bewirkt, dass Direct3D die Textur an allen ganzzahligen Grenzen spiegelt.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Spiegel Textur Adress Modus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471ad8b715d9375947162c66474687b9d6376bec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392537"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a><span data-ttu-id="d6660-103">Spiegel Textur Adress Modus (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d6660-103">Mirror Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="d6660-104">Der vom D3DTADDRESS- \_ Spiegelungs Member des [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) -Enumerationstyps identifizierte Spiegel Textur Adress Modus bewirkt, dass Direct3D die Textur an allen ganzzahligen Grenzen spiegelt.</span><span class="sxs-lookup"><span data-stu-id="d6660-104">The mirror texture address mode, identified by the D3DTADDRESS\_MIRROR member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to mirror the texture at every integer boundary.</span></span> <span data-ttu-id="d6660-105">Angenommen, Ihre Anwendung erstellt ein quadratisches primitiv und gibt Texturkoordinaten von (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) und (3.0, 0,0) an.</span><span class="sxs-lookup"><span data-stu-id="d6660-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="d6660-106">Wenn Sie den Textur Adressierungs Modus auf D3DTADDRESS- \_ Spiegelung festlegen, wird die Textur dreimal in den u-und v-Richtungen angewendet.</span><span class="sxs-lookup"><span data-stu-id="d6660-106">Setting the texture addressing mode to D3DTADDRESS\_MIRROR results in the texture being applied three times in both the u- and v-directions.</span></span> <span data-ttu-id="d6660-107">Jede andere Zeile und Spalte, auf die Sie angewendet wird, ist ein Spiegelbild der vorangehenden Zeile oder Spalte, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d6660-107">Every other row and column that it is applied to is a mirror image of the preceding row or column, as shown in the following illustration.</span></span>

![Abbildung von Spiegelbildern in einem 3X3-Raster](images/mirror.png)

<span data-ttu-id="d6660-109">Die Auswirkungen dieses Textur Adress Modus ähneln denen des Umbruch Modus, unterscheiden sich jedoch davon.</span><span class="sxs-lookup"><span data-stu-id="d6660-109">The effects of this texture address mode are similar to, but distinct from, those of the wrap mode.</span></span> <span data-ttu-id="d6660-110">Weitere Informationen finden Sie unter [Wrap Texture Address Mode (Direct3D 9)](wrap-texture-address-mode.md).</span><span class="sxs-lookup"><span data-stu-id="d6660-110">For more information, see [Wrap Texture Address Mode (Direct3D 9)](wrap-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6660-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d6660-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6660-112">Textur Adressierungs Modi</span><span class="sxs-lookup"><span data-stu-id="d6660-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
