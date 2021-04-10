---
description: Der Member der Vertex-decl, an dem die Software angezeigt werden soll. Dies wird mit der ID3DX10SkinInfo::D osoftwareskinning-API verwendet.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: D3DX10_SKINNING_CHANNEL-Struktur (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 79f5807dc2539d770d3caa41bddf7aa4960ce682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219574"
---
# <a name="d3dx10_skinning_channel-structure"></a><span data-ttu-id="c0d9f-104">D3dx10 \_ Skinning \_ Channel-Struktur</span><span class="sxs-lookup"><span data-stu-id="c0d9f-104">D3DX10\_SKINNING\_CHANNEL structure</span></span>

<span data-ttu-id="c0d9f-105">Der Member der Vertex-decl, an dem die Software angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0d9f-105">The member of the vertex decl to do the software skinning on.</span></span> <span data-ttu-id="c0d9f-106">Dies wird mit der [**ID3DX10SkinInfo::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) -API verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0d9f-106">This is used with the [**ID3DX10SkinInfo::DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md) API.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d9f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0d9f-107">Syntax</span></span>


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a><span data-ttu-id="c0d9f-108">Member</span><span class="sxs-lookup"><span data-stu-id="c0d9f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0d9f-109">**SrcOffset**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-109">**SrcOffset**</span></span>
</dt> <dd>

<span data-ttu-id="c0d9f-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c0d9f-111">Offset vom Anfang jedes Quell Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="c0d9f-111">Offset from the beginning of each source vertex.</span></span>

</dd> <dt>

<span data-ttu-id="c0d9f-112">**Destoffset**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-112">**DestOffset**</span></span>
</dt> <dd>

<span data-ttu-id="c0d9f-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c0d9f-114">Offset vom Anfang jedes Ziel Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="c0d9f-114">Offset from the beginning of each destination vertex.</span></span>

</dd> <dt>

<span data-ttu-id="c0d9f-115">**IsNormal**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-115">**IsNormal**</span></span>
</dt> <dd>

<span data-ttu-id="c0d9f-116">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c0d9f-117">Bestimmt, welches Array von Matrizen in der [**ID3DX10SkinInfo::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) -API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0d9f-117">Determines which array of matrices to use in the [**ID3DX10SkinInfo::DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md) API.</span></span> <span data-ttu-id="c0d9f-118">Wenn dieser Wert true ist, wird *pinverpinversiot bonematrices* verwendet; andernfalls werden *pbonematrices* verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0d9f-118">If this is true, the *pInverseTransposeBoneMatrices* will be used, otherwise *pBoneMatrices* will be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0d9f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0d9f-119">Requirements</span></span>



| <span data-ttu-id="c0d9f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0d9f-120">Requirement</span></span> | <span data-ttu-id="c0d9f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c0d9f-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d9f-122">Header</span><span class="sxs-lookup"><span data-stu-id="c0d9f-122">Header</span></span><br/> | <dl> <span data-ttu-id="c0d9f-123"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0d9f-123"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0d9f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0d9f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0d9f-125">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c0d9f-125">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
