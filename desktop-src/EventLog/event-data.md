---
description: Jedem Ereignis können ereignisspezifische Daten zugeordnet werden.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Ereignisdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459377d9cdf78fba46133b494723008df025caad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357404"
---
# <a name="event-data"></a><span data-ttu-id="961ed-103">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="961ed-103">Event Data</span></span>

<span data-ttu-id="961ed-104">Jedem Ereignis können ereignisspezifische Daten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="961ed-104">Each event can have event-specific data associated with it.</span></span> <span data-ttu-id="961ed-105">Die Ereignisanzeige interpretiert diese Daten nicht. Es werden zusätzliche Daten nur in einem kombinierten Hexadezimal-und Textformat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="961ed-105">The Event Viewer does not interpret this data; it displays extra data only in a combined hexadecimal and text format.</span></span> <span data-ttu-id="961ed-106">Der maximale Grenzwert für die Größe eines Ereignisses in der gerade Protokollierung beträgt 0x3ffff bytes.</span><span class="sxs-lookup"><span data-stu-id="961ed-106">The maximum limit on the size of an event in the even log is 0x3FFFF bytes.</span></span> <span data-ttu-id="961ed-107">Verwenden Sie daher ereignisspezifische Daten sparsam, darunter auch, wenn Sie sicher sind, dass Sie für das Debuggen eines Problems hilfreich sein werden.</span><span class="sxs-lookup"><span data-stu-id="961ed-107">Therefore, use event-specific data sparingly, including it only if you are sure it will be useful to someone debugging a problem.</span></span> <span data-ttu-id="961ed-108">Viele netzwerkbezogene Ereignisse enthalten beispielsweise Netzwerk Steuerungsblöcke (NCB) als ereignisspezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="961ed-108">For example, many network-related events include network control blocks (NCB) as event-specific data.</span></span>

<span data-ttu-id="961ed-109">Wenn Sie ereignisspezifische Daten verwenden, sollte der letzte Teil der Beschreibungs Zeichenfolge einen Hinweis zu den Informationen bereitstellen, die als ereignisspezifische Daten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="961ed-109">When you use event-specific data, the last part of its description string should provide a note about the information provided as event-specific data.</span></span> <span data-ttu-id="961ed-110">Beispielsweise könnte die Netzwerk Software einen Hinweis wie z. b. "(NCB ist die Ereignisdaten)" bereitstellen. Verwenden Sie als Konvention Klammern um diese Hinweise, wie in diesem Beispiel angegeben.</span><span class="sxs-lookup"><span data-stu-id="961ed-110">For example, the network software could provide a note such as: "(The NCB is the event data.)" As a convention, use parentheses around such remarks, as indicated in this example.</span></span>

<span data-ttu-id="961ed-111">Sie können auch ereignisspezifische Daten verwenden, um Informationen zu speichern, die von der Anwendung unabhängig vom Ereignisanzeige verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="961ed-111">You can also use event-specific data to store information the application can process independently of the Event Viewer.</span></span> <span data-ttu-id="961ed-112">Beispielsweise können Sie einen Viewer speziell für Ihre Ereignisse schreiben oder ein Programm schreiben, das das Protokoll scannt und einen Bericht erstellt, der Informationen aus den ereignisspezifischen Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="961ed-112">For example, you could write a viewer specifically for your events, or write a program that scans the log and creates a report that includes information from the event-specific data.</span></span>

 

 



