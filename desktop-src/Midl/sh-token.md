---
title: sh_token-Schlüsselwort
description: Das \ SH \_ Token \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für ein Token ist.
keywords:
- sh_token-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_token keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a33b070af5cd43a095fd6ad45a0dee86f1868171
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "106363871"
---
# <a name="sh_token-keyword"></a><span data-ttu-id="aefe8-104">SH \_ Token-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="aefe8-104">sh\_token keyword</span></span>

<span data-ttu-id="aefe8-105">Das **SH \_ Token** -Schlüsselwort gibt an, dass ein ein `system_handle` Handle für ein Token enthält.</span><span class="sxs-lookup"><span data-stu-id="aefe8-105">The **sh\_token** keyword specifies that a `system_handle` holds a handle to a token.</span></span>

``` syntax
[system_handle(sh_token)]

[system_handle(sh_token, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="aefe8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aefe8-106">Parameters</span></span>

<span data-ttu-id="aefe8-107">Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="aefe8-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="aefe8-108">Die [**system_handle**](system-handle.md) Dokumentation enthält auch Details zur optionalen Verwendung des *Zugriffsrechte* Parameters.</span><span class="sxs-lookup"><span data-stu-id="aefe8-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="aefe8-109">Das Standardverhalten entspricht den `DUPLICATE_SAME_ACCESS` Spezifikationen für [ **Duplikat-andle** -Funktionen](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="aefe8-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="aefe8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aefe8-110">Remarks</span></span>

<span data-ttu-id="aefe8-111">Um dieses Schlüsselwort mit dem-Attribut zu verwenden `system_handle` , `-target` muss das-Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aefe8-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="aefe8-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aefe8-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetToken([in, system_handle(sh_token)] HANDLE token);

    HRESULT GetToken([out, system_handle(sh_token, TOKEN_QUERY)] HANDLE* pToken);
}
```

## <a name="requirements"></a><span data-ttu-id="aefe8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aefe8-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="aefe8-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aefe8-114">Minimum supported client</span></span> | <span data-ttu-id="aefe8-115">Windows 10 Anniversary Update (Version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="aefe8-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="aefe8-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aefe8-116">Minimum supported server</span></span> | <span data-ttu-id="aefe8-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="aefe8-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="aefe8-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aefe8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aefe8-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="aefe8-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="aefe8-120">Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="aefe8-120">Access Tokens</span></span>](../secauthz/access-tokens.md)
</dt> <dt>

[<span data-ttu-id="aefe8-121">Zugriffsrechte für Access-Token Objekte</span><span class="sxs-lookup"><span data-stu-id="aefe8-121">Access Rights for Access-Token Objects</span></span>](../secauthz/access-rights-for-access-token-objects.md)
</dt> </dl>
