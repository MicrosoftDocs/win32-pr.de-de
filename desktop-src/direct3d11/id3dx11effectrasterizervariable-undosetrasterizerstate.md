---
title: ID3DX11EffectRasterizerVariable undotartrasterizerstate-Methode (D3dx11effect. h)
description: Stellt einen zuvor festgelegten Raster-Zustand wieder her.
ms.assetid: 2801479c-cb70-4950-9888-73e271b669aa
keywords:
- Undotartrasterizerstate-Methode Direct3D 11
- Undotartrasterizerstate-Methode Direct3D 11, ID3DX11EffectRasterizerVariable-Schnittstelle
- ID3DX11EffectRasterizerVariable-Schnittstelle Direct3D 11, undotartrasterizerstate-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.UndoSetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed05aa7380a1fb08bbd12d36328d33fa64fb7500
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219715"
---
# <a name="id3dx11effectrasterizervariableundosetrasterizerstate-method"></a><span data-ttu-id="d6a4b-106">ID3DX11EffectRasterizerVariable:: undotartrasterizerstate-Methode</span><span class="sxs-lookup"><span data-stu-id="d6a4b-106">ID3DX11EffectRasterizerVariable::UndoSetRasterizerState method</span></span>

<span data-ttu-id="d6a4b-107">Stellt einen zuvor festgelegten Raster-Zustand wieder her.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-107">Reverts a previously set rasterizer state.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a4b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6a4b-108">Syntax</span></span>


```C++
HRESULT UndoSetRasterizerState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="d6a4b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6a4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6a4b-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="d6a4b-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="d6a4b-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6a4b-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d6a4b-112">Index in ein Array von Raster-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="d6a4b-113">Wenn nur eine Raster-Schnittstelle vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6a4b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6a4b-114">Return value</span></span>

<span data-ttu-id="d6a4b-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d6a4b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d6a4b-116">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d6a4b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6a4b-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d6a4b-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d6a4b-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d6a4b-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d6a4b-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d6a4b-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d6a4b-121">Requirements</span></span>



| <span data-ttu-id="d6a4b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6a4b-122">Requirement</span></span> | <span data-ttu-id="d6a4b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d6a4b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a4b-124">Header</span><span class="sxs-lookup"><span data-stu-id="d6a4b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d6a4b-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6a4b-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d6a4b-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d6a4b-126">Library</span></span><br/> | <dl> <span data-ttu-id="d6a4b-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="d6a4b-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6a4b-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d6a4b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a4b-129">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="d6a4b-129">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

