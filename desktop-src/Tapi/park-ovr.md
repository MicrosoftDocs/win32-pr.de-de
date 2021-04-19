---
description: Der Park-Vorgang ermöglicht es einer Anwendung, eine Sitzung an eine spezielle Adresse zu senden, in der Sie bis zum Entsperren aufbewahrt wird.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Wildpark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aded4657a9d337d6d9c663622a5359856e964b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349879"
---
# <a name="park"></a><span data-ttu-id="b4651-103">Wildpark</span><span class="sxs-lookup"><span data-stu-id="b4651-103">Park</span></span>

<span data-ttu-id="b4651-104">Der Park-Vorgang ermöglicht es einer Anwendung, eine Sitzung an eine spezielle Adresse zu senden, in der Sie bis zum Entsperren aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="b4651-104">The park operation allows an application to send a session to a special address where it will be held until unparked.</span></span> <span data-ttu-id="b4651-105">Aus Sicht der Anwendung sieht dies wie eine Übertragung aus.</span><span class="sxs-lookup"><span data-stu-id="b4651-105">From the point of view of the application, this looks much like a transfer.</span></span> <span data-ttu-id="b4651-106">Der Partei am anderen Ende der Verbindung ähnelt dies dem ablegen.</span><span class="sxs-lookup"><span data-stu-id="b4651-106">To the party on the other end of the connection, this resembles being put on hold.</span></span>

<span data-ttu-id="b4651-107">Der Unterschied zwischen Park und Transfer besteht darin, dass die geparkte Adresse kein Verbindungspunkt für die Sitzung ist, und die Sitzung nicht benachrichtigt wird oder ein Timeout auftritt. Der Unterschied zwischen Park und Hold besteht darin, dass die Sitzung nicht mehr mit der Adresse der Anwendung verknüpft ist, sobald der Park Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b4651-107">The difference between park and transfer is that the parked address is not a connection point for the session, and the session does not alert or time out. The difference between park and hold is that once park operation completes, the session is no longer associated with the application's address.</span></span>

<span data-ttu-id="b4651-108">Zwei Arten von Parken einer Sitzung werden bereitgestellt: der *gesteuerte Park* und der *nicht gesteuerte Park*.</span><span class="sxs-lookup"><span data-stu-id="b4651-108">Two forms of parking a session are provided: *directed park* and *nondirected park*.</span></span> <span data-ttu-id="b4651-109">In einem gerichteten callpark gibt die Anwendung die Zieladresse an, in der der-Befehl geparkt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4651-109">In directed call park, the application specifies the destination address where the call is to be parked.</span></span> <span data-ttu-id="b4651-110">Bei einem nicht gesteuerten Park ermittelt der Dienstanbieter oder die zugrunde liegende Hardware die Adresse und gibt Sie an die Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="b4651-110">With nondirected park, the service provider or underlying hardware determines the address and returns it to the application.</span></span>

<span data-ttu-id="b4651-111">Eine geparierte Sitzung wechselt in der Regel in den Leerlaufzustand, nachdem Sie erfolgreich geparkt wurde, und die Anwendung sollte dann die ihr zugeordneten Ressourcen freigeben.</span><span class="sxs-lookup"><span data-stu-id="b4651-111">A parked session typically enters the idle state after it has been successfully parked, and the application should then release the resources associated with it.</span></span> <span data-ttu-id="b4651-112">Eine Zusammenfassung der Vorgehensweise finden Sie unter [Beenden einer Sitzung](terminate-a-session-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="b4651-112">See [Terminate a Session](terminate-a-session-ovr.md) for a summary of how to do this.</span></span>

<span data-ttu-id="b4651-113">Wenn die Anwendung die Sitzung entbindet, werden neue Sitzungs Ressourcen zugewiesen, selbst wenn die Anwendung die vorherigen Zeiger zurückgegeben hat, sodass das Ausführen von ordnungsgemäßen Releases zu einer Vielzahl von Problemen führen kann.</span><span class="sxs-lookup"><span data-stu-id="b4651-113">If the application unparks the session, new session resources are allocated even if the application has returned the previous pointers, so failure to do proper releases can result in a variety of problems.</span></span>

<span data-ttu-id="b4651-114">Einige Dienstanbieter können den Benutzer erinnern, nachdem eine Sitzung für einen längeren Zeitraum geparkt wurde.</span><span class="sxs-lookup"><span data-stu-id="b4651-114">Some service providers can remind the user after a session has been parked for some long amount of time.</span></span> <span data-ttu-id="b4651-115">Die Anwendung sieht einen Angebots-und einen Anforderungstyp, der auf [Erinnerung festgelegt](reason-ovr.md) ist.</span><span class="sxs-lookup"><span data-stu-id="b4651-115">The application sees an offering call with a call [reason](reason-ovr.md) set to reminder.</span></span>

<span data-ttu-id="b4651-116">Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="b4651-116">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="b4651-117">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linepark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineunpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).</span><span class="sxs-lookup"><span data-stu-id="b4651-117">**TAPI 2.x:** See [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).</span></span>

<span data-ttu-id="b4651-118">**TAPI 3:** Siehe [**itbasiccallcontrol::P arkdirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**itbasiccallcontrol::P arkindirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**itbasiccallcontrol:: unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).</span><span class="sxs-lookup"><span data-stu-id="b4651-118">**TAPI 3:** See [**ITBasicCallControl::ParkDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::ParkIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl::Unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).</span></span>

 

 
