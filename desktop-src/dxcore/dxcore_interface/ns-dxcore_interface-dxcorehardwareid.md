---
title: DXCoreHardwareID
description: Stellt die PnP-Hardware-ID-Teile für einen Adapter dar.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101771"
---
# <a name="dxcorehardwareid-structure"></a><span data-ttu-id="ef589-103">Dxcorehardwareid-Struktur</span><span class="sxs-lookup"><span data-stu-id="ef589-103">DXCoreHardwareID structure</span></span>

<span data-ttu-id="ef589-104">Stellt die PnP-Hardware-ID-Teile für einen Adapter dar.</span><span class="sxs-lookup"><span data-stu-id="ef589-104">Represents the PnP hardware ID parts for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef589-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef589-105">Syntax</span></span>

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a><span data-ttu-id="ef589-106">Member</span><span class="sxs-lookup"><span data-stu-id="ef589-106">Members</span></span>

### <a name="vendorid"></a><span data-ttu-id="ef589-107">vendorId</span><span class="sxs-lookup"><span data-stu-id="ef589-107">vendorId</span></span>

<span data-ttu-id="ef589-108">Typ: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="ef589-108">Type: **uint32_t\***</span></span>

<span data-ttu-id="ef589-109">Die PCI-ID des Hardwareherstellers des Adapters.</span><span class="sxs-lookup"><span data-stu-id="ef589-109">The PCI ID of the adapter's hardware vendor.</span></span>

### <a name="deviceid"></a><span data-ttu-id="ef589-110">deviceId</span><span class="sxs-lookup"><span data-stu-id="ef589-110">deviceId</span></span>

<span data-ttu-id="ef589-111">Typ: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="ef589-111">Type: **uint32_t\***</span></span>

<span data-ttu-id="ef589-112">Die PCI-ID des Hardware Geräts des Adapters.</span><span class="sxs-lookup"><span data-stu-id="ef589-112">The PCI ID of the adapter's hardware device.</span></span>

### <a name="subsysid"></a><span data-ttu-id="ef589-113">subsysid</span><span class="sxs-lookup"><span data-stu-id="ef589-113">subSysId</span></span>

<span data-ttu-id="ef589-114">Typ: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="ef589-114">Type: **uint32_t\***</span></span>

<span data-ttu-id="ef589-115">Die PCI-ID des Hardware Subsystems des Adapters.</span><span class="sxs-lookup"><span data-stu-id="ef589-115">The PCI ID of the adapter's hardware subsystem.</span></span>

### <a name="revision"></a><span data-ttu-id="ef589-116">revision</span><span class="sxs-lookup"><span data-stu-id="ef589-116">revision</span></span>

<span data-ttu-id="ef589-117">Typ: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="ef589-117">Type: **uint32_t\***</span></span>

<span data-ttu-id="ef589-118">Die PCI-ID der Revisionsnummer des Adapters.</span><span class="sxs-lookup"><span data-stu-id="ef589-118">The PCI ID of the adapter's revision number.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef589-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef589-119">See also</span></span>

<span data-ttu-id="ef589-120">[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="ef589-120">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>