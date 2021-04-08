---
title: Suchen nach Geräten
description: Die UPnP-Architektur ist eine dynamische Netzwerkarchitektur, mit der Geräte jederzeit beitreten und das Netzwerk verlassen können.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b8feebd430252b118353681a90ce4cd683ee7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037427"
---
# <a name="finding-devices"></a><span data-ttu-id="66357-103">Suchen nach Geräten</span><span class="sxs-lookup"><span data-stu-id="66357-103">Finding Devices</span></span>

<span data-ttu-id="66357-104">Die UPnP-Architektur ist eine dynamische Netzwerkarchitektur, mit der Geräte jederzeit beitreten und das Netzwerk verlassen können.</span><span class="sxs-lookup"><span data-stu-id="66357-104">The UPnP architecture is a dynamic network architecture that allows devices to join and leave the network at any time.</span></span> <span data-ttu-id="66357-105">Aufgrund dieser dynamischen Architektur können Anwendungen nicht darauf basieren, dass bestimmte UPnP-basierte Geräte zu einem bestimmten Zeitpunkt verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="66357-105">Because of this dynamic architecture, applications cannot rely on specific UPnP-based devices to be available at any given time.</span></span> <span data-ttu-id="66357-106">Aus diesem Grund durchsuchen Anwendungen (oder Steuerungs Punkte) das Netzwerk, um Geräte zu finden, die den angegebenen Kriterien am ehesten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="66357-106">For this reason, applications (or control points) search the network to find devices that most closely match specified criteria.</span></span> <span data-ttu-id="66357-107">Anwendungen warten auch auf Geräte Ankündigungs Meldungen, die darauf hinweisen, dass dem Netzwerk neue Geräte hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="66357-107">Applications also wait for device advertisement messages that indicate new devices have been added to the network.</span></span>

<span data-ttu-id="66357-108">Im folgenden finden Sie gültige Suchkriterien für UPnP-basierte Geräte:</span><span class="sxs-lookup"><span data-stu-id="66357-108">The following are valid search criteria for UPnP-based devices:</span></span>

-   <span data-ttu-id="66357-109">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="66357-109">Device type</span></span>
-   <span data-ttu-id="66357-110">Dienstart</span><span class="sxs-lookup"><span data-stu-id="66357-110">Service type</span></span>
-   <span data-ttu-id="66357-111">Eindeutiger Gerätename (UDN)</span><span class="sxs-lookup"><span data-stu-id="66357-111">Unique device name (UDN)</span></span>
-   <span data-ttu-id="66357-112">Alle Stamm Geräte</span><span class="sxs-lookup"><span data-stu-id="66357-112">All root devices</span></span>

<span data-ttu-id="66357-113">Der Gerätetyp und die Diensttyp Suche werden normalerweise verwendet, um eine Klasse von Geräten mit allgemeinen Merkmalen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="66357-113">The device type and service type searches are typically used to find a class of devices with common characteristics.</span></span> <span data-ttu-id="66357-114">Die udn-Suche wird verwendet, um ein bestimmtes Gerät zu finden.</span><span class="sxs-lookup"><span data-stu-id="66357-114">The UDN search is used to find a specific device.</span></span>

<span data-ttu-id="66357-115">Um nach Geräten zu suchen, muss eine Anwendung zuerst das Device Finder-Objekt instanziieren.</span><span class="sxs-lookup"><span data-stu-id="66357-115">To search for devices, an application must first instantiate the Device Finder object.</span></span> <span data-ttu-id="66357-116">Dieses Objekt macht die [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) -Schnittstelle verfügbar. die zugehörigen Methoden führen die zuvor beschriebenen Suchvorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="66357-116">This object exposes the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface; its methods perform the previously described searches.</span></span>

<span data-ttu-id="66357-117">In den folgenden Abschnitten wird das Auffinden von Geräten beschrieben:</span><span class="sxs-lookup"><span data-stu-id="66357-117">The following sections describe the process of finding devices:</span></span>

-   [<span data-ttu-id="66357-118">Erstellen des Geräte Suchgeräts</span><span class="sxs-lookup"><span data-stu-id="66357-118">Creating the Device Finder</span></span>](creating-the-device-finder.md)
-   [<span data-ttu-id="66357-119">Asynchrone Suche</span><span class="sxs-lookup"><span data-stu-id="66357-119">Asynchronous Searching</span></span>](asynchronous-searching.md)
-   [<span data-ttu-id="66357-120">Synchrone Suche</span><span class="sxs-lookup"><span data-stu-id="66357-120">Synchronous Searching</span></span>](synchronous-searching.md)
-   [<span data-ttu-id="66357-121">Von synchronen suchen zurückgegebene Geräte Sammlungen</span><span class="sxs-lookup"><span data-stu-id="66357-121">Device Collections Returned By Synchronous Searches</span></span>](device-collections-returned-by-synchronous-searches.md)

 

 




