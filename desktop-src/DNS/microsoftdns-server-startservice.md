---
title: Start Service-Methode der MicrosoftDNS_Server-Klasse
description: Mit der Start Service-Methode wird der DNS-Server gestartet.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- Start Service-Methode (DNS)
- Start Service-Methode (DNS), MicrosoftDNS_Server-Klasse
- DNS-MicrosoftDNS_Server Klasse, StartService-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e103b3d2648bf2c061eb047090cfdfeb907518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338347"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="a9a8d-106">Start Service-Methode der MicrosoftDNS- \_ Server Klasse</span><span class="sxs-lookup"><span data-stu-id="a9a8d-106">StartService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="a9a8d-107">Mit der **Start Service** -Methode wird der DNS-Server gestartet.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-107">The **StartService** method starts the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a8d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9a8d-108">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="a9a8d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9a8d-109">Parameters</span></span>

<span data-ttu-id="a9a8d-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9a8d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9a8d-111">Return value</span></span>

<span data-ttu-id="a9a8d-112">Fehler \_ Erfolg gibt an, dass der Dienst erfolgreich gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-112">ERROR\_SUCCESS indicates the service was successfully started.</span></span> <span data-ttu-id="a9a8d-113">Jeder andere Wert ist ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9a8d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9a8d-114">Requirements</span></span>



| <span data-ttu-id="a9a8d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9a8d-115">Requirement</span></span> | <span data-ttu-id="a9a8d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a9a8d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a8d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9a8d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a8d-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a9a8d-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a9a8d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9a8d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a8d-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9a8d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a9a8d-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9a8d-121">Namespace</span></span><br/>                | <span data-ttu-id="a9a8d-122">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="a9a8d-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a9a8d-123">MOF</span><span class="sxs-lookup"><span data-stu-id="a9a8d-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9a8d-124"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a9a8d-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9a8d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9a8d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a8d-126">**MicrosoftDNS- \_ Server**</span><span class="sxs-lookup"><span data-stu-id="a9a8d-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="a9a8d-127">**Stop Service-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="a9a8d-127">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="a9a8d-128">**Startscavenging-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="a9a8d-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="a9a8d-129">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="a9a8d-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





