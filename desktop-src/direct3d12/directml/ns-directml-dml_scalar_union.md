---
UID: NS:directml.DML_SCALAR_UNION
title: DML_SCALAR_UNION
description: Eine Vereinigung von skalaren Typen.
helpviewer_keywords:
- DML_SCALAR_UNION
- DML_SCALAR_UNION structure
- direct3d12.dml_scalar_union
- directml/DML_SCALAR_UNION
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
ms.keywords: DML_SCALAR_UNION, DML_SCALAR_UNION structure, direct3d12.dml_scalar_union, directml/DML_SCALAR_UNION
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_SCALAR_UNION
- directml/DML_SCALAR_UNION
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_SCALAR_UNION
ms.openlocfilehash: d53ec7025d3da5a07a648849e366d436755ad3f1
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417866"
---
# <a name="dml_scalar_union-union-directmlh"></a><span data-ttu-id="5266a-103">DML_SCALAR_UNION Union (directml.h)</span><span class="sxs-lookup"><span data-stu-id="5266a-103">DML_SCALAR_UNION union (directml.h)</span></span>
<span data-ttu-id="5266a-104">Eine Vereinigung von skalaren Typen.</span><span class="sxs-lookup"><span data-stu-id="5266a-104">A union of scalar types.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5266a-105">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="5266a-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5266a-106">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="5266a-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5266a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5266a-107">Syntax</span></span>
```cpp
union DML_SCALAR_UNION {
  BYTE   Bytes[8];
  INT8   Int8;
  UINT8  UInt8;
  INT16  Int16;
  UINT16 UInt16;
  INT32  Int32;
  UINT32 UInt32;
  INT64  Int64;
  UINT64 UInt64;
  FLOAT  Float32;
  DOUBLE Float64;
};
```



## <a name="members"></a><span data-ttu-id="5266a-108">Member</span><span class="sxs-lookup"><span data-stu-id="5266a-108">Members</span></span>

`Bytes`

<span data-ttu-id="5266a-109">Ein 8-Byte-Array.</span><span class="sxs-lookup"><span data-stu-id="5266a-109">An 8-byte array.</span></span>


`Int8`

<span data-ttu-id="5266a-110">Eine 8-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="5266a-110">An 8-bit signed integer.</span></span>


`UInt8`

<span data-ttu-id="5266a-111">Eine 8-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="5266a-111">An 8-bit unsigned integer.</span></span>


`Int16`

<span data-ttu-id="5266a-112">Eine 16-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="5266a-112">A 16-bit signed integer.</span></span>


`UInt16`

<span data-ttu-id="5266a-113">Eine 16-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="5266a-113">A 16-bit unsigned integer.</span></span>


`Int32`

<span data-ttu-id="5266a-114">Eine 32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="5266a-114">A 32-bit signed integer.</span></span>


`UInt32`

<span data-ttu-id="5266a-115">Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="5266a-115">A 32-bit unsigned integer.</span></span>


`Int64`

<span data-ttu-id="5266a-116">Eine 64-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="5266a-116">A 64-bit signed integer.</span></span>


`UInt64`

<span data-ttu-id="5266a-117">Eine 64-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="5266a-117">A 64-bit unsigned integer.</span></span>


`Float32`

<span data-ttu-id="5266a-118">Eine Gleitkommazahl mit einfacher Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="5266a-118">A single precision floating-point number.</span></span>


`Float64`

<span data-ttu-id="5266a-119">Eine Gleitkommazahl mit doppelter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="5266a-119">A double precision floating-point number.</span></span>



## <a name="requirements"></a><span data-ttu-id="5266a-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5266a-120">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5266a-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="5266a-121">**Header**</span></span> | <span data-ttu-id="5266a-122">directml.h</span><span class="sxs-lookup"><span data-stu-id="5266a-122">directml.h</span></span> |