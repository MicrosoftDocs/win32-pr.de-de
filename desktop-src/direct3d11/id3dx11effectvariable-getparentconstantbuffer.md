---
title: ID3DX11EffectVariable getcentconstantbuffer-Methode (D3dx11effect. h)
description: Einen konstanten Puffer erhalten. | ID3DX11EffectVariable getcentconstantbuffer-Methode (D3dx11effect. h)
ms.assetid: 43b46b05-951e-4c52-8bc7-4bb5f657ea78
keywords:
- Getparameentconstantbuffer-Methode Direct3D 11
- Getparameentconstantbuffer-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable Interface Direct3D 11, getparameentconstantbuffer-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetParentConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa424b91b72dca5539fd0f96a1380e86d1f23f58
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996250"
---
# <a name="id3dx11effectvariablegetparentconstantbuffer-method"></a><span data-ttu-id="61a10-107">ID3DX11EffectVariable:: getparameentconstantbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="61a10-107">ID3DX11EffectVariable::GetParentConstantBuffer method</span></span>

<span data-ttu-id="61a10-108">Einen konstanten Puffer erhalten.</span><span class="sxs-lookup"><span data-stu-id="61a10-108">Get a constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="61a10-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="61a10-109">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetParentConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="61a10-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="61a10-110">Parameters</span></span>

<span data-ttu-id="61a10-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="61a10-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61a10-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61a10-112">Return value</span></span>

<span data-ttu-id="61a10-113">Typ: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="61a10-113">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="61a10-114">Ein Zeiger auf eine [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="61a10-114">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="61a10-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61a10-115">Remarks</span></span>

<span data-ttu-id="61a10-116">Effekt Variablen sind Lese-oder Schreibvorgänge in einen konstanten Puffer.</span><span class="sxs-lookup"><span data-stu-id="61a10-116">Effect variables are read-from or written-to a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="61a10-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="61a10-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="61a10-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="61a10-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="61a10-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="61a10-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="61a10-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="61a10-120">Requirements</span></span>



| <span data-ttu-id="61a10-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61a10-121">Requirement</span></span> | <span data-ttu-id="61a10-122">Wert</span><span class="sxs-lookup"><span data-stu-id="61a10-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a10-123">Header</span><span class="sxs-lookup"><span data-stu-id="61a10-123">Header</span></span><br/>  | <dl> <span data-ttu-id="61a10-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="61a10-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="61a10-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="61a10-125">Library</span></span><br/> | <dl> <span data-ttu-id="61a10-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="61a10-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61a10-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="61a10-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a10-128">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="61a10-128">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





