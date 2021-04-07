---
description: Übersicht über die Ereignis Benachrichtigung
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Übersicht über die Ereignis Benachrichtigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746568"
---
# <a name="overview-of-event-notification"></a><span data-ttu-id="23778-103">Übersicht über die Ereignis Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="23778-103">Overview of Event Notification</span></span>

<span data-ttu-id="23778-104">Ein Filter benachrichtigt den Filter-Graph-Manager über ein Ereignis, indem er eine Ereignis Benachrichtigung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="23778-104">A filter notifies the Filter Graph Manager about an event by posting an event notification.</span></span> <span data-ttu-id="23778-105">Das Ereignis ist möglicherweise erwartungsgemäß, wie z. b. das Ende eines Streams, oder es könnte einen Fehler darstellen, z. b. einen Fehler beim Rendering eines Streams.</span><span class="sxs-lookup"><span data-stu-id="23778-105">The event could be something expected, such as the end of a stream, or it could represent an error, such as a failure to render a stream.</span></span> <span data-ttu-id="23778-106">Der Filter Graph-Manager verarbeitet einige Filter Ereignisse allein und lässt andere von der Anwendung verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="23778-106">The Filter Graph Manager handles some filter events by itself, and it leaves others for the application to handle.</span></span> <span data-ttu-id="23778-107">Wenn der Filter Graph-Manager kein Filter Ereignis behandelt, wird die Ereignis Benachrichtigung in eine Warteschlange eingefügt.</span><span class="sxs-lookup"><span data-stu-id="23778-107">If the Filter Graph Manager does not handle a filter event, it places the event notification into a queue.</span></span> <span data-ttu-id="23778-108">Das Filter Diagramm kann auch seine eigenen Ereignis Benachrichtigungen für die Anwendung in die Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="23778-108">The filter graph can also queue its own event notifications for the application.</span></span>

<span data-ttu-id="23778-109">Eine Anwendung ruft Ereignisse aus der Warteschlange ab und antwortet Ihnen basierend auf dem Ereignistyp.</span><span class="sxs-lookup"><span data-stu-id="23778-109">An application retrieves events from the queue and responds to them based on the type of event.</span></span> <span data-ttu-id="23778-110">Die Ereignis Benachrichtigung in DirectShow ähnelt daher dem Microsoft Windows Message queuingschema.</span><span class="sxs-lookup"><span data-stu-id="23778-110">Event notification in DirectShow is therefore similar to the Microsoft Windows message queuing scheme.</span></span> <span data-ttu-id="23778-111">Eine Anwendung kann auch das Standardverhalten des Filter Graph-Managers für einen bestimmten Ereignistyp abbrechen.</span><span class="sxs-lookup"><span data-stu-id="23778-111">An application can also cancel the Filter Graph Manager's default behavior for a given event type.</span></span> <span data-ttu-id="23778-112">Der Filter Graph-Manager fügt diese Ereignisse dann direkt in die Warteschlange ein, damit Sie von der Anwendung behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="23778-112">The Filter Graph Manager then puts those events directly into the queue for the application to handle.</span></span>

<span data-ttu-id="23778-113">Dieser Mechanismus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="23778-113">This mechanism enables</span></span>

-   <span data-ttu-id="23778-114">Der Filter-Graph-Manager für die Kommunikation mit der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="23778-114">The Filter Graph Manager to communicate with the application.</span></span>
-   <span data-ttu-id="23778-115">Filter für die Kommunikation mit der Anwendung und dem Filter-Graph-Manager.</span><span class="sxs-lookup"><span data-stu-id="23778-115">Filters to communicate with both the application and the Filter Graph Manager.</span></span>
-   <span data-ttu-id="23778-116">Die Anwendung, um den Grad der Beteiligung an der Behandlung von Ereignissen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="23778-116">The application to determine its degree of involvement in handling events.</span></span>

 

 



