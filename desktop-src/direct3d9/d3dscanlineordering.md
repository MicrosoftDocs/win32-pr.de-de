---
description: Flags, die die Methode angeben, die der Raster zum Erstellen eines Bilds auf einer Oberfläche verwendet.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: D3DSCANLINEORDERING-Enumeration (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2eaed36577f881266c12b0a927cfcdc2494f0d57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367399"
---
# <a name="d3dscanlineordering-enumeration"></a><span data-ttu-id="35453-103">D3DSCANLINEORDERING-Enumeration</span><span class="sxs-lookup"><span data-stu-id="35453-103">D3DSCANLINEORDERING enumeration</span></span>

<span data-ttu-id="35453-104">Flags, die die Methode angeben, die der Raster zum Erstellen eines Bilds auf einer Oberfläche verwendet.</span><span class="sxs-lookup"><span data-stu-id="35453-104">Flags indicating the method the rasterizer uses to create an image on a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="35453-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35453-105">Syntax</span></span>


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a><span data-ttu-id="35453-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="35453-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="35453-107"><span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ progressiv**</span><span class="sxs-lookup"><span data-stu-id="35453-107"><span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="35453-108">Das Bild wird von der ersten Scanline bis zum letzten erstellt, ohne dass übersprungen wird.</span><span class="sxs-lookup"><span data-stu-id="35453-108">The image is created from the first scanline to the last without skipping any.</span></span>

</dd> <dt>

<span data-ttu-id="35453-109"><span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING-Zeilen Sprung \_**</span><span class="sxs-lookup"><span data-stu-id="35453-109"><span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING\_INTERLACED**</span></span>
</dt> <dd>

<span data-ttu-id="35453-110">Das Bild wird mit der Zeilen Sprung Methode erstellt, in der ungerade nummerierte Linien bei ungeraden nummerierten Durchläufen gezeichnet werden und sogar Linien bei geraden Durchläufen gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="35453-110">The image is created using the interlaced method in which odd-numbered lines are drawn on odd-numbered passes and even lines are drawn on even-numbered passes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35453-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35453-111">Remarks</span></span>

<span data-ttu-id="35453-112">Diese Enumeration wird als Member in [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) und [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="35453-112">This enumeration is used as a member in [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) and [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35453-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35453-113">Requirements</span></span>



| <span data-ttu-id="35453-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35453-114">Requirement</span></span> | <span data-ttu-id="35453-115">Wert</span><span class="sxs-lookup"><span data-stu-id="35453-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35453-116">Header</span><span class="sxs-lookup"><span data-stu-id="35453-116">Header</span></span><br/> | <dl> <span data-ttu-id="35453-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="35453-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35453-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35453-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35453-119">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="35453-119">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




