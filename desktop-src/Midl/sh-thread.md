---
title: sh_thread-Schlüsselwort
description: Das \ SH \_ Thread \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für einen Thread ist.
keywords:
- sh_thread-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_thread keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2c82dc41d2b1c7cba740c897ef6cea9094979cc3
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104218923"
---
# <a name="sh_thread-keyword"></a><span data-ttu-id="1d6d6-104">SH \_ Thread-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="1d6d6-104">sh\_thread keyword</span></span>

<span data-ttu-id="1d6d6-105">Das Schlüsselwort **SH \_ Thread** gibt an, dass ein ein `system_handle` Handle für einen Thread enthält.</span><span class="sxs-lookup"><span data-stu-id="1d6d6-105">The **sh\_thread** keyword specifies that a `system_handle` holds a handle to a thread.</span></span>

``` syntax
[system_handle(sh_thread)]

[system_handle(sh_thread, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="1d6d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d6d6-106">Parameters</span></span>

<span data-ttu-id="1d6d6-107">Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="1d6d6-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="1d6d6-108">Die [**system_handle**](system-handle.md) Dokumentation enthält auch Details zur optionalen Verwendung des *Zugriffsrechte* Parameters.</span><span class="sxs-lookup"><span data-stu-id="1d6d6-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="1d6d6-109">Das Standardverhalten entspricht den `DUPLICATE_SAME_ACCESS` Spezifikationen für [ **Duplikat-andle** -Funktionen](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="1d6d6-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d6d6-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d6d6-110">Remarks</span></span>

<span data-ttu-id="1d6d6-111">Um dieses Schlüsselwort mit dem-Attribut zu verwenden `system_handle` , `-target` muss das-Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1d6d6-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="1d6d6-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d6d6-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetThread([in, system_handle(sh_process)] HANDLE threadHandle);
}
```

## <a name="requirements"></a><span data-ttu-id="1d6d6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d6d6-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="1d6d6-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d6d6-114">Minimum supported client</span></span> | <span data-ttu-id="1d6d6-115">Windows 10 Anniversary Update (Version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="1d6d6-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="1d6d6-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d6d6-116">Minimum supported server</span></span> | <span data-ttu-id="1d6d6-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="1d6d6-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="1d6d6-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d6d6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d6d6-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="1d6d6-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="1d6d6-120">About Processes and Threads (Informationen zu Prozessen und Threads)</span><span class="sxs-lookup"><span data-stu-id="1d6d6-120">About Processes and Threads</span></span>](../procthread/about-processes-and-threads.md)
</dt> <dt>

[<span data-ttu-id="1d6d6-121">Thread Sicherheit und Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="1d6d6-121">Thread Security and Access Rights</span></span>](../procthread/thread-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="1d6d6-122">Funktion " **foratethread** "</span><span class="sxs-lookup"><span data-stu-id="1d6d6-122">**CreateThread** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)
</dt> <dt>

[<span data-ttu-id="1d6d6-123">**Openthread** -Funktion</span><span class="sxs-lookup"><span data-stu-id="1d6d6-123">**OpenThread** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)
</dt> </dl>