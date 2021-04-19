---
title: Strukturen und Funktionen des Hilfsprogramms für D3D12
description: Diese Hilfsstrukturen und Hilfsfunktionen werden in d3dx12. h deklariert.
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Hilfsfunktionen
- Hilfsstrukturen
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d612d97610a749f32a6a23010b632c17d34461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341249"
---
# <a name="helper-structures-and-functions-for-d3d12"></a><span data-ttu-id="67504-106">Strukturen und Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="67504-106">Helper Structures and Functions for D3D12</span></span>

<span data-ttu-id="67504-107">Diese Hilfsstrukturen und Hilfsfunktionen werden in **d3dx12. h** deklariert.</span><span class="sxs-lookup"><span data-stu-id="67504-107">These helper structures and helper functions are declared in **d3dx12.h**.</span></span>

<span data-ttu-id="67504-108">Sie können diese Hilfsstrukturen verwenden, um Direct3D-Strukturen zu erstellen und zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="67504-108">You can use these helper structures to create and initialize Direct3D structures.</span></span> <span data-ttu-id="67504-109">Diese Hilfsstrukturen Verhalten sich wie C++-Klassen.</span><span class="sxs-lookup"><span data-stu-id="67504-109">These helper structures behave like C++ classes.</span></span> <span data-ttu-id="67504-110">Jede hilfsstruktur verfügt in der Regel über einen Standardkonstruktor, einen expliziten Konstruktor, einen destrukturtor und einen Cast Operator für die zugeordnete D3D12-Struktur.</span><span class="sxs-lookup"><span data-stu-id="67504-110">Each helper structure typically has a default constructor, an explicit constructor, a destructor, and a cast operator for the associated D3D12 structure.</span></span> <span data-ttu-id="67504-111">Jede hilfsstruktur verfügt über ein Präfix "c" und ist mit einer D3D12-Struktur verknüpft, der das Präfix "c" fehlt.</span><span class="sxs-lookup"><span data-stu-id="67504-111">Each helper structure has a 'C' prefix and is associated with a D3D12 structure which lacks the 'C' prefix.</span></span> <span data-ttu-id="67504-112">Die meisten Hilfsstrukturen enthalten Methoden für Initialisierungs Member, von denen einige Vergleichsfunktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="67504-112">Most helper structures contain initialization member methods, some contain comparison functions.</span></span>

<span data-ttu-id="67504-113">**d3dx12. h** ist separat von den Direct3D 12-Headern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="67504-113">**d3dx12.h** is available separately from the Direct3D 12 headers.</span></span> <span data-ttu-id="67504-114">Sie können **d3dx12. h** von [der D3D12 Helper Library](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="67504-114">You can download **d3dx12.h** from [The D3D12 Helper Library](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="67504-115">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="67504-115">In this section</span></span>



| <span data-ttu-id="67504-116">Thema</span><span class="sxs-lookup"><span data-stu-id="67504-116">Topic</span></span>                                                                     | <span data-ttu-id="67504-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67504-117">Description</span></span>                                                                                                              |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67504-118">Schnittstellen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="67504-118">Helper Interfaces for D3D12</span></span>](helper-interfaces-for-d3d12.md)<br/> | <span data-ttu-id="67504-119">Diese hilfsschnittstellen helfen insbesondere bei der Behandlung von unter Berichten und werden in **d3dx12. h** deklariert.</span><span class="sxs-lookup"><span data-stu-id="67504-119">These helper interfaces help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>        |
| [<span data-ttu-id="67504-120">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="67504-120">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)<br/> | <span data-ttu-id="67504-121">Diese Hilfsstrukturen helfen dabei, viele der Direct3D 12-Strukturen zu initialisieren, und werden in **d3dx12. h** deklariert.</span><span class="sxs-lookup"><span data-stu-id="67504-121">These helper structures help initialize many of the Direct3D 12 structures, and are declared in **d3dx12.h**.</span></span><br/> |
| [<span data-ttu-id="67504-122">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="67504-122">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)<br/>   | <span data-ttu-id="67504-123">Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von unter Berichten und werden in **d3dx12. h** deklariert.</span><span class="sxs-lookup"><span data-stu-id="67504-123">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="67504-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67504-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67504-125">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="67504-125">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





