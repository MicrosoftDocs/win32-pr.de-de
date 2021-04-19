---
description: Beschreibt eine JPEG-quantisierungstabelle.
ms.assetid: DE1AAB15-B0B8-4594-BBCE-5F8EE5CE0AF7
title: DXGI_JPEG_QUANTIZATION_TABLE-Struktur (dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_QUANTIZATION_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b0a097cb4c364ecc14e471f7c15f642aa65e912
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361858"
---
# <a name="dxgi_jpeg_quantization_table-structure"></a><span data-ttu-id="cec44-103">DXGI- \_ JPEG- \_ quantisierungstabellenstruktur \_</span><span class="sxs-lookup"><span data-stu-id="cec44-103">DXGI\_JPEG\_QUANTIZATION\_TABLE structure</span></span>

<span data-ttu-id="cec44-104">Beschreibt eine JPEG-quantisierungstabelle.</span><span class="sxs-lookup"><span data-stu-id="cec44-104">Describes a JPEG quantization table.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec44-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cec44-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_QUANTIZATION_TABLE {
  BYTE Elements[64];
} DXGI_JPEG_QUANTIZATION_TABLE;
```



## <a name="members"></a><span data-ttu-id="cec44-106">Member</span><span class="sxs-lookup"><span data-stu-id="cec44-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cec44-107">**Elemente**</span><span class="sxs-lookup"><span data-stu-id="cec44-107">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="cec44-108">Ein Bytearray, das die Elemente der quantifizierungstabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="cec44-108">An array of bytes containing the elements of the quantization table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cec44-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cec44-109">Requirements</span></span>



| <span data-ttu-id="cec44-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cec44-110">Requirement</span></span> | <span data-ttu-id="cec44-111">Wert</span><span class="sxs-lookup"><span data-stu-id="cec44-111">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cec44-112">Header</span><span class="sxs-lookup"><span data-stu-id="cec44-112">Header</span></span><br/> | <dl> <span data-ttu-id="cec44-113"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="cec44-113"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec44-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cec44-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec44-115">DXGI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="cec44-115">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




