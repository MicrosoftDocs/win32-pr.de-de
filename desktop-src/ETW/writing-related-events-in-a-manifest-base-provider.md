---
description: Verwenden Sie die EventWrite-Funktion, wenn mehrere Komponenten Ihre Ereignisse in einem End-to-End-Ablauf Verfolgungs Szenario miteinander verknüpfen möchten.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Schreiben verwandter Ereignisse in einem Manifest-basierten Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9508996503f53c738d62fac32905919a8c73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527281"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a><span data-ttu-id="139c7-103">Schreiben verwandter Ereignisse in einem Manifest-basierten Anbieter</span><span class="sxs-lookup"><span data-stu-id="139c7-103">Writing Related Events in a Manifest-based Provider</span></span>

<span data-ttu-id="139c7-104">Verwenden Sie die [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) -Funktion, wenn mehrere Komponenten Ihre Ereignisse in einem End-to-End-Ablauf Verfolgungs Szenario miteinander verknüpfen möchten.</span><span class="sxs-lookup"><span data-stu-id="139c7-104">Use the [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) function when several components want to relate their events in an end-to-end tracing scenario.</span></span> <span data-ttu-id="139c7-105">Die Komponenten A, B und C arbeiten z. b. für eine verwandte Aktivität und möchten alle Ereignisse verknüpfen, die mit dieser Aktivität verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="139c7-105">For example, components A, B and C perform work on a related activity and want to link all the events related to that activity.</span></span>

<span data-ttu-id="139c7-106">Etw verwendet den lokalen Thread Speicher, um den Aktivitäts Bezeichner der vorherigen Komponente für die nächste Komponente verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="139c7-106">ETW uses thread local storage to make the previous component's activity identifier available to the next component.</span></span> <span data-ttu-id="139c7-107">Die Komponente ruft den Bezeichner der vorherigen Komponente aus dem lokalen Speicher ab und legt den zugehörigen Aktivitäts Bezeichner darauf fest.</span><span class="sxs-lookup"><span data-stu-id="139c7-107">The component retrieves the previous component's identifier from the local storage and sets the related activity identifier to it.</span></span> <span data-ttu-id="139c7-108">Der Consumer kann dann den zugehörigen Aktivitäts Bezeichner verwenden, um die Kette der Ereignisse von einer Komponente zum nächsten zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="139c7-108">The consumer can then use the related activity identifier to walk the chain of the events from one component to the next.</span></span>

 

 



