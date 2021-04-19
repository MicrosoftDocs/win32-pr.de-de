---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Definiert Konstanten, die die in den directml-Operatoren angewendete Transformation [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) und **DML_OPERATOR_SPACE_TO_DEPTH1** steuern.
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
ms.openlocfilehash: 21ab43f81a5959fc6722f5f4dedc3f60319ba642
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106355701"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a><span data-ttu-id="ccfd4-103">DML_DEPTH_SPACE_ORDER-Enumeration (directml. h)</span><span class="sxs-lookup"><span data-stu-id="ccfd4-103">DML_DEPTH_SPACE_ORDER enumeration (directml.h)</span></span>

<span data-ttu-id="ccfd4-104">Definiert Konstanten, die die in den directml-Operatoren angewendete Transformation [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) und **DML_OPERATOR_SPACE_TO_DEPTH1** steuern.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-104">Defines constants controlling the transform applied in the DirectML operators [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) and **DML_OPERATOR_SPACE_TO_DEPTH1**.</span></span> <span data-ttu-id="ccfd4-105">Diese werden in den Strukturen [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) und [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-105">These are used within the [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) structures.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ccfd4-106">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="ccfd4-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="ccfd4-107">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ccfd4-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ccfd4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccfd4-108">Syntax</span></span>
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a><span data-ttu-id="ccfd4-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ccfd4-109">Constants</span></span>

| <span data-ttu-id="ccfd4-110">Name</span><span class="sxs-lookup"><span data-stu-id="ccfd4-110">Name</span></span> | <span data-ttu-id="ccfd4-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccfd4-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="ccfd4-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span><span class="sxs-lookup"><span data-stu-id="ccfd4-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span></span> | <span data-ttu-id="ccfd4-113">Bewirkt, dass in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) und [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) verwendete Tensoren mit den folgenden Layouts interpretiert werden, bei denen Dimensionen in Klammern zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-113">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="ccfd4-114">- **Tiefen Version**: [Batch, (blockheight, blockWidth, Channels), Höhe, Breite]</span><span class="sxs-lookup"><span data-stu-id="ccfd4-114">- **Depth version**: [Batch, (BlockHeight, BlockWidth, Channels), Height, Width]</span></span><br><span data-ttu-id="ccfd4-115">- **Speicherplatz Version**: [Batch, Channels, (Height, Block Height), (Width, Block Width)]</span><span class="sxs-lookup"><span data-stu-id="ccfd4-115">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |
| <span data-ttu-id="ccfd4-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span><span class="sxs-lookup"><span data-stu-id="ccfd4-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span></span> | <span data-ttu-id="ccfd4-117">Bewirkt, dass in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) und [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) verwendete Tensoren mit den folgenden Layouts interpretiert werden, bei denen Dimensionen in Klammern zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-117">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="ccfd4-118">- **Tiefen Version**: [Batch, (Channels, blockheight, blockWidth), Höhe, Breite]</span><span class="sxs-lookup"><span data-stu-id="ccfd4-118">- **Depth version**: [Batch, (Channels, BlockHeight, BlockWidth), Height, Width]</span></span><br><span data-ttu-id="ccfd4-119">- **Speicherplatz Version**: [Batch, Channels, (Height, Block Height), (Width, Block Width)]</span><span class="sxs-lookup"><span data-stu-id="ccfd4-119">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |

## <a name="remarks"></a><span data-ttu-id="ccfd4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccfd4-120">Remarks</span></span>

<span data-ttu-id="ccfd4-121">In den [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) -und [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) Dokumentation finden Sie Beispiele, die die Auswirkung dieser Werte veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-121">See [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) documentation for examples showing the effect of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccfd4-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccfd4-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ccfd4-123">**Header**</span><span class="sxs-lookup"><span data-stu-id="ccfd4-123">**Header**</span></span> | <span data-ttu-id="ccfd4-124">directml. h</span><span class="sxs-lookup"><span data-stu-id="ccfd4-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="ccfd4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccfd4-125">See also</span></span>

* [<span data-ttu-id="ccfd4-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="ccfd4-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span></span>](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [<span data-ttu-id="ccfd4-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="ccfd4-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a><span data-ttu-id="ccfd4-128">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ccfd4-128">Availability</span></span>
<span data-ttu-id="ccfd4-129">Diese Enumeration wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="ccfd4-129">This enumeration was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>