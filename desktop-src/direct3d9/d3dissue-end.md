---
description: Dieses Makro erstellt einen Wert, der von Issue verwendet wird, um ein Abfrage Ende auszugeben.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355086"
---
# <a name="d3dissue_end"></a><span data-ttu-id="41612-103">D3DISSUE \_ Ende</span><span class="sxs-lookup"><span data-stu-id="41612-103">D3DISSUE\_END</span></span>

<span data-ttu-id="41612-104">Dieses Makro erstellt einen Wert, der von [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) verwendet wird, um ein Abfrage Ende auszugeben.</span><span class="sxs-lookup"><span data-stu-id="41612-104">This macro creates a value used by [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) to issue a query end.</span></span>

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a><span data-ttu-id="41612-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="41612-105">Parameters</span></span>





 

## <a name="remarks"></a><span data-ttu-id="41612-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41612-106">Remarks</span></span>

<span data-ttu-id="41612-107">Dieses Makro ändert den Abfrage Status in "nicht signalisiert".</span><span class="sxs-lookup"><span data-stu-id="41612-107">This macro changes the query state to nonsignaled.</span></span>

<span data-ttu-id="41612-108">D3DISSUE \_ End ist für die folgenden Abfrage Typen gültig.</span><span class="sxs-lookup"><span data-stu-id="41612-108">D3DISSUE\_END is valid for the following query types.</span></span>

-   <span data-ttu-id="41612-109">D3DQUERYTYPE \_ VCACHE</span><span class="sxs-lookup"><span data-stu-id="41612-109">D3DQUERYTYPE\_VCACHE</span></span>
-   <span data-ttu-id="41612-110">D3DQUERYTYPE \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="41612-110">D3DQUERYTYPE\_ResourceManager</span></span>
-   <span data-ttu-id="41612-111">D3DQUERYTYPE \_ vertexstats</span><span class="sxs-lookup"><span data-stu-id="41612-111">D3DQUERYTYPE\_VERTEXSTATS</span></span>
-   <span data-ttu-id="41612-112">D3DQUERYTYPE- \_ Ereignis</span><span class="sxs-lookup"><span data-stu-id="41612-112">D3DQUERYTYPE\_EVENT</span></span>
-   <span data-ttu-id="41612-113">D3DQUERYTYPE- \_ oksion</span><span class="sxs-lookup"><span data-stu-id="41612-113">D3DQUERYTYPE\_OCCLUSION</span></span>

## <a name="requirements"></a><span data-ttu-id="41612-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41612-114">Requirements</span></span>



| <span data-ttu-id="41612-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41612-115">Requirement</span></span> | <span data-ttu-id="41612-116">Wert</span><span class="sxs-lookup"><span data-stu-id="41612-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41612-117">Header</span><span class="sxs-lookup"><span data-stu-id="41612-117">Header</span></span><br/> | <dl> <span data-ttu-id="41612-118"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="41612-118"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41612-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41612-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41612-120">Makros</span><span class="sxs-lookup"><span data-stu-id="41612-120">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="41612-121">**D3DISSUE \_ Begin**</span><span class="sxs-lookup"><span data-stu-id="41612-121">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md)
</dt> <dt>

[<span data-ttu-id="41612-122">**D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="41612-122">**D3DQUERYTYPE**</span></span>](./d3dquerytype.md)
</dt> </dl>

 

 
