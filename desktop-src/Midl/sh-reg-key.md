---
title: sh_reg_key-Schlüsselwort
description: Das Schlüsselwort \ SH \_ reg \_ Key \ gibt an, dass das Systemobjekt ein Handle für einen Registrierungsschlüssel ist.
keywords:
- sh_reg_key-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: cec526bed766534f82d5a1bc24c55050dea814ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "106351185"
---
# <a name="sh_reg_key-keyword"></a><span data-ttu-id="078a5-104">SH \_ reg \_ Key-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="078a5-104">sh\_reg\_key keyword</span></span>

<span data-ttu-id="078a5-105">Das **Schlüsselwort SH \_ reg \_ Key** gibt an, dass ein ein `system_handle` Handle für einen Registrierungsschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="078a5-105">The **sh\_reg\_key** keyword specifies that a `system_handle` holds a handle to a registry key.</span></span>

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="078a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="078a5-106">Parameters</span></span>

<span data-ttu-id="078a5-107">Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="078a5-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="078a5-108">Die [**system_handle**](system-handle.md) Dokumentation enthält auch Details zur optionalen Verwendung des *Zugriffsrechte* Parameters.</span><span class="sxs-lookup"><span data-stu-id="078a5-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="078a5-109">Das Standardverhalten entspricht den `DUPLICATE_SAME_ACCESS` Spezifikationen für [ **Duplikat-andle** -Funktionen](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="078a5-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="078a5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="078a5-110">Remarks</span></span>

<span data-ttu-id="078a5-111">Um dieses Schlüsselwort mit dem-Attribut zu verwenden `system_handle` , `-target` muss das-Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="078a5-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="078a5-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="078a5-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
}
```

## <a name="requirements"></a><span data-ttu-id="078a5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="078a5-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="078a5-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="078a5-114">Minimum supported client</span></span> | <span data-ttu-id="078a5-115">Windows 10 Anniversary Update (Version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="078a5-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="078a5-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="078a5-116">Minimum supported server</span></span> | <span data-ttu-id="078a5-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="078a5-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="078a5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="078a5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="078a5-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="078a5-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="078a5-120">Registrierung</span><span class="sxs-lookup"><span data-stu-id="078a5-120">Registry</span></span>](../sysinfo/registry.md)
</dt> <dt>

[<span data-ttu-id="078a5-121">Sicherheit und Zugriffsrechte für den Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="078a5-121">Registry Key Security and Access Rights</span></span>](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="078a5-122">**RegOpenKeyEx** -Funktion</span><span class="sxs-lookup"><span data-stu-id="078a5-122">**RegOpenKeyEx** function</span></span>](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
