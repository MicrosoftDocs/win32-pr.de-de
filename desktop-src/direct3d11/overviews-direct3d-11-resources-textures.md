---
title: Texturen
description: In diesem Abschnitt werden die in Direct3D 11 verwendeten Texturen und Links zur aufgabenbasierten Dokumentation für gängige Szenarios beschrieben.
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc3909f354b0709e82ffd2bdffafe6cdb35516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207075"
---
# <a name="textures"></a><span data-ttu-id="b4551-103">Texturen</span><span class="sxs-lookup"><span data-stu-id="b4551-103">Textures</span></span>

<span data-ttu-id="b4551-104">In einer Textur werden Texel-Informationen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b4551-104">A texture stores texel information.</span></span> <span data-ttu-id="b4551-105">In diesem Abschnitt werden die in Direct3D 11 verwendeten Texturen und Links zur aufgabenbasierten Dokumentation für gängige Szenarios beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b4551-105">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b4551-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b4551-106">In this section</span></span>



| <span data-ttu-id="b4551-107">Thema</span><span class="sxs-lookup"><span data-stu-id="b4551-107">Topic</span></span>                                                                                                    | <span data-ttu-id="b4551-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4551-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4551-109">Einführung in Texturen in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b4551-109">Introduction To Textures in Direct3D 11</span></span>](overviews-direct3d-11-resources-textures-intro.md)<br/> | <span data-ttu-id="b4551-110">Eine Textur Ressource ist eine strukturierte Sammlung von Daten, die zum Speichern von texeln entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="b4551-110">A texture resource is a structured collection of data designed to store texels.</span></span> <span data-ttu-id="b4551-111">Ein Texel stellt die kleinste Einheit einer Textur dar, die von der Pipeline gelesen oder geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="b4551-111">A texel represents the smallest unit of a texture that can be read or written to by the pipeline.</span></span> <span data-ttu-id="b4551-112">Im Gegensatz zu puffern können Texturen durch Textur-samplz gefiltert werden, wenn Sie von Shader-Einheiten gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="b4551-112">Unlike buffers, textures can be filtered by texture samplers as they are read by shader units.</span></span> <span data-ttu-id="b4551-113">Der Typ der Textur wirkt sich darauf aus, wie die Textur gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="b4551-113">The type of texture impacts how the texture is filtered.</span></span> <span data-ttu-id="b4551-114">Jede texumeration enthält 1 bis 4 Komponenten, die in einem der DXGI-Formate angeordnet sind, die durch die Enumeration des DXGI-Formats definiert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="b4551-114">Each texel contains 1 to 4 components, arranged in one of the DXGI formats defined by the DXGI\_FORMAT enumeration.</span></span><br/> |
| [<span data-ttu-id="b4551-115">Textur Block Komprimierung in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b4551-115">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)<br/>      | <span data-ttu-id="b4551-116">Block Komprimierungs Unterstützung (BC) für Texturen wurde in Direct3D 11 erweitert, um die BC6H-und bzw bc7-Algorithmen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="b4551-116">Block Compression (BC) support for textures has been extended in Direct3D 11 to include the BC6H and BC7 algorithms.</span></span> <span data-ttu-id="b4551-117">BC6H unterstützt Datenquellen Daten mit hoher dynamischer Bereichs Farbe, und bzw bc7 bietet eine bessere Qualitäts Komprimierung mit weniger Artefakten für Standard-RGB-Quelldaten.</span><span class="sxs-lookup"><span data-stu-id="b4551-117">BC6H supports high-dynamic range color source data, and BC7 provides better-than-average quality compression with less artifacts for standard RGB source data.</span></span><br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="b4551-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4551-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4551-119">Vorgehensweise: Erstellen einer Textur</span><span class="sxs-lookup"><span data-stu-id="b4551-119">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[<span data-ttu-id="b4551-120">Gewusst wie: Programm gesteuertes Initialisieren einer Textur</span><span class="sxs-lookup"><span data-stu-id="b4551-120">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[<span data-ttu-id="b4551-121">Gewusst wie: Initialisieren einer Textur aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="b4551-121">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[<span data-ttu-id="b4551-122">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b4551-122">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





