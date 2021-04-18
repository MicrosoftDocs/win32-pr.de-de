---
description: Effekt Datentypen. Die Daten sind im pValue-Member von D3DXEFFECTDEFAULT enthalten.
ms.assetid: d698ad6e-2ce2-48d6-90be-49bc08f172a9
title: D3DXEFFECTDEFAULTTYPE-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULTTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: ffd31167d712a8270011c061cd6328aa9214352e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354371"
---
# <a name="d3dxeffectdefaulttype-enumeration"></a><span data-ttu-id="b0052-104">D3DXEFFECTDEFAULTTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="b0052-104">D3DXEFFECTDEFAULTTYPE enumeration</span></span>

<span data-ttu-id="b0052-105">Effekt Datentypen.</span><span class="sxs-lookup"><span data-stu-id="b0052-105">Effect data types.</span></span> <span data-ttu-id="b0052-106">Die Daten sind im pValue-Member von [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="b0052-106">The data is contained in the pValue member of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0052-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0052-107">Syntax</span></span>


```C++
typedef enum D3DXEFFECTDEFAULTTYPE { 
  D3DXEDT_STRING      = 1,
  D3DXEDT_FLOATS      = 2,
  D3DXEDT_DWORD       = 3,
  D3DXEDT_FORCEDWORD  = 0x7fffffff
} D3DXEFFECTDEFAULTTYPE, *LPD3DXEFFECTDEFAULTTYPE;
```



## <a name="constants"></a><span data-ttu-id="b0052-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b0052-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b0052-109"><span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**D3DXEDT- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0052-109"><span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**D3DXEDT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="b0052-110">Der-Datentyp ist eine NULL-terminierte ASCII-Text Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b0052-110">The data type is a NULL-terminated ASCII text string.</span></span>

</dd> <dt>

<span data-ttu-id="b0052-111"><span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT \_ float**</span><span class="sxs-lookup"><span data-stu-id="b0052-111"><span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT\_FLOATS**</span></span>
</dt> <dd>

<span data-ttu-id="b0052-112">Der Datentyp ist ein Array vom Typ "float".</span><span class="sxs-lookup"><span data-stu-id="b0052-112">The data type is an array of type float.</span></span> <span data-ttu-id="b0052-113">Die Anzahl von float-Typen im Array wird durch numBytes in [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="b0052-113">The number of float types in the array is specified by NumBytes in [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0052-114"><span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT- \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b0052-114"><span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b0052-115">Der Datentyp ist ein DWORD.</span><span class="sxs-lookup"><span data-stu-id="b0052-115">The data type is a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="b0052-116"><span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT \_ forcedword**</span><span class="sxs-lookup"><span data-stu-id="b0052-116"><span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT\_FORCEDWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b0052-117">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="b0052-117">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b0052-118">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="b0052-118">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b0052-119">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0052-119">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0052-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0052-120">Requirements</span></span>



| <span data-ttu-id="b0052-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0052-121">Requirement</span></span> | <span data-ttu-id="b0052-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b0052-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0052-123">Header</span><span class="sxs-lookup"><span data-stu-id="b0052-123">Header</span></span><br/> | <dl> <span data-ttu-id="b0052-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0052-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0052-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0052-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0052-126">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="b0052-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




