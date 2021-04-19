---
title: sh_pipe-Schlüsselwort
description: Das Schlüsselwort "\ SH \_ Pipe \" gibt an, dass das Systemobjekt ein Handle für eine Pipe ist.
keywords:
- sh_pipe-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_pipe
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 9f9deab2bf5a751d3b2d5956d4d33a1d5b347e18
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "106369918"
---
# <a name="sh_pipe-keyword"></a><span data-ttu-id="436be-104">SH \_ Pipe-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="436be-104">sh\_pipe keyword</span></span>

<span data-ttu-id="436be-105">Das **SH \_ Pipe** -Schlüsselwort gibt an, dass ein ein `system_handle` Handle für eine Pipe enthält.</span><span class="sxs-lookup"><span data-stu-id="436be-105">The **sh\_pipe** keyword specifies that a `system_handle` holds a handle to a pipe.</span></span>

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="436be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="436be-106">Parameters</span></span>

<span data-ttu-id="436be-107">Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="436be-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="436be-108">Die [**system_handle**](system-handle.md) Dokumentation enthält auch Details zur optionalen Verwendung des *Zugriffsrechte* Parameters.</span><span class="sxs-lookup"><span data-stu-id="436be-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="436be-109">Das Standardverhalten entspricht den `DUPLICATE_SAME_ACCESS` Spezifikationen für [ **Duplikat-andle** -Funktionen](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="436be-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="436be-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="436be-110">Remarks</span></span>

<span data-ttu-id="436be-111">Um dieses Schlüsselwort mit dem-Attribut zu verwenden `system_handle` , `-target` muss das-Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="436be-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="436be-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="436be-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
}
```

## <a name="requirements"></a><span data-ttu-id="436be-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="436be-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="436be-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="436be-114">Minimum supported client</span></span> | <span data-ttu-id="436be-115">Windows 10 Anniversary Update (Version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="436be-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="436be-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="436be-116">Minimum supported server</span></span> | <span data-ttu-id="436be-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="436be-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="436be-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="436be-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="436be-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="436be-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="436be-120">Informationen zu Pipes</span><span class="sxs-lookup"><span data-stu-id="436be-120">About Pipes</span></span>](../ipc/about-pipes.md)
</dt> <dt>

[<span data-ttu-id="436be-121">Datei Sicherheit und Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="436be-121">File Security and Access Rights</span></span>](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="436be-122">Funktion "| **atepipe** "</span><span class="sxs-lookup"><span data-stu-id="436be-122">**CreatePipe** function</span></span>](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[<span data-ttu-id="436be-123">" **Kreatenamedpipe** "-Funktion</span><span class="sxs-lookup"><span data-stu-id="436be-123">**CreateNamedPipe** function</span></span>](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
