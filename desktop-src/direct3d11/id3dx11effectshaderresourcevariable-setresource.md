---
title: ID3DX11EffectShaderResourceVariable-Methode für die Ziel Quelle (D3dx11effect. h)
description: Legen Sie eine Shaderressource fest.
ms.assetid: f85c33ff-dc00-4421-939c-74f9317faadc
keywords:
- Methode "-tretresource" Direct3D 11
- Methode ' Direct3D 11 ', ID3DX11EffectShaderResourceVariable-Schnittstelle
- ID3DX11EffectShaderResourceVariable-Schnittstelle Direct3D 11, Methode "Ziel Quelle"
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.SetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec6c7daa2db552d6b5befee02bf57c6047dc5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356097"
---
# <a name="id3dx11effectshaderresourcevariablesetresource-method"></a><span data-ttu-id="45990-106">ID3DX11EffectShaderResourceVariable:: abtresource-Methode</span><span class="sxs-lookup"><span data-stu-id="45990-106">ID3DX11EffectShaderResourceVariable::SetResource method</span></span>

<span data-ttu-id="45990-107">Legen Sie eine Shaderressource fest.</span><span class="sxs-lookup"><span data-stu-id="45990-107">Set a shader resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="45990-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="45990-108">Syntax</span></span>


```C++
HRESULT SetResource(
   ID3D11ShaderResourceView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="45990-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="45990-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45990-110">*vorab Quelle*</span><span class="sxs-lookup"><span data-stu-id="45990-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="45990-111">Typ: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="45990-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span></span>

<span data-ttu-id="45990-112">Die Adresse eines Zeigers auf eine Shader-Resource-View-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="45990-112">The address of a pointer to a shader-resource-view interface.</span></span> <span data-ttu-id="45990-113">Siehe [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="45990-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45990-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45990-114">Return value</span></span>

<span data-ttu-id="45990-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="45990-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="45990-116">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="45990-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="45990-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45990-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="45990-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="45990-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="45990-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="45990-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="45990-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="45990-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="45990-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="45990-121">Requirements</span></span>



| <span data-ttu-id="45990-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45990-122">Requirement</span></span> | <span data-ttu-id="45990-123">Wert</span><span class="sxs-lookup"><span data-stu-id="45990-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45990-124">Header</span><span class="sxs-lookup"><span data-stu-id="45990-124">Header</span></span><br/>  | <dl> <span data-ttu-id="45990-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="45990-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="45990-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="45990-126">Library</span></span><br/> | <dl> <span data-ttu-id="45990-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="45990-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45990-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="45990-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45990-129">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="45990-129">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





