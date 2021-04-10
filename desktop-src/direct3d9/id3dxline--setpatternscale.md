---
description: Dehnt das Stippel Muster entlang der Zeilen Richtung aus.
ms.assetid: 411464db-d721-4252-bff3-bec57252273e
title: 'ID3DXLine:: setpatternscale-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44c040a2e8899784bcea9b93bf0781afb39c2464
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219711"
---
# <a name="id3dxlinesetpatternscale-method"></a><span data-ttu-id="6c00d-103">ID3DXLine:: setpatternscale-Methode</span><span class="sxs-lookup"><span data-stu-id="6c00d-103">ID3DXLine::SetPatternScale method</span></span>

<span data-ttu-id="6c00d-104">Dehnt das Stippel Muster entlang der Zeilen Richtung aus.</span><span class="sxs-lookup"><span data-stu-id="6c00d-104">Stretches the stipple pattern along the line direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c00d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c00d-105">Syntax</span></span>


```C++
HRESULT SetPatternScale(
  [in] FLOAT fPatternScale
);
```



## <a name="parameters"></a><span data-ttu-id="6c00d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c00d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c00d-107">" *bpatternscale* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="6c00d-107">*fPatternScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c00d-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c00d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c00d-109">Skalierungs Wert von Stippel Mustern.</span><span class="sxs-lookup"><span data-stu-id="6c00d-109">Stipple pattern scaling value.</span></span> <span data-ttu-id="6c00d-110">1.0 f ist der Standardwert und stellt keine Skalierung dar.</span><span class="sxs-lookup"><span data-stu-id="6c00d-110">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="6c00d-111">Ein Wert kleiner als 1,0 f verkleinert das Muster, und ein Wert größer als 1,0 dehnt das Muster aus.</span><span class="sxs-lookup"><span data-stu-id="6c00d-111">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c00d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c00d-112">Return value</span></span>

<span data-ttu-id="6c00d-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c00d-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c00d-114">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6c00d-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6c00d-115">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="6c00d-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c00d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c00d-116">Requirements</span></span>



| <span data-ttu-id="6c00d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c00d-117">Requirement</span></span> | <span data-ttu-id="6c00d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6c00d-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c00d-119">Header</span><span class="sxs-lookup"><span data-stu-id="6c00d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6c00d-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c00d-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="6c00d-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c00d-121">Library</span></span><br/> | <dl> <span data-ttu-id="6c00d-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c00d-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c00d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c00d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c00d-124">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="6c00d-124">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
