---
title: ID3DX11EffectBlendVariable getbackingstore-Methode (D3dx11effect. h)
description: Einen Zeiger auf eine Blend-State-Variable erhalten.
ms.assetid: 809daaad-9bf0-48fb-ae91-f237c43db324
keywords:
- Getbackingstore-Methode Direct3D 11
- Getbackingstore-Methode Direct3D 11, ID3DX11EffectBlendVariable-Schnittstelle
- ID3DX11EffectBlendVariable Interface Direct3D 11, getbackingstore-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0220481b58931edace2a5dfe7298d83f7bd1325
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219642"
---
# <a name="id3dx11effectblendvariablegetbackingstore-method"></a><span data-ttu-id="d4b97-106">ID3DX11EffectBlendVariable:: getbackingstore-Methode</span><span class="sxs-lookup"><span data-stu-id="d4b97-106">ID3DX11EffectBlendVariable::GetBackingStore method</span></span>

<span data-ttu-id="d4b97-107">Einen Zeiger auf eine Blend-State-Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4b97-107">Get a pointer to a blend-state variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4b97-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4b97-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT             Index,
   D3D11_BLEND_DESC *pBlendDesc
);
```



## <a name="parameters"></a><span data-ttu-id="d4b97-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4b97-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4b97-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="d4b97-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="d4b97-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4b97-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d4b97-112">Indizieren Sie in ein Array von Blend-Zustandsbeschreibungen.</span><span class="sxs-lookup"><span data-stu-id="d4b97-112">Index into an array of blend-state descriptions.</span></span> <span data-ttu-id="d4b97-113">Wenn nur eine Blend-State-Variable vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="d4b97-113">If there is only one blend-state variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="d4b97-114">*pblenddebug*</span><span class="sxs-lookup"><span data-stu-id="d4b97-114">*pBlendDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="d4b97-115">Typ: **[ **D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)\***</span><span class="sxs-lookup"><span data-stu-id="d4b97-115">Type: **[**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)\***</span></span>

<span data-ttu-id="d4b97-116">Ein Zeiger auf eine Blend-Statusbeschreibung (siehe [**D3D11 \_ Blend \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)-Debug).</span><span class="sxs-lookup"><span data-stu-id="d4b97-116">A pointer to a blend-state description (see [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4b97-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4b97-117">Return value</span></span>

<span data-ttu-id="d4b97-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4b97-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4b97-119">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="d4b97-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4b97-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4b97-120">Remarks</span></span>

<span data-ttu-id="d4b97-121">Effekt Variablen werden im Sicherungs Speicher im Arbeitsspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Sicherungs Speicher auf das Gerät kopiert.</span><span class="sxs-lookup"><span data-stu-id="d4b97-121">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="d4b97-122">Das Sichern von Speicherdaten kann verwendet werden, um die Variable bei Bedarf neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4b97-122">Backing store data can used to recreate the variable when necessary.</span></span>

> [!Note]  
> <span data-ttu-id="d4b97-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="d4b97-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d4b97-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4b97-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d4b97-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d4b97-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d4b97-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d4b97-126">Requirements</span></span>



| <span data-ttu-id="d4b97-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4b97-127">Requirement</span></span> | <span data-ttu-id="d4b97-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d4b97-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b97-129">Header</span><span class="sxs-lookup"><span data-stu-id="d4b97-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d4b97-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4b97-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d4b97-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d4b97-131">Library</span></span><br/> | <dl> <span data-ttu-id="d4b97-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="d4b97-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4b97-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4b97-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b97-134">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="d4b97-134">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

