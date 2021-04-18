---
title: Event Manifest-Schema
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 'Weitere Informationen finden Sie hier: eventmanifest-Schema'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 67e1c2e9b769cd26e81a71853037655220a27d1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368735"
---
# <a name="eventmanifest-schema"></a><span data-ttu-id="8e271-103">Event Manifest-Schema</span><span class="sxs-lookup"><span data-stu-id="8e271-103">EventManifest Schema</span></span>

<span data-ttu-id="8e271-104">Das eventmanifest-Schema definiert die folgenden Elemente und Typen, mit denen Sie ein Instrumentations Manifest schreiben können:</span><span class="sxs-lookup"><span data-stu-id="8e271-104">The EventManifest schema defines the following elements and types that you use to write an instrumentation manifest:</span></span>

-   [<span data-ttu-id="8e271-105">EventManifestSchema-Elemente</span><span class="sxs-lookup"><span data-stu-id="8e271-105">EventManifestSchema Elements</span></span>](eventmanifestschema-elements.md)
-   [<span data-ttu-id="8e271-106">EventManifestSchema einfache Typen</span><span class="sxs-lookup"><span data-stu-id="8e271-106">EventManifestSchema Simple Types</span></span>](eventmanifestschema-simple-types.md)
-   [<span data-ttu-id="8e271-107">Komplexe EventManifestSchema-Typen</span><span class="sxs-lookup"><span data-stu-id="8e271-107">EventManifestSchema Complex Types</span></span>](eventmanifestschema-complex-types.md)

<span data-ttu-id="8e271-108">Der Abschnitt "Elemente" enthält die Namen der Elemente, die Sie im Manifest verwenden. Informationen zu den einzelnen Elementen finden Sie jedoch unter dem komplexen Typ, der das Element enthält.</span><span class="sxs-lookup"><span data-stu-id="8e271-108">The elements section contains the names of the elements that you use in your manifest; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="8e271-109">Ein Instrumentations Manifest ist eine XML-Datei, die einen Ereignis Anbieter definiert, die Kanäle, auf die die Ereignisse geschrieben werden, die Ereignisse selbst, die Ereignis Filterkriterien, wie z. b. Ebenen, Tasks und Opcodes, und die lokalisierten Zeichen folgen, die beim Rendern der Ereignisse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e271-109">An instrumentation manifest is an XML file that defines an event provider, the channels to which the events are written, the events themselves, the event filtering criteria such as levels, tasks, and opcodes, and the localized strings used when rendering the events.</span></span> <span data-ttu-id="8e271-110">Die Konvention besteht darin, ". man" als Erweiterung für Manifest-Dateien zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e271-110">The convention is to use .man as the extension for manifest files.</span></span> <span data-ttu-id="8e271-111">Ausführliche Informationen zum Schreiben eines Manifests finden Sie unter [Schreiben eines Instrumentierungs Manifests](writing-an-instrumentation-manifest.md).</span><span class="sxs-lookup"><span data-stu-id="8e271-111">For details on writing a manifest, see [Writing an Instrumentation Manifest](writing-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="8e271-112">Die Windows SDK enthält das Schema in der \\ include- \\ Datei "eventman. xsd".</span><span class="sxs-lookup"><span data-stu-id="8e271-112">The Windows SDK includes the schema in the \\Include\\Eventman.xsd file.</span></span> <span data-ttu-id="8e271-113">Sie können das Manifest mit XSD validieren.</span><span class="sxs-lookup"><span data-stu-id="8e271-113">You can use the XSD to validate your manifest.</span></span>

<span data-ttu-id="8e271-114">Zusätzlich zum eventmanifest-Schema definiert das Windows-Ereignisprotokoll auch die folgenden Schemas:</span><span class="sxs-lookup"><span data-stu-id="8e271-114">In addition to the EventManifest schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="8e271-115">[Ereignis Schema](eventschema-schema.md)– definiert die Elemente und Typen, die zum Rendering eines Ereignisses verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e271-115">[Event Schema](eventschema-schema.md)—defines the elements and types used to render an event.</span></span>
-   <span data-ttu-id="8e271-116">[Abfrage Schema](queryschema-schema.md)– definiert die Elemente und Typen, mit denen eine Abfrage zum Abrufen von Ereignissen von einem oder mehreren Kanälen geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8e271-116">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




