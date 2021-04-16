---
description: Direct3D verwendet eine Form der linearen Textur Filterung namens bilineare Filtering.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Lineare Textur Filterung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7940bd693ec42ef4f48920a5a362fad5f5b0bf02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521928"
---
# <a name="linear-texture-filtering-direct3d-9"></a><span data-ttu-id="6aedb-103">Lineare Textur Filterung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6aedb-103">Linear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="6aedb-104">Direct3D verwendet eine Form der linearen Textur Filterung namens bilineare Filtering.</span><span class="sxs-lookup"><span data-stu-id="6aedb-104">Direct3D uses a form of linear texture filtering called bilinear filtering.</span></span> <span data-ttu-id="6aedb-105">Wie bei der ersten [Stichprobenentnahme (Direct3D 9)](nearest-point-sampling.md)berechnet die bilineare Textur Filterung zuerst eine texturadresse, die in der Regel keine ganzzahlige Adresse ist.</span><span class="sxs-lookup"><span data-stu-id="6aedb-105">Like [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md), bilinear texture filtering first computes a texel address, which is usually not an integer address.</span></span> <span data-ttu-id="6aedb-106">Die bilineare Filterung findet dann den textexaus, dessen ganzzahlige Adresse der berechneten Adresse am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="6aedb-106">Bilinear filtering then finds the texel whose integer address is closest to the computed address.</span></span> <span data-ttu-id="6aedb-107">Außerdem berechnet das Direct3D-Renderingmodul einen gewichteten Durchschnitt der texeln direkt oberhalb von, Links von und rechts neben dem nächsten Beispiel Punkt.</span><span class="sxs-lookup"><span data-stu-id="6aedb-107">In addition, the Direct3D rendering module computes a weighted average of the texels that are immediately above, below, to the left of, and to the right of the nearest sample point.</span></span>

<span data-ttu-id="6aedb-108">Wählen Sie die bilineare Textur Filterung aus, indem Sie die [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6aedb-108">Select bilinear texture filtering by invoking the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="6aedb-109">Legen Sie den Wert des ersten Parameters auf die ganzzahlige Indexnummer (0-7) der Textur fest, für die Sie eine Textur Filterungs Methode auswählen.</span><span class="sxs-lookup"><span data-stu-id="6aedb-109">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are selecting a texture filtering method.</span></span> <span data-ttu-id="6aedb-110">Übergeben \_ Sie D3DSAMP MagFilter, D3DSAMP \_ MinFilter oder D3DSAMP \_ MipFilter für den zweiten Parameter, um den Filter für die Vergrößerung, minifizierung oder den Mipmapping-Filter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6aedb-110">Pass D3DSAMP\_MAGFILTER, D3DSAMP\_MINFILTER, or D3DSAMP\_MIPFILTER for the second parameter to set the magnification, minification, or mipmapping filter.</span></span> <span data-ttu-id="6aedb-111">Übergeben Sie D3DTEXF \_ linear im dritten Parameter.</span><span class="sxs-lookup"><span data-stu-id="6aedb-111">Pass D3DTEXF\_LINEAR in the third parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6aedb-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6aedb-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6aedb-113">Textur Filterung</span><span class="sxs-lookup"><span data-stu-id="6aedb-113">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 
