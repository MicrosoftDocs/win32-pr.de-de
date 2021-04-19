---
title: Updatesubresources (Heap Zuordnung)-Funktion (D3dx12. h)
description: Aktualisiert unter Ressourcen mit einer Heap Zuweisungs Implementierung.
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
keywords:
- Updatesubresources-Funktion
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97abe59bdd0334fe4b7badf03e44ddc03b85495
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351963"
---
# <a name="updatesubresources-heap-allocating-function"></a><span data-ttu-id="8c449-104">Updatesubresources (Heap Zuordnung)-Funktion</span><span class="sxs-lookup"><span data-stu-id="8c449-104">UpdateSubresources (heap-allocating) function</span></span>

<span data-ttu-id="8c449-105">Aktualisiert unter Ressourcen mit einer Heap Zuweisungs Implementierung.</span><span class="sxs-lookup"><span data-stu-id="8c449-105">Updates subresources with a heap-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c449-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c449-106">Syntax</span></span>


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a><span data-ttu-id="8c449-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c449-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c449-108">*pcmdlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c449-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c449-109">Typ: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="8c449-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="8c449-110">Ein Zeiger auf die [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) -Schnittstelle für die Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="8c449-110">A pointer to the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface for the command list.</span></span>

</dd> <dt>

<span data-ttu-id="8c449-111">*pdestinationresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c449-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c449-112">Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="8c449-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="8c449-113">Ein Zeiger auf die [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) -Schnittstelle, die die Ziel Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="8c449-113">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="8c449-114">*pintermediate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c449-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c449-115">Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="8c449-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="8c449-116">Ein Zeiger auf die [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) -Schnittstelle, die die zwischen Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="8c449-116">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="8c449-117">*Intermediateoffset*</span><span class="sxs-lookup"><span data-stu-id="8c449-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="8c449-118">Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8c449-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8c449-119">Der Offset in Bytes der zwischen Ressource.</span><span class="sxs-lookup"><span data-stu-id="8c449-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="8c449-120">*Firstsubresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c449-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c449-121">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8c449-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8c449-122">Der Index der ersten unter Quelle in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8c449-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="8c449-123">Der Bereich gültiger Werte ist 0 bis D3D12 \_ req \_ subresources.</span><span class="sxs-lookup"><span data-stu-id="8c449-123">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="8c449-124">*Numsubresources* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c449-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c449-125">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8c449-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8c449-126">Die Anzahl der unter Ressourcen in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8c449-126">The number of subresources in the resource.</span></span> <span data-ttu-id="8c449-127">Der Bereich gültiger Werte ist 0 bis (D3D12 \_ req \_ subresources- *firstsubresource*).</span><span class="sxs-lookup"><span data-stu-id="8c449-127">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="8c449-128">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c449-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c449-129">Typ: **[ **D3D12 \_ subresource- \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="8c449-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="8c449-130">Zeiger auf ein Array (der Länge *numsubresources*) von Zeigern auf D3D12-unter Berichts [**\_ \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) Strukturen, die Beschreibungen der für das Update verwendeten unter Berichtsdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c449-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c449-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c449-131">Return value</span></span>

<span data-ttu-id="8c449-132">Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8c449-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8c449-133">Die Größe des Cookies in Bytes.</span><span class="sxs-lookup"><span data-stu-id="8c449-133">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c449-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c449-134">Requirements</span></span>



| <span data-ttu-id="8c449-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c449-135">Requirement</span></span> | <span data-ttu-id="8c449-136">Wert</span><span class="sxs-lookup"><span data-stu-id="8c449-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8c449-137">Header</span><span class="sxs-lookup"><span data-stu-id="8c449-137">Header</span></span><br/>  | <dl> <span data-ttu-id="8c449-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c449-138"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8c449-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8c449-139">Library</span></span><br/> | <dl> <span data-ttu-id="8c449-140"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c449-140"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c449-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8c449-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c449-142"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c449-142"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c449-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c449-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c449-144">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="8c449-144">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8c449-145">Unterressourcen</span><span class="sxs-lookup"><span data-stu-id="8c449-145">Subresources</span></span>](subresources.md)
</dt> </dl>

 

