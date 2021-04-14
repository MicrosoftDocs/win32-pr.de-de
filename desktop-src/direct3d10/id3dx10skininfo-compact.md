---
description: Begrenzen Sie die Anzahl der Knochen, die einen Scheitelpunkt beeinflussen können, und/oder schränken Sie die Menge der Auswirkungen ein, die ein Knochen auf einen Scheitelpunkt aufweisen kann.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'ID3DX10SkinInfo:: Compact-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 379343688a1fd2ffe5ebd968dc984fa09faada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394090"
---
# <a name="id3dx10skininfocompact-method"></a><span data-ttu-id="bb0a0-103">ID3DX10SkinInfo:: Compact-Methode</span><span class="sxs-lookup"><span data-stu-id="bb0a0-103">ID3DX10SkinInfo::Compact method</span></span>

<span data-ttu-id="bb0a0-104">Begrenzen Sie die Anzahl der Knochen, die einen Scheitelpunkt beeinflussen können, und/oder schränken Sie die Menge der Auswirkungen ein, die ein Knochen auf einen Scheitelpunkt aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="bb0a0-104">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb0a0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb0a0-105">Syntax</span></span>


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a><span data-ttu-id="bb0a0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb0a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb0a0-107">*Maxpervertexeinflüsse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb0a0-107">*MaxPerVertexInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb0a0-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb0a0-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb0a0-109">Die maximale Anzahl von Knochen, die einen bestimmten Scheitelpunkt beeinflussen können.</span><span class="sxs-lookup"><span data-stu-id="bb0a0-109">The maximum number of bones that can influence any given vertex.</span></span> <span data-ttu-id="bb0a0-110">Dieser Wert wird ignoriert, wenn er größer ist als der Wert, der von [**ID3DX10SkinInfo:: getmaxbonein fluences**](id3dx10skininfo-getmaxboneinfluences.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="bb0a0-110">This value is ignored if it is greater than the value returned by [**ID3DX10SkinInfo::GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb0a0-111">*Skalemode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb0a0-111">*ScaleMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb0a0-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb0a0-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb0a0-113">Ein Flag, das beschreibt, wie die verbleibenden Gewichtungen auf einem bestimmten Scheitelpunkt skaliert werden, nachdem einige von minweight abgeschnitten wurden.</span><span class="sxs-lookup"><span data-stu-id="bb0a0-113">A flag describing how to scale the remaining weights on a given vertex after some have been chopped off by MinWeight.</span></span> <span data-ttu-id="bb0a0-114">Wenn d3dx10 \_ skininfo \_ keine \_ Skalierung angegeben ist, werden die Gewichtungen überhaupt nicht skaliert.</span><span class="sxs-lookup"><span data-stu-id="bb0a0-114">If D3DX10\_SKININFO\_NO\_SCALING is specified, the weights will not be scaled at all.</span></span> <span data-ttu-id="bb0a0-115">Wenn d3dx10 \_ skininfo \_ \_ auf \_ 1 festgelegt ist, werden die Gewichtungen größer als minweight zentral hochskaliert, sodass Sie bis zu 1,0 addieren.</span><span class="sxs-lookup"><span data-stu-id="bb0a0-115">If D3DX10\_SKININFO\_SCALE\_TO\_1 is specified, the weights greater than MinWeight will be scaled up so that they add up to 1.0.</span></span> <span data-ttu-id="bb0a0-116">Wenn d3dx10 \_ skininfo \_ Scale \_ to \_ Total angegeben wird, werden die Gewichtungen größer als minweight zentral hochskaliert, sodass Sie den ursprünglichen Gesamtwert hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bb0a0-116">If D3DX10\_SKININFO\_SCALE\_TO\_TOTAL is specified, the weights greater than MinWeight will be scaled up so that they add up to the original total.</span></span>

</dd> <dt>

<span data-ttu-id="bb0a0-117">*Minweight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb0a0-117">*MinWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb0a0-118">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bb0a0-118">Type: **float**</span></span>

<span data-ttu-id="bb0a0-119">Der minimale Prozentsatz der Auswirkung (oder Gewichtung), den alle Knochen für einen beliebigen Scheitelpunkt aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="bb0a0-119">The minimum percentage of influence, or weight, that any bone can have on any vertex.</span></span> <span data-ttu-id="bb0a0-120">Dieser Wert muss zwischen 0 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="bb0a0-120">This value must be between 0 and 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb0a0-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb0a0-121">Return value</span></span>

<span data-ttu-id="bb0a0-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb0a0-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb0a0-123">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bb0a0-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bb0a0-124">Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: e \_ outo-Memory oder e \_ invalidArg.</span><span class="sxs-lookup"><span data-stu-id="bb0a0-124">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb0a0-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb0a0-125">Requirements</span></span>



| <span data-ttu-id="bb0a0-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb0a0-126">Requirement</span></span> | <span data-ttu-id="bb0a0-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bb0a0-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb0a0-128">Header</span><span class="sxs-lookup"><span data-stu-id="bb0a0-128">Header</span></span><br/>  | <dl> <span data-ttu-id="bb0a0-129"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb0a0-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb0a0-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb0a0-130">Library</span></span><br/> | <dl> <span data-ttu-id="bb0a0-131"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb0a0-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb0a0-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb0a0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb0a0-133">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="bb0a0-133">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="bb0a0-134">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="bb0a0-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
