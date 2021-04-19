---
title: sh_mutex-Schlüsselwort
description: Das \ SH \_ Mutex \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für einen Mutex ist.
keywords:
- sh_mutex-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8616ded29d1d8c106af21e6cd1252535f4da8457
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363052"
---
# <a name="sh_mutex-keyword"></a><span data-ttu-id="e0834-104">SH \_ Mutex-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="e0834-104">sh\_mutex keyword</span></span>

<span data-ttu-id="e0834-105">Das **SH \_ Mutex** -Schlüsselwort gibt an, dass ein ein `system_handle` Handle für einen Mutex enthält.</span><span class="sxs-lookup"><span data-stu-id="e0834-105">The **sh\_mutex** keyword specifies that a `system_handle` holds a handle to a mutex.</span></span>

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="e0834-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0834-106">Parameters</span></span>

<span data-ttu-id="e0834-107">Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="e0834-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="e0834-108">Die [**system_handle**](system-handle.md) Dokumentation enthält auch Details zur optionalen Verwendung des *Zugriffsrechte* Parameters.</span><span class="sxs-lookup"><span data-stu-id="e0834-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="e0834-109">Das Standardverhalten entspricht den `DUPLICATE_SAME_ACCESS` Spezifikationen für [ **Duplikat-andle** -Funktionen](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="e0834-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0834-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0834-110">Remarks</span></span>

<span data-ttu-id="e0834-111">Um dieses Schlüsselwort mit dem-Attribut zu verwenden `system_handle` , `-target` muss das-Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e0834-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="e0834-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0834-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
}
```

## <a name="requirements"></a><span data-ttu-id="e0834-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0834-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="e0834-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0834-114">Minimum supported client</span></span> | <span data-ttu-id="e0834-115">Windows 10 Anniversary Update (Version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="e0834-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="e0834-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0834-116">Minimum supported server</span></span> | <span data-ttu-id="e0834-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="e0834-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e0834-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0834-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0834-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="e0834-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="e0834-120">Mutex-Objekte</span><span class="sxs-lookup"><span data-stu-id="e0834-120">Mutex Objects</span></span>](../sync/mutex-objects.md)
</dt> <dt>

[<span data-ttu-id="e0834-121">Sicherheits-und Zugriffsrechte für das Synchronisierungs Objekt</span><span class="sxs-lookup"><span data-stu-id="e0834-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="e0834-122">Funktion " **kreatemutex** "</span><span class="sxs-lookup"><span data-stu-id="e0834-122">**CreateMutex** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[<span data-ttu-id="e0834-123">Funktion "up- **MUTEXEX** "</span><span class="sxs-lookup"><span data-stu-id="e0834-123">**CreateMutexEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>