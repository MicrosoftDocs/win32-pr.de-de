---
title: ID3DX11EffectTechnique getannotationbyname-Methode (D3dx11effect. h)
description: Eine Anmerkung anhand des Namens erhalten. | ID3DX11EffectTechnique getannotationbyname-Methode (D3dx11effect. h)
ms.assetid: 3a9e1fa7-4586-42d6-a723-3140f29a01b4
keywords:
- Getannotationbyname-Methode Direct3D 11
- Getannotationbyname-Methode Direct3D 11, ID3DX11EffectTechnique-Schnittstelle
- ID3DX11EffectTechnique Interface Direct3D 11, getannotationbyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae5a7c24d392bd034dfcd69fb67723c9492f982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355126"
---
# <a name="id3dx11effecttechniquegetannotationbyname-method"></a><span data-ttu-id="a2999-107">ID3DX11EffectTechnique:: getannotationbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="a2999-107">ID3DX11EffectTechnique::GetAnnotationByName method</span></span>

<span data-ttu-id="a2999-108">Eine Anmerkung anhand des Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="a2999-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2999-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2999-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="a2999-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2999-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2999-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="a2999-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="a2999-112">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a2999-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a2999-113">Der Name der Anmerkung.</span><span class="sxs-lookup"><span data-stu-id="a2999-113">Name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2999-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2999-114">Return value</span></span>

<span data-ttu-id="a2999-115">Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="a2999-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="a2999-116">Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="a2999-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2999-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2999-117">Remarks</span></span>

<span data-ttu-id="a2999-118">Verwenden Sie eine Anmerkung, um einen Teil der Metadaten an eine Technik anzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2999-118">Use an annotation to attach a piece of metadata to a technique.</span></span>

> [!Note]  
> <span data-ttu-id="a2999-119">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="a2999-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a2999-120">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a2999-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a2999-121">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a2999-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2999-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a2999-122">Requirements</span></span>



| <span data-ttu-id="a2999-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2999-123">Requirement</span></span> | <span data-ttu-id="a2999-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a2999-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2999-125">Header</span><span class="sxs-lookup"><span data-stu-id="a2999-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a2999-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2999-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a2999-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a2999-127">Library</span></span><br/> | <dl> <span data-ttu-id="a2999-128"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="a2999-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2999-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a2999-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2999-130">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="a2999-130">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

