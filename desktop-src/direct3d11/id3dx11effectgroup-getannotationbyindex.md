---
title: ID3DX11EffectGroup getannotationbyindex-Methode (D3dx11effect. h)
description: Eine Anmerkung nach Index erhalten. | ID3DX11EffectGroup getannotationbyindex-Methode (D3dx11effect. h)
ms.assetid: 9d3a54b1-384b-4ed4-96a3-09d6bacafda1
keywords:
- Getannotationbyindex-Methode Direct3D 11
- Getannotationbyindex-Methode Direct3D 11, ID3DX11EffectGroup-Schnittstelle
- ID3DX11EffectGroup Interface Direct3D 11, getannotationbyindex-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 663dc8d487552dba521c8e47f9a1eecf6db38122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219602"
---
# <a name="id3dx11effectgroupgetannotationbyindex-method"></a><span data-ttu-id="82347-107">ID3DX11EffectGroup:: getannotationbyindex-Methode</span><span class="sxs-lookup"><span data-stu-id="82347-107">ID3DX11EffectGroup::GetAnnotationByIndex method</span></span>

<span data-ttu-id="82347-108">Eine Anmerkung nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="82347-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="82347-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="82347-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="82347-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="82347-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82347-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="82347-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="82347-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="82347-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="82347-113">Der Index der Anmerkung.</span><span class="sxs-lookup"><span data-stu-id="82347-113">Index of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82347-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82347-114">Return value</span></span>

<span data-ttu-id="82347-115">Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="82347-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="82347-116">Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="82347-116">Pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="82347-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82347-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="82347-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="82347-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="82347-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="82347-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="82347-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="82347-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="82347-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="82347-121">Requirements</span></span>



| <span data-ttu-id="82347-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82347-122">Requirement</span></span> | <span data-ttu-id="82347-123">Wert</span><span class="sxs-lookup"><span data-stu-id="82347-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82347-124">Header</span><span class="sxs-lookup"><span data-stu-id="82347-124">Header</span></span><br/>  | <dl> <span data-ttu-id="82347-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="82347-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="82347-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="82347-126">Library</span></span><br/> | <dl> <span data-ttu-id="82347-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="82347-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82347-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="82347-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82347-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="82347-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

