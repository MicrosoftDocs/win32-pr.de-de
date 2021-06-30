---
title: Funktionen des Hilfsprogramms für D3D12
description: Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von Unterressourcen und werden in d3dx12.h deklariert.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Hilfsfunktionen
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10736d91da0e2c4efa2a3c981ab5c4f64e2af86d
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102134"
---
# <a name="helper-functions-for-d3d12"></a><span data-ttu-id="833bd-105">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="833bd-105">Helper Functions for D3D12</span></span>

<span data-ttu-id="833bd-106">Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von Unterressourcen und werden in **d3dx12.h deklariert.**</span><span class="sxs-lookup"><span data-stu-id="833bd-106">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="833bd-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="833bd-107">In this section</span></span>



| <span data-ttu-id="833bd-108">Thema</span><span class="sxs-lookup"><span data-stu-id="833bd-108">Topic</span></span>                                                                                             | <span data-ttu-id="833bd-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="833bd-109">Description</span></span>                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="833bd-110">**CommandListCast**</span><span class="sxs-lookup"><span data-stu-id="833bd-110">**CommandListCast**</span></span>](commandlistcast.md)<br/>                                     | <span data-ttu-id="833bd-111">Diese Funktionsvorlage wandelt einen konstanten Zeiger auf eine beliebige Befehlsliste in einen const-Zeiger auf eine ID3D12CommandList um.</span><span class="sxs-lookup"><span data-stu-id="833bd-111">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="833bd-112">**D3D12CalcSubresource**</span><span class="sxs-lookup"><span data-stu-id="833bd-112">**D3D12CalcSubresource**</span></span>](d3d12calcsubresource.md)<br/>                                   | <span data-ttu-id="833bd-113">Berechnet einen Unterressourcenindex für eine Textur.</span><span class="sxs-lookup"><span data-stu-id="833bd-113">Calculates a subresource index for a texture.</span></span> <br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="833bd-114">**D3D12DecomposeSubresource**</span><span class="sxs-lookup"><span data-stu-id="833bd-114">**D3D12DecomposeSubresource**</span></span>](d3d12decomposesubresource.md)<br/>                         | <span data-ttu-id="833bd-115">Gibt den MIP-Slice, den Arrayslice und den Ebenenslice aus, die dem angegebenen Unterressourcenindex entsprechen.</span><span class="sxs-lookup"><span data-stu-id="833bd-115">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span> <br/>                                                                                                                                        |
| [<span data-ttu-id="833bd-116">**D3D12GetFormatPlaneCount**</span><span class="sxs-lookup"><span data-stu-id="833bd-116">**D3D12GetFormatPlaneCount**</span></span>](d3d12getformatplanecount.md)<br/>                           | <span data-ttu-id="833bd-117">Ruft die Anzahl der Ebenen für das angegebene DXGI-Format für den angegebenen virtuellen Adapter ab **(id3D12Device**).</span><span class="sxs-lookup"><span data-stu-id="833bd-117">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="833bd-118">**D3D12IsLayoutOpaque**</span><span class="sxs-lookup"><span data-stu-id="833bd-118">**D3D12IsLayoutOpaque**</span></span>](d3d12islayoutopaque.md)<br/>                                     | <span data-ttu-id="833bd-119">Gibt an, ob das Layout nicht transparent ist.</span><span class="sxs-lookup"><span data-stu-id="833bd-119">Indicates whether the layout is opaque.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="833bd-120">**D3DX12GetBaseSubobjectType**</span><span class="sxs-lookup"><span data-stu-id="833bd-120">**D3DX12GetBaseSubobjectType**</span></span>](d3dx12getbasesubobjecttype.md)<br/>                       | <span data-ttu-id="833bd-121">Gibt den Unterobjekttyp zurück, der der Basisklasse des übergebenen Unterobjekttyps entspricht.</span><span class="sxs-lookup"><span data-stu-id="833bd-121">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="833bd-122">**D3DX12ParsePipelineStateStream**</span><span class="sxs-lookup"><span data-stu-id="833bd-122">**D3DX12ParsePipelineStateStream**</span></span>](d3dx12parsepipelinestream.md)<br/>                    | <span data-ttu-id="833bd-123">Analysiert eine Pipelinezustandsstreambeschreibung und ruft einen benutzerdefinierten Rückruf für jede analysierte Unterobjektinstanz auf.</span><span class="sxs-lookup"><span data-stu-id="833bd-123">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="833bd-124">**D3DX12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="833bd-124">**D3DX12SerializeVersionedRootSignature**</span></span>](d3dx12serializeversionedrootsignature.md)<br/> | <span data-ttu-id="833bd-125">Unterstützt die Aktivierung von Root Signature 1.1-Features, wenn sie verfügbar sind, und erfordert keine Zwei-Codepfade zum Erstellen von Stammsignaturen.</span><span class="sxs-lookup"><span data-stu-id="833bd-125">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="833bd-126">Diese Hilfsmethode rekonstruiert eine Stammsignatur der Version 1.0, wenn Version 1.1 nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="833bd-126">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span><br/> |
| [<span data-ttu-id="833bd-127">**GetRequiredIntermediateSize**</span><span class="sxs-lookup"><span data-stu-id="833bd-127">**GetRequiredIntermediateSize**</span></span>](getrequiredintermediatesize.md)<br/>                     | <span data-ttu-id="833bd-128">Gibt die erforderliche Größe eines Puffers zurück, der für den Datenupload verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="833bd-128">Returns the required size of a buffer to be used for data upload.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="833bd-129">**Memcpysubresource**</span><span class="sxs-lookup"><span data-stu-id="833bd-129">**Memcpysubresource**</span></span>](memcpysubresource.md)<br/>                                         | <span data-ttu-id="833bd-130">Kopiert eine Unterressourcenzeile nach Zeile.</span><span class="sxs-lookup"><span data-stu-id="833bd-130">Copies a subresource row by row.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="833bd-131">**Updatesubresources**</span><span class="sxs-lookup"><span data-stu-id="833bd-131">**Updatesubresources**</span></span>](updatesubresources1.md)<br/>                                      | <span data-ttu-id="833bd-132">Aktualisiert Unterressourcen. Alle Unterressourcenarrays sollten aufgefüllt werden, in der Regel durch Aufrufen von [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="833bd-132">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span> <br/>                                                                  |
| [<span data-ttu-id="833bd-133">**Updatesubresources (heap-allocating)**</span><span class="sxs-lookup"><span data-stu-id="833bd-133">**Updatesubresources (heap-allocating)**</span></span>](updatesubresources2.md)<br/>                    | <span data-ttu-id="833bd-134">Aktualisiert Unterressourcen mit einer Heapzuweisungsimplementierung.</span><span class="sxs-lookup"><span data-stu-id="833bd-134">Updates subresources with a heap-allocating implementation.</span></span> <br/>                                                                                                                                                                                    |
| [<span data-ttu-id="833bd-135">**Updatesubresources (stack-allocating)**</span><span class="sxs-lookup"><span data-stu-id="833bd-135">**Updatesubresources (stack-allocating)**</span></span>](updatesubresources3.md)<br/>                   | <span data-ttu-id="833bd-136">Aktualisiert Unterressourcen mit einer Stapelzuweisungsimplementierung.</span><span class="sxs-lookup"><span data-stu-id="833bd-136">Updates subresources with a stack-allocating implementation.</span></span> <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="833bd-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="833bd-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="833bd-138">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="833bd-138">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="833bd-139">Strukturen und Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="833bd-139">Helper Structures and Functions for D3D12</span></span>](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





