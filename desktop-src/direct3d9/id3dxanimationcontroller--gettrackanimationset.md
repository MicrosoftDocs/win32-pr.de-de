---
description: Ruft den Animations Satz für den angegebenen Titel ab.
ms.assetid: d40669ac-c391-4912-82d6-28c366a0f1dc
title: 'ID3DXAnimationController:: gettrackanimationset-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7ba397fb876d94aa48f635785737ab0448ecef6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961672"
---
# <a name="id3dxanimationcontrollergettrackanimationset-method"></a><span data-ttu-id="d58e1-103">ID3DXAnimationController:: gettrackanimationset-Methode</span><span class="sxs-lookup"><span data-stu-id="d58e1-103">ID3DXAnimationController::GetTrackAnimationSet method</span></span>

<span data-ttu-id="d58e1-104">Ruft den Animations Satz für den angegebenen Titel ab.</span><span class="sxs-lookup"><span data-stu-id="d58e1-104">Gets the animation set for the given track.</span></span>

## <a name="syntax"></a><span data-ttu-id="d58e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d58e1-105">Syntax</span></span>


```C++
HRESULT GetTrackAnimationSet(
  [in]  UINT               Track,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="d58e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d58e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d58e1-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d58e1-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d58e1-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d58e1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d58e1-109">Bezeichner nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="d58e1-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d58e1-110">*ppanimset* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d58e1-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d58e1-111">Typ: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="d58e1-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="d58e1-112">Zeiger auf den [**ID3DXAnimationSet**](id3dxanimationset.md) -Animations Satz für den angegebenen Titel.</span><span class="sxs-lookup"><span data-stu-id="d58e1-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set for the given track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d58e1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d58e1-113">Return value</span></span>

<span data-ttu-id="d58e1-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d58e1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d58e1-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d58e1-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d58e1-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="d58e1-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d58e1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d58e1-117">Requirements</span></span>



| <span data-ttu-id="d58e1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d58e1-118">Requirement</span></span> | <span data-ttu-id="d58e1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d58e1-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d58e1-120">Header</span><span class="sxs-lookup"><span data-stu-id="d58e1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d58e1-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d58e1-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d58e1-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d58e1-122">Library</span></span><br/> | <dl> <span data-ttu-id="d58e1-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d58e1-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d58e1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d58e1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d58e1-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="d58e1-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
