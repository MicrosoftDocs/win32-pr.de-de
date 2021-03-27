---
title: ID3DX11EffectRasterizerVariable getrasterizerstate-Methode (D3dx11effect. h)
description: Einen Zeiger auf eine Raster-Schnittstelle erhalten.
ms.assetid: 4b8515e0-b79a-4572-9142-07c50a8839b8
keywords:
- Getrasterizerstate-Methode Direct3D 11
- Getrasterizerstate-Methode Direct3D 11, ID3DX11EffectRasterizerVariable-Schnittstelle
- ID3DX11EffectRasterizerVariable-Schnittstelle Direct3D 11, getrasterizerstate-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972140a8f74a3e5a6728429faddacc253aaa6c9d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982628"
---
# <a name="id3dx11effectrasterizervariablegetrasterizerstate-method"></a><span data-ttu-id="fb7b3-106">ID3DX11EffectRasterizerVariable:: getrasterizerstate-Methode</span><span class="sxs-lookup"><span data-stu-id="fb7b3-106">ID3DX11EffectRasterizerVariable::GetRasterizerState method</span></span>

<span data-ttu-id="fb7b3-107">Einen Zeiger auf eine Raster-Schnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-107">Get a pointer to a rasterizer interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb7b3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb7b3-108">Syntax</span></span>


```C++
HRESULT GetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState **ppRasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="fb7b3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb7b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb7b3-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="fb7b3-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="fb7b3-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fb7b3-112">Index in ein Array von Raster-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="fb7b3-113">Wenn nur eine Raster-Schnittstelle vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="fb7b3-114">*pprasterizerstate*</span><span class="sxs-lookup"><span data-stu-id="fb7b3-114">*ppRasterizerState*</span></span> 
</dt> <dd>

<span data-ttu-id="fb7b3-115">Typ: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="fb7b3-115">Type: **[**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***</span></span>

<span data-ttu-id="fb7b3-116">Die Adresse eines Zeigers auf eine Raster-Schnittstelle (siehe [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).</span><span class="sxs-lookup"><span data-stu-id="fb7b3-116">The address of a pointer to a rasterizer interface (see [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb7b3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb7b3-117">Return value</span></span>

<span data-ttu-id="fb7b3-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb7b3-119">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb7b3-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb7b3-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fb7b3-121">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fb7b3-122">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fb7b3-123">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fb7b3-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb7b3-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fb7b3-124">Requirements</span></span>



| <span data-ttu-id="fb7b3-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb7b3-125">Requirement</span></span> | <span data-ttu-id="fb7b3-126">Wert</span><span class="sxs-lookup"><span data-stu-id="fb7b3-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb7b3-127">Header</span><span class="sxs-lookup"><span data-stu-id="fb7b3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fb7b3-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb7b3-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fb7b3-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb7b3-129">Library</span></span><br/> | <dl> <span data-ttu-id="fb7b3-130"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="fb7b3-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb7b3-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fb7b3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb7b3-132">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="fb7b3-132">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

