---
title: D3D12CalcSubresource-Funktion (D3dx12. h)
description: Berechnet einen subresource-Index für eine Textur.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- D3D12CalcSubresource-Funktion
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371884"
---
# <a name="d3d12calcsubresource-function"></a><span data-ttu-id="40711-104">D3D12CalcSubresource-Funktion</span><span class="sxs-lookup"><span data-stu-id="40711-104">D3D12CalcSubresource function</span></span>

<span data-ttu-id="40711-105">Berechnet einen subresource-Index für eine Textur.</span><span class="sxs-lookup"><span data-stu-id="40711-105">Calculates a subresource index for a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="40711-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="40711-106">Syntax</span></span>


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="40711-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="40711-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40711-108">*Mipslice*</span><span class="sxs-lookup"><span data-stu-id="40711-108">*MipSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="40711-109">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40711-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="40711-110">Der null basierte Index für die zu Adressier nende MipMap-Ebene. 0 gibt die erste, ausführlichste MipMap-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="40711-110">The zero-based index for the mipmap level to address; 0 indicates the first, most detailed mipmap level.</span></span>

</dd> <dt>

<span data-ttu-id="40711-111">*Arrayslice*</span><span class="sxs-lookup"><span data-stu-id="40711-111">*ArraySlice*</span></span> 
</dt> <dd>

<span data-ttu-id="40711-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40711-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="40711-113">Der null basierte Index für die zu Adressier gende Array Ebene. Verwenden Sie immer 0 für volumenvolumes (3D).</span><span class="sxs-lookup"><span data-stu-id="40711-113">The zero-based index for the array level to address; always use 0 for volume (3D) textures.</span></span>

</dd> <dt>

<span data-ttu-id="40711-114">*Planeslice*</span><span class="sxs-lookup"><span data-stu-id="40711-114">*PlaneSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="40711-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40711-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="40711-116">Der null basierte Index für die zu Adressier Ebene der Ebene.</span><span class="sxs-lookup"><span data-stu-id="40711-116">The zero-based index for the plane level to address.</span></span>

</dd> <dt>

<span data-ttu-id="40711-117">*MipLevels*</span><span class="sxs-lookup"><span data-stu-id="40711-117">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="40711-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40711-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="40711-119">Die Anzahl von MipMap-Ebenen in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="40711-119">The number of mipmap levels in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="40711-120">*ArraySize*</span><span class="sxs-lookup"><span data-stu-id="40711-120">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="40711-121">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40711-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="40711-122">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="40711-122">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40711-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40711-123">Return value</span></span>

<span data-ttu-id="40711-124">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40711-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="40711-125">Der Index, der mipslice + (arrayslice- \* miplevels) gleicht.</span><span class="sxs-lookup"><span data-stu-id="40711-125">The index which equals MipSlice + (ArraySlice \* MipLevels).</span></span>

## <a name="remarks"></a><span data-ttu-id="40711-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40711-126">Remarks</span></span>

<span data-ttu-id="40711-127">Ein Puffer ist eine unstrukturierte Ressource und wird daher als eine einzelne untergeordnete Quelle definiert.</span><span class="sxs-lookup"><span data-stu-id="40711-127">A buffer is an unstructured resource and is therefore defined as containing a single subresource.</span></span> <span data-ttu-id="40711-128">APIs, die Puffer akzeptieren, benötigen keinen unter Quell Index.</span><span class="sxs-lookup"><span data-stu-id="40711-128">APIs that take buffers do not need a subresource index.</span></span> <span data-ttu-id="40711-129">Eine Textur auf der anderen Seite ist stark strukturiert.</span><span class="sxs-lookup"><span data-stu-id="40711-129">A texture on the other hand is highly structured.</span></span> <span data-ttu-id="40711-130">Jedes Textur Objekt kann abhängig von der Größe des Arrays und der Anzahl von MipMap-Ebenen eine oder mehrere unter Ressourcen enthalten.</span><span class="sxs-lookup"><span data-stu-id="40711-130">Each texture object may contain one or more subresources depending on the size of the array and the number of mipmap levels.</span></span>

<span data-ttu-id="40711-131">Bei volumevolumes (3D) handelt es sich bei allen Slices für eine bestimmte MipMap-Ebene um einen einzelnen subresource-Index.</span><span class="sxs-lookup"><span data-stu-id="40711-131">For volume (3D) textures, all slices for a given mipmap level are a single subresource index.</span></span>

## <a name="requirements"></a><span data-ttu-id="40711-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40711-132">Requirements</span></span>



| <span data-ttu-id="40711-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40711-133">Requirement</span></span> | <span data-ttu-id="40711-134">Wert</span><span class="sxs-lookup"><span data-stu-id="40711-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="40711-135">Header</span><span class="sxs-lookup"><span data-stu-id="40711-135">Header</span></span><br/>  | <dl> <span data-ttu-id="40711-136"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="40711-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="40711-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="40711-137">Library</span></span><br/> | <dl> <span data-ttu-id="40711-138"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40711-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="40711-139">DLL</span><span class="sxs-lookup"><span data-stu-id="40711-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="40711-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40711-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40711-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40711-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40711-142">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="40711-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="40711-143">Unterressourcen</span><span class="sxs-lookup"><span data-stu-id="40711-143">Subresources</span></span>](subresources.md)
</dt> </dl>

 

