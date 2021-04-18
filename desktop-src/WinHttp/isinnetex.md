---
description: Bestimmt, ob sich eine IP-Adresse in einem bestimmten Subnetz befindet.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: isinnettex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: d738fbf5788fbe56d8c801b6c5256e96e8d4a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351034"
---
# <a name="isinnetex-function"></a><span data-ttu-id="1b50c-103">isinnettex-Funktion</span><span class="sxs-lookup"><span data-stu-id="1b50c-103">isInNetEx function</span></span>

<span data-ttu-id="1b50c-104">Bestimmt, ob sich eine IP-Adresse in einem bestimmten Subnetz befindet.</span><span class="sxs-lookup"><span data-stu-id="1b50c-104">Determines if an IP address is in a specific subnet.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b50c-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b50c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b50c-106">*IPAddress*</span><span class="sxs-lookup"><span data-stu-id="1b50c-106">*IPaddress*</span></span> 
</dt> <dd>

<span data-ttu-id="1b50c-107">Eine Zeichenfolge, die IPv6/IPv4-Adressen enthält.</span><span class="sxs-lookup"><span data-stu-id="1b50c-107">A string containing IPv6/IPv4 addresses.</span></span>

</dd> <dt>

<span data-ttu-id="1b50c-108">*Ipprefix*</span><span class="sxs-lookup"><span data-stu-id="1b50c-108">*IPprefix*</span></span> 
</dt> <dd>

<span data-ttu-id="1b50c-109">Eine Zeichenfolge mit einem durch Trennzeichen getrennten IP-Präfix mit oberen n Bits, die im Bitfeld angegeben sind (z. b. 3FFE: 8311: FFFF::/48 oder 123.112.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="1b50c-109">A string containing colon delimited IP prefix with top n bits specified in the bit field (i.e. 3ffe:8311:ffff::/48 or 123.112.0.0/16).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b50c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b50c-110">Return value</span></span>

<span data-ttu-id="1b50c-111">TRUE, wenn sich der Host im gleichen Subnetz befindet. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="1b50c-111">TRUE if the host is in the same subnet; otherwise, FALSE.</span></span>

<span data-ttu-id="1b50c-112">Gibt auch false zurück, wenn das Präfix nicht im richtigen Format vorliegt oder wenn Adressen und Präfixe verschiedener Typen im Vergleich verwendet werden (d.h. IPv4-Präfix und eine IPv6-Adresse).</span><span class="sxs-lookup"><span data-stu-id="1b50c-112">Also returns FALSE if the prefix is not in the correct format or if addresses and prefixes of different types are used in the comparison (i.e. IPv4 prefix and an IPv6 address).</span></span>

## <a name="examples"></a><span data-ttu-id="1b50c-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b50c-113">Examples</span></span>

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a><span data-ttu-id="1b50c-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1b50c-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b50c-115">IPv6-abhängige proxyhilfsobjekts-Definitionen</span><span class="sxs-lookup"><span data-stu-id="1b50c-115">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="1b50c-116">IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators</span><span class="sxs-lookup"><span data-stu-id="1b50c-116">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



