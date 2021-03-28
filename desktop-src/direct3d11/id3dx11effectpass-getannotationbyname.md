---
title: ID3DX11EffectPass getannotationbyname-Methode (D3dx11effect. h)
description: Eine Anmerkung anhand des Namens erhalten. | ID3DX11EffectPass getannotationbyname-Methode (D3dx11effect. h)
ms.assetid: b54a4fb0-62c7-4d96-af30-f9ae04ff7dab
keywords:
- Getannotationbyname-Methode Direct3D 11
- Getannotationbyname-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass Interface Direct3D 11, getannotationbyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129f1548e7f63c47906ac736cbddb5f6b2548b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961688"
---
# <a name="id3dx11effectpassgetannotationbyname-method"></a><span data-ttu-id="b61fd-107">ID3DX11EffectPass:: getannotationbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="b61fd-107">ID3DX11EffectPass::GetAnnotationByName method</span></span>

<span data-ttu-id="b61fd-108">Eine Anmerkung anhand des Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="b61fd-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="b61fd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b61fd-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="b61fd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b61fd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b61fd-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="b61fd-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="b61fd-112">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b61fd-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b61fd-113">Der Name des Annotation-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b61fd-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b61fd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b61fd-114">Return value</span></span>

<span data-ttu-id="b61fd-115">Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="b61fd-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="b61fd-116">Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="b61fd-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b61fd-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b61fd-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b61fd-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="b61fd-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b61fd-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b61fd-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b61fd-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b61fd-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b61fd-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b61fd-121">Requirements</span></span>



| <span data-ttu-id="b61fd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b61fd-122">Requirement</span></span> | <span data-ttu-id="b61fd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b61fd-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b61fd-124">Header</span><span class="sxs-lookup"><span data-stu-id="b61fd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b61fd-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b61fd-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b61fd-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b61fd-126">Library</span></span><br/> | <dl> <span data-ttu-id="b61fd-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="b61fd-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b61fd-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b61fd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b61fd-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="b61fd-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

