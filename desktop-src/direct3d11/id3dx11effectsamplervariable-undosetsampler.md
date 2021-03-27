---
title: ID3DX11EffectSamplerVariable undosetsampler-Methode (D3dx11effect. h)
description: Einen zuvor festgelegten samplerstatus zurücksetzen.
ms.assetid: bb837b12-d6c3-47e9-a0a1-0bfcfe0f3e4e
keywords:
- Undosetsampler-Methode Direct3D 11
- Undosetsampler-Methode Direct3D 11, ID3DX11EffectSamplerVariable-Schnittstelle
- ID3DX11EffectSamplerVariable-Schnittstelle Direct3D 11, undosetsampler-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.UndoSetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e89d72130e92a477b3824f8e5f8fc935e99bd5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355757"
---
# <a name="id3dx11effectsamplervariableundosetsampler-method"></a><span data-ttu-id="99dcd-106">ID3DX11EffectSamplerVariable:: undosetsampler-Methode</span><span class="sxs-lookup"><span data-stu-id="99dcd-106">ID3DX11EffectSamplerVariable::UndoSetSampler method</span></span>

<span data-ttu-id="99dcd-107">Einen zuvor festgelegten samplerstatus zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="99dcd-107">Revert a previously set sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="99dcd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="99dcd-108">Syntax</span></span>


```C++
HRESULT UndoSetSampler(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="99dcd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="99dcd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99dcd-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="99dcd-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="99dcd-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="99dcd-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="99dcd-112">Indizieren Sie in ein Array von samplingschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="99dcd-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="99dcd-113">Wenn nur eine samplerschnittstelle vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="99dcd-113">If there is only one sampler interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99dcd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99dcd-114">Return value</span></span>

<span data-ttu-id="99dcd-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99dcd-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99dcd-116">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="99dcd-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="99dcd-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99dcd-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="99dcd-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="99dcd-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="99dcd-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="99dcd-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="99dcd-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="99dcd-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="99dcd-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="99dcd-121">Requirements</span></span>



| <span data-ttu-id="99dcd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99dcd-122">Requirement</span></span> | <span data-ttu-id="99dcd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="99dcd-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99dcd-124">Header</span><span class="sxs-lookup"><span data-stu-id="99dcd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="99dcd-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="99dcd-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="99dcd-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="99dcd-126">Library</span></span><br/> | <dl> <span data-ttu-id="99dcd-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="99dcd-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99dcd-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="99dcd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99dcd-129">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="99dcd-129">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

