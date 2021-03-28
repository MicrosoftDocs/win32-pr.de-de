---
title: ID3DX11EffectUnorderedAccessViewVariable-Methode für die Methode "-Methode" (D3dx11effect. h)
description: Legen Sie eine ungeordnete Zugriffs Ansicht fest.
ms.assetid: a147879c-c5cf-4453-b27f-8716cb33962b
keywords:
- Methode "stunorderedaccessview" Direct3D 11
- "\"Stunorderedaccessview\"-Methode Direct3D 11, ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle"
- ID3DX11EffectUnorderedAccessViewVariable Interface Direct3D 11, Methode "stunorderedaccessview"
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d665ab5b298e3a7549fb068cf0fcc4cce644765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995830"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessview-method"></a><span data-ttu-id="9b927-106">ID3DX11EffectUnorderedAccessViewVariable:: stunorderedaccessview-Methode</span><span class="sxs-lookup"><span data-stu-id="9b927-106">ID3DX11EffectUnorderedAccessViewVariable::SetUnorderedAccessView method</span></span>

<span data-ttu-id="9b927-107">Legen Sie eine ungeordnete Zugriffs Ansicht fest.</span><span class="sxs-lookup"><span data-stu-id="9b927-107">Set an unordered-access-view.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b927-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b927-108">Syntax</span></span>


```C++
HRESULT SetUnorderedAccessView(
   ID3D11UnorderedAccessView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="9b927-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b927-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b927-110">*vorab Quelle*</span><span class="sxs-lookup"><span data-stu-id="9b927-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="9b927-111">Typ: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\***</span><span class="sxs-lookup"><span data-stu-id="9b927-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\***</span></span>

<span data-ttu-id="9b927-112">Zeiger auf eine [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview).</span><span class="sxs-lookup"><span data-stu-id="9b927-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b927-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b927-113">Return value</span></span>

<span data-ttu-id="9b927-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b927-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b927-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="9b927-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b927-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b927-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9b927-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="9b927-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9b927-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b927-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9b927-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9b927-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b927-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9b927-120">Requirements</span></span>



| <span data-ttu-id="9b927-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b927-121">Requirement</span></span> | <span data-ttu-id="9b927-122">Wert</span><span class="sxs-lookup"><span data-stu-id="9b927-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b927-123">Header</span><span class="sxs-lookup"><span data-stu-id="9b927-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9b927-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b927-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9b927-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9b927-125">Library</span></span><br/> | <dl> <span data-ttu-id="9b927-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="9b927-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b927-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9b927-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b927-128">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="9b927-128">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





