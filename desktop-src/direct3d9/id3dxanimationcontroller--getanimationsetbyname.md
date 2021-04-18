---
description: Ruft einen Animations Satz mit dem angegebenen Namen ab.
ms.assetid: 4c3f3002-45f6-49b2-8a42-18d5824fb36f
title: 'ID3DXAnimationController:: getanimationsetbyname-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSetByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d520625e457a50fe962ae74d6e25fc17e2beb729
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354396"
---
# <a name="id3dxanimationcontrollergetanimationsetbyname-method"></a><span data-ttu-id="dffc5-103">ID3DXAnimationController:: getanimationsetbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="dffc5-103">ID3DXAnimationController::GetAnimationSetByName method</span></span>

<span data-ttu-id="dffc5-104">Ruft einen Animations Satz mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="dffc5-104">Gets an animation set, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="dffc5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dffc5-105">Syntax</span></span>


```C++
HRESULT GetAnimationSetByName(
  [in]  LPCSTR             pName,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="dffc5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dffc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dffc5-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dffc5-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dffc5-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dffc5-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dffc5-109">Zeichenfolge, die den Namen des Animations Satzes enthält.</span><span class="sxs-lookup"><span data-stu-id="dffc5-109">String containing the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="dffc5-110">*ppanimset* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dffc5-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dffc5-111">Typ: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="dffc5-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="dffc5-112">Zeiger auf den [**ID3DXAnimationSet**](id3dxanimationset.md) -Animations Satz.</span><span class="sxs-lookup"><span data-stu-id="dffc5-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dffc5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dffc5-113">Return value</span></span>

<span data-ttu-id="dffc5-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dffc5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dffc5-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dffc5-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dffc5-116">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="dffc5-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="dffc5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dffc5-117">Remarks</span></span>

<span data-ttu-id="dffc5-118">Der Animations Controller enthält ein Array von Animations Sätzen.</span><span class="sxs-lookup"><span data-stu-id="dffc5-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="dffc5-119">Diese Methode gibt einen Animations Satz mit dem angegebenen Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="dffc5-119">This method returns an animation set that has the given name.</span></span>

## <a name="requirements"></a><span data-ttu-id="dffc5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dffc5-120">Requirements</span></span>



| <span data-ttu-id="dffc5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dffc5-121">Requirement</span></span> | <span data-ttu-id="dffc5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="dffc5-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dffc5-123">Header</span><span class="sxs-lookup"><span data-stu-id="dffc5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="dffc5-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="dffc5-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="dffc5-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dffc5-125">Library</span></span><br/> | <dl> <span data-ttu-id="dffc5-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dffc5-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dffc5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dffc5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dffc5-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="dffc5-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
