---
description: Definiert die Debug-Monitor Token.
ms.assetid: c0df4c9f-a232-45cf-b543-e95ee84a4a8d
title: D3DDEBUGMONITORTOKENS-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEBUGMONITORTOKENS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 82c3ecfa7d197e1ab912dbafe0d26fcb2281e605
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961566"
---
# <a name="d3ddebugmonitortokens-enumeration"></a><span data-ttu-id="ee5bb-103">D3DDEBUGMONITORTOKENS-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ee5bb-103">D3DDEBUGMONITORTOKENS enumeration</span></span>

<span data-ttu-id="ee5bb-104">Definiert die Debug-Monitor Token.</span><span class="sxs-lookup"><span data-stu-id="ee5bb-104">Defines the debug monitor tokens.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee5bb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee5bb-105">Syntax</span></span>


```C++
typedef enum D3DDEBUGMONITORTOKENS { 
  D3DDMT_ENABLE       = 0,
  D3DDMT_DISABLE      = 1,
  D3DDMT_FORCE_DWORD  = 0x7fffffff
} D3DDEBUGMONITORTOKENS, *LPD3DDEBUGMONITORTOKENS;
```



## <a name="constants"></a><span data-ttu-id="ee5bb-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ee5bb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ee5bb-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT \_ aktivieren**</span><span class="sxs-lookup"><span data-stu-id="ee5bb-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="ee5bb-108">Aktivieren Sie den Debug-Monitor.</span><span class="sxs-lookup"><span data-stu-id="ee5bb-108">Enable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ee5bb-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**D3DDMT \_ Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="ee5bb-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**D3DDMT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="ee5bb-110">Deaktivieren Sie den Debugmonitor.</span><span class="sxs-lookup"><span data-stu-id="ee5bb-110">Disable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ee5bb-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ee5bb-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ee5bb-112">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="ee5bb-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ee5bb-113">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="ee5bb-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ee5bb-114">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee5bb-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee5bb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee5bb-115">Remarks</span></span>

<span data-ttu-id="ee5bb-116">Die Werte in diesem enumerierten Typ werden vom D3DRS \_ debugmonitortoken-gerengerzustand verwendet und sind nur für Debugbuilds relevant.</span><span class="sxs-lookup"><span data-stu-id="ee5bb-116">The values in this enumerated type are used by the D3DRS\_DEBUGMONITORTOKEN render state and are only relevant for debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee5bb-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee5bb-117">Requirements</span></span>



| <span data-ttu-id="ee5bb-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee5bb-118">Requirement</span></span> | <span data-ttu-id="ee5bb-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ee5bb-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee5bb-120">Header</span><span class="sxs-lookup"><span data-stu-id="ee5bb-120">Header</span></span><br/> | <dl> <span data-ttu-id="ee5bb-121"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee5bb-121"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee5bb-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee5bb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee5bb-123">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="ee5bb-123">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="ee5bb-124">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="ee5bb-124">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
