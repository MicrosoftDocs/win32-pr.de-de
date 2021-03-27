---
title: ID3DX11EffectDepthStencilVariable getbackingstore-Methode (D3dx11effect. h)
description: Einen Zeiger auf eine Variable mit dem Status der tiefen Schablone erhalten.
ms.assetid: 6aeed5ac-f0ee-4e8c-b87b-022f58c9094c
keywords:
- Getbackingstore-Methode Direct3D 11
- Getbackingstore-Methode Direct3D 11, ID3DX11EffectDepthStencilVariable-Schnittstelle
- ID3DX11EffectDepthStencilVariable Interface Direct3D 11, getbackingstore-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9335817b9c954958c97294a88291f83bf0e967d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982306"
---
# <a name="id3dx11effectdepthstencilvariablegetbackingstore-method"></a><span data-ttu-id="7e9e7-106">ID3DX11EffectDepthStencilVariable:: getbackingstore-Methode</span><span class="sxs-lookup"><span data-stu-id="7e9e7-106">ID3DX11EffectDepthStencilVariable::GetBackingStore method</span></span>

<span data-ttu-id="7e9e7-107">Einen Zeiger auf eine Variable mit dem Status der tiefen Schablone erhalten.</span><span class="sxs-lookup"><span data-stu-id="7e9e7-107">Get a pointer to a variable that contains depth-stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e9e7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e9e7-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT                     Index,
   D3D11_DEPTH_STENCIL_DESC *pDepthStencilDesc
);
```



## <a name="parameters"></a><span data-ttu-id="7e9e7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e9e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e9e7-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="7e9e7-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="7e9e7-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7e9e7-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7e9e7-112">Indizieren Sie in ein Array von Beschreibungen der tiefen Schablone.</span><span class="sxs-lookup"><span data-stu-id="7e9e7-112">Index into an array of depth-stencil-state descriptions.</span></span> <span data-ttu-id="7e9e7-113">Wenn nur eine tiefen Schablone-Variable vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="7e9e7-113">If there is only one depth-stencil variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="7e9e7-114">*pdepthstencildesc*</span><span class="sxs-lookup"><span data-stu-id="7e9e7-114">*pDepthStencilDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="7e9e7-115">Typ: **[ **D3D11 \_ tiefen \_ Schablone \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)\***</span><span class="sxs-lookup"><span data-stu-id="7e9e7-115">Type: **[**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)\***</span></span>

<span data-ttu-id="7e9e7-116">Ein Zeiger auf eine Beschreibung des tiefen Schablone-Zustands (siehe [**D3D11 \_ tiefen Schablone- \_ modificil \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span><span class="sxs-lookup"><span data-stu-id="7e9e7-116">A pointer to a depth-stencil-state description (see [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e9e7-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e9e7-117">Return value</span></span>

<span data-ttu-id="7e9e7-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e9e7-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e9e7-119">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="7e9e7-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7e9e7-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e9e7-120">Remarks</span></span>

<span data-ttu-id="7e9e7-121">Effekt Variablen werden im Sicherungs Speicher im Arbeitsspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Sicherungs Speicher auf das Gerät kopiert.</span><span class="sxs-lookup"><span data-stu-id="7e9e7-121">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="7e9e7-122">Das Sichern von Speicherdaten kann verwendet werden, um die Variable bei Bedarf neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7e9e7-122">Backing store data can used to recreate the variable when necessary.</span></span>

> [!Note]  
> <span data-ttu-id="7e9e7-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="7e9e7-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7e9e7-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7e9e7-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7e9e7-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7e9e7-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7e9e7-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7e9e7-126">Requirements</span></span>



| <span data-ttu-id="7e9e7-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e9e7-127">Requirement</span></span> | <span data-ttu-id="7e9e7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7e9e7-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e9e7-129">Header</span><span class="sxs-lookup"><span data-stu-id="7e9e7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7e9e7-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e9e7-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7e9e7-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7e9e7-131">Library</span></span><br/> | <dl> <span data-ttu-id="7e9e7-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="7e9e7-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e9e7-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7e9e7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e9e7-134">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="7e9e7-134">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

