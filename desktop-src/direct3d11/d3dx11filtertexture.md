---
title: D3DX11FilterTexture-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie die directxtex-Bibliothek, generatemipmaps und GenerateMipMaps3D verwenden, anstatt diese Funktion zu verwenden. Generiert eine MipMap-Kette mithilfe eines bestimmten Textur Filters.
ms.assetid: 52ae3228-f9d7-4944-b49c-55df1816f1f7
keywords:
- D3DX11FilterTexture-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11FilterTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e74e60e9d66e2a5251c161e4df6451266d3fb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982335"
---
# <a name="d3dx11filtertexture-function"></a><span data-ttu-id="35fc5-106">D3DX11FilterTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="35fc5-106">D3DX11FilterTexture function</span></span>

> [!Note]  
> <span data-ttu-id="35fc5-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="35fc5-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="35fc5-108">Anstatt diese Funktion zu verwenden, wird empfohlen, dass Sie die [directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek, **generatemipmaps** und **GenerateMipMaps3D** verwenden.</span><span class="sxs-lookup"><span data-stu-id="35fc5-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GenerateMipMaps** and **GenerateMipMaps3D**.</span></span>

 

<span data-ttu-id="35fc5-109">Generiert eine MipMap-Kette mithilfe eines bestimmten Textur Filters.</span><span class="sxs-lookup"><span data-stu-id="35fc5-109">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="35fc5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="35fc5-110">Syntax</span></span>


```C++
HRESULT D3DX11FilterTexture(
   ID3D11DeviceContext *pContext,
   ID3D11Resource      *pTexture,
   UINT                SrcLevel,
   UINT                MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="35fc5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="35fc5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fc5-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="35fc5-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="35fc5-113">Typ: **[ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="35fc5-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="35fc5-114">Ein Zeiger auf ein [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="35fc5-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="35fc5-115">*ptexture*</span><span class="sxs-lookup"><span data-stu-id="35fc5-115">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="35fc5-116">Typ: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="35fc5-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="35fc5-117">Das zu filternde Textur Objekt.</span><span class="sxs-lookup"><span data-stu-id="35fc5-117">The texture object to be filtered.</span></span> <span data-ttu-id="35fc5-118">Siehe [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="35fc5-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="35fc5-119">*Srclevel*</span><span class="sxs-lookup"><span data-stu-id="35fc5-119">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="35fc5-120">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35fc5-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="35fc5-121">Die MipMap-Ebene, deren Daten verwendet werden, um den Rest der MipMap-Kette zu generieren.</span><span class="sxs-lookup"><span data-stu-id="35fc5-121">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="35fc5-122">*MipFilter*</span><span class="sxs-lookup"><span data-stu-id="35fc5-122">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="35fc5-123">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35fc5-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="35fc5-124">Flags, die Steuern, wie die einzelnen miplevel-Werte gefiltert werden (oder Bibliothek d3dx11 \_ default for Bibliothek d3dx11 \_ Filter \_ linear).</span><span class="sxs-lookup"><span data-stu-id="35fc5-124">Flags controlling how each miplevel is filtered (or D3DX11\_DEFAULT for D3DX11\_FILTER\_LINEAR).</span></span> <span data-ttu-id="35fc5-125">Siehe [**Bibliothek d3dx11 \_ Filter- \_ Flag**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="35fc5-125">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fc5-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35fc5-126">Return value</span></span>

<span data-ttu-id="35fc5-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35fc5-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35fc5-128">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="35fc5-128">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35fc5-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="35fc5-129">Requirements</span></span>



| <span data-ttu-id="35fc5-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35fc5-130">Requirement</span></span> | <span data-ttu-id="35fc5-131">Wert</span><span class="sxs-lookup"><span data-stu-id="35fc5-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35fc5-132">Header</span><span class="sxs-lookup"><span data-stu-id="35fc5-132">Header</span></span><br/>  | <dl> <span data-ttu-id="35fc5-133"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="35fc5-133"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="35fc5-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="35fc5-134">Library</span></span><br/> | <dl> <span data-ttu-id="35fc5-135"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35fc5-135"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="35fc5-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="35fc5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fc5-137">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="35fc5-137">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

