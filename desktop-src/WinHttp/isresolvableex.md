---
description: Bestimmt, ob eine angegebene Host Zeichenfolge in eine IP-Adresse aufgelöst werden kann.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: isresolvableex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isResolvableEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1172aaed93a9fc6cede5ae5393c5dd430613a466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355342"
---
# <a name="isresolvableex-function"></a><span data-ttu-id="c436c-103">isresolvableex-Funktion</span><span class="sxs-lookup"><span data-stu-id="c436c-103">isResolvableEx function</span></span>

<span data-ttu-id="c436c-104">Bestimmt, ob eine angegebene Host Zeichenfolge in eine IP-Adresse aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="c436c-104">Determines if a given host string can resolve to an IP address.</span></span>

## <a name="parameters"></a><span data-ttu-id="c436c-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="c436c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c436c-106">*host*</span><span class="sxs-lookup"><span data-stu-id="c436c-106">*host*</span></span> 
</dt> <dd>

<span data-ttu-id="c436c-107">Eine Zeichenfolge, die den HTTP-Host enthält, der für FindProxyForURL bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c436c-107">A string containing the HTTP host that is supplied to FindProxyForUrl.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c436c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c436c-108">Return value</span></span>

<span data-ttu-id="c436c-109">TRUE, wenn der Host in eine IPv4-oder IPv6-Adresse aufgelöst werden kann. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="c436c-109">TRUE if the host is resolvable to a IPv4 or IPv6 address; otherwise, FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="c436c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c436c-110">Examples</span></span>

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a><span data-ttu-id="c436c-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c436c-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c436c-112">IPv6-abhängige proxyhilfsobjekts-Definitionen</span><span class="sxs-lookup"><span data-stu-id="c436c-112">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="c436c-113">IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators</span><span class="sxs-lookup"><span data-stu-id="c436c-113">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



