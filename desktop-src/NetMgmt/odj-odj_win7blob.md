---
title: ODJ_WIN7BLOB
description: ODJ_WIN7BLOB IDL-Definition
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104316706"
---
# <a name="odj_win7blob-structure"></a><span data-ttu-id="0f307-103">ODJ_WIN7BLOB Struktur</span><span class="sxs-lookup"><span data-stu-id="0f307-103">ODJ_WIN7BLOB structure</span></span>

<span data-ttu-id="0f307-104">Enthält die grundlegenden Informationen, die erforderlich sind, um einen Client einer Domäne hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0f307-104">Contains the basic information required to join a client to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f307-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f307-105">Syntax</span></span>

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a><span data-ttu-id="0f307-106">Member</span><span class="sxs-lookup"><span data-stu-id="0f307-106">Members</span></span>

### <a name="lpdomain"></a><span data-ttu-id="0f307-107">lpdomain</span><span class="sxs-lookup"><span data-stu-id="0f307-107">lpDomain</span></span>

<span data-ttu-id="0f307-108">Muss auf den Domänen Namen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0f307-108">Must be set to the domain name.</span></span>

### <a name="lpmachinename"></a><span data-ttu-id="0f307-109">lpmachinename</span><span class="sxs-lookup"><span data-stu-id="0f307-109">lpMachineName</span></span>

<span data-ttu-id="0f307-110">Muss auf den Computernamen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0f307-110">Must be set to the machine name.</span></span>

### <a name="lpmachinepassword"></a><span data-ttu-id="0f307-111">lpmachinepassword</span><span class="sxs-lookup"><span data-stu-id="0f307-111">lpMachinePassword</span></span>

<span data-ttu-id="0f307-112">Muss auf ein Klartext-Kennwort für das Computer Konto festgelegt werden, das von lpmachinename identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="0f307-112">Must be set to a cleartext password for the machine account identified by lpMachineName</span></span>

### <a name="dnsdomaininfo"></a><span data-ttu-id="0f307-113">Dnsdomaininfo</span><span class="sxs-lookup"><span data-stu-id="0f307-113">DnsDomainInfo</span></span>

<span data-ttu-id="0f307-114">Enthält Informationen über die Domäne, die verknüpft wird.</span><span class="sxs-lookup"><span data-stu-id="0f307-114">Contains information about the domain being joined.</span></span>

### <a name="dcinfo"></a><span data-ttu-id="0f307-115">Dcinfo</span><span class="sxs-lookup"><span data-stu-id="0f307-115">DcInfo</span></span>

<span data-ttu-id="0f307-116">Enthält Benennungs-und Adressierungs Informationen über den Domänen Controller, der zum Erstellen des Computer Kontos Active Directory verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0f307-116">Contains naming and addressing information about the domain controller that was used to create the machine account Active Directory.</span></span>

### <a name="options"></a><span data-ttu-id="0f307-117">Optionen</span><span class="sxs-lookup"><span data-stu-id="0f307-117">Options</span></span>

<span data-ttu-id="0f307-118">Muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0f307-118">Must be set to zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f307-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f307-119">See also</span></span>

[<span data-ttu-id="0f307-120">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="0f307-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="0f307-121">**ODJ- \_ Richtlinie \_ DNS- \_ Domänen \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="0f307-121">**ODJ\_POLICY\_DNS\_DOMAIN\_INFO**</span></span>](odj-odj_policy_dns_domain_info.md)

[<span data-ttu-id="0f307-122">**DOMAIN_CONTROLLER_INFOW**</span><span class="sxs-lookup"><span data-stu-id="0f307-122">**DOMAIN_CONTROLLER_INFOW**</span></span>](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



