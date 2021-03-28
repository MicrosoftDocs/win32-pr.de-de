---
title: ID3DX11EffectGroup getannotationbyname-Methode (D3dx11effect. h)
description: Eine Anmerkung anhand des Namens erhalten. | ID3DX11EffectGroup getannotationbyname-Methode (D3dx11effect. h)
ms.assetid: c526a249-fb56-47bb-a0c2-b829a1da88e8
keywords:
- Getannotationbyname-Methode Direct3D 11
- Getannotationbyname-Methode Direct3D 11, ID3DX11EffectGroup-Schnittstelle
- ID3DX11EffectGroup Interface Direct3D 11, getannotationbyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1880983785fcfea8a4cda4aa09c8baec2cfebf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995961"
---
# <a name="id3dx11effectgroupgetannotationbyname-method"></a><span data-ttu-id="ee8f6-107">ID3DX11EffectGroup:: getannotationbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="ee8f6-107">ID3DX11EffectGroup::GetAnnotationByName method</span></span>

<span data-ttu-id="ee8f6-108">Eine Anmerkung anhand des Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="ee8f6-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee8f6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee8f6-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="ee8f6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee8f6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee8f6-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="ee8f6-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="ee8f6-112">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ee8f6-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ee8f6-113">Der Name des Annotation-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ee8f6-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee8f6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee8f6-114">Return value</span></span>

<span data-ttu-id="ee8f6-115">Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee8f6-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="ee8f6-116">Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="ee8f6-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="ee8f6-117">Beachten Sie, dass die zurückgegebene **ID3DX11EffectVariable** leer ist, wenn die Anmerkung nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="ee8f6-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="ee8f6-118">Die [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md) -Methode sollte aufgerufen werden, um zu bestimmen, ob die Anmerkung gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="ee8f6-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee8f6-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee8f6-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ee8f6-120">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="ee8f6-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ee8f6-121">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee8f6-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ee8f6-122">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ee8f6-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee8f6-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ee8f6-123">Requirements</span></span>



| <span data-ttu-id="ee8f6-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee8f6-124">Requirement</span></span> | <span data-ttu-id="ee8f6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ee8f6-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8f6-126">Header</span><span class="sxs-lookup"><span data-stu-id="ee8f6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ee8f6-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee8f6-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ee8f6-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ee8f6-128">Library</span></span><br/> | <dl> <span data-ttu-id="ee8f6-129"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="ee8f6-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee8f6-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ee8f6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee8f6-131">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="ee8f6-131">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

