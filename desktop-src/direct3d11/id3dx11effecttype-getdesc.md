---
title: ID3DX11EffectType getdesc-Methode (D3dx11effect. h)
description: Geben Sie eine Beschreibung des Effekt Typs an.
ms.assetid: 08a8a1b6-fe2d-431b-a0e4-d628f0ceb1a0
keywords:
- Getdesc-Methode Direct3D 11
- Getdesc-Methode Direct3D 11, ID3DX11EffectType-Schnittstelle
- ID3DX11EffectType-Schnittstelle Direct3D 11, getdesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1ee52e4c6628c00b0155e5bd3081b6c4fd8c46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996242"
---
# <a name="id3dx11effecttypegetdesc-method"></a><span data-ttu-id="4ecce-106">ID3DX11EffectType:: getdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="4ecce-106">ID3DX11EffectType::GetDesc method</span></span>

<span data-ttu-id="4ecce-107">Geben Sie eine Beschreibung des Effekt Typs an.</span><span class="sxs-lookup"><span data-stu-id="4ecce-107">Get an effect-type description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ecce-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ecce-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_TYPE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="4ecce-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ecce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ecce-110">*PDE SC*</span><span class="sxs-lookup"><span data-stu-id="4ecce-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="4ecce-111">Type: **[ **Bibliothek d3dx11 \_ Effect \_ Type \_ DESC**](d3dx11-effect-type-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ecce-111">Type: **[**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md)\***</span></span>

<span data-ttu-id="4ecce-112">Ein Zeiger auf eine Effekts-Typbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="4ecce-112">A pointer to an effect-type description.</span></span> <span data-ttu-id="4ecce-113">Weitere Informationen finden Sie unter [**Bibliothek d3dx11 \_ Effect \_ Type \_ DESC**](d3dx11-effect-type-desc.md).</span><span class="sxs-lookup"><span data-stu-id="4ecce-113">See [**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ecce-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ecce-114">Return value</span></span>

<span data-ttu-id="4ecce-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ecce-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ecce-116">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="4ecce-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ecce-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ecce-117">Remarks</span></span>

<span data-ttu-id="4ecce-118">Die Beschreibung der Effekt Variablen enthält Daten über den Namen, die Anmerkungen, die Semantik, die Flags und den Puffer Offset des Effekt Typs.</span><span class="sxs-lookup"><span data-stu-id="4ecce-118">The effect-variable description contains data about the name, annotations, semantic, flags and buffer offset of the effect type.</span></span>

> [!Note]  
> <span data-ttu-id="4ecce-119">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="4ecce-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4ecce-120">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ecce-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4ecce-121">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4ecce-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ecce-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4ecce-122">Requirements</span></span>



| <span data-ttu-id="4ecce-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ecce-123">Requirement</span></span> | <span data-ttu-id="4ecce-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4ecce-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ecce-125">Header</span><span class="sxs-lookup"><span data-stu-id="4ecce-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4ecce-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ecce-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4ecce-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4ecce-127">Library</span></span><br/> | <dl> <span data-ttu-id="4ecce-128"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="4ecce-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ecce-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4ecce-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ecce-130">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="4ecce-130">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

 





