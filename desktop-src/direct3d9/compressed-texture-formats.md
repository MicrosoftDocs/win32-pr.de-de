---
description: Dieser Abschnitt enthält Informationen über die interne Organisation von komprimierten Textur Formaten.
ms.assetid: a916d635-2be4-48be-ba70-a743b2969553
title: Komprimierte Textur Formate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcecf6e98d125f3a391ab0e7a7c569a8dbd27d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748800"
---
# <a name="compressed-texture-formats-direct3d-9"></a><span data-ttu-id="24e88-103">Komprimierte Textur Formate (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="24e88-103">Compressed Texture Formats (Direct3D 9)</span></span>

<span data-ttu-id="24e88-104">Dieser Abschnitt enthält Informationen über die interne Organisation von komprimierten Textur Formaten.</span><span class="sxs-lookup"><span data-stu-id="24e88-104">This section contains information about the internal organization of compressed texture formats.</span></span> <span data-ttu-id="24e88-105">Sie benötigen diese Details nicht zur Verwendung komprimierter Texturen, da Sie D3DX-Funktionen für die Konvertierung in und aus komprimierten Formaten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="24e88-105">You do not need these details to use compressed textures, because you can use D3DX functions for conversion to and from compressed formats.</span></span> <span data-ttu-id="24e88-106">Diese Informationen sind jedoch nützlich, wenn Sie direkt mit komprimierten Oberflächendaten arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="24e88-106">However, this information is useful if you want to operate on compressed surface data directly.</span></span>

<span data-ttu-id="24e88-107">Direct3D verwendet ein Komprimierungs Format, das Textur Zuordnungen in 4 x 4 textrotze unterteilt.</span><span class="sxs-lookup"><span data-stu-id="24e88-107">Direct3D uses a compression format that divides texture maps into 4x4 texel blocks.</span></span> <span data-ttu-id="24e88-108">Wenn die Textur keine Transparenz enthält (nicht transparent) oder wenn die Transparenz durch ein 1-Bit-Alpha angegeben wird, stellt ein 8-Byte-Block den Textur Zuordnungs Block dar.</span><span class="sxs-lookup"><span data-stu-id="24e88-108">If the texture contains no transparency - is opaque - or if the transparency is specified by a 1-bit alpha, an 8-byte block represents the texture map block.</span></span> <span data-ttu-id="24e88-109">Wenn die Textur Zuordnung transparente Texels mit einem Alphakanal enthält, stellt Sie einen 16-Byte-Block dar.</span><span class="sxs-lookup"><span data-stu-id="24e88-109">If the texture map does contain transparent texels, using an alpha channel, a 16-byte block represents it.</span></span>

-   [<span data-ttu-id="24e88-110">Undurchsichtige und 1-Bit-Alpha Texturen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="24e88-110">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>](opaque-and-1-bit-alpha-textures.md)
-   [<span data-ttu-id="24e88-111">Texturen mit Alpha Kanälen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="24e88-111">Textures with Alpha Channels (Direct3D 9)</span></span>](textures-with-alpha-channels.md)

<span data-ttu-id="24e88-112">Jede einzelne Textur muss angeben, dass Ihre Daten als 64-oder 128 Bits pro Gruppe von 16 texeln gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="24e88-112">Any single texture must specify that its data is stored as 64 or 128 bits per group of 16 texels.</span></span> <span data-ttu-id="24e88-113">Wenn 64-Bit-Blöcke, d. h. Format DXT1, für die Textur verwendet werden, ist es möglich, die nicht transparenten und 1-Bit-Alpha Formate auf Block Basis innerhalb derselben Textur zu mischen.</span><span class="sxs-lookup"><span data-stu-id="24e88-113">If 64-bit blocks - that is, format DXT1 - are used for the texture, it is possible to mix the opaque and 1-bit alpha formats on a per-block basis within the same texture.</span></span> <span data-ttu-id="24e88-114">Anders ausgedrückt: der Vergleich der Größenordnung ohne Vorzeichen von Farbe \_ 0 und Farbe \_ 1 wird für jeden Block von 16 texeln eindeutig ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24e88-114">In other words, the comparison of the unsigned integer magnitude of color\_0 and color\_1 is performed uniquely for each block of 16 texels.</span></span>

<span data-ttu-id="24e88-115">Wenn 128-Bit-Blöcke verwendet werden, muss der Alphakanal entweder im expliziten Format (Format DXT2 oder DXT3) oder im interinterinterformatierten Modus (Format DXT4 oder DXT5) für die gesamte Textur angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="24e88-115">When 128-bit blocks are used, the alpha channel must be specified in either explicit (format DXT2 or DXT3) or interpolated mode (format DXT4 or DXT5) for the entire texture.</span></span> <span data-ttu-id="24e88-116">Wenn der interaktivierte Modus ausgewählt ist, können die beiden acht interaktivierten Premultiplied-und sechs interpoliert Premultiplied-Modi in Form von Farben für blockweise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24e88-116">As with color, when interpolated mode is selected, either eight interpolated alphas or six interpolated alphas mode can be used on a block-by-block basis.</span></span> <span data-ttu-id="24e88-117">Auch hier wird der Größenvergleich von Alpha \_ 0 und Alpha \_ 1 eindeutig auf Block-für-Block-Basis durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="24e88-117">Again the magnitude comparison of alpha\_0 and alpha\_1 is done uniquely on a block-by-block basis.</span></span>

<span data-ttu-id="24e88-118">Die Tonhöhe für DXTn-Formate unterscheidet sich von dem, was in DirectX 7,0 zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="24e88-118">The pitch for DXTn formats is different from what was returned in DirectX 7.0.</span></span> <span data-ttu-id="24e88-119">Die Tonhöhe wird jetzt in Bytes (nicht in Blöcken) gemessen.</span><span class="sxs-lookup"><span data-stu-id="24e88-119">Pitch is now measured in bytes (not blocks).</span></span> <span data-ttu-id="24e88-120">Wenn Sie z. b. eine Breite von 16 haben, verfügen Sie über eine Höhe von vier Blöcken (4 \* 8 für DXT1, 4 \* 16 für DXT2-5).</span><span class="sxs-lookup"><span data-stu-id="24e88-120">For example, if you have a width of 16, then you will have a pitch of four blocks (4\*8 for DXT1, 4\*16 for DXT2-5).</span></span>

## <a name="related-topics"></a><span data-ttu-id="24e88-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24e88-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24e88-122">Komprimierte Textur Ressourcen</span><span class="sxs-lookup"><span data-stu-id="24e88-122">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



