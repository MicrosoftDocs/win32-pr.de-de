---
description: Legt die von rechts ausgebene World-View-Transformation für ein Sprite fest. Ein Aufrufe dieser Methode ist vor dem abgleichen oder Sortieren von Sprites erforderlich.
ms.assetid: 83654e9a-8991-49ec-ab28-cf9063126dbe
title: 'ID3DXSprite:: SetWorldViewRH-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewRH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7521f60f819829fc72ba907b57d4e4eb13682a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353739"
---
# <a name="id3dxspritesetworldviewrh-method"></a><span data-ttu-id="008cb-104">ID3DXSprite:: SetWorldViewRH-Methode</span><span class="sxs-lookup"><span data-stu-id="008cb-104">ID3DXSprite::SetWorldViewRH method</span></span>

<span data-ttu-id="008cb-105">Legt die von rechts ausgebene World-View-Transformation für ein Sprite fest.</span><span class="sxs-lookup"><span data-stu-id="008cb-105">Sets the right-handed world-view transform for a sprite.</span></span> <span data-ttu-id="008cb-106">Ein Aufrufe dieser Methode ist vor dem abgleichen oder Sortieren von Sprites erforderlich.</span><span class="sxs-lookup"><span data-stu-id="008cb-106">A call to this method is required before billboarding or sorting sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="008cb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="008cb-107">Syntax</span></span>


```C++
HRESULT SetWorldViewRH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a><span data-ttu-id="008cb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="008cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="008cb-109">*pworld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="008cb-109">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="008cb-110">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="008cb-110">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="008cb-111">Zeiger auf ein [**D3DXMATRIX**](d3dxmatrix.md) -Wert, der eine Welt Transformation enthält.</span><span class="sxs-lookup"><span data-stu-id="008cb-111">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a world transform.</span></span> <span data-ttu-id="008cb-112">Wenn der Wert **null** ist, wird die Identitätsmatrix für die weltweite Transformation verwendet.</span><span class="sxs-lookup"><span data-stu-id="008cb-112">If **NULL**, the identity matrix is used for the world transform.</span></span>

</dd> <dt>

<span data-ttu-id="008cb-113">*PView* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="008cb-113">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="008cb-114">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="008cb-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="008cb-115">Zeiger auf ein [**D3DXMATRIX**](d3dxmatrix.md) -Wert, der eine Ansichts Transformation enthält.</span><span class="sxs-lookup"><span data-stu-id="008cb-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a view transform.</span></span> <span data-ttu-id="008cb-116">Wenn der Wert **null** ist, wird die Identitätsmatrix für die Ansichts Transformation verwendet.</span><span class="sxs-lookup"><span data-stu-id="008cb-116">If **NULL**, the identity matrix is used for the view transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="008cb-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="008cb-117">Return value</span></span>

<span data-ttu-id="008cb-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="008cb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="008cb-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="008cb-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="008cb-120">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="008cb-120">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="008cb-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="008cb-121">Remarks</span></span>

<span data-ttu-id="008cb-122">Ein Aufrufen dieser Methode (oder an [**ID3DXSprite:: SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) ist erforderlich, wenn das Sprite mit dem Flag [D3DXSprite \_ \_ Billboard](d3dxsprite.md), D3DXSprite \_ \_ Sort \_ Tiefe \_ frontbackback oder D3DXSprite \_ \_ Sort \_ Tiefe \_ backto Front Flag in [**ID3DXSprite:: begin**](id3dxsprite--begin.md)gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="008cb-122">A call to this method (or to [**ID3DXSprite::SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) is required if the sprite will be rendered with the [D3DXSprite\_\_BILLBOARD](d3dxsprite.md), D3DXSprite\_\_SORT\_DEPTH\_FRONTTOBACK, or D3DXSprite\_\_SORT\_DEPTH\_BACKTOFRONT flag value in [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="008cb-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="008cb-123">Requirements</span></span>



| <span data-ttu-id="008cb-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="008cb-124">Requirement</span></span> | <span data-ttu-id="008cb-125">Wert</span><span class="sxs-lookup"><span data-stu-id="008cb-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="008cb-126">Header</span><span class="sxs-lookup"><span data-stu-id="008cb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="008cb-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="008cb-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="008cb-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="008cb-128">Library</span></span><br/> | <dl> <span data-ttu-id="008cb-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="008cb-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="008cb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="008cb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="008cb-131">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="008cb-131">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




