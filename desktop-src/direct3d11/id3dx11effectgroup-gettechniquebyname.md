---
title: ID3DX11EffectGroup gettechniquebyname-Methode (D3dx11effect. h)
description: Holen Sie sich eine Technik anhand des Namens. | ID3DX11EffectGroup gettechniquebyname-Methode (D3dx11effect. h)
ms.assetid: 160c6d57-bec4-4718-8fad-fc9c0746736c
keywords:
- Gettechniquebyname-Methode Direct3D 11
- Gettechniquebyname-Methode Direct3D 11, ID3DX11EffectGroup-Schnittstelle
- ID3DX11EffectGroup-Schnittstelle Direct3D 11, gettechniquebyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5121f67345ba863d773d8e7a73a5d6fa8b69895
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982293"
---
# <a name="id3dx11effectgroupgettechniquebyname-method"></a><span data-ttu-id="767dd-107">ID3DX11EffectGroup:: gettechniquebyname-Methode</span><span class="sxs-lookup"><span data-stu-id="767dd-107">ID3DX11EffectGroup::GetTechniqueByName method</span></span>

<span data-ttu-id="767dd-108">Holen Sie sich eine Technik anhand des Namens.</span><span class="sxs-lookup"><span data-stu-id="767dd-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="767dd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="767dd-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="767dd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="767dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="767dd-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="767dd-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="767dd-112">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="767dd-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="767dd-113">Der Name der Technik.</span><span class="sxs-lookup"><span data-stu-id="767dd-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="767dd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="767dd-114">Return value</span></span>

<span data-ttu-id="767dd-115">Typ: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="767dd-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="767dd-116">Ein Zeiger auf ein [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)-oder **null** -Wert, wenn die Technik nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="767dd-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md), or **NULL** if the technique is not found.</span></span>

## <a name="remarks"></a><span data-ttu-id="767dd-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="767dd-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="767dd-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="767dd-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="767dd-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="767dd-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="767dd-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="767dd-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="767dd-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="767dd-121">Requirements</span></span>



| <span data-ttu-id="767dd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="767dd-122">Requirement</span></span> | <span data-ttu-id="767dd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="767dd-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="767dd-124">Header</span><span class="sxs-lookup"><span data-stu-id="767dd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="767dd-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="767dd-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="767dd-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="767dd-126">Library</span></span><br/> | <dl> <span data-ttu-id="767dd-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="767dd-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="767dd-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="767dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="767dd-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="767dd-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

