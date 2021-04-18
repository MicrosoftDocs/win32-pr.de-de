---
description: Identifiziert Arbeitsspeicher Daten. Veraltet.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: Dxfileloadmemory-Struktur (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 02424abd354811a6522b58dd0011ecdddce24564
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355032"
---
# <a name="dxfileloadmemory-structure"></a><span data-ttu-id="0d7b8-104">Dxfileloadmemory-Struktur</span><span class="sxs-lookup"><span data-stu-id="0d7b8-104">DXFILELOADMEMORY structure</span></span>

<span data-ttu-id="0d7b8-105">Identifiziert Arbeitsspeicher Daten.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-105">Identifies memory data.</span></span> <span data-ttu-id="0d7b8-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d7b8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d7b8-107">Syntax</span></span>


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="0d7b8-108">Member</span><span class="sxs-lookup"><span data-stu-id="0d7b8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0d7b8-109">**lpmemory**</span><span class="sxs-lookup"><span data-stu-id="0d7b8-109">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="0d7b8-110">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d7b8-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0d7b8-111">Zeiger auf einen Speicherblock, der geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-111">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="0d7b8-112">**dsize**</span><span class="sxs-lookup"><span data-stu-id="0d7b8-112">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="0d7b8-113">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d7b8-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0d7b8-114">Größe des zu ladenden Speicherblocks in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-114">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d7b8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d7b8-115">Remarks</span></span>

<span data-ttu-id="0d7b8-116">Diese Struktur identifiziert eine Ressource, die geladen werden soll, wenn eine Anwendung die Methode " [**kreateenumubject**](idirectxfile--createenumobject.md) " verwendet und dxfileload \_ frommemory angibt.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-116">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d7b8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d7b8-117">Requirements</span></span>



| <span data-ttu-id="0d7b8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d7b8-118">Requirement</span></span> | <span data-ttu-id="0d7b8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0d7b8-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0d7b8-120">Header</span><span class="sxs-lookup"><span data-stu-id="0d7b8-120">Header</span></span><br/> | <dl> <span data-ttu-id="0d7b8-121"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d7b8-121"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d7b8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d7b8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d7b8-123">X-Dateistrukturen</span><span class="sxs-lookup"><span data-stu-id="0d7b8-123">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="0d7b8-124">**"Kreateendumuject"**</span><span class="sxs-lookup"><span data-stu-id="0d7b8-124">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="0d7b8-125">Dxfile-Konstanten</span><span class="sxs-lookup"><span data-stu-id="0d7b8-125">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
