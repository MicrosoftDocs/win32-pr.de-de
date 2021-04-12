---
description: Beschreibt eine JPEG-DC-Huffman-Tabelle.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: DXGI_JPEG_DC_HUFFMAN_TABLE-Struktur (dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_DC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: b2f5f73f7c6def745b987818b9ec30fb3e2752e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219487"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a><span data-ttu-id="7cef3-103">DXGI \_ JPEG- \_ DC- \_ Huffman- \_ Tabellenstruktur</span><span class="sxs-lookup"><span data-stu-id="7cef3-103">DXGI\_JPEG\_DC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="7cef3-104">Beschreibt eine JPEG-DC-Huffman-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7cef3-104">Describes a JPEG DC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cef3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cef3-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="7cef3-106">Member</span><span class="sxs-lookup"><span data-stu-id="7cef3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7cef3-107">**Codecount**</span><span class="sxs-lookup"><span data-stu-id="7cef3-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="7cef3-108">Die Anzahl der Codes für jede Codelänge.</span><span class="sxs-lookup"><span data-stu-id="7cef3-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="7cef3-109">**Codevalues**</span><span class="sxs-lookup"><span data-stu-id="7cef3-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="7cef3-110">Die Huffman-Codewerte in der Reihenfolge, in der die Codelänge erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="7cef3-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7cef3-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cef3-111">Requirements</span></span>



| <span data-ttu-id="7cef3-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7cef3-112">Requirement</span></span> | <span data-ttu-id="7cef3-113">Wert</span><span class="sxs-lookup"><span data-stu-id="7cef3-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7cef3-114">Header</span><span class="sxs-lookup"><span data-stu-id="7cef3-114">Header</span></span><br/> | <dl> <span data-ttu-id="7cef3-115"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cef3-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cef3-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cef3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cef3-117">DXGI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7cef3-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




