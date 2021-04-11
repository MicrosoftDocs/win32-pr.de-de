---
description: Legt die linke Seite "World-View Transform" für ein Sprite fest. Ein Aufrufe dieser Methode ist vor dem abgleichen oder Sortieren von Sprites erforderlich.
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: 'ID3DXSprite:: SetWorldViewLH-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewLH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 397c3803f6d4e445f74a8b24a61e86e72e471648
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219576"
---
# <a name="id3dxspritesetworldviewlh-method"></a><span data-ttu-id="18603-104">ID3DXSprite:: SetWorldViewLH-Methode</span><span class="sxs-lookup"><span data-stu-id="18603-104">ID3DXSprite::SetWorldViewLH method</span></span>

<span data-ttu-id="18603-105">Legt die linke Seite "World-View Transform" für ein Sprite fest.</span><span class="sxs-lookup"><span data-stu-id="18603-105">Sets the left-handed world-view transform for a sprite.</span></span> <span data-ttu-id="18603-106">Ein Aufrufe dieser Methode ist vor dem abgleichen oder Sortieren von Sprites erforderlich.</span><span class="sxs-lookup"><span data-stu-id="18603-106">A call to this method is required before billboarding or sorting sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="18603-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="18603-107">Syntax</span></span>


```C++
HRESULT SetWorldViewLH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a><span data-ttu-id="18603-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="18603-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18603-109">*pworld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18603-109">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18603-110">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="18603-110">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="18603-111">Zeiger auf ein [**D3DXMATRIX**](d3dxmatrix.md) -Wert, der eine Welt Transformation enthält.</span><span class="sxs-lookup"><span data-stu-id="18603-111">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a world transform.</span></span> <span data-ttu-id="18603-112">Wenn der Wert **null** ist, wird die Identitätsmatrix für die weltweite Transformation verwendet.</span><span class="sxs-lookup"><span data-stu-id="18603-112">If **NULL**, the identity matrix is used for the world transform.</span></span>

</dd> <dt>

<span data-ttu-id="18603-113">*PView* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18603-113">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18603-114">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="18603-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="18603-115">Zeiger auf ein [**D3DXMATRIX**](d3dxmatrix.md) -Wert, der eine Ansichts Transformation enthält.</span><span class="sxs-lookup"><span data-stu-id="18603-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a view transform.</span></span> <span data-ttu-id="18603-116">Wenn der Wert **null** ist, wird die Identitätsmatrix für die Ansichts Transformation verwendet.</span><span class="sxs-lookup"><span data-stu-id="18603-116">If **NULL**, the identity matrix is used for the view transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18603-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18603-117">Return value</span></span>

<span data-ttu-id="18603-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="18603-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="18603-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="18603-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="18603-120">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="18603-120">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="18603-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18603-121">Remarks</span></span>

<span data-ttu-id="18603-122">Ein Aufrufen dieser Methode (oder an [**ID3DXSprite:: SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) ist erforderlich, wenn das Sprite mit dem [D3DXSprite \_ \_ Billboard](d3dxsprite.md), D3DXSprite \_ \_ Sort \_ Tiefe \_ frontbackback oder D3DXSprite \_ \_ Sort \_ Tiefe \_ backbackfront-Flagwert in [**ID3DXSprite:: begin**](id3dxsprite--begin.md)gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="18603-122">A call to this method (or to [**ID3DXSprite::SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) is required if the sprite will be rendered with the [D3DXSprite\_\_BILLBOARD](d3dxsprite.md), D3DXSprite\_\_SORT\_DEPTH\_FRONTTOBACK, or D3DXSprite\_\_SORT\_DEPTH\_BACKTOFRONT flag value in [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18603-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18603-123">Requirements</span></span>



| <span data-ttu-id="18603-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18603-124">Requirement</span></span> | <span data-ttu-id="18603-125">Wert</span><span class="sxs-lookup"><span data-stu-id="18603-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18603-126">Header</span><span class="sxs-lookup"><span data-stu-id="18603-126">Header</span></span><br/>  | <dl> <span data-ttu-id="18603-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="18603-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="18603-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="18603-128">Library</span></span><br/> | <dl> <span data-ttu-id="18603-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18603-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="18603-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18603-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18603-131">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="18603-131">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




