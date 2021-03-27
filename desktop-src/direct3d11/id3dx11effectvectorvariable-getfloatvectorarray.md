---
title: ID3DX11EffectVectorVariable getfloatvectorarray-Methode (D3dx11effect. h)
description: Sie erhalten ein Array von Vektoren mit vier Komponenten, die Gleit Komma Daten enthalten.
ms.assetid: 30ecbd97-c16d-4ea9-b7d9-364887f42a04
keywords:
- Getfloatvectorarray-Methode Direct3D 11
- Getfloatvectorarray-Methode Direct3D 11, ID3DX11EffectVectorVariable-Schnittstelle
- ID3DX11EffectVectorVariable-Schnittstelle Direct3D 11, getfloatvectorarray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetFloatVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a4c53b884c623ca3d11fb4a9a44660ce21d8a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982401"
---
# <a name="id3dx11effectvectorvariablegetfloatvectorarray-method"></a><span data-ttu-id="aa888-106">ID3DX11EffectVectorVariable:: getfloatvectorarray-Methode</span><span class="sxs-lookup"><span data-stu-id="aa888-106">ID3DX11EffectVectorVariable::GetFloatVectorArray method</span></span>

<span data-ttu-id="aa888-107">Sie erhalten ein Array von Vektoren mit vier Komponenten, die Gleit Komma Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa888-107">Get an array of four-component vectors that contain floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa888-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa888-108">Syntax</span></span>


```C++
HRESULT GetFloatVectorArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="aa888-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa888-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa888-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="aa888-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="aa888-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="aa888-111">Type: **float\***</span></span>

<span data-ttu-id="aa888-112">Ein Zeiger auf den Anfang der festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="aa888-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="aa888-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="aa888-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="aa888-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aa888-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="aa888-115">Muss auf 0 (null) festgelegt werden. Dies ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="aa888-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="aa888-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="aa888-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="aa888-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aa888-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="aa888-118">Die Anzahl der festzulegenden Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="aa888-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa888-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa888-119">Return value</span></span>

<span data-ttu-id="aa888-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aa888-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aa888-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="aa888-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aa888-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa888-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="aa888-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="aa888-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="aa888-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aa888-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="aa888-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="aa888-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aa888-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="aa888-126">Requirements</span></span>



| <span data-ttu-id="aa888-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa888-127">Requirement</span></span> | <span data-ttu-id="aa888-128">Wert</span><span class="sxs-lookup"><span data-stu-id="aa888-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa888-129">Header</span><span class="sxs-lookup"><span data-stu-id="aa888-129">Header</span></span><br/>  | <dl> <span data-ttu-id="aa888-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa888-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="aa888-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aa888-131">Library</span></span><br/> | <dl> <span data-ttu-id="aa888-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="aa888-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa888-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aa888-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa888-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="aa888-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

