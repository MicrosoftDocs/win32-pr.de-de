---
description: Wenn Sie den Code für die Lebensdauer der Zelle ändern, wurden mehrere Richtlinien für das Schreiben von hochleistungsfähigen Netzwerkanwendungen entdeckt.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Bewährte Methoden für interaktive Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354478"
---
# <a name="best-practices-for-interactive-applications"></a><span data-ttu-id="4c9fb-103">Bewährte Methoden für interaktive Anwendungen</span><span class="sxs-lookup"><span data-stu-id="4c9fb-103">Best Practices for Interactive Applications</span></span>

<span data-ttu-id="4c9fb-104">Wenn Sie den Code für die Lebensdauer der Zelle ändern, wurden mehrere Richtlinien für das Schreiben von hochleistungsfähigen Netzwerkanwendungen entdeckt.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-104">In morphing the Life cell update code, several guidelines for writing high performance network applications have been uncovered.</span></span> <span data-ttu-id="4c9fb-105">Beim Schreiben dieser Arten von Anwendungen gelten die folgenden allgemeinen Strategien:</span><span class="sxs-lookup"><span data-stu-id="4c9fb-105">Some general strategies to apply when writing these types of applications are:</span></span>

-   <span data-ttu-id="4c9fb-106">Machen Sie den Datenstrom so weit wie möglich, anstatt in Blöcke zu gehen.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-106">Make the data stream as much as possible, rather than going in chunks.</span></span>
-   <span data-ttu-id="4c9fb-107">Verwenden Sie ein paar große Transaktionen, anstatt viele kleine Transaktionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-107">Use a few large transactions rather than many small ones.</span></span> <span data-ttu-id="4c9fb-108">Große Transaktionen können auch effizient gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-108">Large transactions can also be efficiently streamed.</span></span>
-   <span data-ttu-id="4c9fb-109">Erkennen Sie, dass das Netzwerk eine langsame und unzuverlässige Ressource ist, und entwickeln Sie jede Anwendung, um die Netzwerk Abhängigkeit zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-109">Recognize that the network is a slow, unreliable resource and develop each application to minimize its reliance on the network.</span></span>
-   <span data-ttu-id="4c9fb-110">Verwenden Sie eine gut konstruierte Darstellung der Daten im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-110">Use a well-architected representation of the data on the network.</span></span> <span data-ttu-id="4c9fb-111">Die Datendarstellung sollte Computerarchitektur agnostisch sein, kein FAT enthalten und möglicherweise komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-111">The data representation should be computer-architecture agnostic, contain no fat, and possibly be compressed.</span></span>
-   <span data-ttu-id="4c9fb-112">Lassen Sie den Benutzer während der Initialisierung und des herunter Fahrens nicht warten, bis das Netzwerk gestartet oder heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-112">During initialization and shutdown, do not make the user wait for the network to start up or shut down.</span></span> <span data-ttu-id="4c9fb-113">Die netzwerkbezogene Initialisierung kann relativ lange dauern.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-113">Network related initialization could take a relatively long time.</span></span> <span data-ttu-id="4c9fb-114">Trennen Sie den nicht kritischen Netzwerkcode.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-114">Separate the noncritical network code.</span></span>
-   <span data-ttu-id="4c9fb-115">Behandeln Sie Fehler entsprechend ihren Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-115">Handle errors as appropriate to their impact.</span></span> <span data-ttu-id="4c9fb-116">Nicht alle Fehler sind von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-116">Not all errors are critical.</span></span> <span data-ttu-id="4c9fb-117">Implementieren von Wiederherstellungs Mechanismen und Bereitstellen von nicht eindringlichem Benutzer Feedback.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-117">Implement recovery mechanisms and provide nonintrusive user feedback.</span></span>
-   <span data-ttu-id="4c9fb-118">Verwenden Sie Remote Prozedur Aufrufe (RPC) nur, wenn dies angebracht ist.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-118">Use remote procedure calls (RPC) only when appropriate.</span></span> <span data-ttu-id="4c9fb-119">RPC ist unter Windows Me/98 synchron und führt immer zu einer Chatty, FAT-Protokolle, wenn Sie zum Senden kleiner Datenmengen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-119">RPC is synchronous on Windows Me/98 and always results in chatty, fat protocols when used to send small amounts of data.</span></span>
-   <span data-ttu-id="4c9fb-120">Messen Sie den Netzwerk Aufwand mithilfe von netstat. Möglicherweise sind Sie überrascht, was Ihre Messungen zeigen.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-120">Measure your network overhead using Netstat; you may be surprised at what your measurements reveal.</span></span>
-   <span data-ttu-id="4c9fb-121">Testen Sie die Anwendung in einer Vielzahl von Netzwerken, insbesondere bei langsamen oder Ausfall anfälligen Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-121">Test the application on a variety of networks, especially slow or loss-prone networks.</span></span> <span data-ttu-id="4c9fb-122">Drahtlose LAN-Netzwerke, Modems und virtuelle private Netzwerke (VPN) über das Internet sind gute Netzwerke für Tests.</span><span class="sxs-lookup"><span data-stu-id="4c9fb-122">Wireless LAN networks, modems, and virtual private networks (VPN) over the Internet are good networks for testing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c9fb-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c9fb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c9fb-124">Hochleistungsfähige Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="4c9fb-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



