---
title: Updatesubresources (Stapel Zuordnung)-Funktion (D3dx12. h)
description: Aktualisiert unter Ressourcen mit einer Implementierung zur Stapel Zuweisung.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
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
ms.openlocfilehash: 237e7df26b35b4cb5b1dba7b2a80c1baaac64e8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357226"
---
# <a name="updatesubresources-stack-allocating-function"></a><span data-ttu-id="d76ef-104">Updatesubresources (Stapel Zuordnung)-Funktion</span><span class="sxs-lookup"><span data-stu-id="d76ef-104">UpdateSubresources (stack-allocating) function</span></span>

<span data-ttu-id="d76ef-105">Aktualisiert unter Ressourcen mit einer Implementierung zur Stapel Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="d76ef-105">Updates subresources with a stack-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d76ef-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d76ef-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d76ef-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d76ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76ef-108">*pcmdlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d76ef-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d76ef-109">Typ: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="d76ef-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="d76ef-110">Die Befehlsliste als Zeiger auf eine [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="d76ef-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="d76ef-111">*pdestinationresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d76ef-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d76ef-112">Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="d76ef-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="d76ef-113">Die Ziel Ressource als Zeiger auf eine [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="d76ef-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="d76ef-114">*pintermediate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d76ef-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d76ef-115">Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="d76ef-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="d76ef-116">Die zwischen Ressource als Zeiger auf eine [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="d76ef-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="d76ef-117">*Intermediateoffset*</span><span class="sxs-lookup"><span data-stu-id="d76ef-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="d76ef-118">Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d76ef-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d76ef-119">Der Offset in Bytes der zwischen Ressource.</span><span class="sxs-lookup"><span data-stu-id="d76ef-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="d76ef-120">*Firstsubresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d76ef-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d76ef-121">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d76ef-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d76ef-122">Der Index der ersten unter Quelle in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d76ef-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="d76ef-123">Gültige Werte reichen von 0 bis *maxsubresources*.</span><span class="sxs-lookup"><span data-stu-id="d76ef-123">Valid values range from 0 to *MaxSubresources*.</span></span>

</dd> <dt>

<span data-ttu-id="d76ef-124">*Numsubresources* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d76ef-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d76ef-125">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d76ef-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d76ef-126">Die Anzahl der unter Ressourcen in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d76ef-126">The number of subresources in the resource.</span></span> <span data-ttu-id="d76ef-127">Gültige Werte liegen zwischen 1 und (*maxsubresources*  -  *firstsubresource*).</span><span class="sxs-lookup"><span data-stu-id="d76ef-127">Valid values range from 1 to (*MaxSubresources* - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="d76ef-128">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d76ef-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d76ef-129">Typ: **[ **D3D12 \_ subresource- \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="d76ef-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="d76ef-130">Zeiger auf ein Array (der Länge *numsubresources*) von Zeigern auf D3D12-unter Berichts [**\_ \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) Strukturen, die Beschreibungen der für das Update verwendeten unter Berichtsdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="d76ef-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d76ef-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d76ef-131">Return value</span></span>

<span data-ttu-id="d76ef-132">Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d76ef-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d76ef-133">Die Größe des Cookies in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d76ef-133">The size, in bytes, of the buffer.</span></span>

## <a name="remarks"></a><span data-ttu-id="d76ef-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d76ef-134">Remarks</span></span>

<span data-ttu-id="d76ef-135">Die Deklaration dieser Funktion beginnt mit: `template <UINT MaxSubresources>`</span><span class="sxs-lookup"><span data-stu-id="d76ef-135">The declaration of this function begins with: `template <UINT MaxSubresources>`</span></span>

## <a name="requirements"></a><span data-ttu-id="d76ef-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d76ef-136">Requirements</span></span>



| <span data-ttu-id="d76ef-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d76ef-137">Requirement</span></span> | <span data-ttu-id="d76ef-138">Wert</span><span class="sxs-lookup"><span data-stu-id="d76ef-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d76ef-139">Header</span><span class="sxs-lookup"><span data-stu-id="d76ef-139">Header</span></span><br/>  | <dl> <span data-ttu-id="d76ef-140"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d76ef-140"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d76ef-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d76ef-141">Library</span></span><br/> | <dl> <span data-ttu-id="d76ef-142"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d76ef-142"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d76ef-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d76ef-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="d76ef-144"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d76ef-144"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d76ef-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d76ef-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d76ef-146">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="d76ef-146">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d76ef-147">Unterressourcen</span><span class="sxs-lookup"><span data-stu-id="d76ef-147">Subresources</span></span>](subresources.md)
</dt> </dl>

 

