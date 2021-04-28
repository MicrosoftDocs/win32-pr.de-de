---
description: 'D3DXERR-Enumeration: Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.'
ms.assetid: 2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba
title: D3DXERR-Enumeration (D3dx9.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXERR
api_type:
- HeaderDef
api_location:
- d3dx9.h
ms.openlocfilehash: 1c1dd03500a493b30d7c1d3bfdfdf800b65a6d82
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094304"
---
# <a name="d3dxerr-enumeration"></a><span data-ttu-id="519c7-103">D3DXERR-Enumeration</span><span class="sxs-lookup"><span data-stu-id="519c7-103">D3DXERR enumeration</span></span>

<span data-ttu-id="519c7-104">Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="519c7-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="519c7-105">Im Folgenden finden Sie eine Liste der Werte, die von Methoden zurückgegeben werden können, die in der D3DX-Hilfsprogrammbibliothek enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="519c7-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="519c7-106">Listen der Werte, die von den einzelnen Methoden zurückgegeben werden können, finden Sie in den beschreibungen der einzelnen Methoden.</span><span class="sxs-lookup"><span data-stu-id="519c7-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="519c7-107">Diese Listen sind nicht unbedingt umfassend.</span><span class="sxs-lookup"><span data-stu-id="519c7-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="519c7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="519c7-108">Syntax</span></span>


```C++
enum _D3DXERR {
  D3DXERR_CANNOTMODIFYINDEXBUFFER, 
  D3DXERR_INVALIDMESH, 
  D3DXERR_CANNOTATTRSORT, 
  D3DXERR_SKINNINGNOTSUPPORTED, 
  D3DXERR_TOOMANYINFLUENCES, 
  D3DXERR_INVALIDDATA, 
  D3DXERR_LOADEDMESHASNODATA, 
  D3DXERR_DUPLICATENAMEDFRAGMENT, 
  D3DXERR_CANNOTREMOVELASTITEM 

};
```



## <a name="constants"></a><span data-ttu-id="519c7-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="519c7-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="519c7-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ CANNOTMODIFYINDEXBUFFER**</span><span class="sxs-lookup"><span data-stu-id="519c7-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR\_CANNOTMODIFYINDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="519c7-111">Der Indexpuffer kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="519c7-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="519c7-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ INVALIDMESH**</span><span class="sxs-lookup"><span data-stu-id="519c7-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR\_INVALIDMESH**</span></span>
</dt> <dd>

<span data-ttu-id="519c7-113">Das Gitternetz ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="519c7-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="519c7-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ CANNOTATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="519c7-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR\_CANNOTATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="519c7-115">Die Attributsortierung (D3DXMESHOPT \_ ATTRSORT) wird als Optimierungstechnik nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="519c7-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="519c7-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR \_ SKINNINGNOTSUPPORTED**</span><span class="sxs-lookup"><span data-stu-id="519c7-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR\_SKINNINGNOTSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="519c7-117">Skinning wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="519c7-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="519c7-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR \_ TOOMANYINFLUENCES**</span><span class="sxs-lookup"><span data-stu-id="519c7-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR\_TOOMANYINFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="519c7-119">Es wurden zu viele Einflussfaktoren angegeben.</span><span class="sxs-lookup"><span data-stu-id="519c7-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="519c7-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR \_ INVALIDDATA**</span><span class="sxs-lookup"><span data-stu-id="519c7-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR\_INVALIDDATA**</span></span>
</dt> <dd>

<span data-ttu-id="519c7-121">Die Daten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="519c7-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="519c7-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR \_ LOADEDMESHASNODATA**</span><span class="sxs-lookup"><span data-stu-id="519c7-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR\_LOADEDMESHASNODATA**</span></span>
</dt> <dd>

<span data-ttu-id="519c7-123">Das Gitternetz verfügt über keine Daten.</span><span class="sxs-lookup"><span data-stu-id="519c7-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="519c7-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR \_ DUPLICATENAMEDFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="519c7-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR\_DUPLICATENAMEDFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="519c7-125">Ein Fragment mit diesem Namen ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="519c7-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="519c7-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ CANNOTREMOVELASTITEM**</span><span class="sxs-lookup"><span data-stu-id="519c7-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR\_CANNOTREMOVELASTITEM**</span></span>
</dt> <dd>

<span data-ttu-id="519c7-127">Das letzte Element kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="519c7-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="519c7-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="519c7-128">Remarks</span></span>

<span data-ttu-id="519c7-129">Der Einrichtungscode \_ FACDD wird zum Generieren von Fehlercodes verwendet, wie in den folgenden Makros zu sehen.</span><span class="sxs-lookup"><span data-stu-id="519c7-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="519c7-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="519c7-130">Requirements</span></span>



| <span data-ttu-id="519c7-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="519c7-131">Requirement</span></span> | <span data-ttu-id="519c7-132">Wert</span><span class="sxs-lookup"><span data-stu-id="519c7-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="519c7-133">Header</span><span class="sxs-lookup"><span data-stu-id="519c7-133">Header</span></span><br/> | <dl> <span data-ttu-id="519c7-134"><dt>D3dx9.h</dt></span><span class="sxs-lookup"><span data-stu-id="519c7-134"><dt>D3dx9.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="519c7-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="519c7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="519c7-136">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="519c7-136">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




