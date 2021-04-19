---
title: D3D12DecomposeSubresource-Funktion (D3dx12.h)
description: Gibt die MIP-Slice, den Array Slice und den Ebenen-Slice aus, die dem angegebenen unter Quell Index entsprechen.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- D3D12DecomposeSubresource-Funktion
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec147833ee94969880865f679d40a198e0b22852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361840"
---
# <a name="d3d12decomposesubresource-function"></a><span data-ttu-id="6e581-104">D3D12DecomposeSubresource-Funktion</span><span class="sxs-lookup"><span data-stu-id="6e581-104">D3D12DecomposeSubresource function</span></span>

<span data-ttu-id="6e581-105">Gibt die MIP-Slice, den Array Slice und den Ebenen-Slice aus, die dem angegebenen unter Quell Index entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6e581-105">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e581-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e581-106">Syntax</span></span>


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a><span data-ttu-id="6e581-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e581-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e581-108">*Unterressource*</span><span class="sxs-lookup"><span data-stu-id="6e581-108">*Subresource*</span></span> 
</dt> <dd>

<span data-ttu-id="6e581-109">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6e581-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6e581-110">Der Index der untergeordneten Quelle.</span><span class="sxs-lookup"><span data-stu-id="6e581-110">The index of the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="6e581-111">*MipLevels*</span><span class="sxs-lookup"><span data-stu-id="6e581-111">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="6e581-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6e581-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6e581-113">Die maximale Anzahl von MipMap-Ebenen in der Unterstruktur.</span><span class="sxs-lookup"><span data-stu-id="6e581-113">The maximum number of mipmap levels in the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="6e581-114">*ArraySize*</span><span class="sxs-lookup"><span data-stu-id="6e581-114">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="6e581-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6e581-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6e581-116">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="6e581-116">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="6e581-117">*Mipslice* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="6e581-117">*MipSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6e581-118">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="6e581-118">Type: **T**</span></span>

<span data-ttu-id="6e581-119">Gibt den MIP-Slice aus, der dem angegebenen subresource-Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="6e581-119">Outputs the mip slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="6e581-120">*Arrayslice* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="6e581-120">*ArraySlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6e581-121">Typ: **U**</span><span class="sxs-lookup"><span data-stu-id="6e581-121">Type: **U**</span></span>

<span data-ttu-id="6e581-122">Gibt das Array Slice aus, das dem angegebenen subresource-Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="6e581-122">Outputs the array slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="6e581-123">*Planeslice* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="6e581-123">*PlaneSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6e581-124">Typ: **V**</span><span class="sxs-lookup"><span data-stu-id="6e581-124">Type: **V**</span></span>

<span data-ttu-id="6e581-125">Gibt den flachen Slice aus, der dem angegebenen subresource-Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="6e581-125">Outputs the plane slice that corresponds to the given subresource index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e581-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e581-126">Return value</span></span>

<span data-ttu-id="6e581-127">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6e581-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e581-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e581-128">Remarks</span></span>

<span data-ttu-id="6e581-129">Diese Funktion bestimmt, welches MIP-Slice, Array Slice und der flache Slice einem angegebenen unter Quell Index entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6e581-129">This function determines which mip slice, array slice, and plane slice correspond to a given subresource index.</span></span> <span data-ttu-id="6e581-130">Dies ist ein nützliches Hilfsprogramm, obwohl es C++ spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="6e581-130">This is a useful utility, though it is C++ specific.</span></span>

<span data-ttu-id="6e581-131">Diese Funktion wird wie folgt mit C++-Vorlagen-Parametern für die Typen **T**, **U** und **V** deklariert:</span><span class="sxs-lookup"><span data-stu-id="6e581-131">This function is declared as follows, with C++ templatized parameters for types **T**, **U**, and **V**:</span></span>


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a><span data-ttu-id="6e581-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e581-132">Requirements</span></span>



| <span data-ttu-id="6e581-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e581-133">Requirement</span></span> | <span data-ttu-id="6e581-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6e581-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6e581-135">Header</span><span class="sxs-lookup"><span data-stu-id="6e581-135">Header</span></span><br/>  | <dl> <span data-ttu-id="6e581-136"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e581-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="6e581-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6e581-137">Library</span></span><br/> | <dl> <span data-ttu-id="6e581-138"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e581-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e581-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6e581-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="6e581-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e581-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e581-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e581-141">See also</span></span>

[<span data-ttu-id="6e581-142">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="6e581-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)

[<span data-ttu-id="6e581-143">Unterressourcen</span><span class="sxs-lookup"><span data-stu-id="6e581-143">Subresources</span></span>](subresources.md)
