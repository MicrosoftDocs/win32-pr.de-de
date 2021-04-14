---
title: D3DPERF_EndEvent-Funktion
description: Markiert das Ende eines benutzerdefinierten Ereignisses. Pix kann dieses Ereignis verwenden, um eine Aktion zu initiieren.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "104390006"
---
# <a name="d3dperf_endevent-function"></a><span data-ttu-id="3045b-104">D3DPERF_EndEvent-Funktion</span><span class="sxs-lookup"><span data-stu-id="3045b-104">D3DPERF_EndEvent function</span></span>

<span data-ttu-id="3045b-105">Markiert das Ende eines benutzerdefinierten Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="3045b-105">Marks the end of a user-defined event.</span></span> <span data-ttu-id="3045b-106">Pix kann dieses Ereignis verwenden, um eine Aktion zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="3045b-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="3045b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3045b-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a><span data-ttu-id="3045b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3045b-108">Return value</span></span>

<span data-ttu-id="3045b-109">Die Ebene der Hierarchie, in der das Ereignis endet.</span><span class="sxs-lookup"><span data-stu-id="3045b-109">The level of the hierarchy in which the event is ending.</span></span> <span data-ttu-id="3045b-110">Wenn ein Fehler auftritt, ist dieser Wert negativ.</span><span class="sxs-lookup"><span data-stu-id="3045b-110">If an error occurs, this value is negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="3045b-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3045b-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3045b-112">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="3045b-112">**Target Platform**</span></span> | <span data-ttu-id="3045b-113">Windows</span><span class="sxs-lookup"><span data-stu-id="3045b-113">Windows</span></span> |
| <span data-ttu-id="3045b-114">**Header**</span><span class="sxs-lookup"><span data-stu-id="3045b-114">**Header**</span></span> | <span data-ttu-id="3045b-115">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="3045b-115">d3d9.h</span></span> |
| <span data-ttu-id="3045b-116">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="3045b-116">**Library**</span></span> | <span data-ttu-id="3045b-117">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="3045b-117">d3d9.lib</span></span> |
| <span data-ttu-id="3045b-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="3045b-118">**DLL**</span></span> | <span data-ttu-id="3045b-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="3045b-119">d3d9.dll</span></span> |