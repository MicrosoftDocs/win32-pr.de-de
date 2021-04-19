---
title: sh_event-Schlüsselwort
description: Das \ SH \_ Event \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für ein Ereignis ist.
keywords:
- sh_event-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1a9b6dc7cc9dc4de4abd5dcc88a53588167db59d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "106367259"
---
# <a name="sh_event-keyword"></a><span data-ttu-id="2705b-104">SH \_ Event-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="2705b-104">sh\_event keyword</span></span>

<span data-ttu-id="2705b-105">Das **SH- \_ Ereignis** Schlüsselwort gibt an, dass ein `system_handle` ein Handle für ein Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="2705b-105">The **sh\_event** keyword specifies that a `system_handle` holds a handle to an event.</span></span>

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="2705b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2705b-106">Parameters</span></span>

<span data-ttu-id="2705b-107">Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="2705b-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="2705b-108">Die [**system_handle**](system-handle.md) Dokumentation enthält auch Details zur optionalen Verwendung des *Zugriffsrechte* Parameters.</span><span class="sxs-lookup"><span data-stu-id="2705b-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="2705b-109">Das Standardverhalten entspricht den `DUPLICATE_SAME_ACCESS` Spezifikationen für [ **Duplikat-andle** -Funktionen](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="2705b-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="2705b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2705b-110">Remarks</span></span>

<span data-ttu-id="2705b-111">Um dieses Schlüsselwort mit dem-Attribut zu verwenden `system_handle` , `-target` muss das-Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2705b-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="2705b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2705b-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
}
```

## <a name="requirements"></a><span data-ttu-id="2705b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2705b-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="2705b-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2705b-114">Minimum supported client</span></span> | <span data-ttu-id="2705b-115">Windows 10 Anniversary Update (Version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="2705b-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="2705b-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2705b-116">Minimum supported server</span></span> | <span data-ttu-id="2705b-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="2705b-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="2705b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2705b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2705b-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="2705b-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="2705b-120">Ereignis Objekte</span><span class="sxs-lookup"><span data-stu-id="2705b-120">Event Objects</span></span>](../sync/event-objects.md)
</dt> <dt>

[<span data-ttu-id="2705b-121">Sicherheits-und Zugriffsrechte für das Synchronisierungs Objekt</span><span class="sxs-lookup"><span data-stu-id="2705b-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="2705b-122">Funktion " **kreateevent** "</span><span class="sxs-lookup"><span data-stu-id="2705b-122">**CreateEvent** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="2705b-123">Funktion " **kreateeventex** "</span><span class="sxs-lookup"><span data-stu-id="2705b-123">**CreateEventEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
