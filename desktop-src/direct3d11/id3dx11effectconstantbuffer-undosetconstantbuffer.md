---
title: ID3DX11EffectConstantBuffer undosetconstantbuffer-Methode (D3dx11effect. h)
description: Stellt einen zuvor festgelegten Konstanten Puffer wieder her.
ms.assetid: 6c5e1256-3a92-4bfe-8614-f09d627bc3db
keywords:
- Undosetconstantbuffer-Methode Direct3D 11
- Undosetconstantbuffer-Methode Direct3D 11, ID3DX11EffectConstantBuffer-Schnittstelle
- ID3DX11EffectConstantBuffer-Schnittstelle Direct3D 11, undosetconstantbuffer-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.UndoSetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c95a26f1ea92d5bfe1975e3fe4dc1961046e5535
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394222"
---
# <a name="id3dx11effectconstantbufferundosetconstantbuffer-method"></a><span data-ttu-id="f3a3c-106">ID3DX11EffectConstantBuffer:: undosetconstantbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="f3a3c-106">ID3DX11EffectConstantBuffer::UndoSetConstantBuffer method</span></span>

<span data-ttu-id="f3a3c-107">Stellt einen zuvor festgelegten Konstanten Puffer wieder her.</span><span class="sxs-lookup"><span data-stu-id="f3a3c-107">Reverts a previously set constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a3c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3a3c-108">Syntax</span></span>


```C++
HRESULT UndoSetConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="f3a3c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3a3c-109">Parameters</span></span>

<span data-ttu-id="f3a3c-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f3a3c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3a3c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3a3c-111">Return value</span></span>

<span data-ttu-id="f3a3c-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f3a3c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f3a3c-113">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="f3a3c-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a3c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3a3c-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f3a3c-115">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="f3a3c-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f3a3c-116">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f3a3c-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f3a3c-117">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f3a3c-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f3a3c-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f3a3c-118">Requirements</span></span>



| <span data-ttu-id="f3a3c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3a3c-119">Requirement</span></span> | <span data-ttu-id="f3a3c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f3a3c-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a3c-121">Header</span><span class="sxs-lookup"><span data-stu-id="f3a3c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f3a3c-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3a3c-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f3a3c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f3a3c-123">Library</span></span><br/> | <dl> <span data-ttu-id="f3a3c-124"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="f3a3c-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a3c-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f3a3c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a3c-126">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="f3a3c-126">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





