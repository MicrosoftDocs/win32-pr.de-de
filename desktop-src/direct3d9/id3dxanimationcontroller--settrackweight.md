---
description: Legt die Last des Titels fest. Die Gewichtung wird verwendet, um zu bestimmen, wie mehrere Titel miteinander verknüpft werden.
ms.assetid: a00ceae4-47b4-4fb9-a028-97493e3dc071
title: 'ID3DXAnimationController:: settrackweight-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc42d283231a0e49359531827cc785bd83aefc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762363"
---
# <a name="id3dxanimationcontrollersettrackweight-method"></a><span data-ttu-id="c2807-104">ID3DXAnimationController:: settrackweight-Methode</span><span class="sxs-lookup"><span data-stu-id="c2807-104">ID3DXAnimationController::SetTrackWeight method</span></span>

<span data-ttu-id="c2807-105">Legt die Last des Titels fest.</span><span class="sxs-lookup"><span data-stu-id="c2807-105">Sets the track weight.</span></span> <span data-ttu-id="c2807-106">Die Gewichtung wird verwendet, um zu bestimmen, wie mehrere Titel miteinander verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="c2807-106">The weight is used to determine how to blend multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2807-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2807-107">Syntax</span></span>


```C++
HRESULT SetTrackWeight(
  [in] UINT  Track,
  [in] FLOAT Weight
);
```



## <a name="parameters"></a><span data-ttu-id="c2807-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2807-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2807-109">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2807-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2807-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2807-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2807-111">Der Bezeichner des Titels, für den die Gewichtung festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2807-111">Identifier of the track to set the weight on.</span></span>

</dd> <dt>

<span data-ttu-id="c2807-112">*Gewichtung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2807-112">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2807-113">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2807-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2807-114">Gewichtungswert.</span><span class="sxs-lookup"><span data-stu-id="c2807-114">Weight value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2807-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2807-115">Return value</span></span>

<span data-ttu-id="c2807-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c2807-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c2807-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c2807-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c2807-118">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="c2807-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2807-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2807-119">Requirements</span></span>



| <span data-ttu-id="c2807-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2807-120">Requirement</span></span> | <span data-ttu-id="c2807-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c2807-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2807-122">Header</span><span class="sxs-lookup"><span data-stu-id="c2807-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c2807-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2807-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c2807-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2807-124">Library</span></span><br/> | <dl> <span data-ttu-id="c2807-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2807-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c2807-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2807-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2807-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="c2807-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
