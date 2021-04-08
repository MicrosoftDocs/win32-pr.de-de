---
description: Legt Sampling-Eigenschaften fest, die vom PRT-Simulator (preberechnetes Radiance Transfer) verwendet werden.
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'ID3DXPRTEngine:: setsamplinginfo-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ab229652fe9e333519acce7d8474d3c4f0cf7ef9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762126"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a><span data-ttu-id="36ee4-103">ID3DXPRTEngine:: setsamplinginfo-Methode</span><span class="sxs-lookup"><span data-stu-id="36ee4-103">ID3DXPRTEngine::SetSamplingInfo method</span></span>

<span data-ttu-id="36ee4-104">Legt Sampling-Eigenschaften fest, die vom PRT-Simulator (preberechnetes Radiance Transfer) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36ee4-104">Sets sampling properties used by the precomputed radiance transfer (PRT) simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="36ee4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="36ee4-105">Syntax</span></span>


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a><span data-ttu-id="36ee4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="36ee4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36ee4-107">*Numrays* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36ee4-107">*NumRays* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36ee4-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36ee4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36ee4-109">Die Anzahl der Lichtstrahlen, die an jedem Beispiel weitergeleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="36ee4-109">Number of light rays to direct at each sample.</span></span> <span data-ttu-id="36ee4-110">Muss größer sein als Null.</span><span class="sxs-lookup"><span data-stu-id="36ee4-110">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="36ee4-111">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36ee4-111">*UseSphere* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36ee4-112">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36ee4-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36ee4-113">**True** gibt an, dass die Stichproben über eine vollständige Kugel berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="36ee4-113">If **TRUE**, samples will be computed over a full sphere.</span></span> <span data-ttu-id="36ee4-114">Der Wert **false** gibt an, dass die Stichproben über eine Hemisphäre berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="36ee4-114">If **FALSE**, samples will be computed over a hemisphere.</span></span>

</dd> <dt>

<span data-ttu-id="36ee4-115">*Usekosinus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36ee4-115">*UseCosine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36ee4-116">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36ee4-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36ee4-117">Wenn **true**, verwenden Sie eine Kosinus-Gewichtung von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="36ee4-117">If **TRUE**, use a cosine weighting of samples.</span></span> <span data-ttu-id="36ee4-118">Wenn sowohl usecosinus als auch usesphere den Wert **true** aufweisen, schlägt die Methode fehl, und es wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="36ee4-118">If both UseCosine and UseSphere are **TRUE**, the method will fail and an error will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="36ee4-119">*Adaptive* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36ee4-119">*Adaptive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36ee4-120">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36ee4-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36ee4-121">Muss den Wert **false** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="36ee4-121">Must be **FALSE**.</span></span> <span data-ttu-id="36ee4-122">Adaptive Stichprobenentnahme ist zurzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="36ee4-122">Adaptive sampling is currently not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="36ee4-123">*Adaptivethresh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36ee4-123">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36ee4-124">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36ee4-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36ee4-125">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="36ee4-125">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36ee4-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36ee4-126">Return value</span></span>

<span data-ttu-id="36ee4-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="36ee4-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="36ee4-128">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="36ee4-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="36ee4-129">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, e \_ notimpl, e \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="36ee4-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="36ee4-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36ee4-130">Requirements</span></span>



| <span data-ttu-id="36ee4-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36ee4-131">Requirement</span></span> | <span data-ttu-id="36ee4-132">Wert</span><span class="sxs-lookup"><span data-stu-id="36ee4-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36ee4-133">Header</span><span class="sxs-lookup"><span data-stu-id="36ee4-133">Header</span></span><br/>  | <dl> <span data-ttu-id="36ee4-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="36ee4-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="36ee4-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="36ee4-135">Library</span></span><br/> | <dl> <span data-ttu-id="36ee4-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36ee4-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="36ee4-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36ee4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36ee4-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="36ee4-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
