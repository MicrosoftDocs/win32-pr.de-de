---
description: Der Umbruch-Textur Adress Modus, der durch den D3DTADDRESS \_ Wrap-Member des D3DTEXTUREADDRESS-Enumerationstyps identifiziert wird, bewirkt, dass Direct3D die Textur für jede ganzzahlige Verknüpfung wiederholt
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Wrap-Textur Adress Modus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721ace45599236022f32e6b0ec3723e346befbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213838"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a><span data-ttu-id="54340-103">Wrap-Textur Adress Modus (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="54340-103">Wrap Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="54340-104">Der Umbruch-Textur Adress Modus, der durch den D3DTADDRESS \_ Wrap-Member des [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) -Enumerationstyps identifiziert wird, bewirkt, dass Direct3D die Textur für jede ganzzahlige Verknüpfung wiederholt</span><span class="sxs-lookup"><span data-stu-id="54340-104">The wrap texture address mode, identified by the D3DTADDRESS\_WRAP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, makes Direct3D repeat the texture on every integer junction.</span></span> <span data-ttu-id="54340-105">Angenommen, Ihre Anwendung erstellt ein quadratisches primitiv und gibt Texturkoordinaten von (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) und (3.0, 0,0) an.</span><span class="sxs-lookup"><span data-stu-id="54340-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="54340-106">Wenn Sie den Textur Adressierungs Modus auf D3DTADDRESS \_ Wrap festlegen, wird die Textur dreimal in den u-und v-Richtungen angewendet, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="54340-106">Setting the texture addressing mode to D3DTADDRESS\_WRAP results in the texture being applied three times in both the u-and v-directions, as shown in the following illustration.</span></span>

![Abbildung einer Gesichts Textur, die in der u-Richtung und der v-Richtung umschließt](images/wrap.png)

<span data-ttu-id="54340-108">Die Auswirkungen dieses Textur Adress Modus ähneln denen des Spiegelmodus, unterscheiden sich jedoch davon.</span><span class="sxs-lookup"><span data-stu-id="54340-108">The effects of this texture address mode are similar to, but distinct from, those of the mirror mode.</span></span> <span data-ttu-id="54340-109">Weitere Informationen finden Sie unter [Spiegel Textur Adress Modus (Direct3D 9)](mirror-texture-address-mode.md).</span><span class="sxs-lookup"><span data-stu-id="54340-109">For more information, see [Mirror Texture Address Mode (Direct3D 9)](mirror-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="54340-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54340-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54340-111">Textur Adressierungs Modi</span><span class="sxs-lookup"><span data-stu-id="54340-111">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
