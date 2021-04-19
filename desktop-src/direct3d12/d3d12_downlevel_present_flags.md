---
title: D3D12_DOWNLEVEL_PRESENT_FLAGS-Enumeration
description: Flags, die an die ID3D12CommandQueueDownlevel::P Resent-Methode weitergegeben werden.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363959"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a><span data-ttu-id="94f01-103">D3D12 \_ Downlevel \_ Present- \_ Flags-Enumeration</span><span class="sxs-lookup"><span data-stu-id="94f01-103">D3D12\_DOWNLEVEL\_PRESENT\_FLAGS enumeration</span></span>

<span data-ttu-id="94f01-104">An die [**ID3D12CommandQueueDownlevel::P Resent**](id3d12commandqueuedownlevel-present.md) -Funktion übergebenen Flags, um das Verhalten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="94f01-104">Flags passed to the [**ID3D12CommandQueueDownlevel::Present**](id3d12commandqueuedownlevel-present.md) function to modify behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="94f01-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="94f01-105">Syntax</span></span>

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a><span data-ttu-id="94f01-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="94f01-106">Constants</span></span>

<span data-ttu-id="94f01-107">**D3D12 \_ Downlevel \_ Present- \_ Flag " \_ None"**</span><span class="sxs-lookup"><span data-stu-id="94f01-107">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_NONE**</span></span>

<span data-ttu-id="94f01-108">Es sind keine Optionen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="94f01-108">No options selected.</span></span>

<span data-ttu-id="94f01-109">**D3D12 \_ Downlevel \_ Present- \_ Flag \_ warten \_ auf \_ vblank**</span><span class="sxs-lookup"><span data-stu-id="94f01-109">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_WAIT\_FOR\_VBLANK**</span></span>

<span data-ttu-id="94f01-110">Der **aktuelle** Vorgang wird erst ausgeführt, wenn eine VSYNC seit dem letzten Mal ausgeführt wurde .</span><span class="sxs-lookup"><span data-stu-id="94f01-110">The **Present** operation won't be done until a VSync has occurred since the last time you **Present** ed.</span></span>

## <a name="requirements"></a><span data-ttu-id="94f01-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94f01-111">Requirements</span></span>

| <span data-ttu-id="94f01-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94f01-112">Requirement</span></span> | <span data-ttu-id="94f01-113">Wert</span><span class="sxs-lookup"><span data-stu-id="94f01-113">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="94f01-114">Header</span><span class="sxs-lookup"><span data-stu-id="94f01-114">Header</span></span> | <span data-ttu-id="94f01-115">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="94f01-115">d3d12downlevel.h</span></span> |
| <span data-ttu-id="94f01-116">DLL</span><span class="sxs-lookup"><span data-stu-id="94f01-116">DLL</span></span>    | <span data-ttu-id="94f01-117">D3D12.dll (nur Windows 7)</span><span class="sxs-lookup"><span data-stu-id="94f01-117">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="94f01-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94f01-118">See also</span></span>
* [<span data-ttu-id="94f01-119">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="94f01-119">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="94f01-120">Direct3D 12 auf Windows 7-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="94f01-120">Direct3D 12 On Windows 7 enumerations</span></span>](direct3d-12on7-enumerations.md)
* [<span data-ttu-id="94f01-121">Referenz zu Direct3D 12 auf Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="94f01-121">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="94f01-122">Direct3D 12 unter Windows 7</span><span class="sxs-lookup"><span data-stu-id="94f01-122">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
