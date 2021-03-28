---
title: ID3DX11Effect gettechniquebyindex-Methode (D3dx11effect. h)
description: Holen Sie sich eine Technik nach Index. | ID3DX11Effect gettechniquebyindex-Methode (D3dx11effect. h)
ms.assetid: ee9c0cc3-0ca1-42e8-bd37-5878fd56cff1
keywords:
- Gettechniquebyindex-Methode Direct3D 11
- Gettechniquebyindex-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, gettechniquebyindex-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81d3be5ec403fb25ab3a49792ed77fd4d96bf571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961706"
---
# <a name="id3dx11effectgettechniquebyindex-method"></a><span data-ttu-id="37b70-107">ID3DX11Effect:: gettechniquebyindex-Methode</span><span class="sxs-lookup"><span data-stu-id="37b70-107">ID3DX11Effect::GetTechniqueByIndex method</span></span>

<span data-ttu-id="37b70-108">Holen Sie sich eine Technik nach Index.</span><span class="sxs-lookup"><span data-stu-id="37b70-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="37b70-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="37b70-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="37b70-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="37b70-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b70-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="37b70-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="37b70-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="37b70-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="37b70-113">Ein NULL basierter Index.</span><span class="sxs-lookup"><span data-stu-id="37b70-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b70-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37b70-114">Return value</span></span>

<span data-ttu-id="37b70-115">Typ: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="37b70-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="37b70-116">Ein Zeiger auf eine [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="37b70-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="37b70-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37b70-117">Remarks</span></span>

<span data-ttu-id="37b70-118">Ein Effekt enthält mindestens eine Technik. jede Technik enthält einen oder mehrere Durchgänge.</span><span class="sxs-lookup"><span data-stu-id="37b70-118">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="37b70-119">Sie können auf eine Technik mithilfe Ihres Namens oder eines Indexes zugreifen.</span><span class="sxs-lookup"><span data-stu-id="37b70-119">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="37b70-120">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="37b70-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="37b70-121">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="37b70-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="37b70-122">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="37b70-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="37b70-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="37b70-123">Requirements</span></span>



| <span data-ttu-id="37b70-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37b70-124">Requirement</span></span> | <span data-ttu-id="37b70-125">Wert</span><span class="sxs-lookup"><span data-stu-id="37b70-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37b70-126">Header</span><span class="sxs-lookup"><span data-stu-id="37b70-126">Header</span></span><br/>  | <dl> <span data-ttu-id="37b70-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="37b70-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="37b70-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="37b70-128">Library</span></span><br/> | <dl> <span data-ttu-id="37b70-129"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="37b70-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37b70-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="37b70-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b70-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="37b70-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

