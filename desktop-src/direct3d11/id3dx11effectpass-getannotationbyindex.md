---
title: ID3DX11EffectPass getannotationbyindex-Methode (D3dx11effect. h)
description: Eine Anmerkung nach Index erhalten. | ID3DX11EffectPass getannotationbyindex-Methode (D3dx11effect. h)
ms.assetid: 734eeeca-58c2-4f0c-84d1-2898394a03d6
keywords:
- Getannotationbyindex-Methode Direct3D 11
- Getannotationbyindex-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass Interface Direct3D 11, getannotationbyindex-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afd43a52758e82434a0e0a4161484ea0d4dcc611
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982438"
---
# <a name="id3dx11effectpassgetannotationbyindex-method"></a><span data-ttu-id="45cb3-107">ID3DX11EffectPass:: getannotationbyindex-Methode</span><span class="sxs-lookup"><span data-stu-id="45cb3-107">ID3DX11EffectPass::GetAnnotationByIndex method</span></span>

<span data-ttu-id="45cb3-108">Eine Anmerkung nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="45cb3-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="45cb3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="45cb3-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="45cb3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="45cb3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45cb3-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="45cb3-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="45cb3-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="45cb3-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="45cb3-113">Ein NULL basierter Index.</span><span class="sxs-lookup"><span data-stu-id="45cb3-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45cb3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45cb3-114">Return value</span></span>

<span data-ttu-id="45cb3-115">Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="45cb3-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="45cb3-116">Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="45cb3-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="45cb3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45cb3-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="45cb3-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="45cb3-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="45cb3-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="45cb3-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="45cb3-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="45cb3-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="45cb3-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="45cb3-121">Requirements</span></span>



| <span data-ttu-id="45cb3-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45cb3-122">Requirement</span></span> | <span data-ttu-id="45cb3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="45cb3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45cb3-124">Header</span><span class="sxs-lookup"><span data-stu-id="45cb3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="45cb3-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="45cb3-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="45cb3-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="45cb3-126">Library</span></span><br/> | <dl> <span data-ttu-id="45cb3-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="45cb3-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45cb3-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="45cb3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45cb3-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="45cb3-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

