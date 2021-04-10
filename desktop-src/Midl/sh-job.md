---
title: sh_job-Schlüsselwort
description: Das \ SH \_ Job \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für einen Auftrag ist.
keywords:
- sh_job-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_job
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: db24f9dc84f2bb56f57327090485b406ad1a437f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "103961061"
---
# <a name="sh_job-keyword"></a><span data-ttu-id="efd6c-104">SH \_ Job-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="efd6c-104">sh\_job keyword</span></span>

<span data-ttu-id="efd6c-105">Das Schlüsselwort **SH \_ Job** gibt an, dass ein ein `system_handle` Handle für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="efd6c-105">The **sh\_job** keyword specifies that a `system_handle` holds a handle to a job.</span></span>

``` syntax
[system_handle(sh_job)]

[system_handle(sh_job, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="efd6c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="efd6c-106">Parameters</span></span>

<span data-ttu-id="efd6c-107">Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="efd6c-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="efd6c-108">Die [**system_handle**](system-handle.md) Dokumentation enthält auch Details zur optionalen Verwendung des *Zugriffsrechte* Parameters.</span><span class="sxs-lookup"><span data-stu-id="efd6c-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="efd6c-109">Das Standardverhalten entspricht den `DUPLICATE_SAME_ACCESS` Spezifikationen für [ **Duplikat-andle** -Funktionen](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="efd6c-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="efd6c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="efd6c-110">Remarks</span></span>

<span data-ttu-id="efd6c-111">Um dieses Schlüsselwort mit dem-Attribut zu verwenden `system_handle` , `-target` muss das-Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="efd6c-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="efd6c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="efd6c-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetJob([in, system_handle(sh_job)] HANDLE job);

    HRESULT GetJobForAccounting([out, system_handle(sh_job, JOB_OBJECT_QUERY)] HANDLE* pJob);
}
```

## <a name="requirements"></a><span data-ttu-id="efd6c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efd6c-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="efd6c-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="efd6c-114">Minimum supported client</span></span> | <span data-ttu-id="efd6c-115">Windows 10 Anniversary Update (Version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="efd6c-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="efd6c-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="efd6c-116">Minimum supported server</span></span> | <span data-ttu-id="efd6c-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="efd6c-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="efd6c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efd6c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efd6c-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="efd6c-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="efd6c-120">Auftrags Objekte</span><span class="sxs-lookup"><span data-stu-id="efd6c-120">Job Objects</span></span>](../procthread/job-objects.md)
</dt> <dt>

[<span data-ttu-id="efd6c-121">Sicherheit und Zugriffsrechte für das Auftrags Objekt</span><span class="sxs-lookup"><span data-stu-id="efd6c-121">Job Object Security and Access Rights</span></span>](../procthread/job-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="efd6c-122">Funktion " **kreatejobobject** "</span><span class="sxs-lookup"><span data-stu-id="efd6c-122">**CreateJobObject** function</span></span>](/windows/win32/api/winbase/nf-winbase-createjobobjecta)
</dt> </dl>
