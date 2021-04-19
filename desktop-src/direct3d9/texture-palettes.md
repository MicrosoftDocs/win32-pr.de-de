---
description: Direct3D 9 unterstützt Palettentexturen durch eine Reihe von 256-Einträge, die mit dem IDirect3DDevice9-Objekt verknüpft sind.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Textur Paletten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a0fbb1c5d6766b879b898145ec2385a41d94b8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346398"
---
# <a name="texture-palettes-direct3d-9"></a><span data-ttu-id="72658-103">Textur Paletten (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="72658-103">Texture Palettes (Direct3D 9)</span></span>

<span data-ttu-id="72658-104">Direct3D 9 unterstützt Palettentexturen durch eine Reihe von 256-Einträge, die mit dem [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Objekt verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="72658-104">Direct3D 9 supports paletted textures through a set of 256 entry palettes associated with the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) object.</span></span> <span data-ttu-id="72658-105">Eine Palette wird durch Aufrufen der [**IDirect3DDevice9:: setcurrenttexturepalette**](/windows/desktop/api) -Methode aktuell gemacht.</span><span class="sxs-lookup"><span data-stu-id="72658-105">A palette is made current by calling the [**IDirect3DDevice9::SetCurrentTexturePalette**](/windows/desktop/api) method.</span></span> <span data-ttu-id="72658-106">Mit der aktuellen Palette werden alle Palettentexturen für alle aktiven Textur Stufen übersetzt.</span><span class="sxs-lookup"><span data-stu-id="72658-106">The current palette is used for translating all paletted textures for all active texture stages.</span></span> <span data-ttu-id="72658-107">[**IDirect3DDevice9:: setpaletteentries**](/windows/desktop/api) aktualisiert alle 256-Einträge einer Palette.</span><span class="sxs-lookup"><span data-stu-id="72658-107">[**IDirect3DDevice9::SetPaletteEntries**](/windows/desktop/api) updates all of a palette's 256 entries.</span></span> <span data-ttu-id="72658-108">Jeder Eintrag ist eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur im Format D3DFMT \_ A8R8G8B8.</span><span class="sxs-lookup"><span data-stu-id="72658-108">Each entry is a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure of the format D3DFMT\_A8R8G8B8.</span></span> <span data-ttu-id="72658-109">Alle Einträge werden standardmäßig auf "0xffffffff" eingestellt.</span><span class="sxs-lookup"><span data-stu-id="72658-109">All entries default to 0xFFFFFFFF.</span></span>

<span data-ttu-id="72658-110">Die [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) Paletten enthalten einen Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="72658-110">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) palettes contain an alpha channel.</span></span> <span data-ttu-id="72658-111">Dieser Alphakanal kann verwendet werden, wenn das D3DPTEXTURECAPS \_ alphapalette Device Capability-Flag festgelegt ist, was bedeutet, dass das Gerät Alpha aus der Palette unterstützt.</span><span class="sxs-lookup"><span data-stu-id="72658-111">This alpha channel can be used when the D3DPTEXTURECAPS\_ALPHAPALETTE device capability flag is set, indicating that the device supports alpha from the palette.</span></span> <span data-ttu-id="72658-112">Der palettenalpha Kanal wird verwendet, wenn das Textur Format keinen Alpha-Kanal hat.</span><span class="sxs-lookup"><span data-stu-id="72658-112">The palette alpha channel is used when the texture format does not have an alpha channel.</span></span> <span data-ttu-id="72658-113">Wenn das Gerät Alpha aus der Palette nicht unterstützt und das Textur Format keinen Alphakanal aufweist, wird der Wert 0xFF für Alpha verwendet.</span><span class="sxs-lookup"><span data-stu-id="72658-113">If the device does not support alpha from the palette and the texture format does not have an alpha channel, then a value of 0xFF is used for alpha.</span></span>

<span data-ttu-id="72658-114">Es sind maximal 65.536 (0X0000FFFF) Paletten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="72658-114">There is a maximum of 65,536 (0x0000FFFF) palettes.</span></span> <span data-ttu-id="72658-115">Da die dem Satz von Paletten zugeordneten Speicherressourcen proportional zur maximalen Palettennummer sind, auf die eine Anwendung verweist, verwenden Sie angrenzende Palettennummern, beginnend bei Null.</span><span class="sxs-lookup"><span data-stu-id="72658-115">Because memory resources associated with the set of palettes are proportional to the maximum palette number that an application references, use contiguous palette numbers starting at zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72658-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72658-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72658-117">Grundlegende Konzepte der Texturierung</span><span class="sxs-lookup"><span data-stu-id="72658-117">Basic Texturing Concepts</span></span>](basic-texturing-concepts.md)
</dt> </dl>

 

 
