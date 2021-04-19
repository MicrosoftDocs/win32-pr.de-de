---
title: sh_process-Schlüsselwort
description: Das \ SH \_ Process \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für einen Prozess ist.
keywords:
- sh_process-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3652c6889c687173bbf7b397cddff4659c0329f1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "106362804"
---
# <a name="sh_process-keyword"></a><span data-ttu-id="3f801-104">SH \_ Process-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="3f801-104">sh\_process keyword</span></span>

<span data-ttu-id="3f801-105">Das **SH \_ Process** -Schlüsselwort gibt an, dass ein ein `system_handle` Handle für einen Prozess enthält.</span><span class="sxs-lookup"><span data-stu-id="3f801-105">The **sh\_process** keyword specifies that a `system_handle` holds a handle to a process.</span></span>

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="3f801-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f801-106">Parameters</span></span>

<span data-ttu-id="3f801-107">Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="3f801-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="3f801-108">Die [**system_handle**](system-handle.md) Dokumentation enthält auch Details zur optionalen Verwendung des *Zugriffsrechte* Parameters.</span><span class="sxs-lookup"><span data-stu-id="3f801-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="3f801-109">Das Standardverhalten entspricht den `DUPLICATE_SAME_ACCESS` Spezifikationen für [ **Duplikat-andle** -Funktionen](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="3f801-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f801-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f801-110">Remarks</span></span>

<span data-ttu-id="3f801-111">Um dieses Schlüsselwort mit dem-Attribut zu verwenden `system_handle` , `-target` muss das-Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3f801-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="3f801-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f801-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetStubProcess([out, system_handle(sh_process)] HANDLE* processHandle);

    HRESULT WatchProcess([in, system_handle(sh_process, PROCESS_QUERY_INFORMATION | PROCESS_QUERY_LIMITED_INFORMATION)] HANDLE processHandle);
}
```

## <a name="requirements"></a><span data-ttu-id="3f801-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f801-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="3f801-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f801-114">Minimum supported client</span></span> | <span data-ttu-id="3f801-115">Windows 10 Anniversary Update (Version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="3f801-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="3f801-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f801-116">Minimum supported server</span></span> | <span data-ttu-id="3f801-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="3f801-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="3f801-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f801-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f801-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="3f801-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="3f801-120">About Processes and Threads (Informationen zu Prozessen und Threads)</span><span class="sxs-lookup"><span data-stu-id="3f801-120">About Processes and Threads</span></span>](../procthread/about-processes-and-threads.md)
</dt> <dt>

[<span data-ttu-id="3f801-121">Prozesssicherheit und Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="3f801-121">Process Security and Access Rights</span></span>](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="3f801-122">Funktion " **deateprocess** "</span><span class="sxs-lookup"><span data-stu-id="3f801-122">**CreateProcess** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[<span data-ttu-id="3f801-123">**OpenProcess** -Funktion</span><span class="sxs-lookup"><span data-stu-id="3f801-123">**OpenProcess** function</span></span>](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>