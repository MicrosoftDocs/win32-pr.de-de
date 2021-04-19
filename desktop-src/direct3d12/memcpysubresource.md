---
title: Memcpysubresource-Funktion (D3dx12. h)
description: Kopiert eine untergeordnete Quelle zeilenweise.
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- Memcpysubresource-Funktion
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955211a490927033186442480b3449773b4ebcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370446"
---
# <a name="memcpysubresource-function"></a><span data-ttu-id="77660-104">Memcpysubresource-Funktion</span><span class="sxs-lookup"><span data-stu-id="77660-104">MemcpySubresource function</span></span>

<span data-ttu-id="77660-105">Kopiert eine untergeordnete Quelle zeilenweise.</span><span class="sxs-lookup"><span data-stu-id="77660-105">Copies a subresource row by row.</span></span>

## <a name="syntax"></a><span data-ttu-id="77660-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="77660-106">Syntax</span></span>


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a><span data-ttu-id="77660-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="77660-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77660-108">*pdest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77660-108">*pDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77660-109">Typ: **Konstanten [**D3D12 \_ memcpy \_ dest**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***</span><span class="sxs-lookup"><span data-stu-id="77660-109">Type: **const [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest)\***</span></span>

<span data-ttu-id="77660-110">Ein Zeiger auf eine [**D3D12 \_ memcpy \_ dest**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) -Struktur, die das Ziel des Speicher Kopiervorgangs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="77660-110">A pointer to a [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) structure that describes the destination of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="77660-111">*psrc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77660-111">*pSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77660-112">Typ: **Konstanten [**D3D12 \_ subresource- \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***</span><span class="sxs-lookup"><span data-stu-id="77660-112">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="77660-113">Ein Zeiger auf eine [**D3D12 \_ subresource- \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) Struktur, die die Quelle des Speicher Kopiervorgangs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="77660-113">A pointer to a [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structure that describes the source of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="77660-114">*Rowsizeinbytes*</span><span class="sxs-lookup"><span data-stu-id="77660-114">*RowSizeInBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="77660-115">Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77660-115">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="77660-116">Die Größe (in Bytes) der einzelnen Zeilen.</span><span class="sxs-lookup"><span data-stu-id="77660-116">The size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="77660-117">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="77660-117">*NumRows*</span></span> 
</dt> <dd>

<span data-ttu-id="77660-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77660-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="77660-119">Die Anzahl von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="77660-119">The number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="77660-120">*Numslices*</span><span class="sxs-lookup"><span data-stu-id="77660-120">*NumSlices*</span></span> 
</dt> <dd>

<span data-ttu-id="77660-121">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77660-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="77660-122">Die Anzahl der Slices.</span><span class="sxs-lookup"><span data-stu-id="77660-122">The number of slices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77660-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77660-123">Return value</span></span>

<span data-ttu-id="77660-124">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="77660-124">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77660-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77660-125">Remarks</span></span>

<span data-ttu-id="77660-126">Beachten Sie auch die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="77660-126">Also consider the following methods:</span></span>

-   [<span data-ttu-id="77660-127">**ID3D12Resource:: Write Items**</span><span class="sxs-lookup"><span data-stu-id="77660-127">**ID3D12Resource::WriteToSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [<span data-ttu-id="77660-128">**ID3D12Resource:: Read fromsubresource**</span><span class="sxs-lookup"><span data-stu-id="77660-128">**ID3D12Resource::ReadFromSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [<span data-ttu-id="77660-129">**ID3D12GraphicsCommandList:: copyresource**</span><span class="sxs-lookup"><span data-stu-id="77660-129">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

## <a name="requirements"></a><span data-ttu-id="77660-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77660-130">Requirements</span></span>



| <span data-ttu-id="77660-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77660-131">Requirement</span></span> | <span data-ttu-id="77660-132">Wert</span><span class="sxs-lookup"><span data-stu-id="77660-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="77660-133">Header</span><span class="sxs-lookup"><span data-stu-id="77660-133">Header</span></span><br/>  | <dl> <span data-ttu-id="77660-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="77660-134"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="77660-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="77660-135">Library</span></span><br/> | <dl> <span data-ttu-id="77660-136"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77660-136"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="77660-137">DLL</span><span class="sxs-lookup"><span data-stu-id="77660-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="77660-138"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77660-138"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77660-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77660-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77660-140">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="77660-140">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="77660-141">Unterressourcen</span><span class="sxs-lookup"><span data-stu-id="77660-141">Subresources</span></span>](subresources.md)
</dt> </dl>

 

