---
description: Legt den Track auf die angegebene lokale Animations Zeit fest.
ms.assetid: 2ce87b06-1196-415f-958c-7bd407d6c69c
title: 'ID3DXAnimationController:: settrackposition-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95c408a43df3047a52d93da0cca3d9b17053d320
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355042"
---
# <a name="id3dxanimationcontrollersettrackposition-method"></a><span data-ttu-id="cd909-103">ID3DXAnimationController:: settrackposition-Methode</span><span class="sxs-lookup"><span data-stu-id="cd909-103">ID3DXAnimationController::SetTrackPosition method</span></span>

<span data-ttu-id="cd909-104">Legt den Track auf die angegebene lokale Animations Zeit fest.</span><span class="sxs-lookup"><span data-stu-id="cd909-104">Sets the track to the specified local animation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd909-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd909-105">Syntax</span></span>


```C++
HRESULT SetTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE Position
);
```



## <a name="parameters"></a><span data-ttu-id="cd909-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd909-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd909-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd909-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd909-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd909-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd909-109">Bezeichner nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="cd909-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="cd909-110">*Position* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd909-110">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd909-111">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd909-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd909-112">Der Wert der lokalen Animations Zeit, der der Spur zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd909-112">Local animation time value to assign to the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd909-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd909-113">Return value</span></span>

<span data-ttu-id="cd909-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd909-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd909-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cd909-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cd909-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="cd909-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd909-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd909-117">Requirements</span></span>



| <span data-ttu-id="cd909-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd909-118">Requirement</span></span> | <span data-ttu-id="cd909-119">Wert</span><span class="sxs-lookup"><span data-stu-id="cd909-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd909-120">Header</span><span class="sxs-lookup"><span data-stu-id="cd909-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cd909-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd909-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="cd909-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cd909-122">Library</span></span><br/> | <dl> <span data-ttu-id="cd909-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd909-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd909-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd909-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd909-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="cd909-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
