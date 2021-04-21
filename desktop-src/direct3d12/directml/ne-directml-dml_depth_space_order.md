---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Definiert Konstanten, die die Transformation steuern, die in den DirectML-Operatoren [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) und **DML_OPERATOR_SPACE_TO_DEPTH1** angewendet wird.
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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803536"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a><span data-ttu-id="e8f67-103">DML_DEPTH_SPACE_ORDER-Enumeration (directml.h)</span><span class="sxs-lookup"><span data-stu-id="e8f67-103">DML_DEPTH_SPACE_ORDER enumeration (directml.h)</span></span>

<span data-ttu-id="e8f67-104">Definiert Konstanten, die die Transformation steuern, die in den DirectML-Operatoren [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) und **DML_OPERATOR_SPACE_TO_DEPTH1** angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8f67-104">Defines constants controlling the transform applied in the DirectML operators [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) and **DML_OPERATOR_SPACE_TO_DEPTH1**.</span></span> <span data-ttu-id="e8f67-105">Diese werden innerhalb der [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) und [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) Strukturen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8f67-105">These are used within the [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) structures.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8f67-106">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="e8f67-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e8f67-107">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="e8f67-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8f67-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8f67-108">Syntax</span></span>
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a><span data-ttu-id="e8f67-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e8f67-109">Constants</span></span>

| <span data-ttu-id="e8f67-110">Name</span><span class="sxs-lookup"><span data-stu-id="e8f67-110">Name</span></span> | <span data-ttu-id="e8f67-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8f67-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="e8f67-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span><span class="sxs-lookup"><span data-stu-id="e8f67-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span></span> | <span data-ttu-id="e8f67-113">Bewirkt, dass tensors, die in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) und [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) verwendet werden, mit den folgenden Layouts interpretiert werden, wobei Dimensionen in Klammern zusammengestrichen werden.</span><span class="sxs-lookup"><span data-stu-id="e8f67-113">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="e8f67-114">- **Tiefenversion:**[Batch, (BlockHeight, BlockWidth, Channels), Height, Width]</span><span class="sxs-lookup"><span data-stu-id="e8f67-114">- **Depth version**: [Batch, (BlockHeight, BlockWidth, Channels), Height, Width]</span></span><br><span data-ttu-id="e8f67-115">- **Space-Version:**[Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span><span class="sxs-lookup"><span data-stu-id="e8f67-115">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |
| <span data-ttu-id="e8f67-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span><span class="sxs-lookup"><span data-stu-id="e8f67-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span></span> | <span data-ttu-id="e8f67-117">Bewirkt, dass tensors, die in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) und [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) verwendet werden, mit den folgenden Layouts interpretiert werden, wobei Dimensionen in Klammern zusammengestrichen werden.</span><span class="sxs-lookup"><span data-stu-id="e8f67-117">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="e8f67-118">- **Tiefenversion:**[Batch, (Channels, BlockHeight, BlockWidth), Height, Width]</span><span class="sxs-lookup"><span data-stu-id="e8f67-118">- **Depth version**: [Batch, (Channels, BlockHeight, BlockWidth), Height, Width]</span></span><br><span data-ttu-id="e8f67-119">- **Space-Version:**[Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span><span class="sxs-lookup"><span data-stu-id="e8f67-119">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |

## <a name="remarks"></a><span data-ttu-id="e8f67-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e8f67-120">Remarks</span></span>

<span data-ttu-id="e8f67-121">Beispiele zur Auswirkung dieser Werte finden Sie in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) und [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="e8f67-121">See [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) documentation for examples showing the effect of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8f67-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8f67-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e8f67-123">**Header**</span><span class="sxs-lookup"><span data-stu-id="e8f67-123">**Header**</span></span> | <span data-ttu-id="e8f67-124">directml.h</span><span class="sxs-lookup"><span data-stu-id="e8f67-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="e8f67-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8f67-125">See also</span></span>

* [<span data-ttu-id="e8f67-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="e8f67-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span></span>](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [<span data-ttu-id="e8f67-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="e8f67-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a><span data-ttu-id="e8f67-128">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="e8f67-128">Availability</span></span>
<span data-ttu-id="e8f67-129">Diese Enumeration wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e8f67-129">This enumeration was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>