---
description: Datentyp zum Verwalten eines Satzes von Standardeffekt Parametern.
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: D3DXEFFECTINSTANCE-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354886"
---
# <a name="d3dxeffectinstance-structure"></a><span data-ttu-id="7a322-103">D3DXEFFECTINSTANCE-Struktur</span><span class="sxs-lookup"><span data-stu-id="7a322-103">D3DXEFFECTINSTANCE structure</span></span>

<span data-ttu-id="7a322-104">Datentyp zum Verwalten eines Satzes von Standardeffekt Parametern.</span><span class="sxs-lookup"><span data-stu-id="7a322-104">Data type for managing a set of default effect parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a322-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a322-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a><span data-ttu-id="7a322-106">Member</span><span class="sxs-lookup"><span data-stu-id="7a322-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a322-107">**"Peer Name"**</span><span class="sxs-lookup"><span data-stu-id="7a322-107">**pEffectFilename**</span></span>
</dt> <dd>

<span data-ttu-id="7a322-108">Typ: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="7a322-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="7a322-109">Der Name der Effekt Datei.</span><span class="sxs-lookup"><span data-stu-id="7a322-109">Name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="7a322-110">**Numdefaults**</span><span class="sxs-lookup"><span data-stu-id="7a322-110">**NumDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="7a322-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a322-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a322-112">Anzahl der Standardparameter.</span><span class="sxs-lookup"><span data-stu-id="7a322-112">Number of default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="7a322-113">**pdefaults**</span><span class="sxs-lookup"><span data-stu-id="7a322-113">**pDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="7a322-114">Typ: **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span><span class="sxs-lookup"><span data-stu-id="7a322-114">Type: **[**LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a322-115">Ein Zeiger auf ein Array von [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) -Elementen, die jeweils einen Effektparameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="7a322-115">Pointer to an array of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) elements, each of which contains an effect parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a322-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a322-116">Requirements</span></span>



| <span data-ttu-id="7a322-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a322-117">Requirement</span></span> | <span data-ttu-id="7a322-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7a322-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a322-119">Header</span><span class="sxs-lookup"><span data-stu-id="7a322-119">Header</span></span><br/> | <dl> <span data-ttu-id="7a322-120"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a322-120"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a322-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a322-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a322-122">Effekt Strukturen</span><span class="sxs-lookup"><span data-stu-id="7a322-122">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
