---
title: ID3D12DeviceDownlevel-Schnittstelle
description: Stellt eine Windows-7-spezifische Abfrage für die Speicher Statistik bereit.
keywords:
- ID3D12DeviceDownlevel-Schnittstelle
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 401cbd0045211ef51e3ef6b06042262964ae2ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373483"
---
# <a name="id3d12devicedownlevel-interface"></a><span data-ttu-id="a3910-104">ID3D12DeviceDownlevel-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a3910-104">ID3D12DeviceDownlevel interface</span></span>

<span data-ttu-id="a3910-105">Auf diese Schnittstelle kann über **QueryInterface** von einem [Direct3D 12-Gerät](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) aus zugegriffen werden, wenn [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3910-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 device](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="a3910-106">Es stellt eine Windows-7-spezifische Abfrage für die Speicher Statistik bereit.</span><span class="sxs-lookup"><span data-stu-id="a3910-106">It provides a Windows-7-specific memory statistics query.</span></span>

### <a name="methods"></a><span data-ttu-id="a3910-107">Methoden</span><span class="sxs-lookup"><span data-stu-id="a3910-107">Methods</span></span>

<span data-ttu-id="a3910-108">Die **ID3D12DeviceDownlevel** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a3910-108">The **ID3D12DeviceDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="a3910-109">Methode</span><span class="sxs-lookup"><span data-stu-id="a3910-109">Method</span></span> | <span data-ttu-id="a3910-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3910-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="a3910-111">**Queryvideomemoryinfo**</span><span class="sxs-lookup"><span data-stu-id="a3910-111">**QueryVideoMemoryInfo**</span></span>](id3d12devicedownlevel-queryvideomemoryinfo.md) | <span data-ttu-id="a3910-112">Stellt Arbeitsspeicher Statistiken für Windows 7 bereit.</span><span class="sxs-lookup"><span data-stu-id="a3910-112">Provides memory statistics on Windows 7.</span></span> |

## <a name="requirements"></a><span data-ttu-id="a3910-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3910-113">Requirements</span></span>

| <span data-ttu-id="a3910-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3910-114">Requirement</span></span> | <span data-ttu-id="a3910-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a3910-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="a3910-116">Header</span><span class="sxs-lookup"><span data-stu-id="a3910-116">Header</span></span> | <span data-ttu-id="a3910-117">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="a3910-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="a3910-118">DLL</span><span class="sxs-lookup"><span data-stu-id="a3910-118">DLL</span></span>    | <span data-ttu-id="a3910-119">D3D12.dll (nur Windows 7)</span><span class="sxs-lookup"><span data-stu-id="a3910-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="a3910-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3910-120">See also</span></span>
* [<span data-ttu-id="a3910-121">Direct3D 12 auf Windows 7-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a3910-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="a3910-122">Referenz zu Direct3D 12 auf Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="a3910-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="a3910-123">Direct3D 12 unter Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3910-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
