---
description: Standardparameter beeinflussen.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: D3DXEFFECTDEFAULT-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fee415cbd7d8ec28daa079dd2f224949402a813b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361866"
---
# <a name="d3dxeffectdefault-structure"></a><span data-ttu-id="28792-103">D3DXEFFECTDEFAULT-Struktur</span><span class="sxs-lookup"><span data-stu-id="28792-103">D3DXEFFECTDEFAULT structure</span></span>

<span data-ttu-id="28792-104">Standardparameter beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="28792-104">Effect default parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="28792-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28792-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a><span data-ttu-id="28792-106">Member</span><span class="sxs-lookup"><span data-stu-id="28792-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="28792-107">**pparamname**</span><span class="sxs-lookup"><span data-stu-id="28792-107">**pParamName**</span></span>
</dt> <dd>

<span data-ttu-id="28792-108">Typ: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="28792-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="28792-109">Parametername.</span><span class="sxs-lookup"><span data-stu-id="28792-109">Parameter name.</span></span>

</dd> <dt>

<span data-ttu-id="28792-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="28792-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="28792-111">Typ: **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span><span class="sxs-lookup"><span data-stu-id="28792-111">Type: **[**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="28792-112">Datentyp in pValue.</span><span class="sxs-lookup"><span data-stu-id="28792-112">Data type in pValue.</span></span> <span data-ttu-id="28792-113">Weitere Informationen finden Sie unter [ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span><span class="sxs-lookup"><span data-stu-id="28792-113">For more information, see [**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span></span>

</dd> <dt>

<span data-ttu-id="28792-114">**NumBytes**</span><span class="sxs-lookup"><span data-stu-id="28792-114">**NumBytes**</span></span>
</dt> <dd>

<span data-ttu-id="28792-115">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28792-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="28792-116">Größe (in Bytes) der Daten, auf die von pValue verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="28792-116">Size, in bytes, of the data pointed to by pValue.</span></span>

</dd> <dt>

<span data-ttu-id="28792-117">**pValue**</span><span class="sxs-lookup"><span data-stu-id="28792-117">**pValue**</span></span>
</dt> <dd>

<span data-ttu-id="28792-118">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28792-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="28792-119">Ein Zeiger auf den Speicherort, der die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="28792-119">Pointer to the memory location that contains the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28792-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28792-120">Requirements</span></span>



| <span data-ttu-id="28792-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28792-121">Requirement</span></span> | <span data-ttu-id="28792-122">Wert</span><span class="sxs-lookup"><span data-stu-id="28792-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28792-123">Header</span><span class="sxs-lookup"><span data-stu-id="28792-123">Header</span></span><br/> | <dl> <span data-ttu-id="28792-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="28792-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28792-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28792-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28792-126">Effekt Strukturen</span><span class="sxs-lookup"><span data-stu-id="28792-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
