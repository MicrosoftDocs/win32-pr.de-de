---
description: 'D3DX10_ERR Enumeration: Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.'
ms.assetid: 4149ce6d-e87a-4003-b123-5555c6b3b086
title: D3DX10_ERR -Enumeration (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ERR
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 520abae0409dd4214106363d7ffde0cfb5c81ff1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094353"
---
# <a name="d3dx10_err-enumeration"></a><span data-ttu-id="2ba6d-103">D3DX10 \_ ERR-Enumeration</span><span class="sxs-lookup"><span data-stu-id="2ba6d-103">D3DX10\_ERR enumeration</span></span>

<span data-ttu-id="2ba6d-104">Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="2ba6d-105">Im Folgenden finden Sie eine Liste von Werten, die von Methoden zurückgegeben werden können, die in der D3DX-Hilfsprogrammbibliothek enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="2ba6d-106">Listen der Werte, die jeweils zurückgeben können, finden Sie in den Beschreibungen der einzelnen Methoden.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="2ba6d-107">Diese Listen sind nicht unbedingt umfassend.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ba6d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ba6d-108">Syntax</span></span>


```C++
typedef enum D3DX10_ERR { 
  D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX10_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX10_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX10_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX10_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX10_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX10_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX10_ERR, *LPD3DX10_ERR;
```



## <a name="constants"></a><span data-ttu-id="2ba6d-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="2ba6d-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2ba6d-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10 \_ ERR \_ KANN \_ INDEXPUFFER NICHT \_ \_ ÄNDERN**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-111">Der Indexpuffer kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10 \_ ERR \_ INVALID \_ MESH**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-113">Das Gitternetz ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10 \_ ERR \_ CANNOT \_ ATTR \_ SORT**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-115">Die Attributsortierung (D3DXMESHOPT \_ ATTRSORT) wird als Optimierungsmethode nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10 \_ ERR \_ SKINNING \_ NICHT \_ UNTERSTÜTZT**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-117">Skinning wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10 \_ ERR \_ ZU VIELE \_ \_ FAKTOREN**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-119">Es wurden zu viele Faktoren angegeben.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10 \_ ERR \_ UNGÜLTIGE \_ DATEN**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-121">Die Daten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3DX10 \_ ERR \_ LOADED \_ MESH \_ HAS \_ NO \_ DATA**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3DX10\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-123">Das Gitternetz verfügt über keine Daten.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10 \_ ERR \_ DUPLICATE \_ NAMED \_ FRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-125">Ein Fragment mit diesem Namen ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10 \_ ERR \_ KANN LETZTES ELEMENT \_ NICHT \_ \_ ENTFERNEN**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-127">Das letzte Element kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ba6d-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ba6d-128">Remarks</span></span>

<span data-ttu-id="2ba6d-129">Der Einrichtungscode \_ FACDD wird zum Generieren von Fehlercodes verwendet, wie in den folgenden Makros zu sehen.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="2ba6d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ba6d-130">Requirements</span></span>



| <span data-ttu-id="2ba6d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ba6d-131">Requirement</span></span> | <span data-ttu-id="2ba6d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2ba6d-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba6d-133">Header</span><span class="sxs-lookup"><span data-stu-id="2ba6d-133">Header</span></span><br/> | <dl> <span data-ttu-id="2ba6d-134"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="2ba6d-134"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ba6d-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2ba6d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba6d-136">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="2ba6d-136">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




