---
description: Sortiert eine Liste von IP-Adressen.
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: menpaddresslist-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 600d87a58248aafdef5b0a8a7f284f4094c95780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343632"
---
# <a name="sortipaddresslist-function"></a><span data-ttu-id="4995c-103">menpaddresslist-Funktion</span><span class="sxs-lookup"><span data-stu-id="4995c-103">sortIpAddressList function</span></span>

<span data-ttu-id="4995c-104">Sortiert eine Liste von IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="4995c-104">Sorts a list of IP addresses.</span></span>

## <a name="parameters"></a><span data-ttu-id="4995c-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="4995c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4995c-106">*Ipaddresslist*</span><span class="sxs-lookup"><span data-stu-id="4995c-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="4995c-107">Eine durch Semikolons getrennte Zeichenfolge, die IP-Adressen enthält.</span><span class="sxs-lookup"><span data-stu-id="4995c-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4995c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4995c-108">Return value</span></span>

<span data-ttu-id="4995c-109">Eine Liste von durch Trennzeichen getrennten, durch Semikola getrennten IP-Adressen oder eine leere Zeichenfolge, wenn die IP-Adressliste nicht sortiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4995c-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="4995c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4995c-110">Remarks</span></span>

<span data-ttu-id="4995c-111">Findproxyforurlex-Implementierer sollten Code hinzufügen, der die Zeichenfolge von durch Semikola getrennten IP-Adressen in separate Adressen unterbricht.</span><span class="sxs-lookup"><span data-stu-id="4995c-111">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="4995c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4995c-112">Examples</span></span>

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a><span data-ttu-id="4995c-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4995c-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4995c-114">IPv6-abhängige proxyhilfsobjekts-Definitionen</span><span class="sxs-lookup"><span data-stu-id="4995c-114">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="4995c-115">IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators</span><span class="sxs-lookup"><span data-stu-id="4995c-115">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



