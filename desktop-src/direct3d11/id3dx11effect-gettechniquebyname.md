---
title: ID3DX11Effect gettechniquebyname-Methode (D3dx11effect. h)
description: Holen Sie sich eine Technik anhand des Namens. | ID3DX11Effect gettechniquebyname-Methode (D3dx11effect. h)
ms.assetid: 0f7fa02c-dfbf-4971-86ad-3429f99f84e0
keywords:
- Gettechniquebyname-Methode Direct3D 11
- Gettechniquebyname-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, gettechniquebyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d26b6067352d4ca898cc1fc970524040d407bda1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982419"
---
# <a name="id3dx11effectgettechniquebyname-method"></a><span data-ttu-id="2cf93-107">ID3DX11Effect:: gettechniquebyname-Methode</span><span class="sxs-lookup"><span data-stu-id="2cf93-107">ID3DX11Effect::GetTechniqueByName method</span></span>

<span data-ttu-id="2cf93-108">Holen Sie sich eine Technik anhand des Namens.</span><span class="sxs-lookup"><span data-stu-id="2cf93-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf93-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cf93-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="2cf93-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cf93-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cf93-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="2cf93-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="2cf93-112">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2cf93-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2cf93-113">Der Name der Technik.</span><span class="sxs-lookup"><span data-stu-id="2cf93-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cf93-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cf93-114">Return value</span></span>

<span data-ttu-id="2cf93-115">Typ: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cf93-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="2cf93-116">Ein Zeiger auf eine [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="2cf93-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span> <span data-ttu-id="2cf93-117">Wenn eine Technik mit dem entsprechenden Namen nicht gefunden wird, wird eine ungültige Technik zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2cf93-117">If a technique with the appropriate name is not found an invalid technique is returned.</span></span> <span data-ttu-id="2cf93-118">[**ID3DX11EffectTechnique:: IsValid**](id3dx11effecttechnique-isvalid.md) sollte für die zurückgegebene Technik aufgerufen werden, um zu bestimmen, ob Sie gültig ist.</span><span class="sxs-lookup"><span data-stu-id="2cf93-118">[**ID3DX11EffectTechnique::IsValid**](id3dx11effecttechnique-isvalid.md) should be called on the returned technique to determine whether it is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cf93-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cf93-119">Remarks</span></span>

<span data-ttu-id="2cf93-120">Ein Effekt enthält mindestens eine Technik. jede Technik enthält einen oder mehrere Durchgänge.</span><span class="sxs-lookup"><span data-stu-id="2cf93-120">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="2cf93-121">Sie können auf eine Technik mithilfe Ihres Namens oder eines Indexes zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2cf93-121">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="2cf93-122">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="2cf93-122">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2cf93-123">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2cf93-123">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2cf93-124">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2cf93-124">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2cf93-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2cf93-125">Requirements</span></span>



| <span data-ttu-id="2cf93-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cf93-126">Requirement</span></span> | <span data-ttu-id="2cf93-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2cf93-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf93-128">Header</span><span class="sxs-lookup"><span data-stu-id="2cf93-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2cf93-129"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cf93-129"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2cf93-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2cf93-130">Library</span></span><br/> | <dl> <span data-ttu-id="2cf93-131"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="2cf93-131"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cf93-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2cf93-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf93-133">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="2cf93-133">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

