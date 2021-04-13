---
title: DXCoreAdapterPreference
description: Definiert Konstanten, die DXCore-Adapter Einstellungen angeben, die als Listen Sortierkriterien verwendet werden sollen.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390745"
---
# <a name="dxcoreadapterpreference-enum"></a><span data-ttu-id="7099e-103">Dxcoreadapterpreference-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="7099e-103">DXCoreAdapterPreference enum</span></span>

## <a name="description"></a><span data-ttu-id="7099e-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7099e-104">Description</span></span>

<span data-ttu-id="7099e-105">Definiert Konstanten, die DXCore-Adapter Einstellungen angeben, die als Listen Sortierkriterien verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7099e-105">Defines constants that specify DXCore adapter preferences to be used as list-sorting criteria.</span></span> <span data-ttu-id="7099e-106">Sie können eine DXCore-Adapter Liste sortieren, indem Sie ein Array von **dxcoreadapterpreference** an [idxcoreadapterlist:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md)übergeben.</span><span class="sxs-lookup"><span data-stu-id="7099e-106">You can sort a DXCore adapter list by passing an array of **DXCoreAdapterPreference** to [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7099e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7099e-107">Syntax</span></span>

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a><span data-ttu-id="7099e-108">Aufzählungs Felder</span><span class="sxs-lookup"><span data-stu-id="7099e-108">Enum fields</span></span>

### <a name="hardware"></a><span data-ttu-id="7099e-109">Hardware</span><span class="sxs-lookup"><span data-stu-id="7099e-109">Hardware</span></span>

<span data-ttu-id="7099e-110">Gibt eine bevorzugte Einstellung für Hardware Adapter an (im Gegensatz zu Software Adaptern).</span><span class="sxs-lookup"><span data-stu-id="7099e-110">Specifies a preference for hardware adapters (as opposed to software adapters).</span></span>

### <a name="minimumpower"></a><span data-ttu-id="7099e-111">Minimumpower</span><span class="sxs-lookup"><span data-stu-id="7099e-111">MinimumPower</span></span>

<span data-ttu-id="7099e-112">Gibt eine bevorzugte GPU (z. b. einen integrierten Grafikprozessor oder igpu) an.</span><span class="sxs-lookup"><span data-stu-id="7099e-112">Specifies a preference for the minimum-powered GPU (such as an integrated graphics processor, or iGPU).</span></span>

### <a name="highperformance"></a><span data-ttu-id="7099e-113">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="7099e-113">HighPerformance</span></span>

<span data-ttu-id="7099e-114">Gibt die bevorzugte GPU an, z. b. einen externen Grafikprozessor (xgpu), falls verfügbar, oder einen diskreten Grafikprozessor (dGPU), falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7099e-114">Specifies a preference for the highest-performance GPU, such as an external graphics processor (xGPU), if available, or discrete graphics processor (dGPU) if available.</span></span>

## <a name="see-also"></a><span data-ttu-id="7099e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7099e-115">See also</span></span>

<span data-ttu-id="7099e-116">[Idxcoreadapterlist:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="7099e-116">[IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>