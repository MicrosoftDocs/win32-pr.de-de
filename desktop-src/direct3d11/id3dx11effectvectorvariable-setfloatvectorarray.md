---
title: ID3DX11EffectVectorVariable setfloatvectorarray-Methode (D3dx11effect. h)
description: Legen Sie ein Array von Vektoren mit vier Komponenten fest, die Gleit Komma Daten enthalten.
ms.assetid: f07edf0f-8a90-41bf-ae03-5a62a19e57e2
keywords:
- Setfloatvectorarray-Methode Direct3D 11
- Setfloatvectorarray-Methode Direct3D 11, ID3DX11EffectVectorVariable-Schnittstelle
- ID3DX11EffectVectorVariable-Schnittstelle Direct3D 11, setfloatvectorarray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetFloatVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f8f731dd90251848095f899bdc141bbc1d6748
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982395"
---
# <a name="id3dx11effectvectorvariablesetfloatvectorarray-method"></a><span data-ttu-id="2eaa9-106">ID3DX11EffectVectorVariable:: setfloatvectorarray-Methode</span><span class="sxs-lookup"><span data-stu-id="2eaa9-106">ID3DX11EffectVectorVariable::SetFloatVectorArray method</span></span>

<span data-ttu-id="2eaa9-107">Legen Sie ein Array von Vektoren mit vier Komponenten fest, die Gleit Komma Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-107">Set an array of four-component vectors that contain floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eaa9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eaa9-108">Syntax</span></span>


```C++
HRESULT SetFloatVectorArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="2eaa9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2eaa9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eaa9-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="2eaa9-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="2eaa9-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="2eaa9-111">Type: **float\***</span></span>

<span data-ttu-id="2eaa9-112">Ein Zeiger auf den Anfang der festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="2eaa9-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="2eaa9-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="2eaa9-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2eaa9-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2eaa9-115">Muss auf 0 (null) festgelegt werden. Dies ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="2eaa9-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="2eaa9-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="2eaa9-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2eaa9-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2eaa9-118">Die Anzahl der festzulegenden Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eaa9-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2eaa9-119">Return value</span></span>

<span data-ttu-id="2eaa9-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2eaa9-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2eaa9-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2eaa9-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2eaa9-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2eaa9-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2eaa9-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2eaa9-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2eaa9-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2eaa9-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2eaa9-126">Requirements</span></span>



| <span data-ttu-id="2eaa9-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2eaa9-127">Requirement</span></span> | <span data-ttu-id="2eaa9-128">Wert</span><span class="sxs-lookup"><span data-stu-id="2eaa9-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eaa9-129">Header</span><span class="sxs-lookup"><span data-stu-id="2eaa9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2eaa9-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eaa9-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2eaa9-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2eaa9-131">Library</span></span><br/> | <dl> <span data-ttu-id="2eaa9-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="2eaa9-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eaa9-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2eaa9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eaa9-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="2eaa9-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

