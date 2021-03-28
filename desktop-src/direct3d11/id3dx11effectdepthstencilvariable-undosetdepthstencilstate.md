---
title: ID3DX11EffectDepthStencilVariable undosetdepthstencilstate-Methode (D3dx11effect. h)
description: Stellt einen zuvor festgelegten tiefen Schablone Zustand wieder her.
ms.assetid: 558bc777-a520-4235-84d3-db2d9f1ce4b6
keywords:
- Undosetdepthstencilstate-Methode Direct3D 11
- Undosetdepthstencilstate-Methode Direct3D 11, ID3DX11EffectDepthStencilVariable-Schnittstelle
- ID3DX11EffectDepthStencilVariable-Schnittstelle Direct3D 11, undosetdepthstencilstate-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.UndoSetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd44d486d2613406617f0534046c54818267dd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996146"
---
# <a name="id3dx11effectdepthstencilvariableundosetdepthstencilstate-method"></a><span data-ttu-id="9bf62-106">ID3DX11EffectDepthStencilVariable:: undosetdepthstencilstate-Methode</span><span class="sxs-lookup"><span data-stu-id="9bf62-106">ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState method</span></span>

<span data-ttu-id="9bf62-107">Stellt einen zuvor festgelegten tiefen Schablone Zustand wieder her.</span><span class="sxs-lookup"><span data-stu-id="9bf62-107">Reverts a previously set depth stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf62-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bf62-108">Syntax</span></span>


```C++
HRESULT UndoSetDepthStencilState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="9bf62-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bf62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bf62-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="9bf62-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="9bf62-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9bf62-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9bf62-112">Indizieren Sie in ein Array von tiefen Schablonen Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="9bf62-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="9bf62-113">Wenn nur eine tiefen Schablone-Schnittstelle vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="9bf62-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bf62-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9bf62-114">Return value</span></span>

<span data-ttu-id="9bf62-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9bf62-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9bf62-116">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="9bf62-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9bf62-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bf62-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9bf62-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="9bf62-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9bf62-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9bf62-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9bf62-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9bf62-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9bf62-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9bf62-121">Requirements</span></span>



| <span data-ttu-id="9bf62-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bf62-122">Requirement</span></span> | <span data-ttu-id="9bf62-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9bf62-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf62-124">Header</span><span class="sxs-lookup"><span data-stu-id="9bf62-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9bf62-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bf62-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9bf62-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9bf62-126">Library</span></span><br/> | <dl> <span data-ttu-id="9bf62-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="9bf62-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bf62-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9bf62-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf62-129">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="9bf62-129">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

