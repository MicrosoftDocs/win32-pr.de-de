---
title: ID3DX11EffectConstantBuffer getconstantbuffer-Methode (D3dx11effect. h)
description: Einen konstanten Puffer erhalten.
ms.assetid: 857b3dc2-41ae-4a52-904a-9ca8f0afeb9e
keywords:
- Getconstantbuffer-Methode Direct3D 11
- Getconstantbuffer-Methode Direct3D 11, ID3DX11EffectConstantBuffer-Schnittstelle
- ID3DX11EffectConstantBuffer-Schnittstelle Direct3D 11, getconstantbuffer-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041ca2fea028cb86d0959313bae73c320e6e5a36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050941"
---
# <a name="id3dx11effectconstantbuffergetconstantbuffer-method"></a><span data-ttu-id="30df6-106">ID3DX11EffectConstantBuffer:: getconstantbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="30df6-106">ID3DX11EffectConstantBuffer::GetConstantBuffer method</span></span>

<span data-ttu-id="30df6-107">Einen konstanten Puffer erhalten.</span><span class="sxs-lookup"><span data-stu-id="30df6-107">Get a constant-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="30df6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30df6-108">Syntax</span></span>


```C++
HRESULT GetConstantBuffer(
   ID3D11Buffer **ppConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="30df6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="30df6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30df6-110">*ppconstantbuffer*</span><span class="sxs-lookup"><span data-stu-id="30df6-110">*ppConstantBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="30df6-111">Typ: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="30df6-111">Type: **[**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***</span></span>

<span data-ttu-id="30df6-112">Die Adresse eines Zeigers auf eine Konstante Puffer Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="30df6-112">The address of a pointer to a constant-buffer interface.</span></span> <span data-ttu-id="30df6-113">Siehe [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span><span class="sxs-lookup"><span data-stu-id="30df6-113">See [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30df6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30df6-114">Return value</span></span>

<span data-ttu-id="30df6-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30df6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30df6-116">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="30df6-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30df6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30df6-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30df6-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="30df6-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="30df6-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="30df6-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="30df6-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="30df6-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30df6-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="30df6-121">Requirements</span></span>



| <span data-ttu-id="30df6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30df6-122">Requirement</span></span> | <span data-ttu-id="30df6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="30df6-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30df6-124">Header</span><span class="sxs-lookup"><span data-stu-id="30df6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="30df6-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="30df6-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="30df6-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30df6-126">Library</span></span><br/> | <dl> <span data-ttu-id="30df6-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="30df6-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30df6-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="30df6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30df6-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="30df6-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





