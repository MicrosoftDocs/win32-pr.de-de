---
description: Eine Bump Map ist ein IDirect3DTexture9-Objekt, das ein spezielles Pixel Format verwendet.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Bump Map-Pixel Formate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21bbe4a9999d875e43d33389f86b35d22c81b3bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041497"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a><span data-ttu-id="d4180-103">Bump Map-Pixel Formate (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d4180-103">Bump Map Pixel Formats (Direct3D 9)</span></span>

<span data-ttu-id="d4180-104">Eine Bump Map ist ein [**IDirect3DTexture9**](/windows/desktop/api) -Objekt, das ein spezielles Pixel Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4180-104">A bump map is an [**IDirect3DTexture9**](/windows/desktop/api) object that uses a specialized pixel format.</span></span> <span data-ttu-id="d4180-105">Anstelle von roten, grünen und blauen Farbkomponenten speichert jedes Pixel in einer Bump-Karte die Delta Werte für Sie und v<sub>(d und d</sub> <sub>v</sub>) und manchmal eine Leuchtkraft Komponente (L). Diese Werte werden vom System angewendet, wie im Thema [Bump Mapping-Formeln (Direct3D 9)](bump-mapping-formulas.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d4180-105">Rather than storing red, green, and blue color components, each pixel in a bump map stores the delta values for u and v (D<sub>U</sub> and D<sub>V</sub>) and sometimes a luminance component, L. These values are applied by the system as described in the [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md) topic.</span></span>

<span data-ttu-id="d4180-106">Sie können ein Bump Map-Pixel Format angeben, indem Sie das Format auf eine der folgenden Einstellungen festlegen: D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8U8, D3DFMT \_ Q8W8V8U8 oder D3DFMT V16U16 \_ .</span><span class="sxs-lookup"><span data-stu-id="d4180-106">You can specify a bump map pixel format by setting the format to one of the following: D3DFMT\_CxV8U8, D3DFMT\_V8U8, D3DFMT\_L6V5U5, D3DFMT\_X8L8V8U8, D3DFMT\_Q8W8V8U8, or D3DFMT\_V16U16.</span></span> <span data-ttu-id="d4180-107">Beschreibungen finden Sie unter [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="d4180-107">For descriptions, see [D3DFORMAT](d3dformat.md).</span></span>

<span data-ttu-id="d4180-108">Die Komponenten d<sub>U</sub> und d<sub>V</sub> eines Pixels sind signierte Werte zwischen-1,0 und + 1,0.</span><span class="sxs-lookup"><span data-stu-id="d4180-108">The D<sub>U</sub> and D<sub>V</sub> components of a pixel are signed values that range from - 1.0 to +1.0.</span></span> <span data-ttu-id="d4180-109">Bei Verwendung der "Leuchtdichte"-Komponente handelt es sich um einen ganzzahligen Wert ohne Vorzeichen, der zwischen 0 und 255 liegt.</span><span class="sxs-lookup"><span data-stu-id="d4180-109">The luminance component, when used, is an unsigned integer value that ranges from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="d4180-110">Überprüfen Sie vor dem Auswählen eines Kugel Karten-Pixel Formats, ob das jeweilige Format unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d4180-110">Before picking a bump map pixel format, check if the particular format is supported.</span></span> <span data-ttu-id="d4180-111">Weitere Informationen finden Sie unter [Verwenden der Bump-Zuordnung (Direct3D 9)](using-bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="d4180-111">For more information, see [Using Bump Mapping (Direct3D 9)](using-bump-mapping.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d4180-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d4180-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4180-113">Bump-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="d4180-113">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



