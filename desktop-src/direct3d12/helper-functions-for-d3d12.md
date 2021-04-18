---
title: Funktionen des Hilfsprogramms für D3D12
description: Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von unter Berichten und werden in d3dx12. h deklariert.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Hilfsfunktionen
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cacaaf5ad2a8204cc35b8a89f7c3c00e756116
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341250"
---
# <a name="helper-functions-for-d3d12"></a><span data-ttu-id="72743-105">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="72743-105">Helper Functions for D3D12</span></span>

<span data-ttu-id="72743-106">Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von unter Berichten und werden in **d3dx12. h** deklariert.</span><span class="sxs-lookup"><span data-stu-id="72743-106">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="72743-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="72743-107">In this section</span></span>



| <span data-ttu-id="72743-108">Thema</span><span class="sxs-lookup"><span data-stu-id="72743-108">Topic</span></span>                                                                                             | <span data-ttu-id="72743-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72743-109">Description</span></span>                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72743-110">**CommandListCast**</span><span class="sxs-lookup"><span data-stu-id="72743-110">**CommandListCast**</span></span>](cd3dx12-shader-bytecode.md)<br/>                                     | <span data-ttu-id="72743-111">Diese Funktions Vorlage wandelt einen Konstanten Zeiger auf eine beliebige Befehlsliste in einen Konstanten Zeiger auf einen ID3D12CommandList um.</span><span class="sxs-lookup"><span data-stu-id="72743-111">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="72743-112">**D3D12CalcSubresource**</span><span class="sxs-lookup"><span data-stu-id="72743-112">**D3D12CalcSubresource**</span></span>](d3d12calcsubresource.md)<br/>                                   | <span data-ttu-id="72743-113">Berechnet einen subresource-Index für eine Textur.</span><span class="sxs-lookup"><span data-stu-id="72743-113">Calculates a subresource index for a texture.</span></span> <br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="72743-114">**D3D12DecomposeSubresource**</span><span class="sxs-lookup"><span data-stu-id="72743-114">**D3D12DecomposeSubresource**</span></span>](d3d12decomposesubresource.md)<br/>                         | <span data-ttu-id="72743-115">Gibt die MIP-Slice, den Array Slice und den Ebenen-Slice aus, die dem angegebenen unter Quell Index entsprechen.</span><span class="sxs-lookup"><span data-stu-id="72743-115">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span> <br/>                                                                                                                                        |
| [<span data-ttu-id="72743-116">**D3D12GetFormatPlaneCount**</span><span class="sxs-lookup"><span data-stu-id="72743-116">**D3D12GetFormatPlaneCount**</span></span>](d3d12getformatplanecount.md)<br/>                           | <span data-ttu-id="72743-117">Ruft die Anzahl der Ebenen für das angegebene DXGI-Format für den angegebenen virtuellen Adapter (ein **ID3D12Device**) ab.</span><span class="sxs-lookup"><span data-stu-id="72743-117">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="72743-118">**D3D12IsLayoutOpaque**</span><span class="sxs-lookup"><span data-stu-id="72743-118">**D3D12IsLayoutOpaque**</span></span>](d3d12islayoutopaque.md)<br/>                                     | <span data-ttu-id="72743-119">Gibt an, ob das Layout nicht transparent ist.</span><span class="sxs-lookup"><span data-stu-id="72743-119">Indicates whether the layout is opaque.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="72743-120">**D3DX12GetBaseSubobjectType**</span><span class="sxs-lookup"><span data-stu-id="72743-120">**D3DX12GetBaseSubobjectType**</span></span>](d3dx12getbasesubobjecttype.md)<br/>                       | <span data-ttu-id="72743-121">Gibt den untergeordneten Objekttyp zurück, der der Basisklasse des übergeordneten untergeordneten Objekts entspricht.</span><span class="sxs-lookup"><span data-stu-id="72743-121">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="72743-122">**D3DX12ParsePipelineStateStream**</span><span class="sxs-lookup"><span data-stu-id="72743-122">**D3DX12ParsePipelineStateStream**</span></span>](d3dx12parsepipelinestream.md)<br/>                    | <span data-ttu-id="72743-123">Analysiert eine Pipeline Status-Datenstrom Beschreibung und ruft für jede analysierte untergeordnete Instanz einen benutzerdefinierten Rückruf auf.</span><span class="sxs-lookup"><span data-stu-id="72743-123">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="72743-124">**D3DX12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="72743-124">**D3DX12SerializeVersionedRootSignature**</span></span>](d3dx12serializeversionedrootsignature.md)<br/> | <span data-ttu-id="72743-125">Unterstützt die Aktivierung von root Signature 1,1-Features, wenn diese verfügbar sind. es ist nicht erforderlich, zwei Codepfade zum Aufbauen von Stamm Signaturen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="72743-125">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="72743-126">Diese Hilfsmethode rekonstruiert eine Stamm Signatur der Version 1,0, wenn Version 1,1 nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="72743-126">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span><br/> |
| [<span data-ttu-id="72743-127">**GetRequiredIntermediateSize**</span><span class="sxs-lookup"><span data-stu-id="72743-127">**GetRequiredIntermediateSize**</span></span>](getrequiredintermediatesize.md)<br/>                     | <span data-ttu-id="72743-128">Gibt die erforderliche Größe eines Puffers zurück, der zum Hochladen von Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72743-128">Returns the required size of a buffer to be used for data upload.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="72743-129">**Memcpysubresource**</span><span class="sxs-lookup"><span data-stu-id="72743-129">**Memcpysubresource**</span></span>](memcpysubresource.md)<br/>                                         | <span data-ttu-id="72743-130">Kopiert eine untergeordnete Quelle zeilenweise.</span><span class="sxs-lookup"><span data-stu-id="72743-130">Copies a subresource row by row.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="72743-131">**Updatesubresources**</span><span class="sxs-lookup"><span data-stu-id="72743-131">**Updatesubresources**</span></span>](updatesubresources1.md)<br/>                                      | <span data-ttu-id="72743-132">Aktualisiert unter Berichte, alle unter Quell Arrays sollten aufgefüllt werden, in der Regel durch Aufrufen von [**ID3D12Device:: getcopyablefootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="72743-132">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span> <br/>                                                                  |
| [<span data-ttu-id="72743-133">**Updatesubresources (heap-allocating)**</span><span class="sxs-lookup"><span data-stu-id="72743-133">**Updatesubresources (heap-allocating)**</span></span>](updatesubresources2.md)<br/>                    | <span data-ttu-id="72743-134">Aktualisiert unter Ressourcen mit einer Heap Zuweisungs Implementierung.</span><span class="sxs-lookup"><span data-stu-id="72743-134">Updates subresources with a heap-allocating implementation.</span></span> <br/>                                                                                                                                                                                    |
| [<span data-ttu-id="72743-135">**Updatesubresources (stack-allocating)**</span><span class="sxs-lookup"><span data-stu-id="72743-135">**Updatesubresources (stack-allocating)**</span></span>](updatesubresources3.md)<br/>                   | <span data-ttu-id="72743-136">Aktualisiert unter Ressourcen mit einer Implementierung zur Stapel Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="72743-136">Updates subresources with a stack-allocating implementation.</span></span> <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="72743-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72743-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72743-138">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="72743-138">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="72743-139">Strukturen und Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="72743-139">Helper Structures and Functions for D3D12</span></span>](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





