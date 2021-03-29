---
title: ID3DX11EffectRasterizerVariable tartrasterizerstate-Methode (D3dx11effect. h)
description: Legt den Status des Rasterizers fest.
ms.assetid: b2cd93fb-77bb-4a39-b686-7b8f683c9172
keywords:
- "\"Tartrasterizerstate\"-Methode Direct3D 11"
- "\"Tartrasterizerstate\"-Methode Direct3D 11, ID3DX11EffectRasterizerVariable-Schnittstelle"
- ID3DX11EffectRasterizerVariable Interface Direct3D 11, Methode "tartrasterizerstate"
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.SetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1f44df653339f274207bfa4283fc8470c8844f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219716"
---
# <a name="id3dx11effectrasterizervariablesetrasterizerstate-method"></a><span data-ttu-id="47723-106">ID3DX11EffectRasterizerVariable:: tartrasterizerstate-Methode</span><span class="sxs-lookup"><span data-stu-id="47723-106">ID3DX11EffectRasterizerVariable::SetRasterizerState method</span></span>

<span data-ttu-id="47723-107">Legt den Status des Rasterizers fest.</span><span class="sxs-lookup"><span data-stu-id="47723-107">Sets the rasterizer state.</span></span>

## <a name="syntax"></a><span data-ttu-id="47723-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="47723-108">Syntax</span></span>


```C++
HRESULT SetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState *pRasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="47723-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="47723-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47723-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="47723-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="47723-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="47723-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="47723-112">Index in ein Array von Raster-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="47723-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="47723-113">Wenn nur eine Raster-Schnittstelle vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="47723-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="47723-114">*"prasterizerstate"*</span><span class="sxs-lookup"><span data-stu-id="47723-114">*pRasterizerState*</span></span> 
</dt> <dd>

<span data-ttu-id="47723-115">Typ: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***</span><span class="sxs-lookup"><span data-stu-id="47723-115">Type: **[**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***</span></span>

<span data-ttu-id="47723-116">Zeiger auf eine [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="47723-116">Pointer to an [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47723-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47723-117">Return value</span></span>

<span data-ttu-id="47723-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47723-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47723-119">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="47723-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="47723-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47723-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="47723-121">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="47723-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="47723-122">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="47723-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="47723-123">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="47723-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="47723-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="47723-124">Requirements</span></span>



| <span data-ttu-id="47723-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47723-125">Requirement</span></span> | <span data-ttu-id="47723-126">Wert</span><span class="sxs-lookup"><span data-stu-id="47723-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47723-127">Header</span><span class="sxs-lookup"><span data-stu-id="47723-127">Header</span></span><br/>  | <dl> <span data-ttu-id="47723-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="47723-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="47723-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="47723-129">Library</span></span><br/> | <dl> <span data-ttu-id="47723-130"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="47723-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47723-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="47723-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47723-132">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="47723-132">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

