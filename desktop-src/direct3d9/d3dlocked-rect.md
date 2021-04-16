---
description: Beschreibt einen gesperrten rechteckigen Bereich.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: D3DLOCKED_RECT-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530956"
---
# <a name="d3dlocked_rect-structure"></a><span data-ttu-id="a9869-103">D3DLOCKED \_ Rect-Struktur</span><span class="sxs-lookup"><span data-stu-id="a9869-103">D3DLOCKED\_RECT structure</span></span>

<span data-ttu-id="a9869-104">Beschreibt einen gesperrten rechteckigen Bereich.</span><span class="sxs-lookup"><span data-stu-id="a9869-104">Describes a locked rectangular region.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9869-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9869-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a><span data-ttu-id="a9869-106">Member</span><span class="sxs-lookup"><span data-stu-id="a9869-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9869-107">**Neigung**</span><span class="sxs-lookup"><span data-stu-id="a9869-107">**Pitch**</span></span>
</dt> <dd>

<span data-ttu-id="a9869-108">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9869-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a9869-109">Anzahl von Bytes in einer Zeile der-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="a9869-109">Number of bytes in one row of the surface.</span></span>

</dd> <dt>

<span data-ttu-id="a9869-110">**PBITS**</span><span class="sxs-lookup"><span data-stu-id="a9869-110">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="a9869-111">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="a9869-111">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="a9869-112">Zeiger auf die gesperrten Bits.</span><span class="sxs-lookup"><span data-stu-id="a9869-112">Pointer to the locked bits.</span></span> <span data-ttu-id="a9869-113">Wenn ein [**Rect**](/previous-versions//dd162897(v=vs.85)) für den [**lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) -Befehl bereitgestellt wurde, ist PBITS entsprechend dem Anfang der Oberfläche ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="a9869-113">If a [**RECT**](/previous-versions//dd162897(v=vs.85)) was provided to the [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) call, pBits will be appropriately offset from the start of the surface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9869-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9869-114">Remarks</span></span>

<span data-ttu-id="a9869-115">Die Tonhöhe für DXTn-Formate unterscheidet sich von dem, was in DirectX 7 zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a9869-115">The pitch for DXTn formats is different from what was returned in DirectX 7.</span></span> <span data-ttu-id="a9869-116">Sie verweist jetzt auf die Anzahl der Bytes in einer Zeile von Blöcken.</span><span class="sxs-lookup"><span data-stu-id="a9869-116">It now refers to the number of bytes in a row of blocks.</span></span> <span data-ttu-id="a9869-117">Wenn Sie z. b. eine Breite von 16 haben, verfügen Sie über eine Höhe von 4 Blöcken (4 \* 8 für DXT1, 4 \* 16 für DXT2-5).</span><span class="sxs-lookup"><span data-stu-id="a9869-117">For example, if you have a width of 16, then you will have a pitch of 4 blocks (4\*8 for DXT1, 4\*16 for DXT2-5.)</span></span>

## <a name="requirements"></a><span data-ttu-id="a9869-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9869-118">Requirements</span></span>



| <span data-ttu-id="a9869-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9869-119">Requirement</span></span> | <span data-ttu-id="a9869-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a9869-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9869-121">Header</span><span class="sxs-lookup"><span data-stu-id="a9869-121">Header</span></span><br/> | <dl> <span data-ttu-id="a9869-122"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9869-122"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9869-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9869-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9869-124">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a9869-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="a9869-125">**IDirect3DCubeTexture9:: lockrect**</span><span class="sxs-lookup"><span data-stu-id="a9869-125">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="a9869-126">**IDirect3DSurface9:: lockrect**</span><span class="sxs-lookup"><span data-stu-id="a9869-126">**IDirect3DSurface9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[<span data-ttu-id="a9869-127">**IDirect3DTexture9:: lockrect**</span><span class="sxs-lookup"><span data-stu-id="a9869-127">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
