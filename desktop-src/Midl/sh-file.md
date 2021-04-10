---
title: sh_file-Schlüsselwort
description: Das \ SH \_ File \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für eine Datei ist.
keywords:
- sh_file-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f7d2ae0ef4a8166f90700267fa8459525ad4be2f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104350968"
---
# <a name="sh_file-keyword"></a><span data-ttu-id="745e0-104">SH \_ File-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="745e0-104">sh\_file keyword</span></span>

<span data-ttu-id="745e0-105">Das Schlüsselwort **SH \_ File** gibt an, dass ein ein `system_handle` Handle für eine Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="745e0-105">The **sh\_file** keyword specifies that a `system_handle` holds a handle to a file.</span></span>

``` syntax
[system_handle(sh_file)]

[system_handle(sh_file, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="745e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="745e0-106">Parameters</span></span>

<span data-ttu-id="745e0-107">Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="745e0-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="745e0-108">Die [**system_handle**](system-handle.md) Dokumentation enthält auch Details zur optionalen Verwendung des *Zugriffsrechte* Parameters.</span><span class="sxs-lookup"><span data-stu-id="745e0-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="745e0-109">Das Standardverhalten entspricht den `DUPLICATE_SAME_ACCESS` Spezifikationen für [ **Duplikat-andle** -Funktionen](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="745e0-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="745e0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="745e0-110">Remarks</span></span>

<span data-ttu-id="745e0-111">Um dieses Schlüsselwort mit dem-Attribut zu verwenden `system_handle` , `-target` muss das-Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="745e0-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="745e0-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="745e0-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WriteThisFile([in, system_handle(sh_file)] HANDLE file);

    HRESULT GetFileToRead([out, system_handle(sh_file, READ_CONTROL | SYNCHRONIZE | FILE_READ_DATA | FILE_READ_keywordS | FILE_READ_EA)] HANDLE* pReadThisFile);
}
```

## <a name="requirements"></a><span data-ttu-id="745e0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="745e0-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="745e0-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="745e0-114">Minimum supported client</span></span> | <span data-ttu-id="745e0-115">Windows 10 Anniversary Update (Version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="745e0-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="745e0-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="745e0-116">Minimum supported server</span></span> | <span data-ttu-id="745e0-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="745e0-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="745e0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="745e0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="745e0-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="745e0-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="745e0-120">Datei Sicherheit und Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="745e0-120">File Security and Access Rights</span></span>](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="745e0-121">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="745e0-121">DirectComposition</span></span>](/windows/win32/api/_directcomp/)
</dt> <dt>

[<span data-ttu-id="745e0-122">**Dcompositionkreatesurfakehandle** -Funktion</span><span class="sxs-lookup"><span data-stu-id="745e0-122">**DCompositionCreateSurfaceHandle** function</span></span>](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> <dt>
