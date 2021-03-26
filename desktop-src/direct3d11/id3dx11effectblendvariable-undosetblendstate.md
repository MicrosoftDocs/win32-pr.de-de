---
title: ID3DX11EffectBlendVariable undosetblendstate-Methode (D3dx11effect. h)
description: Kehrt einen zuvor festgelegten Blend-Status zurück.
ms.assetid: 375c225b-558f-4ad0-81e7-62eff3e28cf1
keywords:
- Undosetblendstate-Methode Direct3D 11
- Undosetblendstate-Methode Direct3D 11, ID3DX11EffectBlendVariable-Schnittstelle
- ID3DX11EffectBlendVariable-Schnittstelle Direct3D 11, undosetblendstate-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.UndoSetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e117eafa9b6379b2240cf491809c58d8600d840f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996076"
---
# <a name="id3dx11effectblendvariableundosetblendstate-method"></a><span data-ttu-id="de4b3-106">ID3DX11EffectBlendVariable:: undosetblendstate-Methode</span><span class="sxs-lookup"><span data-stu-id="de4b3-106">ID3DX11EffectBlendVariable::UndoSetBlendState method</span></span>

<span data-ttu-id="de4b3-107">Kehrt einen zuvor festgelegten Blend-Status zurück.</span><span class="sxs-lookup"><span data-stu-id="de4b3-107">Reverts a previously set blend-state.</span></span>

## <a name="syntax"></a><span data-ttu-id="de4b3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="de4b3-108">Syntax</span></span>


```C++
HRESULT UndoSetBlendState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="de4b3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="de4b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de4b3-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="de4b3-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="de4b3-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="de4b3-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="de4b3-112">Indizieren Sie in ein Array von Blend-State-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="de4b3-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="de4b3-113">Wenn nur eine Blend-State-Schnittstelle vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="de4b3-113">If there is only one blend-state interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de4b3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de4b3-114">Return value</span></span>

<span data-ttu-id="de4b3-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="de4b3-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="de4b3-116">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="de4b3-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="de4b3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de4b3-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="de4b3-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="de4b3-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="de4b3-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="de4b3-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="de4b3-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="de4b3-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de4b3-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="de4b3-121">Requirements</span></span>



| <span data-ttu-id="de4b3-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de4b3-122">Requirement</span></span> | <span data-ttu-id="de4b3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="de4b3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de4b3-124">Header</span><span class="sxs-lookup"><span data-stu-id="de4b3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="de4b3-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="de4b3-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="de4b3-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de4b3-126">Library</span></span><br/> | <dl> <span data-ttu-id="de4b3-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="de4b3-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de4b3-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="de4b3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4b3-129">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="de4b3-129">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

