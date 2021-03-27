---
title: ID3DX11EffectUnorderedAccessViewVariable getunorderedaccessview-Methode (D3dx11effect. h)
description: Erhalten Sie eine ungeordnete Zugriffs Ansicht.
ms.assetid: 46f61c4f-b3ee-4058-99b9-a43ca6944fb2
keywords:
- Getunorderedaccessview-Methode Direct3D 11
- Getunorderedaccessview-Methode Direct3D 11, ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle
- ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle Direct3D 11, getunorderedaccessview-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7743d15c2380ff4e38bdcae1d38bbd8905cbccda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996186"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessview-method"></a><span data-ttu-id="71ffb-106">ID3DX11EffectUnorderedAccessViewVariable:: getunorderedaccessview-Methode</span><span class="sxs-lookup"><span data-stu-id="71ffb-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessView method</span></span>

<span data-ttu-id="71ffb-107">Erhalten Sie eine ungeordnete Zugriffs Ansicht.</span><span class="sxs-lookup"><span data-stu-id="71ffb-107">Get an unordered-access-view.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ffb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="71ffb-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessView(
   ID3D11UnorderedAccessView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="71ffb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="71ffb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ffb-110">*ppresource*</span><span class="sxs-lookup"><span data-stu-id="71ffb-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="71ffb-111">Typ: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="71ffb-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="71ffb-112">Zeiger auf einen [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) -Zeiger, der bei der Rückgabe festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="71ffb-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ffb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71ffb-113">Return value</span></span>

<span data-ttu-id="71ffb-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71ffb-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71ffb-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="71ffb-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="71ffb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71ffb-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="71ffb-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="71ffb-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="71ffb-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="71ffb-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="71ffb-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="71ffb-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="71ffb-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="71ffb-120">Requirements</span></span>



| <span data-ttu-id="71ffb-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71ffb-121">Requirement</span></span> | <span data-ttu-id="71ffb-122">Wert</span><span class="sxs-lookup"><span data-stu-id="71ffb-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71ffb-123">Header</span><span class="sxs-lookup"><span data-stu-id="71ffb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="71ffb-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="71ffb-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="71ffb-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71ffb-125">Library</span></span><br/> | <dl> <span data-ttu-id="71ffb-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="71ffb-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ffb-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="71ffb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ffb-128">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="71ffb-128">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





