---
title: Startscavenging-Methode der MicrosoftDNS_Server-Klasse
description: Die startscavenging-Methode beginnt mit dem ablöschen veralteter Datensätze in den Zonen, die sich in der scräging befinden.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- Startscavenging-Methode (DNS)
- Startscavenging-Methode (DNS), MicrosoftDNS_Server-Klasse
- DNS-MicrosoftDNS_Server Klasse, startscavenging-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8e1927ed069d3e3e3cf27fd94b1ffd54e6bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956618"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="9f461-106">Startscavenging-Methode der MicrosoftDNS- \_ Server Klasse</span><span class="sxs-lookup"><span data-stu-id="9f461-106">StartScavenging method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="9f461-107">Die **startscavenging** -Methode beginnt mit dem ablöschen veralteter Datensätze in den Zonen, die sich in der scräging befinden.</span><span class="sxs-lookup"><span data-stu-id="9f461-107">The **StartScavenging** method starts scavenging stale records in the zones subjected to scavenging.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f461-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f461-108">Syntax</span></span>


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a><span data-ttu-id="9f461-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f461-109">Parameters</span></span>

<span data-ttu-id="9f461-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9f461-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f461-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f461-111">Return value</span></span>

<span data-ttu-id="9f461-112">Fehler \_ Erfolg gibt an, dass das scräging erfolgreich gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="9f461-112">ERROR\_SUCCESS indicates the scavenging was successfully started.</span></span> <span data-ttu-id="9f461-113">Jeder andere Wert ist ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9f461-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f461-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f461-114">Requirements</span></span>



| <span data-ttu-id="9f461-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f461-115">Requirement</span></span> | <span data-ttu-id="9f461-116">Wert</span><span class="sxs-lookup"><span data-stu-id="9f461-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f461-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f461-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9f461-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9f461-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9f461-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f461-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9f461-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f461-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9f461-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f461-121">Namespace</span></span><br/>                | <span data-ttu-id="9f461-122">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="9f461-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9f461-123">MOF</span><span class="sxs-lookup"><span data-stu-id="9f461-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f461-124"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9f461-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f461-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f461-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f461-126">**MicrosoftDNS- \_ Server**</span><span class="sxs-lookup"><span data-stu-id="9f461-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="9f461-127">**Start Service-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="9f461-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="9f461-128">**Stop Service-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="9f461-128">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="9f461-129">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="9f461-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





