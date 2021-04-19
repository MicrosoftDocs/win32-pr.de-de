---
title: ID3D12CommandQueueDownlevel-Schnittstelle
description: Stellt einen Windows-7-spezifischen, vorhandenen Mechanismus bereit.
keywords:
- ID3D12CommandQueueDownlevel-Schnittstelle
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 6f2aee6fd1b0f58469162c640d92aeb187bd9641
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370401"
---
# <a name="id3d12commandqueuedownlevel-interface"></a><span data-ttu-id="037e6-104">ID3D12CommandQueueDownlevel-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="037e6-104">ID3D12CommandQueueDownlevel interface</span></span>

<span data-ttu-id="037e6-105">Auf diese Schnittstelle kann über **QueryInterface** aus einer [Direct3D 12-Befehls Warteschlange](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) zugegriffen werden, wenn [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="037e6-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 command queue](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="037e6-106">Es stellt einen Windows-7-spezifischen Mechanismus bereit.</span><span class="sxs-lookup"><span data-stu-id="037e6-106">It provides a Windows-7-specific present mechanism.</span></span>

### <a name="methods"></a><span data-ttu-id="037e6-107">Methoden</span><span class="sxs-lookup"><span data-stu-id="037e6-107">Methods</span></span>

<span data-ttu-id="037e6-108">Die **ID3D12CommandQueueDownlevel** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="037e6-108">The **ID3D12CommandQueueDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="037e6-109">Methode</span><span class="sxs-lookup"><span data-stu-id="037e6-109">Method</span></span> | <span data-ttu-id="037e6-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="037e6-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="037e6-111">**Anzahl**</span><span class="sxs-lookup"><span data-stu-id="037e6-111">**Present**</span></span>](id3d12commandqueuedownlevel-present.md) | <span data-ttu-id="037e6-112">Kopiert Inhalt aus einer D3D12 Texture2D-Ressource in ein-Fenster.</span><span class="sxs-lookup"><span data-stu-id="037e6-112">Copies contents from a D3D12 Texture2D resource into a window.</span></span> |

## <a name="requirements"></a><span data-ttu-id="037e6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="037e6-113">Requirements</span></span>

| <span data-ttu-id="037e6-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="037e6-114">Requirement</span></span> | <span data-ttu-id="037e6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="037e6-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="037e6-116">Header</span><span class="sxs-lookup"><span data-stu-id="037e6-116">Header</span></span> | <span data-ttu-id="037e6-117">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="037e6-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="037e6-118">DLL</span><span class="sxs-lookup"><span data-stu-id="037e6-118">DLL</span></span>    | <span data-ttu-id="037e6-119">D3D12.dll (nur Windows 7)</span><span class="sxs-lookup"><span data-stu-id="037e6-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="037e6-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="037e6-120">See also</span></span>
* [<span data-ttu-id="037e6-121">Direct3D 12 auf Windows 7-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="037e6-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="037e6-122">Referenz zu Direct3D 12 auf Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="037e6-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="037e6-123">Direct3D 12 unter Windows 7</span><span class="sxs-lookup"><span data-stu-id="037e6-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
