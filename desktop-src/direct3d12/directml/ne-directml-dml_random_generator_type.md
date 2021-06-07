---
UID: NE:directml.DML_RANDOM_GENERATOR_TYPE
title: DML_RANDOM_GENERATOR_TYPE
description: Definiert Konstanten, die Typen des Zufallszahlengenerators angeben.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_TYPE
- DML_RANDOM_GENERATOR_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_RANDOM_GENERATOR_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_TYPE, DML_RANDOM_GENERATOR_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_RANDOM_GENERATOR_TYPE
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
- DML_RANDOM_GENERATOR_TYPE
- directml/DML_RANDOM_GENERATOR_TYPE
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
- DML_RANDOM_GENERATOR_TYPE
ms.openlocfilehash: c08b5cdc07280a2851636a555415ecce515fa79b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417170"
---
# <a name="dml_random_generator_type-enumeration-directmlh"></a><span data-ttu-id="35938-103">DML_RANDOM_GENERATOR_TYPE -Enumeration (directml.h)</span><span class="sxs-lookup"><span data-stu-id="35938-103">DML_RANDOM_GENERATOR_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="35938-104">Definiert Konstanten, die Typen des Zufallszahlengenerators angeben.</span><span class="sxs-lookup"><span data-stu-id="35938-104">Defines constants that specify types of random random-number generator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35938-105">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="35938-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="35938-106">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="35938-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="35938-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="35938-107">Syntax</span></span>
```cpp
enum DML_RANDOM_GENERATOR_TYPE
{
  DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10
};
```

## <a name="constants"></a><span data-ttu-id="35938-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="35938-108">Constants</span></span>

| <span data-ttu-id="35938-109">Name</span><span class="sxs-lookup"><span data-stu-id="35938-109">Name</span></span> | <span data-ttu-id="35938-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35938-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="35938-111">DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10</span><span class="sxs-lookup"><span data-stu-id="35938-111">DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10</span></span> | <span data-ttu-id="35938-112">Gibt einen Generator für Pseudozufallszahlen gemäß dem [Algorithmus Desox 4x32-10 an.](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf)</span><span class="sxs-lookup"><span data-stu-id="35938-112">Specifies a generator for pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span> |


## <a name="requirements"></a><span data-ttu-id="35938-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="35938-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="35938-114">**Header**</span><span class="sxs-lookup"><span data-stu-id="35938-114">**Header**</span></span> | <span data-ttu-id="35938-115">directml.h</span><span class="sxs-lookup"><span data-stu-id="35938-115">directml.h</span></span> |