---
title: sh_section-Schlüsselwort
description: Der \ SH \_ section \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für einen Abschnitt ist.
keywords:
- sh_section-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_section keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 056112deb790e727206a5ac1a1a2a5043a68f5e1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "106365210"
---
# <a name="sh_section-keyword"></a><span data-ttu-id="fa62d-104">SH \_ section-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="fa62d-104">sh\_section keyword</span></span>

<span data-ttu-id="fa62d-105">Das **SH \_ section** -Schlüsselwort gibt an, dass ein ein `system_handle` Handle für einen Abschnitt enthält.</span><span class="sxs-lookup"><span data-stu-id="fa62d-105">The **sh\_section** keyword specifies that a `system_handle` holds a handle to a section.</span></span>

``` syntax
[system_handle(sh_section)]

[system_handle(sh_section, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="fa62d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa62d-106">Parameters</span></span>

<span data-ttu-id="fa62d-107">Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="fa62d-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="fa62d-108">Die [**system_handle**](system-handle.md) Dokumentation enthält auch Details zur optionalen Verwendung des *Zugriffsrechte* Parameters.</span><span class="sxs-lookup"><span data-stu-id="fa62d-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="fa62d-109">Das Standardverhalten entspricht den `DUPLICATE_SAME_ACCESS` Spezifikationen für [ **Duplikat-andle** -Funktionen](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="fa62d-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa62d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa62d-110">Remarks</span></span>

<span data-ttu-id="fa62d-111">Um dieses Schlüsselwort mit dem-Attribut zu verwenden `system_handle` , `-target` muss das-Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fa62d-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="fa62d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa62d-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GiveSection([in, system_handle(sh_section)] HANDLE section);

    HRESULT GetSectionToWatch([out, system_handle(sh_section, SECTION_MAP_READ)] HANDLE* pSection);
}
```

## <a name="requirements"></a><span data-ttu-id="fa62d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa62d-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="fa62d-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa62d-114">Minimum supported client</span></span> | <span data-ttu-id="fa62d-115">Windows 10 Anniversary Update (Version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="fa62d-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="fa62d-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa62d-116">Minimum supported server</span></span> | <span data-ttu-id="fa62d-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="fa62d-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="fa62d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa62d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa62d-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="fa62d-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="fa62d-120">Abschnitts Objekte und-Sichten</span><span class="sxs-lookup"><span data-stu-id="fa62d-120">Section Objects and Views</span></span>](/windows-hardware/drivers/kernel/section-objects-and-views)
</dt> <dt>

[<span data-ttu-id="fa62d-121">**Zwkreatesection** -Funktion (einschließlich Zugriffs Spezifikationen)</span><span class="sxs-lookup"><span data-stu-id="fa62d-121">**ZwCreateSection** function (including access specifications)</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-zwcreatesection)
</dt> </dl>
