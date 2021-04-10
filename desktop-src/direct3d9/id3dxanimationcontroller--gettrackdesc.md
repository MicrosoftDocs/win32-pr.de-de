---
description: Ruft die Titel Beschreibung ab.
ms.assetid: 7663a26f-5ad3-4a17-a502-c0dcfa730db2
title: 'ID3DXAnimationController:: gettrackdesc-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 940b43ede480766155d09ebe51dfb55eba114c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762156"
---
# <a name="id3dxanimationcontrollergettrackdesc-method"></a><span data-ttu-id="96657-103">ID3DXAnimationController:: gettrackdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="96657-103">ID3DXAnimationController::GetTrackDesc method</span></span>

<span data-ttu-id="96657-104">Ruft die Titel Beschreibung ab.</span><span class="sxs-lookup"><span data-stu-id="96657-104">Gets the track description.</span></span>

## <a name="syntax"></a><span data-ttu-id="96657-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96657-105">Syntax</span></span>


```C++
HRESULT GetTrackDesc(
  [in]  UINT             Track,
  [out] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="96657-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96657-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96657-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96657-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96657-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96657-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96657-109">Bezeichner nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="96657-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="96657-110">*PDE SC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="96657-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96657-111">Typ: **[ **LPD3DXTRACK \_ DESC**](d3dxtrack-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="96657-111">Type: **[**LPD3DXTRACK\_DESC**](d3dxtrack-desc.md)**</span></span>

<span data-ttu-id="96657-112">Zeiger auf die Titel Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="96657-112">Pointer to the track description.</span></span> <span data-ttu-id="96657-113">Weitere Informationen finden Sie unter [**D3DXTRACK \_**](d3dxtrack-desc.md).</span><span class="sxs-lookup"><span data-stu-id="96657-113">See [**D3DXTRACK\_DESC**](d3dxtrack-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96657-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96657-114">Return value</span></span>

<span data-ttu-id="96657-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96657-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96657-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="96657-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="96657-117">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="96657-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="96657-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96657-118">Requirements</span></span>



| <span data-ttu-id="96657-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96657-119">Requirement</span></span> | <span data-ttu-id="96657-120">Wert</span><span class="sxs-lookup"><span data-stu-id="96657-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96657-121">Header</span><span class="sxs-lookup"><span data-stu-id="96657-121">Header</span></span><br/>  | <dl> <span data-ttu-id="96657-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="96657-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="96657-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="96657-123">Library</span></span><br/> | <dl> <span data-ttu-id="96657-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96657-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96657-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96657-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96657-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="96657-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
