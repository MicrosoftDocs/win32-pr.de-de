---
title: Neuerungen in den UPnP-APIs
description: Die UPnP-™-APIs verfügen über neue Features und aktualisierte Dokumentation für Windows XP SP2. In der folgenden Tabelle ist die neue Dokumentation aufgeführt.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27747c6185b5aecea86e240d388ab10410aa29f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714351"
---
# <a name="whats-new-in-the-upnp-apis"></a><span data-ttu-id="d5ca7-104">Neuerungen in den UPnP-APIs</span><span class="sxs-lookup"><span data-stu-id="d5ca7-104">What's New in the UPnP APIs</span></span>

<span data-ttu-id="d5ca7-105">Die UPnP-™-APIs verfügen über neue Features und aktualisierte Dokumentation für Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-105">The UPnP™ APIs have new features and updated documentation for Windows XP SP2.</span></span> <span data-ttu-id="d5ca7-106">In der folgenden Tabelle ist die neue Dokumentation aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-106">The following table identifies the new documentation.</span></span>



| <span data-ttu-id="d5ca7-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="d5ca7-107">Feature</span></span>                                                          | <span data-ttu-id="d5ca7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5ca7-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5ca7-109">**Iupnpremoteendpointinfo**</span><span class="sxs-lookup"><span data-stu-id="d5ca7-109">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | <span data-ttu-id="d5ca7-110">Diese neue Schnittstelle ermöglicht einem gehosteten Gerät das Abrufen von Informationen über einen Anforderer (d. h. einen Steuerungspunkt) und die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-110">This new interface allows a hosted device to obtain information about a requester (that is, a control point) and the request.</span></span> <span data-ttu-id="d5ca7-111">Sie enthält drei Methoden, von denen jede einen anderen Informationstyp bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-111">It includes three methods, each of which provides a different type of information.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="d5ca7-112">Implementieren von Geräteverhalten</span><span class="sxs-lookup"><span data-stu-id="d5ca7-112">Implementing Device Behavior</span></span>](implementing-device-behavior.md) | <span data-ttu-id="d5ca7-113">Dieses Thema enthält einen neuen Abschnitt, in dem erläutert wird, wie Endpunkt Informationen mithilfe der neuen [**iupnpremoteendpointinfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) -Schnittstelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-113">This topic includes a new section that explains how to obtain endpoint information by using the new [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="d5ca7-114">Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d5ca7-114">Configuration Settings</span></span>](configuration-settings.md)             | <span data-ttu-id="d5ca7-115">Dieses neue Thema enthält Informationen zu den Registrierungs Einstellungen, die das Verhalten der UPnP-APIs beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-115">This new topic provides information about the registry settings that affect the behavior of the UPnP APIs.</span></span>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="d5ca7-116">Gerätefehler Codes</span><span class="sxs-lookup"><span data-stu-id="d5ca7-116">Device Error Codes</span></span>](device-error-codes.md)                     | <span data-ttu-id="d5ca7-117">In diesem neuen Thema wird erläutert, wie ein Fehlercode von einem Gerät in einen HRESULT-Wert und umgekehrt konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-117">This new topic explains how an error code from a device is converted to an HRESULT value and vice versa.</span></span> <span data-ttu-id="d5ca7-118">Ein Verständnis dieses Prozesses ist erforderlich, um einen HRESULT-Wert auszuwerten, der von der [**iupnpservice:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) -Methode und der [**iupnpservice:: querystatuevariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-118">An understanding of this process is necessary in order to evaluate an HRESULT value that is returned by the [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**IUPnPService::QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods.</span></span> |



 

 

 




