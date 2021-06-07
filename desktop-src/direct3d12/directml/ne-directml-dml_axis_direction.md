---
UID: NE:directml.DML_AXIS_DIRECTION
title: DML_AXIS_DIRECTION
description: Definiert Konstanten, die die Richtung eines Vorgangs entlang der angegebenen Achse für den Operator angeben (z. B. Summierung, Auswählen der obersten k Elemente, Auswählen des Minimalelements).
ms.topic: reference
tech.root: directml
ms.date: 10/28/2020
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
- DML_AXIS_DIRECTION
- directml/DML_AXIS_DIRECTION
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
- DML_AXIS_DIRECTION
ms.openlocfilehash: e54d2abed3843ea9b2a22cb3c385f9edd1541ba5
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417218"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a><span data-ttu-id="3b8b5-103">DML_AXIS_DIRECTION-Enumeration (directml.h)</span><span class="sxs-lookup"><span data-stu-id="3b8b5-103">DML_AXIS_DIRECTION enumeration (directml.h)</span></span>

<span data-ttu-id="3b8b5-104">Definiert Konstanten, die die Richtung eines Vorgangs entlang der angegebenen Achse für den Operator angeben (z. B. Summierung, Auswählen der obersten k Elemente, Auswählen des Minimalelements).</span><span class="sxs-lookup"><span data-stu-id="3b8b5-104">Defines constants that specify the direction of an operation along the given axis for the operator (for example, summation, selecting the top-k elements, selecting the minimum element).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b8b5-105">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="3b8b5-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="3b8b5-106">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="3b8b5-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8b5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b8b5-107">Syntax</span></span>
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a><span data-ttu-id="3b8b5-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="3b8b5-108">Constants</span></span>

| <span data-ttu-id="3b8b5-109">Name</span><span class="sxs-lookup"><span data-stu-id="3b8b5-109">Name</span></span> | <span data-ttu-id="3b8b5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b8b5-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="3b8b5-111">DML_AXIS_DIRECTION_INCREASING</span><span class="sxs-lookup"><span data-stu-id="3b8b5-111">DML_AXIS_DIRECTION_INCREASING</span></span> | <span data-ttu-id="3b8b5-112">Gibt die aufsteigende Reihenfolge an (vom niedrigen index zum hohen Index).</span><span class="sxs-lookup"><span data-stu-id="3b8b5-112">Specifies increasing order (from the low index to the high index).</span></span> |
| <span data-ttu-id="3b8b5-113">DML_AXIS_DIRECTION_DECREASING</span><span class="sxs-lookup"><span data-stu-id="3b8b5-113">DML_AXIS_DIRECTION_DECREASING</span></span> | <span data-ttu-id="3b8b5-114">Gibt die absteigende Reihenfolge an (vom hohen zum unteren Index).</span><span class="sxs-lookup"><span data-stu-id="3b8b5-114">Specifies decreasing order (from the high index to the low index).</span></span> |


## <a name="requirements"></a><span data-ttu-id="3b8b5-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3b8b5-115">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3b8b5-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="3b8b5-116">**Header**</span></span> | <span data-ttu-id="3b8b5-117">directml.h</span><span class="sxs-lookup"><span data-stu-id="3b8b5-117">directml.h</span></span> |