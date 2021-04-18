---
title: DXCoreSegmentGroup
description: Definiert Konstanten, die die Speichersegment Gruppierung eines Adapters angeben.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ce94d5f806879ea84f64c88d3a62b074a5c5415b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337441"
---
# <a name="dxcoresegmentgroup-enum"></a><span data-ttu-id="a22c6-103">Dxcoresegmentgroup-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a22c6-103">DXCoreSegmentGroup enum</span></span>

<span data-ttu-id="a22c6-104">Definiert Konstanten, die die Speichersegment Gruppierung eines Adapters angeben.</span><span class="sxs-lookup"><span data-stu-id="a22c6-104">Defines constants that specify an adapter's memory segment grouping.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a22c6-105">Syntax</span></span>

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a><span data-ttu-id="a22c6-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a22c6-106">Constants</span></span>

### <a name="local"></a><span data-ttu-id="a22c6-107">Lokal</span><span class="sxs-lookup"><span data-stu-id="a22c6-107">Local</span></span>

<span data-ttu-id="a22c6-108">Gibt eine Gruppierung von Segmenten an, die für den Adapter als lokal angesehen werden, und stellt den schnellsten verfügbaren Arbeitsspeicher für die GPU dar.</span><span class="sxs-lookup"><span data-stu-id="a22c6-108">Specifies a grouping of segments that is considered local to the adapter, and represents the fastest memory available to the GPU.</span></span> <span data-ttu-id="a22c6-109">Die Anwendung sollte die lokale Segment Gruppe als Zielgröße für das Workingset als Ziel festlegen.</span><span class="sxs-lookup"><span data-stu-id="a22c6-109">Your application should target the local segment group as the target size for its working set.</span></span>

### <a name="nonlocal"></a><span data-ttu-id="a22c6-110">Nicht lokalen</span><span class="sxs-lookup"><span data-stu-id="a22c6-110">NonLocal</span></span>

<span data-ttu-id="a22c6-111">Gibt eine Gruppierung von Segmenten an, die für den Adapter als nicht lokal betrachtet werden und möglicherweise eine langsamere Leistung als die lokale Segment Gruppe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a22c6-111">Specifies a grouping of segments that is considered non-local to the adapter, and may have slower performance than the local segment group.</span></span>

## <a name="see-also"></a><span data-ttu-id="a22c6-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a22c6-112">See also</span></span>

<span data-ttu-id="a22c6-113">[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="a22c6-113">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>