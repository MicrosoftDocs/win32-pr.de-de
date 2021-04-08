---
title: delete iplisten
description: Gibt eine IPv4-oder IPv6-Adresse an, die aus der IP-Abhörliste gelöscht werden soll.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- Löschen von iplauschen http
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed7356d8dea3b4313a46c7d7906de15b7389edc
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104038217"
---
# <a name="delete-iplisten"></a><span data-ttu-id="10a5e-104">delete iplisten</span><span class="sxs-lookup"><span data-stu-id="10a5e-104">delete iplisten</span></span>

<span data-ttu-id="10a5e-105">Gibt eine IPv4-oder IPv6-Adresse an, die aus der IP-Abhörliste gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="10a5e-105">Specifies an IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="10a5e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10a5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10a5e-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ Address = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="10a5e-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[address=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="10a5e-108">Gibt die IPv4-oder IPv6-Adresse an, die aus der IP-Abhörliste gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="10a5e-108">Specifies the IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10a5e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10a5e-109">Remarks</span></span>

<span data-ttu-id="10a5e-110">Löscht eine IP-Adresse in der IP-Abhörliste.</span><span class="sxs-lookup"><span data-stu-id="10a5e-110">Deletes an IP address to the IP listen list.</span></span> <span data-ttu-id="10a5e-111">Dies schließt nicht die Portnummer ein.</span><span class="sxs-lookup"><span data-stu-id="10a5e-111">This does not include the port number.</span></span> <span data-ttu-id="10a5e-112">Die IP-Abhörliste wird verwendet, um die Liste der Adressen zu erweitern, an die der HTTP-Dienst gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="10a5e-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="10a5e-113">„0.0.0.0“ bedeutet eine beliebige IPv4-Adresse und „::“ bedeutet eine beliebige IPv6-Adresse.</span><span class="sxs-lookup"><span data-stu-id="10a5e-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="10a5e-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10a5e-114">Examples</span></span>

<span data-ttu-id="10a5e-115">**IP-Adresse löschen = FE80:: 1**</span><span class="sxs-lookup"><span data-stu-id="10a5e-115">**delete iplisten address=fe80::1**</span></span>

<span data-ttu-id="10a5e-116">**Löschen der ipabhör Adresse = 1.1.1.1**</span><span class="sxs-lookup"><span data-stu-id="10a5e-116">**delete iplisten address=1.1.1.1**</span></span>

<span data-ttu-id="10a5e-117">**Löschen der ipabhör Adresse = 0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="10a5e-117">**delete iplisten address=0.0.0.0**</span></span>

<span data-ttu-id="10a5e-118">**Löschen Sie die IP-Abhör Adresse =::**</span><span class="sxs-lookup"><span data-stu-id="10a5e-118">**delete iplisten address=::**</span></span>

 

 




