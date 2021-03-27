---
title: ID3DX11EffectTechnique getpassbyname-Methode (D3dx11effect. h)
description: Einen Pass-Through-Namen erhalten.
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- Getpassbyname-Methode Direct3D 11
- Getpassbyname-Methode Direct3D 11, ID3DX11EffectTechnique-Schnittstelle
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11, getpassbyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84bbe9b954efff12e458ee6172665118a7b8ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995973"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a><span data-ttu-id="0b9da-106">ID3DX11EffectTechnique:: getpassbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="0b9da-106">ID3DX11EffectTechnique::GetPassByName method</span></span>

<span data-ttu-id="0b9da-107">Einen Pass-Through-Namen erhalten.</span><span class="sxs-lookup"><span data-stu-id="0b9da-107">Get a pass by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b9da-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b9da-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="0b9da-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b9da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b9da-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="0b9da-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="0b9da-111">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0b9da-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0b9da-112">Der Name des Pass-.</span><span class="sxs-lookup"><span data-stu-id="0b9da-112">The name of the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b9da-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b9da-113">Return value</span></span>

<span data-ttu-id="0b9da-114">Typ: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b9da-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="0b9da-115">Ein Zeiger auf eine [**ID3DX11EffectPass**](id3dx11effectpass.md).</span><span class="sxs-lookup"><span data-stu-id="0b9da-115">A pointer to an [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b9da-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b9da-116">Remarks</span></span>

<span data-ttu-id="0b9da-117">Eine Technik enthält einen oder mehrere Durchgänge. Sie erhalten einen Durchlauf mithilfe eines Namens oder eines Indexes.</span><span class="sxs-lookup"><span data-stu-id="0b9da-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="0b9da-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="0b9da-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0b9da-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b9da-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0b9da-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0b9da-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b9da-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0b9da-121">Requirements</span></span>



| <span data-ttu-id="0b9da-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b9da-122">Requirement</span></span> | <span data-ttu-id="0b9da-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0b9da-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b9da-124">Header</span><span class="sxs-lookup"><span data-stu-id="0b9da-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0b9da-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b9da-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0b9da-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b9da-126">Library</span></span><br/> | <dl> <span data-ttu-id="0b9da-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="0b9da-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b9da-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0b9da-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b9da-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="0b9da-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

