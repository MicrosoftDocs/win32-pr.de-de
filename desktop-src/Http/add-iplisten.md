---
title: add iplisten
description: Gibt eine IPv4-oder IPv6-Adresse an, die der IP-Abhörliste hinzugefügt werden soll.
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- Hinzufügen von iplauschen http
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6090d3044be134035edb5f1f42a9790859d0301d
ms.sourcegitcommit: 243954e695c6ab5372b2935b095c3cd0b1202e16
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "103948485"
---
# <a name="add-iplisten"></a><span data-ttu-id="2071f-104">add iplisten</span><span class="sxs-lookup"><span data-stu-id="2071f-104">add iplisten</span></span>

<span data-ttu-id="2071f-105">Gibt eine IPv4-oder IPv6-Adresse an, die der IP-Abhörliste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2071f-105">Specifies an IPv4 or IPv6 address to be added to the IP listen list.</span></span>

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="2071f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2071f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2071f-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ IPAddress = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="2071f-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ ipaddress=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="2071f-108">Gibt die IPv4-oder IPv6-Adresse an, die der IP-Abhörliste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2071f-108">Specifies the IPv4 or IPv6 address to be added to the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2071f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2071f-109">Remarks</span></span>

<span data-ttu-id="2071f-110">Fügt der IP-Abhörliste eine neue IP-Adresse hinzu.</span><span class="sxs-lookup"><span data-stu-id="2071f-110">Adds a new IP address to the IP listen list.</span></span> <span data-ttu-id="2071f-111">Dies schließt nicht die Portnummer ein.</span><span class="sxs-lookup"><span data-stu-id="2071f-111">This does not include the port number.</span></span> <span data-ttu-id="2071f-112">Die IP-Abhörliste wird verwendet, um die Liste der Adressen zu erweitern, an die der HTTP-Dienst gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="2071f-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="2071f-113">„0.0.0.0“ bedeutet eine beliebige IPv4-Adresse und „::“ bedeutet eine beliebige IPv6-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2071f-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="2071f-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2071f-114">Examples</span></span>

<span data-ttu-id="2071f-115">**add iplisten ipaddress=fe80::1**</span><span class="sxs-lookup"><span data-stu-id="2071f-115">**add iplisten ipaddress=fe80::1**</span></span>

<span data-ttu-id="2071f-116">**add iplisten ipaddress=1.1.1.1**</span><span class="sxs-lookup"><span data-stu-id="2071f-116">**add iplisten ipaddress=1.1.1.1**</span></span>

<span data-ttu-id="2071f-117">**add iplisten ipaddress=0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="2071f-117">**add iplisten ipaddress=0.0.0.0**</span></span>

<span data-ttu-id="2071f-118">**add iplisten ipaddress=::**</span><span class="sxs-lookup"><span data-stu-id="2071f-118">**add iplisten ipaddress=::**</span></span>

 

 




