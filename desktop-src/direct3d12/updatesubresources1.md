---
title: Updatesubresources-Funktion (D3dx12. h)
description: Aktualisiert unter Berichte, alle unter Quell Arrays sollten aufgefüllt werden, in der Regel durch Aufrufen von ID3D12Device getcopyablefootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
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
ms.openlocfilehash: 885ee058aacbfca238448830f2b7b1b54a298f89
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369332"
---
# <a name="updatesubresources-function"></a><span data-ttu-id="2dfec-104">Updatesubresources-Funktion</span><span class="sxs-lookup"><span data-stu-id="2dfec-104">UpdateSubresources function</span></span>

<span data-ttu-id="2dfec-105">Aktualisiert unter Berichte, alle unter Quell Arrays sollten aufgefüllt werden, in der Regel durch Aufrufen von [**ID3D12Device:: getcopyablefootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="2dfec-105">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span>

## <a name="syntax"></a><span data-ttu-id="2dfec-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dfec-106">Syntax</span></span>


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
);
```



## <a name="parameters"></a><span data-ttu-id="2dfec-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dfec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dfec-108">*pcmdlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dfec-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dfec-109">Typ: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="2dfec-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="2dfec-110">Die Befehlsliste als Zeiger auf eine [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="2dfec-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="2dfec-111">*pdestinationresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dfec-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dfec-112">Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="2dfec-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="2dfec-113">Die Ziel Ressource als Zeiger auf eine [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="2dfec-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="2dfec-114">*pintermediate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dfec-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dfec-115">Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="2dfec-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="2dfec-116">Die zwischen Ressource als Zeiger auf eine [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="2dfec-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="2dfec-117">*Firstsubresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dfec-117">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dfec-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2dfec-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2dfec-119">Der Index der ersten unter Quelle in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2dfec-119">The index of the first subresource in the resource.</span></span> <span data-ttu-id="2dfec-120">Der Bereich gültiger Werte ist 0 bis D3D12 \_ req \_ subresources.</span><span class="sxs-lookup"><span data-stu-id="2dfec-120">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="2dfec-121">*Numsubresources* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dfec-121">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dfec-122">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2dfec-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2dfec-123">Die Anzahl der unter Ressourcen in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2dfec-123">The number of subresources in the resource.</span></span> <span data-ttu-id="2dfec-124">Der Bereich gültiger Werte ist 0 bis (D3D12 \_ req \_ subresources- *firstsubresource*).</span><span class="sxs-lookup"><span data-stu-id="2dfec-124">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="2dfec-125">*Requirements-size*</span><span class="sxs-lookup"><span data-stu-id="2dfec-125">*RequiredSize*</span></span> 
</dt> <dd>

<span data-ttu-id="2dfec-126">Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2dfec-126">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2dfec-127">Die erforderliche Größe (in Bytes) für das Update.</span><span class="sxs-lookup"><span data-stu-id="2dfec-127">The required size, in bytes, for the update.</span></span>

</dd> <dt>

<span data-ttu-id="2dfec-128">*playouts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dfec-128">*pLayouts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dfec-129">Typ: Konstante **[**D3D12 \_ Platzierung \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) der untergeordneten Quelle \***</span><span class="sxs-lookup"><span data-stu-id="2dfec-129">Type: **const [**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)\***</span></span>

<span data-ttu-id="2dfec-130">Zeiger auf ein Array (der Länge *numsubresources*) von Zeigern auf die Strukturen, die die Beschreibung und Platzierung der unter Ressourcen der Ressource enthalten.</span><span class="sxs-lookup"><span data-stu-id="2dfec-130">Pointer to an array (of length *NumSubresources*) of pointers to the structures that contains the description and placement of the resource's subresources.</span></span>

</dd> <dt>

<span data-ttu-id="2dfec-131">*pnumrows* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dfec-131">*pNumRows* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dfec-132">Typ: Konstante **[**uint**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="2dfec-132">Type: **const [**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="2dfec-133">Zeiger auf ein Array (der Länge *numsubresources*) von uints, das die Anzahl der Zeilen für die einzelnen unter Berichte enthält.</span><span class="sxs-lookup"><span data-stu-id="2dfec-133">Pointer to an array (of length *NumSubresources*) of UINTS containing the number of rows for each subresource.</span></span>

</dd> <dt>

<span data-ttu-id="2dfec-134">*prowsizesinbytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dfec-134">*pRowSizesInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dfec-135">Typ: **Konstanten [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="2dfec-135">Type: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="2dfec-136">Zeiger auf ein Array (der Länge *numsubresources*) von uints, das die Größe (in Bytes) der einzelnen Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="2dfec-136">Pointer to an array (of length *NumSubresources*) of UINTS containing the size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="2dfec-137">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dfec-137">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dfec-138">Typ: **Konstanten [**D3D12 \_ subresource- \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***</span><span class="sxs-lookup"><span data-stu-id="2dfec-138">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="2dfec-139">Zeiger auf ein Array (der Länge *numsubresources*) von Zeigern auf D3D12-unter Berichts [**\_ \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) Strukturen, die Beschreibungen der für das Update verwendeten unter Berichtsdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="2dfec-139">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dfec-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2dfec-140">Return value</span></span>

<span data-ttu-id="2dfec-141">Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2dfec-141">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2dfec-142">Die Größe des Cookies in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2dfec-142">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dfec-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2dfec-143">Requirements</span></span>



| <span data-ttu-id="2dfec-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2dfec-144">Requirement</span></span> | <span data-ttu-id="2dfec-145">Wert</span><span class="sxs-lookup"><span data-stu-id="2dfec-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2dfec-146">Header</span><span class="sxs-lookup"><span data-stu-id="2dfec-146">Header</span></span><br/>  | <dl> <span data-ttu-id="2dfec-147"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dfec-147"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="2dfec-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2dfec-148">Library</span></span><br/> | <dl> <span data-ttu-id="2dfec-149"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2dfec-149"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="2dfec-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2dfec-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="2dfec-151"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dfec-151"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dfec-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dfec-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dfec-153">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="2dfec-153">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="2dfec-154">Unterressourcen</span><span class="sxs-lookup"><span data-stu-id="2dfec-154">Subresources</span></span>](subresources.md)
</dt> </dl>

 

