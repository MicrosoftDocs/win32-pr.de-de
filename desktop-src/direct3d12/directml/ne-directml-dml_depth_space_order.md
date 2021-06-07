---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Definiert Konstanten, die die Transformation steuern, die in den DirectML-Operatoren DML_OPERATOR_DEPTH_TO_SPACE1 **und** DML_OPERATOR_SPACE_TO_DEPTH1. [](/windows/win32/api/directml/ne-directml-dml_operator_type)
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_SPACE_ORDER
- directml/DML_DEPTH_SPACE_ORDER
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
- DML_DEPTH_SPACE_ORDER
ms.openlocfilehash: 009686adfc054c7b6344f01edafedaf2921693d5
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417217"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a><span data-ttu-id="62520-103">DML_DEPTH_SPACE_ORDER -Enumeration (directml.h)</span><span class="sxs-lookup"><span data-stu-id="62520-103">DML_DEPTH_SPACE_ORDER enumeration (directml.h)</span></span>

<span data-ttu-id="62520-104">Definiert Konstanten, die die Transformation steuern, die in den DirectML-Operatoren DML_OPERATOR_DEPTH_TO_SPACE1 **und** DML_OPERATOR_SPACE_TO_DEPTH1. [](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="62520-104">Defines constants controlling the transform applied in the DirectML operators [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) and **DML_OPERATOR_SPACE_TO_DEPTH1**.</span></span> <span data-ttu-id="62520-105">Diese werden innerhalb der [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) [und](./ns-directml-dml_space_to_depth1_operator_desc.md) DML_SPACE_TO_DEPTH1_OPERATOR_DESC verwendet.</span><span class="sxs-lookup"><span data-stu-id="62520-105">These are used within the [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) structures.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62520-106">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="62520-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="62520-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="62520-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="62520-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="62520-108">Syntax</span></span>
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a><span data-ttu-id="62520-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="62520-109">Constants</span></span>

| <span data-ttu-id="62520-110">Name</span><span class="sxs-lookup"><span data-stu-id="62520-110">Name</span></span> | <span data-ttu-id="62520-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62520-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="62520-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span><span class="sxs-lookup"><span data-stu-id="62520-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span></span> | <span data-ttu-id="62520-113">Bewirkt, dass tensors, die in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) und [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) verwendet werden, mit den folgenden Layouts interpretiert werden, wobei Dimensionen in Klammern zusammen flach werden.</span><span class="sxs-lookup"><span data-stu-id="62520-113">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="62520-114">- **Tiefenversion:**[Batch, (BlockHeight, BlockWidth, Channels), Height, Width]</span><span class="sxs-lookup"><span data-stu-id="62520-114">- **Depth version**: [Batch, (BlockHeight, BlockWidth, Channels), Height, Width]</span></span><br><span data-ttu-id="62520-115">- **Raumversion:**[Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span><span class="sxs-lookup"><span data-stu-id="62520-115">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |
| <span data-ttu-id="62520-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span><span class="sxs-lookup"><span data-stu-id="62520-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span></span> | <span data-ttu-id="62520-117">Bewirkt, dass tensors, die in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) und [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) verwendet werden, mit den folgenden Layouts interpretiert werden, wobei Dimensionen in Klammern zusammen flach werden.</span><span class="sxs-lookup"><span data-stu-id="62520-117">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="62520-118">- **Tiefenversion:**[Batch, (Channels, BlockHeight, BlockWidth), Height, Width]</span><span class="sxs-lookup"><span data-stu-id="62520-118">- **Depth version**: [Batch, (Channels, BlockHeight, BlockWidth), Height, Width]</span></span><br><span data-ttu-id="62520-119">- **Raumversion:**[Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span><span class="sxs-lookup"><span data-stu-id="62520-119">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |

## <a name="remarks"></a><span data-ttu-id="62520-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="62520-120">Remarks</span></span>

<span data-ttu-id="62520-121">Beispiele [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) auswirkungen [dieser DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) finden Sie in der Dokumentation zu DML_SPACE_TO_DEPTH1_OPERATOR_DESC Und-Daten.</span><span class="sxs-lookup"><span data-stu-id="62520-121">See [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) documentation for examples showing the effect of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="62520-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="62520-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="62520-123">**Header**</span><span class="sxs-lookup"><span data-stu-id="62520-123">**Header**</span></span> | <span data-ttu-id="62520-124">directml.h</span><span class="sxs-lookup"><span data-stu-id="62520-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="62520-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62520-125">See also</span></span>

* [<span data-ttu-id="62520-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="62520-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span></span>](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [<span data-ttu-id="62520-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="62520-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a><span data-ttu-id="62520-128">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="62520-128">Availability</span></span>
<span data-ttu-id="62520-129">Diese Enumeration wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="62520-129">This enumeration was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>