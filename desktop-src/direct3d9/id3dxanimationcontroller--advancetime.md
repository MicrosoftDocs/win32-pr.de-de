---
description: Animiert das Mesh und erhöht die globale Animations Zeit um einen angegebenen Betrag.
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: 'ID3DXAnimationController:: AdvanceTime-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 848e1f8aadd302b9194168e92b2b0abe732a2c2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364389"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a><span data-ttu-id="2913d-103">ID3DXAnimationController:: AdvanceTime-Methode</span><span class="sxs-lookup"><span data-stu-id="2913d-103">ID3DXAnimationController::AdvanceTime method</span></span>

<span data-ttu-id="2913d-104">Animiert das Mesh und erhöht die globale Animations Zeit um einen angegebenen Betrag.</span><span class="sxs-lookup"><span data-stu-id="2913d-104">Animates the mesh and advances the global animation time by a specified amount.</span></span>

## <a name="syntax"></a><span data-ttu-id="2913d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2913d-105">Syntax</span></span>


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a><span data-ttu-id="2913d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2913d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2913d-107">*Timedelta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2913d-107">*TimeDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2913d-108">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2913d-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2913d-109">Der Betrag in Sekunden, um den die globale Animations Zeit fort gestiegen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2913d-109">Amount, in seconds, by which to advance the global animation time.</span></span> <span data-ttu-id="2913d-110">Der Timedelta-Wert darf nicht negativ oder NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2913d-110">TimeDelta value must be non-negative or zero.</span></span>

</dd> <dt>

<span data-ttu-id="2913d-111">*pcallbackhandler* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2913d-111">*pCallbackHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2913d-112">Typ: **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span><span class="sxs-lookup"><span data-stu-id="2913d-112">Type: **[**LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span></span>

<span data-ttu-id="2913d-113">Zeiger auf eine benutzerdefinierte Animations-Rückruf Handler-Schnittstelle, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span><span class="sxs-lookup"><span data-stu-id="2913d-113">Pointer to a user-defined animation callback handler interface, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2913d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2913d-114">Return value</span></span>

<span data-ttu-id="2913d-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2913d-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2913d-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2913d-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2913d-117">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="2913d-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2913d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2913d-118">Requirements</span></span>



| <span data-ttu-id="2913d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2913d-119">Requirement</span></span> | <span data-ttu-id="2913d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2913d-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2913d-121">Header</span><span class="sxs-lookup"><span data-stu-id="2913d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2913d-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2913d-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2913d-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2913d-123">Library</span></span><br/> | <dl> <span data-ttu-id="2913d-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2913d-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2913d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2913d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2913d-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="2913d-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
