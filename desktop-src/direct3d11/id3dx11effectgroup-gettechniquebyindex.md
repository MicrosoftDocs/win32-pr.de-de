---
title: ID3DX11EffectGroup gettechniquebyindex-Methode (D3dx11effect. h)
description: Holen Sie sich eine Technik nach Index. | ID3DX11EffectGroup gettechniquebyindex-Methode (D3dx11effect. h)
ms.assetid: b0962957-20d1-4ec6-9f8e-acc7a62c5f4e
keywords:
- Gettechniquebyindex-Methode Direct3D 11
- Gettechniquebyindex-Methode Direct3D 11, ID3DX11EffectGroup-Schnittstelle
- ID3DX11EffectGroup-Schnittstelle Direct3D 11, gettechniquebyindex-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe42d71886ae93bdaff7ac956554ff9a97fc9f8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961670"
---
# <a name="id3dx11effectgroupgettechniquebyindex-method"></a><span data-ttu-id="308f7-107">ID3DX11EffectGroup:: gettechniquebyindex-Methode</span><span class="sxs-lookup"><span data-stu-id="308f7-107">ID3DX11EffectGroup::GetTechniqueByIndex method</span></span>

<span data-ttu-id="308f7-108">Holen Sie sich eine Technik nach Index.</span><span class="sxs-lookup"><span data-stu-id="308f7-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="308f7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="308f7-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="308f7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="308f7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="308f7-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="308f7-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="308f7-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="308f7-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="308f7-113">Ein NULL basierter Index.</span><span class="sxs-lookup"><span data-stu-id="308f7-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="308f7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="308f7-114">Return value</span></span>

<span data-ttu-id="308f7-115">Typ: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="308f7-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="308f7-116">Ein Zeiger auf eine [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="308f7-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="308f7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="308f7-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="308f7-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="308f7-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="308f7-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="308f7-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="308f7-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="308f7-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="308f7-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="308f7-121">Requirements</span></span>



| <span data-ttu-id="308f7-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="308f7-122">Requirement</span></span> | <span data-ttu-id="308f7-123">Wert</span><span class="sxs-lookup"><span data-stu-id="308f7-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="308f7-124">Header</span><span class="sxs-lookup"><span data-stu-id="308f7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="308f7-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="308f7-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="308f7-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="308f7-126">Library</span></span><br/> | <dl> <span data-ttu-id="308f7-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="308f7-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="308f7-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="308f7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="308f7-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="308f7-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

