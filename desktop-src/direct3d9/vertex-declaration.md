---
description: Eine Scheitelpunkt Deklaration definiert das vertexpufferlayout und die Programme der Mosaik-Engine.
ms.assetid: 09dae498-3b33-4c33-bc7e-47f2bf784e4c
title: Vertex-Deklaration (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c769aa6fb80de1fd83067ebb9f32b591baa8e883
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345581"
---
# <a name="vertex-declaration-direct3d-9"></a><span data-ttu-id="0903e-103">Vertex-Deklaration (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0903e-103">Vertex Declaration (Direct3D 9)</span></span>

<span data-ttu-id="0903e-104">Eine Scheitelpunkt Deklaration definiert das vertexpufferlayout und die Programme der Mosaik-Engine.</span><span class="sxs-lookup"><span data-stu-id="0903e-104">A vertex declaration defines the vertex buffer layout and programs the tessellation engine.</span></span> <span data-ttu-id="0903e-105">Ab Direct3D 9 werden Scheitelpunkt Datenströme als Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Strukturen ausgedrückt (anstatt flexible Scheitelpunkt Formate (FVF)) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0903e-105">Starting with Direct3D 9, vertex streams are expressed as an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures (instead of using flexible vertex format (FVF) codes).</span></span> <span data-ttu-id="0903e-106">Jedes Array Element beschreibt jeden Datentyp pro Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="0903e-106">Each array element describes each per-vertex data type.</span></span> <span data-ttu-id="0903e-107">Das Umrechnen von f-> Codes in das neue Format wird in den folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="0903e-107">Converting FVF> codes into the new format is covered in the following topics:</span></span>

-   [<span data-ttu-id="0903e-108">Zuordnung von FVF-Codes zu einer Direct3D 9-Deklaration (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0903e-108">Mapping FVF Codes to a Direct3D 9 Declaration (Direct3D 9)</span></span>](mapping-fvf-codes-to-a-directx-9-declaration.md)
-   [<span data-ttu-id="0903e-109">Code der Fixed-Funktion (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0903e-109">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
-   [<span data-ttu-id="0903e-110">Zuordnung zwischen einer Direct3D-Deklaration und einem f-Code (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0903e-110">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-fvf-codes.md)
-   [<span data-ttu-id="0903e-111">Zuordnung zwischen einer Direct3D 9-Deklaration und einer Direct3D 8-Deklaration (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0903e-111">Mapping between a Direct3D 9 Declaration and a Direct3D 8 Declaration (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-directx-8.md)
-   [<span data-ttu-id="0903e-112">Programmieren von mindestens einem Stream (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0903e-112">Programming One or More Streams (Direct3D 9)</span></span>](programming-one-or-more-streams.md)

## <a name="related-topics"></a><span data-ttu-id="0903e-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0903e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0903e-114">Vertex-Puffer</span><span class="sxs-lookup"><span data-stu-id="0903e-114">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 



