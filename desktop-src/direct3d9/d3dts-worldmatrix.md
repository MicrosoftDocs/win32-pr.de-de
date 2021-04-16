---
description: Ordnet Indizes im Bereich von 0 bis 255 den entsprechenden Transformations Zuständen zu.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: D3DTS_WORLDMATRIX-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530875"
---
# <a name="d3dts_worldmatrix-macro"></a><span data-ttu-id="dc2a3-103">D3DTS \_ worldmatrix-Makro</span><span class="sxs-lookup"><span data-stu-id="dc2a3-103">D3DTS\_WORLDMATRIX macro</span></span>

<span data-ttu-id="dc2a3-104">Ordnet Indizes im Bereich von 0 bis 255 den entsprechenden Transformations Zuständen zu.</span><span class="sxs-lookup"><span data-stu-id="dc2a3-104">Maps indices in the range 0 through 255 to the corresponding transform states.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc2a3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc2a3-105">Syntax</span></span>


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a><span data-ttu-id="dc2a3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc2a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc2a3-107">*Index*</span><span class="sxs-lookup"><span data-stu-id="dc2a3-107">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="dc2a3-108">Ein Indexwert im Bereich von 0 bis 255.</span><span class="sxs-lookup"><span data-stu-id="dc2a3-108">An index value in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc2a3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc2a3-109">Return value</span></span>

<span data-ttu-id="dc2a3-110">Der [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) , der dem angegebenen *Index* zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dc2a3-110">The [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) that maps to the given *index*.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc2a3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc2a3-111">Remarks</span></span>

<span data-ttu-id="dc2a3-112">Transformations Zustände im Bereich von 256 bis 511 sind zum Speichern von bis zu 256 Matrizen reserviert, die mithilfe von 8-Bit-Indizes indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="dc2a3-112">Transform states in the range 256 through 511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc2a3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc2a3-113">Requirements</span></span>



| <span data-ttu-id="dc2a3-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc2a3-114">Requirement</span></span> | <span data-ttu-id="dc2a3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="dc2a3-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2a3-116">Header</span><span class="sxs-lookup"><span data-stu-id="dc2a3-116">Header</span></span><br/> | <dl> <span data-ttu-id="dc2a3-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc2a3-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc2a3-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc2a3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc2a3-119">Makros</span><span class="sxs-lookup"><span data-stu-id="dc2a3-119">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="dc2a3-120">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="dc2a3-120">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
