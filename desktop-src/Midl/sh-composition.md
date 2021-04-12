---
title: sh_composition-Schlüsselwort
description: Das \ SH \_ Composition \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für eine Kompositions Oberfläche ist.
keywords:
- sh_composition-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_composition
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5a7e723c65ca6320dbec4a2f8a379cfed2f85f72
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104218918"
---
# <a name="sh_composition-keyword"></a><span data-ttu-id="4d097-104">SH \_ Composition-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="4d097-104">sh\_composition keyword</span></span>

<span data-ttu-id="4d097-105">Das Schlüsselwort **SH \_ Composition** gibt an, dass ein ein `system_handle` Handle für eine Kompositions Oberfläche enthält.</span><span class="sxs-lookup"><span data-stu-id="4d097-105">The **sh\_composition** keyword specifies that a `system_handle` holds a handle to a composition surface.</span></span>

``` syntax
[system_handle(sh_composition)]

[system_handle(sh_composition, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="4d097-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d097-106">Parameters</span></span>

<span data-ttu-id="4d097-107">Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="4d097-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="4d097-108">Die [**system_handle**](system-handle.md) Dokumentation enthält auch Details zur optionalen Verwendung des *Zugriffsrechte* Parameters.</span><span class="sxs-lookup"><span data-stu-id="4d097-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="4d097-109">Das Standardverhalten entspricht den `DUPLICATE_SAME_ACCESS` Spezifikationen für [ **Duplikat-andle** -Funktionen](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="4d097-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d097-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d097-110">Remarks</span></span>

<span data-ttu-id="4d097-111">Um dieses Schlüsselwort mit dem-Attribut zu verwenden `system_handle` , `-target` muss das-Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4d097-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="4d097-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d097-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetVisualSurface([out, system_handle(sh_composition)] HANDLE* visual);
}
```

## <a name="requirements"></a><span data-ttu-id="4d097-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d097-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="4d097-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d097-114">Minimum supported client</span></span> | <span data-ttu-id="4d097-115">Windows 10 Anniversary Update (Version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="4d097-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="4d097-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d097-116">Minimum supported server</span></span> | <span data-ttu-id="4d097-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="4d097-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="4d097-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d097-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d097-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="4d097-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="4d097-120">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="4d097-120">DirectComposition</span></span>](/windows/win32/api/_directcomp/)
</dt> <dt>

[<span data-ttu-id="4d097-121">**Dcompositionkreatesurfakehandle** -Funktion</span><span class="sxs-lookup"><span data-stu-id="4d097-121">**DCompositionCreateSurfaceHandle** function</span></span>](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> </dl>
