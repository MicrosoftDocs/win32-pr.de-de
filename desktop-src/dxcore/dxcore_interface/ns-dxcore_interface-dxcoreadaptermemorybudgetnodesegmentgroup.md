---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Beschreibt eine Speichersegment Gruppe für einen Adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390460"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a><span data-ttu-id="551ba-103">Dxcoreadaptermemorybudgetnoentsegmentgroup-Struktur</span><span class="sxs-lookup"><span data-stu-id="551ba-103">DXCoreAdapterMemoryBudgetNodeSegmentGroup structure</span></span>

<span data-ttu-id="551ba-104">Beschreibt eine Speichersegment Gruppe für einen Adapter.</span><span class="sxs-lookup"><span data-stu-id="551ba-104">Describes a memory segment group for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="551ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="551ba-105">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a><span data-ttu-id="551ba-106">Member</span><span class="sxs-lookup"><span data-stu-id="551ba-106">Members</span></span>

### <a name="nodeindex"></a><span data-ttu-id="551ba-107">nodeindex</span><span class="sxs-lookup"><span data-stu-id="551ba-107">nodeIndex</span></span>

<span data-ttu-id="551ba-108">Typ: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="551ba-108">Type: **uint32_t**</span></span>

<span data-ttu-id="551ba-109">Gibt den physischen Adapter des Geräts an, für den die Adapter Speicherinformationen abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="551ba-109">Specifies the device's physical adapter for which the adapter memory information is queried.</span></span> <span data-ttu-id="551ba-110">Legen Sie für den Einzel Adapter Vorgang den Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="551ba-110">For single-adapter operation, set this to zero.</span></span> <span data-ttu-id="551ba-111">Wenn mehrere Adapter Knoten vorhanden sind, legen Sie diese auf den Index des Knotens (den physischen Adapter des Geräts) fest, für den Sie die Informationen zum Adapter Speicher Abfragen möchten (siehe [multiadaptersysteme](../../direct3d12/multi-engine.md)).</span><span class="sxs-lookup"><span data-stu-id="551ba-111">If there are multiple adapter nodes, then set this to the index of the node (the device's physical adapter) for which you want to query for adapter memory information (see [Multi-adapter systems](../../direct3d12/multi-engine.md)).</span></span>

### <a name="segmentgroup"></a><span data-ttu-id="551ba-112">segmentgroup</span><span class="sxs-lookup"><span data-stu-id="551ba-112">segmentGroup</span></span>

<span data-ttu-id="551ba-113">Typ: **[dxcoresegmentgroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span><span class="sxs-lookup"><span data-stu-id="551ba-113">Type: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span></span>

<span data-ttu-id="551ba-114">Gibt die Gruppe der Adapter Speichersegmente an, die Sie Abfragen möchten.</span><span class="sxs-lookup"><span data-stu-id="551ba-114">Specifies the adapter memory segment grouping that you want to query about.</span></span>

## <a name="see-also"></a><span data-ttu-id="551ba-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="551ba-115">See also</span></span>

[<span data-ttu-id="551ba-116">DXCore-Referenz</span><span class="sxs-lookup"><span data-stu-id="551ba-116">DXCore Reference</span></span>](../dxcore-reference.md)

[<span data-ttu-id="551ba-117">Verwenden von DXCore zum Auflisten von Adaptern</span><span class="sxs-lookup"><span data-stu-id="551ba-117">Using DXCore to enumerate adapters</span></span>](../dxcore-enum-adapters.md)

[<span data-ttu-id="551ba-118">Systeme mit mehreren Adaptern</span><span class="sxs-lookup"><span data-stu-id="551ba-118">Multi-adapter systems</span></span>](../../direct3d12/multi-engine.md)