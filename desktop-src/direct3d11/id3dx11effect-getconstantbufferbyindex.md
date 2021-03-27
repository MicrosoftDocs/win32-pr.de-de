---
title: ID3DX11Effect getconstantbufferbyindex-Methode (D3dx11effect. h)
description: Einen konstanten Puffer nach Index erhalten.
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- Getconstantbufferbyindex-Methode Direct3D 11
- Getconstantbufferbyindex-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, getconstantbufferbyindex-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbc44b2d9ceea1bcfbf854a8d3c6998d03e3eec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982425"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a><span data-ttu-id="f82ec-106">ID3DX11Effect:: getconstantbufferbyindex-Methode</span><span class="sxs-lookup"><span data-stu-id="f82ec-106">ID3DX11Effect::GetConstantBufferByIndex method</span></span>

<span data-ttu-id="f82ec-107">Einen konstanten Puffer nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="f82ec-107">Get a constant buffer by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f82ec-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f82ec-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="f82ec-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f82ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f82ec-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="f82ec-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="f82ec-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f82ec-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f82ec-112">Ein NULL basierter Index.</span><span class="sxs-lookup"><span data-stu-id="f82ec-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f82ec-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f82ec-113">Return value</span></span>

<span data-ttu-id="f82ec-114">Typ: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f82ec-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="f82ec-115">Ein Zeiger auf eine [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="f82ec-115">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f82ec-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f82ec-116">Remarks</span></span>

<span data-ttu-id="f82ec-117">Ein Effekt, der eine Variable enthält, die von einer Anwendung gelesen/geschrieben wird, erfordert mindestens einen konstanten Puffer.</span><span class="sxs-lookup"><span data-stu-id="f82ec-117">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="f82ec-118">Um die optimale Leistung zu erzielen, sollten Sie die Variablen basierend auf Ihrer Aktualisierungshäufigkeit in mindestens einen konstanten Puffer anordnen.</span><span class="sxs-lookup"><span data-stu-id="f82ec-118">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="f82ec-119">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="f82ec-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f82ec-120">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f82ec-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f82ec-121">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f82ec-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f82ec-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f82ec-122">Requirements</span></span>



| <span data-ttu-id="f82ec-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f82ec-123">Requirement</span></span> | <span data-ttu-id="f82ec-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f82ec-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f82ec-125">Header</span><span class="sxs-lookup"><span data-stu-id="f82ec-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f82ec-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f82ec-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f82ec-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f82ec-127">Library</span></span><br/> | <dl> <span data-ttu-id="f82ec-128"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="f82ec-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f82ec-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f82ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f82ec-130">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="f82ec-130">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

