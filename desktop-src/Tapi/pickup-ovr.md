---
description: Der Pickup-Vorgang ermöglicht es einer Anwendung, eine Sitzung zu beantworten, bei der eine Warnung an einer anderen Adresse angezeigt wird. Die Anwendung identifiziert das Ziel der Abholung und gibt eine Sitzungs-ID für den aufzurufenden-Befehl zurück.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Aufhol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e033689ffccf6ba01ad06eb071514c1c37aaca03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758335"
---
# <a name="pickup"></a><span data-ttu-id="8d13f-104">Aufhol</span><span class="sxs-lookup"><span data-stu-id="8d13f-104">Pickup</span></span>

<span data-ttu-id="8d13f-105">Der Pickup-Vorgang ermöglicht es einer Anwendung, eine Sitzung zu beantworten, bei der eine Warnung an einer anderen Adresse angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8d13f-105">The pickup operation allows an application to answer a session that is alerting at another address.</span></span> <span data-ttu-id="8d13f-106">Die Anwendung identifiziert das Ziel der Abholung und gibt eine Sitzungs-ID für den aufzurufenden-Befehl zurück.</span><span class="sxs-lookup"><span data-stu-id="8d13f-106">The application identifies the target of the pickup and is returned a session identifier for the picked-up call.</span></span>

<span data-ttu-id="8d13f-107">Es gibt mehrere Möglichkeiten, das Ziel der Abhol Anforderung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8d13f-107">There are several ways to identify the target of the pickup request.</span></span> <span data-ttu-id="8d13f-108">Zuerst kann die Anwendung die Adresse der Warnungs Partei angeben.</span><span class="sxs-lookup"><span data-stu-id="8d13f-108">First, the application may specify the address of the alerting party.</span></span> <span data-ttu-id="8d13f-109">Zweitens: Wenn keine Adresse angegeben wird und der Switch dies zulässt, kann die Anwendung jede Warnungs Sitzung in der Pickup-Gruppe abrufen.</span><span class="sxs-lookup"><span data-stu-id="8d13f-109">Second, if no address is specified and the switch allows it, the application can pick up any alerting session in its pickup group.</span></span> <span data-ttu-id="8d13f-110">Drittens ermöglichen einige Switches das Abfangen einer Sitzungs Warnung in einer anderen abholgruppe, wenn der Gruppen Bezeichner angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8d13f-110">Third, some switches allow pickup of a session alerting in a different pickup group if the group identifier is specified.</span></span>

<span data-ttu-id="8d13f-111">Einige Schlüssel Telefonsysteme unterstützen eine *Übertragung durch die Hold* -Funktion bei überbrückenden exklusiven anrufen.</span><span class="sxs-lookup"><span data-stu-id="8d13f-111">Some key telephone systems support a *transfer through hold* capability on bridged-exclusive call appearances.</span></span> <span data-ttu-id="8d13f-112">In diesem Schema besitzt ein bestimmtes Telefon einen Anruf exklusiv, wenn der Anruf aktiv ist, aber wenn der Anruf angehalten ist, kann jedes Telefon, das eine Darstellung der Linie aufweist, den Anruf aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="8d13f-112">In this scheme, a particular phone owns a call exclusively when the call is active, but when the call is on hold, any phone that has an appearance of the line can pick up the call.</span></span>

<span data-ttu-id="8d13f-113">**TAPI 2. x:** Eine Anwendung kann zu diesem Zweck einen Abholvorgang mit einer **null** -Zieladresse verwenden, ähnlich wie bei der Verwendung der Funktion zum Abrufen eines aufrufwartenden Aufrufens in einer analogen Zeile.</span><span class="sxs-lookup"><span data-stu-id="8d13f-113">**TAPI 2.x:** An application can use a pickup operation with a **NULL** target address for this purpose, similar to how the function is used to pick up a call waiting call on an analog line.</span></span> <span data-ttu-id="8d13f-114">Lineaddrfeature \_ pickbestätigte gibt an, dass die Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8d13f-114">LINEADDRFEATURE\_PICKUPHELD indicates the existence of the capability.</span></span>

<span data-ttu-id="8d13f-115">Wenn lineaddrcapflags \_ pickupcallwait den Wert **true** hat, kann eine Sitzung übernommen werden, für die der Benutzer das aufrufende Signal, aber für das der Dienstanbieter die Erkennung nicht ausführen kann, übernommen hat.</span><span class="sxs-lookup"><span data-stu-id="8d13f-115">If LINEADDRCAPFLAGS\_PICKUPCALLWAIT is **TRUE**, a session can be picked up for which the user has audibly detected the call-waiting signal but for which the service provider is unable to perform the detection.</span></span> <span data-ttu-id="8d13f-116">Dadurch erhält der Benutzer einen Mechanismus zum Beantworten eines wartenden Aufrufs, auch wenn der Dienstanbieter das Anruf Ende Signal nicht erkennen konnte.</span><span class="sxs-lookup"><span data-stu-id="8d13f-116">This gives the user a mechanism to "answer" a waiting call even though the service provider was unable to detect the call-waiting signal.</span></span> <span data-ttu-id="8d13f-117">Sowohl die Zieladresse als auch die Gruppen-ID müssen **null** sein, um einen Rückruf aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="8d13f-117">Both the destination address and the group ID must be **NULL** to pick up a call-waiting call.</span></span>

<span data-ttu-id="8d13f-118">Wenn eine Sitzung erfolgreich abgerufen wurde, empfängt die Anwendung eine Benachrichtigung über Statusänderungen, wobei der [Grund](reason-ovr.md) auf linecallreason Pickup festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="8d13f-118">When a session has been picked up successfully, the application receives a state change notification with the [reason](reason-ovr.md) set to LINECALLREASON\_PICKUP.</span></span>

<span data-ttu-id="8d13f-119">Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="8d13f-119">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="8d13f-120">**TAPI 2. x:** Weitere Informationen finden [**Sie unter linepickup**](/windows/win32/api/tapi/nf-tapi-linepickup).</span><span class="sxs-lookup"><span data-stu-id="8d13f-120">**TAPI 2.x:** See [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).</span></span>

<span data-ttu-id="8d13f-121">**TAPI 3. x:** Weitere Informationen finden [**Sie unter itbasiccallcontrol::P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).</span><span class="sxs-lookup"><span data-stu-id="8d13f-121">**TAPI 3.x:** See [**ITBasicCallControl::Pickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).</span></span>

 

 
