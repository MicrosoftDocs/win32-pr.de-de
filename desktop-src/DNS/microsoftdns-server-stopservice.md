---
title: Stop Service-Methode der MicrosoftDNS_Server-Klasse
description: Die Stop Service-Methode beendet den DNS-Server.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- Stop Service-Methode (DNS)
- Stop Service-Methode, DNS, MicrosoftDNS_Server-Klasse
- DNS-MicrosoftDNS_Server Klasse, Stop Service-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StopService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f811533c66185304c5c674fdfff2eda8cf5bef69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477268"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="ddc90-106">Stop Service-Methode der MicrosoftDNS- \_ Server Klasse</span><span class="sxs-lookup"><span data-stu-id="ddc90-106">StopService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="ddc90-107">Die **Stop Service** -Methode beendet den DNS-Server.</span><span class="sxs-lookup"><span data-stu-id="ddc90-107">The **StopService** method stops the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc90-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddc90-108">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="ddc90-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddc90-109">Parameters</span></span>

<span data-ttu-id="ddc90-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ddc90-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ddc90-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ddc90-111">Return value</span></span>

<span data-ttu-id="ddc90-112">Fehler \_ Erfolg gibt an, dass der Dienst erfolgreich beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ddc90-112">ERROR\_SUCCESS indicates the service was successfully stopped.</span></span> <span data-ttu-id="ddc90-113">Jeder andere Wert ist ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ddc90-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc90-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddc90-114">Requirements</span></span>



| <span data-ttu-id="ddc90-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddc90-115">Requirement</span></span> | <span data-ttu-id="ddc90-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ddc90-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc90-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ddc90-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ddc90-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ddc90-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ddc90-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ddc90-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ddc90-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddc90-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ddc90-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="ddc90-121">Namespace</span></span><br/>                | <span data-ttu-id="ddc90-122">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="ddc90-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ddc90-123">MOF</span><span class="sxs-lookup"><span data-stu-id="ddc90-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddc90-124"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ddc90-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddc90-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddc90-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc90-126">**MicrosoftDNS- \_ Server**</span><span class="sxs-lookup"><span data-stu-id="ddc90-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="ddc90-127">**Start Service-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="ddc90-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="ddc90-128">**Startscavenging-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="ddc90-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="ddc90-129">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="ddc90-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





