---
description: Beschreibt eine JPEG AC-Huffman-Tabelle.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: DXGI_JPEG_AC_HUFFMAN_TABLE-Struktur (dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 760840822eb6b9411983c72324bc1e86a3208195
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353353"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a><span data-ttu-id="2fa01-103">DXGI \_ JPEG \_ AC- \_ Huffman- \_ Tabellenstruktur</span><span class="sxs-lookup"><span data-stu-id="2fa01-103">DXGI\_JPEG\_AC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="2fa01-104">Beschreibt eine JPEG AC-Huffman-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2fa01-104">Describes a JPEG AC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa01-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fa01-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="2fa01-106">Member</span><span class="sxs-lookup"><span data-stu-id="2fa01-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2fa01-107">**Codecount**</span><span class="sxs-lookup"><span data-stu-id="2fa01-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="2fa01-108">Die Anzahl der Codes für jede Codelänge.</span><span class="sxs-lookup"><span data-stu-id="2fa01-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="2fa01-109">**Codevalues**</span><span class="sxs-lookup"><span data-stu-id="2fa01-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="2fa01-110">Die Huffman-Codewerte in der Reihenfolge, in der die Codelänge erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="2fa01-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fa01-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fa01-111">Requirements</span></span>



| <span data-ttu-id="2fa01-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fa01-112">Requirement</span></span> | <span data-ttu-id="2fa01-113">Wert</span><span class="sxs-lookup"><span data-stu-id="2fa01-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa01-114">Header</span><span class="sxs-lookup"><span data-stu-id="2fa01-114">Header</span></span><br/> | <dl> <span data-ttu-id="2fa01-115"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fa01-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fa01-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fa01-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa01-117">DXGI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2fa01-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




