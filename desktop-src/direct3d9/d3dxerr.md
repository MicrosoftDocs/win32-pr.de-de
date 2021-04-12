---
description: Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.
ms.assetid: 2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba
title: D3DXERR-Enumeration (D3dx9. h)
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
ms.openlocfilehash: 0d4ef0fddf70effd63a0fcdc42b46889a879c13a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219517"
---
# <a name="d3dxerr-enumeration"></a><span data-ttu-id="53e6f-103">D3DXERR-Enumeration</span><span class="sxs-lookup"><span data-stu-id="53e6f-103">D3DXERR enumeration</span></span>

<span data-ttu-id="53e6f-104">Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="53e6f-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="53e6f-105">Im folgenden finden Sie eine Liste von Werten, die von Methoden zurückgegeben werden können, die in der D3DX Utility Library enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="53e6f-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="53e6f-106">In den einzelnen Methodenbeschreibungen finden Sie Listen der Werte, die von den einzelnen Methoden zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="53e6f-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="53e6f-107">Diese Listen sind nicht notwendigerweise vollständig.</span><span class="sxs-lookup"><span data-stu-id="53e6f-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="53e6f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="53e6f-108">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="53e6f-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="53e6f-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="53e6f-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ cannotmodifyindexbuffer**</span><span class="sxs-lookup"><span data-stu-id="53e6f-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR\_CANNOTMODIFYINDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="53e6f-111">Der Index Puffer kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="53e6f-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="53e6f-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ invalidmesh**</span><span class="sxs-lookup"><span data-stu-id="53e6f-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR\_INVALIDMESH**</span></span>
</dt> <dd>

<span data-ttu-id="53e6f-113">Das Mesh ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="53e6f-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="53e6f-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ cannotattrsort**</span><span class="sxs-lookup"><span data-stu-id="53e6f-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR\_CANNOTATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="53e6f-115">Die Attribut Sortierung (D3DXMESHOPT \_ attrsort) wird nicht als Optimierungstechnik unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53e6f-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="53e6f-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR \_ skinningnotsupported**</span><span class="sxs-lookup"><span data-stu-id="53e6f-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR\_SKINNINGNOTSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="53e6f-117">Das Skinning wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53e6f-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="53e6f-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="53e6f-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR\_TOOMANYINFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="53e6f-119">Es wurden zu viele Einflüsse angegeben.</span><span class="sxs-lookup"><span data-stu-id="53e6f-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="53e6f-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR \_ InvalidData**</span><span class="sxs-lookup"><span data-stu-id="53e6f-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR\_INVALIDDATA**</span></span>
</dt> <dd>

<span data-ttu-id="53e6f-121">Die Daten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="53e6f-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="53e6f-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR \_ loadedmeshasnodata**</span><span class="sxs-lookup"><span data-stu-id="53e6f-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR\_LOADEDMESHASNODATA**</span></span>
</dt> <dd>

<span data-ttu-id="53e6f-123">Das Mesh weist keine Daten auf.</span><span class="sxs-lookup"><span data-stu-id="53e6f-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="53e6f-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR \_ duplialisienamedfragment**</span><span class="sxs-lookup"><span data-stu-id="53e6f-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR\_DUPLICATENAMEDFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="53e6f-125">Ein Fragment mit diesem Namen ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="53e6f-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="53e6f-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ cannotremuvelastitem**</span><span class="sxs-lookup"><span data-stu-id="53e6f-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR\_CANNOTREMOVELASTITEM**</span></span>
</dt> <dd>

<span data-ttu-id="53e6f-127">Das letzte Element kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="53e6f-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53e6f-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53e6f-128">Remarks</span></span>

<span data-ttu-id="53e6f-129">Der Einrichtungs Code- \_ fakdd wird zum Generieren von Fehlercodes verwendet, wie in den folgenden Makros.</span><span class="sxs-lookup"><span data-stu-id="53e6f-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="53e6f-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53e6f-130">Requirements</span></span>



| <span data-ttu-id="53e6f-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53e6f-131">Requirement</span></span> | <span data-ttu-id="53e6f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="53e6f-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53e6f-133">Header</span><span class="sxs-lookup"><span data-stu-id="53e6f-133">Header</span></span><br/> | <dl> <span data-ttu-id="53e6f-134"><dt>D3dx9. h</dt></span><span class="sxs-lookup"><span data-stu-id="53e6f-134"><dt>D3dx9.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53e6f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53e6f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e6f-136">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="53e6f-136">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




