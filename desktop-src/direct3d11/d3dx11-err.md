---
title: D3DX11_ERR-Enumeration (Bibliothek d3dx11. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- D3DX11_ERR-Enumeration Direct3D 11
- LPD3DX11_ERR enumerationszeiger Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_ERR
api_location:
- D3DX11.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0607bd495bad4bdeacf66ae593670dbe3ad0d2e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996202"
---
# <a name="d3dx11_err-enumeration"></a><span data-ttu-id="447bc-106">Bibliothek d3dx11 \_ Err-Enumeration</span><span class="sxs-lookup"><span data-stu-id="447bc-106">D3DX11\_ERR enumeration</span></span>

> [!Note]  
> <span data-ttu-id="447bc-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="447bc-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="447bc-108">Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="447bc-108">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="447bc-109">Im folgenden finden Sie eine Liste von Werten, die von Methoden zurückgegeben werden können, die in der D3DX Utility Library enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="447bc-109">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="447bc-110">In den einzelnen Methodenbeschreibungen finden Sie Listen der Werte, die von den einzelnen Methoden zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="447bc-110">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="447bc-111">Diese Listen sind nicht notwendigerweise vollständig.</span><span class="sxs-lookup"><span data-stu-id="447bc-111">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="447bc-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="447bc-112">Syntax</span></span>


```C++
typedef enum D3DX11_ERR { 
  D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX11_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX11_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX11_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX11_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX11_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX11_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX11_ERR, *LPD3DX11_ERR;
```



## <a name="constants"></a><span data-ttu-id="447bc-113">Konstanten</span><span class="sxs-lookup"><span data-stu-id="447bc-113">Constants</span></span>

<dl> <dt>

<span data-ttu-id="447bc-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**Bibliothek d3dx11 \_ Err \_ kann \_ den \_ Index \_ Puffer nicht ändern**</span><span class="sxs-lookup"><span data-stu-id="447bc-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="447bc-115">Der Index Puffer kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="447bc-115">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="447bc-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**Bibliothek d3dx11 \_ Err ( \_ ungültiges \_ Mesh)**</span><span class="sxs-lookup"><span data-stu-id="447bc-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="447bc-117">Das Mesh ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="447bc-117">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="447bc-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**Bibliothek d3dx11 \_ Err \_ kann nicht in der \_ \_ Sortierreihenfolge**</span><span class="sxs-lookup"><span data-stu-id="447bc-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="447bc-119">Die Attribut Sortierung (D3DXMESHOPT \_ attrsort) wird nicht als Optimierungstechnik unterstützt.</span><span class="sxs-lookup"><span data-stu-id="447bc-119">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="447bc-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**Bibliothek d3dx11 \_ Err- \_ Skinning \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="447bc-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="447bc-121">Das Skinning wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="447bc-121">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="447bc-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**Bibliothek d3dx11 \_ Err \_ zu \_ viele \_ Einflüsse**</span><span class="sxs-lookup"><span data-stu-id="447bc-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="447bc-123">Es wurden zu viele Einflüsse angegeben.</span><span class="sxs-lookup"><span data-stu-id="447bc-123">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="447bc-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**Bibliothek d3dx11 \_ Err \_ ungültige \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="447bc-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="447bc-125">Die Daten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="447bc-125">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="447bc-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**Bibliothek d3dx11 \_ Err \_ geladenes \_ Mesh \_ hat \_ keine \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="447bc-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="447bc-127">Das Mesh weist keine Daten auf.</span><span class="sxs-lookup"><span data-stu-id="447bc-127">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="447bc-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**Bibliothek d3dx11 \_ Err- \_ doppeltes \_ benanntes \_ Fragment**</span><span class="sxs-lookup"><span data-stu-id="447bc-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="447bc-129">Ein Fragment mit diesem Namen ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="447bc-129">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="447bc-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**Bibliothek d3dx11 \_ Err \_ kann \_ das \_ Letzte \_ Element nicht entfernen.**</span><span class="sxs-lookup"><span data-stu-id="447bc-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="447bc-131">Das letzte Element kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="447bc-131">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="447bc-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="447bc-132">Remarks</span></span>

<span data-ttu-id="447bc-133">Der Einrichtungs Code- \_ fakdd wird zum Generieren von Fehlercodes verwendet, wie in den folgenden Makros.</span><span class="sxs-lookup"><span data-stu-id="447bc-133">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="447bc-134">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="447bc-134">Requirements</span></span>



| <span data-ttu-id="447bc-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="447bc-135">Requirement</span></span> | <span data-ttu-id="447bc-136">Wert</span><span class="sxs-lookup"><span data-stu-id="447bc-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="447bc-137">Header</span><span class="sxs-lookup"><span data-stu-id="447bc-137">Header</span></span><br/> | <dl> <span data-ttu-id="447bc-138"><dt>Bibliothek d3dx11. h</dt></span><span class="sxs-lookup"><span data-stu-id="447bc-138"><dt>D3DX11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="447bc-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="447bc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="447bc-140">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="447bc-140">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





