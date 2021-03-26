---
title: ID3DX11EffectScalarVariable getboolarray-Methode (D3dx11effect. h)
description: Ein Array von booleschen Variablen erhalten.
ms.assetid: 0335417a-a0aa-4157-881d-7828ffb3f47a
keywords:
- Getboolarray-Methode Direct3D 11
- Getboolarray-Methode Direct3D 11, ID3DX11EffectScalarVariable-Schnittstelle
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11, getboolarray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetBoolArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff039fb90bae187cc86eda14d80d541b3b050634
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219561"
---
# <a name="id3dx11effectscalarvariablegetboolarray-method"></a><span data-ttu-id="3b2df-106">ID3DX11EffectScalarVariable:: getboolarray-Methode</span><span class="sxs-lookup"><span data-stu-id="3b2df-106">ID3DX11EffectScalarVariable::GetBoolArray method</span></span>

<span data-ttu-id="3b2df-107">Ein Array von booleschen Variablen erhalten.</span><span class="sxs-lookup"><span data-stu-id="3b2df-107">Get an array of boolean variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b2df-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b2df-108">Syntax</span></span>


```C++
HRESULT GetBoolArray(
   BOOL *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="3b2df-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b2df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b2df-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="3b2df-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="3b2df-111">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="3b2df-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="3b2df-112">Ein Zeiger auf den Anfang der festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="3b2df-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="3b2df-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="3b2df-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="3b2df-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3b2df-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3b2df-115">Muss auf 0 (null) festgelegt werden. Dies ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b2df-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="3b2df-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="3b2df-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="3b2df-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3b2df-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3b2df-118">Die Anzahl der festzulegenden Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="3b2df-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b2df-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b2df-119">Return value</span></span>

<span data-ttu-id="3b2df-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b2df-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b2df-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="3b2df-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3b2df-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b2df-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3b2df-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="3b2df-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3b2df-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3b2df-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3b2df-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3b2df-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3b2df-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3b2df-126">Requirements</span></span>



| <span data-ttu-id="3b2df-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b2df-127">Requirement</span></span> | <span data-ttu-id="3b2df-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3b2df-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b2df-129">Header</span><span class="sxs-lookup"><span data-stu-id="3b2df-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3b2df-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b2df-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3b2df-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3b2df-131">Library</span></span><br/> | <dl> <span data-ttu-id="3b2df-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="3b2df-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b2df-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3b2df-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b2df-134">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="3b2df-134">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

