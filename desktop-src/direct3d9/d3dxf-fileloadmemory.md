---
description: Identifiziert Arbeitsspeicher Daten.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: D3DXF_FILELOADMEMORY-Struktur (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961604"
---
# <a name="d3dxf_fileloadmemory-structure"></a><span data-ttu-id="987a5-103">D3DXF \_ fileloadmemory-Struktur</span><span class="sxs-lookup"><span data-stu-id="987a5-103">D3DXF\_FILELOADMEMORY structure</span></span>

<span data-ttu-id="987a5-104">Identifiziert Arbeitsspeicher Daten.</span><span class="sxs-lookup"><span data-stu-id="987a5-104">Identifies memory data.</span></span>

## <a name="syntax"></a><span data-ttu-id="987a5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="987a5-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="987a5-106">Member</span><span class="sxs-lookup"><span data-stu-id="987a5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="987a5-107">**lpmemory**</span><span class="sxs-lookup"><span data-stu-id="987a5-107">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="987a5-108">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="987a5-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="987a5-109">Zeiger auf einen Speicherblock, der geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="987a5-109">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="987a5-110">**dsize**</span><span class="sxs-lookup"><span data-stu-id="987a5-110">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="987a5-111">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="987a5-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="987a5-112">Größe des zu ladenden Speicherblocks in Bytes.</span><span class="sxs-lookup"><span data-stu-id="987a5-112">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="987a5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="987a5-113">Remarks</span></span>

<span data-ttu-id="987a5-114">Diese Struktur identifiziert Daten, die aus dem Arbeitsspeicher geladen werden sollen, wenn eine Anwendung die Methode " [**kreateenumuject**](id3dxfile--createenumobject.md) " verwendet und das Flag "D3DXF \_ fileload \_ frommemory" angibt.</span><span class="sxs-lookup"><span data-stu-id="987a5-114">This structure identifies data to be loaded from memory when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the D3DXF\_FILELOAD\_FROMMEMORY flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="987a5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="987a5-115">Requirements</span></span>



| <span data-ttu-id="987a5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="987a5-116">Requirement</span></span> | <span data-ttu-id="987a5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="987a5-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="987a5-118">Header</span><span class="sxs-lookup"><span data-stu-id="987a5-118">Header</span></span><br/> | <dl> <span data-ttu-id="987a5-119"><dt>D3dx9xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="987a5-119"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="987a5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="987a5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="987a5-121">D3DX X-Dateistrukturen</span><span class="sxs-lookup"><span data-stu-id="987a5-121">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
