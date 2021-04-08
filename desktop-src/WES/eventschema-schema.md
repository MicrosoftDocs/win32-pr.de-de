---
title: Ereignisschema
ms.assetid: 36037697-b777-4e5c-99af-77964200a3e4
description: 'Weitere Informationen finden Sie hier: Ereignis Schema'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bfb26f6c71d544e0c0a6a4d833b40a5d15ae5485
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864979"
---
# <a name="event-schema"></a><span data-ttu-id="7a9e7-103">Ereignisschema</span><span class="sxs-lookup"><span data-stu-id="7a9e7-103">Event Schema</span></span>

<span data-ttu-id="7a9e7-104">Das Ereignis Schema definiert die folgenden Elemente und Typen, mit denen die Elemente und Attribute eines protokollierten Ereignisses identifiziert werden:</span><span class="sxs-lookup"><span data-stu-id="7a9e7-104">The Event schema defines the following elements and types that identify the elements and attributes of a logged event:</span></span>

-   [<span data-ttu-id="7a9e7-105">Eventschema-Elemente</span><span class="sxs-lookup"><span data-stu-id="7a9e7-105">EventSchema Elements</span></span>](eventschema-elements.md)
-   [<span data-ttu-id="7a9e7-106">Einfache eventschema-Typen</span><span class="sxs-lookup"><span data-stu-id="7a9e7-106">EventSchema Simple Types</span></span>](eventschema-simple-types.md)
-   [<span data-ttu-id="7a9e7-107">Komplexe eventschema-Typen</span><span class="sxs-lookup"><span data-stu-id="7a9e7-107">EventSchema Complex Types</span></span>](eventschema-complex-types.md)

<span data-ttu-id="7a9e7-108">Der Abschnitt "Elemente" enthält die Namen der Elemente, die in einem protokollierten Ereignis gefunden werden. Informationen zu den einzelnen Elementen finden Sie jedoch unter dem komplexen Typ, der das Element enthält.</span><span class="sxs-lookup"><span data-stu-id="7a9e7-108">The elements section contains the names of the elements that you would find in a logged events; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="7a9e7-109">Der Windows SDK enthält das Schema in der \\ include- \\ Datei "Event. xsd".</span><span class="sxs-lookup"><span data-stu-id="7a9e7-109">The Windows SDK includes the schema in the \\Include\\Event.xsd file.</span></span>

<span data-ttu-id="7a9e7-110">Sie können dieses Schema verwenden, um die Elemente und Attribute zu identifizieren, wenn Sie die [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) -Funktion aufrufen, um bestimmte Abschnitte oder Eigenschaften des Ereignisses zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="7a9e7-110">You can use this schema to identify the elements and attributes when calling the [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function to render specific sections or properties of the event.</span></span> <span data-ttu-id="7a9e7-111">Ein Beispiel für die Verwendung dieses Schemas beim Rendern von Ereignissen finden Sie unter [Rendern von Ereignissen](rendering-events.md).</span><span class="sxs-lookup"><span data-stu-id="7a9e7-111">For an example that shows how to use this schema when rendering events, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="7a9e7-112">Zusätzlich zum Ereignis Schema definiert das Windows-Ereignisprotokoll auch die folgenden Schemas:</span><span class="sxs-lookup"><span data-stu-id="7a9e7-112">In addition to the Event schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="7a9e7-113">[Eventmanifest-Schema](eventmanifestschema-schema.md)– definiert die Elemente und Typen, die zum Schreiben eines Instrumentierungs Manifests verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a9e7-113">[EventManifest Schema](eventmanifestschema-schema.md)—defines the elements and types used to write an instrumentation manifest.</span></span>
-   <span data-ttu-id="7a9e7-114">[Abfrage Schema](queryschema-schema.md)– definiert die Elemente und Typen, mit denen eine Abfrage zum Abrufen von Ereignissen von einem oder mehreren Kanälen geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7a9e7-114">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




