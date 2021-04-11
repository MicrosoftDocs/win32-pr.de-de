---
description: Ruft einen Animations Satz ab.
ms.assetid: 61785f60-82c1-4ddc-b4cd-2e7f665cfe8c
title: 'ID3DXAnimationController:: getanimationset-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c21f073b74d1ab7dac09ddd8bfb3d6be543e122a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132365"
---
# <a name="id3dxanimationcontrollergetanimationset-method"></a><span data-ttu-id="ea93c-103">ID3DXAnimationController:: getanimationset-Methode</span><span class="sxs-lookup"><span data-stu-id="ea93c-103">ID3DXAnimationController::GetAnimationSet method</span></span>

<span data-ttu-id="ea93c-104">Ruft einen Animations Satz ab.</span><span class="sxs-lookup"><span data-stu-id="ea93c-104">Gets an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea93c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea93c-105">Syntax</span></span>


```C++
HRESULT GetAnimationSet(
  [in]  UINT               Index,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="ea93c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea93c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea93c-107">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea93c-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea93c-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea93c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea93c-109">Der Index des Animations Satzes.</span><span class="sxs-lookup"><span data-stu-id="ea93c-109">Index of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="ea93c-110">*ppanimset* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ea93c-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea93c-111">Typ: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea93c-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="ea93c-112">Zeiger auf den [**ID3DXAnimationSet**](id3dxanimationset.md) -Animations Satz.</span><span class="sxs-lookup"><span data-stu-id="ea93c-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea93c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea93c-113">Return value</span></span>

<span data-ttu-id="ea93c-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea93c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea93c-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea93c-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ea93c-116">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="ea93c-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea93c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea93c-117">Remarks</span></span>

<span data-ttu-id="ea93c-118">Der Animations Controller enthält ein Array von Animations Sätzen.</span><span class="sxs-lookup"><span data-stu-id="ea93c-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="ea93c-119">Diese Methode gibt eine dieser Elemente am angegebenen Index zurück.</span><span class="sxs-lookup"><span data-stu-id="ea93c-119">This method returns one of them at the given index.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea93c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea93c-120">Requirements</span></span>



| <span data-ttu-id="ea93c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea93c-121">Requirement</span></span> | <span data-ttu-id="ea93c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ea93c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea93c-123">Header</span><span class="sxs-lookup"><span data-stu-id="ea93c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ea93c-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea93c-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ea93c-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ea93c-125">Library</span></span><br/> | <dl> <span data-ttu-id="ea93c-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea93c-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ea93c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea93c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea93c-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ea93c-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
