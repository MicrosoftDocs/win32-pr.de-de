---
title: Iwmdrmnetreceiver-Schnittstelle
description: Die iwmdrmnetreceiver-Schnittstelle stellt Methoden bereit, die für die Verwendung von Microsoft Windows Media DRM für Netzwerkgeräte als Empfänger benötigt werden. Um eine Instanz dieser Schnittstelle zu erhalten, rufen Sie iwmdrmprovider-Erstellungsobjekt auf. Übergeben Sie IID \_ iwmdrmnetreceiver als riid-Parameter.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- Iwmdrmnetreceiver-Schnittstelle Windows Media-Format
- Iwmdrmnetreceiver-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a85ae1525a81e97984e29a5dd28763d934dba2b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389340"
---
# <a name="iwmdrmnetreceiver-interface"></a><span data-ttu-id="13e8f-106">Iwmdrmnetreceiver-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="13e8f-106">IWMDRMNetReceiver interface</span></span>

<span data-ttu-id="13e8f-107">Die **iwmdrmnetreceiver** -Schnittstelle stellt Methoden bereit, die für die Verwendung von Microsoft Windows Media DRM für Netzwerkgeräte als Empfänger benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="13e8f-107">The **IWMDRMNetReceiver** interface provides methods needed to use Microsoft Windows Media DRM for Network Devices as a receiver.</span></span>

<span data-ttu-id="13e8f-108">Um eine Instanz dieser Schnittstelle abzurufen, rufen Sie [**iwmdrmprovider:: builateobject**](iwmdrmprovider-createobject.md)auf.</span><span class="sxs-lookup"><span data-stu-id="13e8f-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="13e8f-109">Übergeben Sie **IID \_ iwmdrmnetreceiver** als *riid* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="13e8f-109">Pass **IID\_IWMDRMNetReceiver** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="13e8f-110">Member</span><span class="sxs-lookup"><span data-stu-id="13e8f-110">Members</span></span>

<span data-ttu-id="13e8f-111">Die **iwmdrmnetreceiver** -Schnittstelle erbt von [**iwmdrmeventgenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="13e8f-111">The **IWMDRMNetReceiver** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="13e8f-112">**Iwmdrmnetreceiver** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="13e8f-112">**IWMDRMNetReceiver** also has these types of members:</span></span>

-   [<span data-ttu-id="13e8f-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="13e8f-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="13e8f-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="13e8f-114">Methods</span></span>

<span data-ttu-id="13e8f-115">Die **iwmdrmnetreceiver** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="13e8f-115">The **IWMDRMNetReceiver** interface has these methods.</span></span>



| <span data-ttu-id="13e8f-116">Methode</span><span class="sxs-lookup"><span data-stu-id="13e8f-116">Method</span></span>                                                                               | <span data-ttu-id="13e8f-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13e8f-117">Description</span></span>                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13e8f-118">**Getlicenanchallenge**</span><span class="sxs-lookup"><span data-stu-id="13e8f-118">**GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)                 | <span data-ttu-id="13e8f-119">Generiert eine Lizenz Aufforderung, die beim Anfordern geschützter Inhalte an den Sender gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="13e8f-119">Generates a license challenge that is sent to the transmitter when requesting protected content.</span></span><br/>                     |
| [<span data-ttu-id="13e8f-120">**Getregistrationchallenge**</span><span class="sxs-lookup"><span data-stu-id="13e8f-120">**GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)       | <span data-ttu-id="13e8f-121">Generiert eine Registrierungs Aufforderung, die beim Registrieren oder erneuten Validieren des Empfängers an den Sender gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="13e8f-121">Generates a registration challenge that is sent to the transmitter when the receiver is registering or revalidating.</span></span><br/> |
| [<span data-ttu-id="13e8f-122">**Processlicenseresponse**</span><span class="sxs-lookup"><span data-stu-id="13e8f-122">**ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)           | <span data-ttu-id="13e8f-123">Verarbeitet die vom Sender gesendete Lizenz Antwort als Antwort auf eine Lizenz Herausforderung.</span><span class="sxs-lookup"><span data-stu-id="13e8f-123">Processes the license response sent by the transmitter in reply to a license challenge.</span></span><br/>                              |
| [<span data-ttu-id="13e8f-124">**Processregistrationresponse**</span><span class="sxs-lookup"><span data-stu-id="13e8f-124">**ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md) | <span data-ttu-id="13e8f-125">Verarbeitet die vom Sender gesendete Registrierungs Antwort als Antwort auf eine Registrierungs Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="13e8f-125">Processes the registration response sent by the transmitter in reply to a registration challenge.</span></span><br/>                    |



 

## <a name="see-also"></a><span data-ttu-id="13e8f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13e8f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e8f-127">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="13e8f-127">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="13e8f-128">**Iwmdrmeventgenerator**</span><span class="sxs-lookup"><span data-stu-id="13e8f-128">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> <dt>

[<span data-ttu-id="13e8f-129">**Iwmdrmnettransmitter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="13e8f-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





