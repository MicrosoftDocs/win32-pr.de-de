---
title: ID3DX11EffectConstantBuffer undosettexturebuffer-Methode (D3dx11effect. h)
description: Stellt einen zuvor festgelegten Textur Puffer wieder her.
ms.assetid: 982e7899-9569-4611-9fe0-b78624acba2c
keywords:
- Undosettexturebuffer-Methode Direct3D 11
- Undosettexturebuffer-Methode Direct3D 11, ID3DX11EffectConstantBuffer-Schnittstelle
- ID3DX11EffectConstantBuffer-Schnittstelle Direct3D 11, undosettexturebuffer-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.UndoSetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5e1e1b2be167466da5a4d92999646bb7c8f225
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355257"
---
# <a name="id3dx11effectconstantbufferundosettexturebuffer-method"></a><span data-ttu-id="60be2-106">ID3DX11EffectConstantBuffer:: undosettexturebuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="60be2-106">ID3DX11EffectConstantBuffer::UndoSetTextureBuffer method</span></span>

<span data-ttu-id="60be2-107">Stellt einen zuvor festgelegten Textur Puffer wieder her.</span><span class="sxs-lookup"><span data-stu-id="60be2-107">Reverts a previously set texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="60be2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="60be2-108">Syntax</span></span>


```C++
HRESULT UndoSetTextureBuffer();
```



## <a name="parameters"></a><span data-ttu-id="60be2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="60be2-109">Parameters</span></span>

<span data-ttu-id="60be2-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="60be2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="60be2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60be2-111">Return value</span></span>

<span data-ttu-id="60be2-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60be2-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60be2-113">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="60be2-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="60be2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60be2-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="60be2-115">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="60be2-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="60be2-116">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="60be2-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="60be2-117">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="60be2-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="60be2-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="60be2-118">Requirements</span></span>



| <span data-ttu-id="60be2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60be2-119">Requirement</span></span> | <span data-ttu-id="60be2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="60be2-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60be2-121">Header</span><span class="sxs-lookup"><span data-stu-id="60be2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="60be2-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="60be2-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="60be2-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60be2-123">Library</span></span><br/> | <dl> <span data-ttu-id="60be2-124"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="60be2-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60be2-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="60be2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60be2-126">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="60be2-126">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





