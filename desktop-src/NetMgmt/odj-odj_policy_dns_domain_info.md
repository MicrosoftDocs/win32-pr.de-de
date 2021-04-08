---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: ODJ_POLICY_DNS_DOMAIN_INFO IDL-Definition
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 36b7759451811844a91b3ee66ff3460fa4c4db34
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "103734689"
---
# <a name="odj_policy_dns_domain_info-structure"></a><span data-ttu-id="dc581-103">ODJ_POLICY_DNS_DOMAIN_INFO Struktur</span><span class="sxs-lookup"><span data-stu-id="dc581-103">ODJ_POLICY_DNS_DOMAIN_INFO structure</span></span>

<span data-ttu-id="dc581-104">Enthält Informationen über die Domäne und die Gesamtstruktur, mit denen ein Client verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc581-104">Contains information about the domain and forest that a client should be joined to.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc581-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc581-105">Syntax</span></span>

```C++
typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
{
    ODJ_UNICODE_STRING Name;
    ODJ_UNICODE_STRING DnsDomainName;
    ODJ_UNICODE_STRING DnsForestName;
    GUID DomainGuid;
    PODJ_SID Sid;
} ODJ_POLICY_DNS_DOMAIN_INFO;
```

## <a name="members"></a><span data-ttu-id="dc581-106">Member</span><span class="sxs-lookup"><span data-stu-id="dc581-106">Members</span></span>

### <a name="name"></a><span data-ttu-id="dc581-107">name</span><span class="sxs-lookup"><span data-stu-id="dc581-107">Name</span></span>

<span data-ttu-id="dc581-108">Muss auf einen NetBIOS-Domänen Namen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc581-108">Must be set to a Netbios domain name.</span></span>

### <a name="dnsdomainname"></a><span data-ttu-id="dc581-109">DnsDomainName</span><span class="sxs-lookup"><span data-stu-id="dc581-109">DnsDomainName</span></span>

<span data-ttu-id="dc581-110">Muss auf einen Domänen Namen im DNS-Format festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc581-110">Must be set to a domain name in DNS format.</span></span>

### <a name="dnsforestname"></a><span data-ttu-id="dc581-111">DnsForestName</span><span class="sxs-lookup"><span data-stu-id="dc581-111">DnsForestName</span></span>

<span data-ttu-id="dc581-112">Muss im DNS-Format auf einen Gesamtstruktur Namen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc581-112">Must be set to a forest name in DNS format.</span></span>

### <a name="domainguid"></a><span data-ttu-id="dc581-113">Domainguid</span><span class="sxs-lookup"><span data-stu-id="dc581-113">DomainGuid</span></span>

<span data-ttu-id="dc581-114">Muss auf die Domänen-GUID festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc581-114">Must be set to the domain guid.</span></span>

### <a name="sid"></a><span data-ttu-id="dc581-115">Sid</span><span class="sxs-lookup"><span data-stu-id="dc581-115">Sid</span></span>

<span data-ttu-id="dc581-116">Muss auf die Domänen-SID festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc581-116">Must be set to the domain sid.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc581-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc581-117">See also</span></span>

[<span data-ttu-id="dc581-118">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="dc581-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="dc581-119">**ODJ- \_ Unicode- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc581-119">**ODJ\_UNICODE\_STRING**</span></span>](odj-odj_unicode_string.md)

[<span data-ttu-id="dc581-120">**ODJ- \_ sid**</span><span class="sxs-lookup"><span data-stu-id="dc581-120">**ODJ\_SID**</span></span>](odj-odj_sid.md)
