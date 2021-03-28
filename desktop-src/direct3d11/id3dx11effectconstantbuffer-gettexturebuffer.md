---
title: ID3DX11EffectConstantBuffer gettexturebuffer-Methode (D3dx11effect. h)
description: Einen Textur Puffer erhalten.
ms.assetid: 8d09e67c-358e-49ee-8ca4-e1f548b52c3a
keywords:
- Gettexturebuffer-Methode Direct3D 11
- Gettexturebuffer-Methode Direct3D 11, ID3DX11EffectConstantBuffer-Schnittstelle
- ID3DX11EffectConstantBuffer-Schnittstelle Direct3D 11, gettexturebuffer-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03000338c725e71096e57715a49a70b4347b358
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982477"
---
# <a name="id3dx11effectconstantbuffergettexturebuffer-method"></a><span data-ttu-id="ffec1-106">ID3DX11EffectConstantBuffer:: gettexturebuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="ffec1-106">ID3DX11EffectConstantBuffer::GetTextureBuffer method</span></span>

<span data-ttu-id="ffec1-107">Einen Textur Puffer erhalten.</span><span class="sxs-lookup"><span data-stu-id="ffec1-107">Get a texture-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffec1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffec1-108">Syntax</span></span>


```C++
HRESULT GetTextureBuffer(
   ID3D11ShaderResourceView **ppTextureBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ffec1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffec1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffec1-110">*pptexturebuffer*</span><span class="sxs-lookup"><span data-stu-id="ffec1-110">*ppTextureBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="ffec1-111">Typ: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="ffec1-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="ffec1-112">Die Adresse eines Zeigers auf eine Shader-Resource-View-Schnittstelle für den Zugriff auf einen Textur Puffer.</span><span class="sxs-lookup"><span data-stu-id="ffec1-112">The address of a pointer to a shader-resource-view interface for accessing a texture buffer.</span></span> <span data-ttu-id="ffec1-113">Siehe [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="ffec1-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffec1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffec1-114">Return value</span></span>

<span data-ttu-id="ffec1-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ffec1-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ffec1-116">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="ffec1-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ffec1-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffec1-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ffec1-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="ffec1-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ffec1-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ffec1-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ffec1-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ffec1-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ffec1-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ffec1-121">Requirements</span></span>



| <span data-ttu-id="ffec1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffec1-122">Requirement</span></span> | <span data-ttu-id="ffec1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ffec1-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffec1-124">Header</span><span class="sxs-lookup"><span data-stu-id="ffec1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ffec1-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffec1-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ffec1-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ffec1-126">Library</span></span><br/> | <dl> <span data-ttu-id="ffec1-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="ffec1-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffec1-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ffec1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffec1-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="ffec1-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





