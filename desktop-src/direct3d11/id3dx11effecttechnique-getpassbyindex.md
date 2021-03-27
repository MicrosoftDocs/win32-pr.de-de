---
title: ID3DX11EffectTechnique getpassbyindex-Methode (D3dx11effect. h)
description: Einen Pass-by-Index erhalten.
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- Getpassbyindex-Methode Direct3D 11
- Getpassbyindex-Methode Direct3D 11, ID3DX11EffectTechnique-Schnittstelle
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11, getpassbyindex-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6af222298cc3d00ad87e5037f9de20139e4fc40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961719"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a><span data-ttu-id="27063-106">ID3DX11EffectTechnique:: getpassbyindex-Methode</span><span class="sxs-lookup"><span data-stu-id="27063-106">ID3DX11EffectTechnique::GetPassByIndex method</span></span>

<span data-ttu-id="27063-107">Einen Pass-by-Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="27063-107">Get a pass by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="27063-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="27063-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="27063-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="27063-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27063-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="27063-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="27063-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="27063-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="27063-112">Ein NULL basierter Index.</span><span class="sxs-lookup"><span data-stu-id="27063-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27063-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27063-113">Return value</span></span>

<span data-ttu-id="27063-114">Typ: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="27063-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="27063-115">Ein Zeiger auf eine [**ID3DX11EffectPass**](id3dx11effectpass.md).</span><span class="sxs-lookup"><span data-stu-id="27063-115">A pointer to a [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="27063-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27063-116">Remarks</span></span>

<span data-ttu-id="27063-117">Eine Technik enthält einen oder mehrere Durchgänge. Sie erhalten einen Durchlauf mithilfe eines Namens oder eines Indexes.</span><span class="sxs-lookup"><span data-stu-id="27063-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="27063-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="27063-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="27063-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="27063-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="27063-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="27063-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27063-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="27063-121">Requirements</span></span>



| <span data-ttu-id="27063-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27063-122">Requirement</span></span> | <span data-ttu-id="27063-123">Wert</span><span class="sxs-lookup"><span data-stu-id="27063-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27063-124">Header</span><span class="sxs-lookup"><span data-stu-id="27063-124">Header</span></span><br/>  | <dl> <span data-ttu-id="27063-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="27063-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="27063-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="27063-126">Library</span></span><br/> | <dl> <span data-ttu-id="27063-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="27063-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27063-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="27063-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27063-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="27063-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

