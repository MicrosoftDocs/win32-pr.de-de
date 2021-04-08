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
# <a name="event-schema"></a>Ereignisschema

Das Ereignis Schema definiert die folgenden Elemente und Typen, mit denen die Elemente und Attribute eines protokollierten Ereignisses identifiziert werden:

-   [Eventschema-Elemente](eventschema-elements.md)
-   [Einfache eventschema-Typen](eventschema-simple-types.md)
-   [Komplexe eventschema-Typen](eventschema-complex-types.md)

Der Abschnitt "Elemente" enthält die Namen der Elemente, die in einem protokollierten Ereignis gefunden werden. Informationen zu den einzelnen Elementen finden Sie jedoch unter dem komplexen Typ, der das Element enthält.

Der Windows SDK enthält das Schema in der \\ include- \\ Datei "Event. xsd".

Sie können dieses Schema verwenden, um die Elemente und Attribute zu identifizieren, wenn Sie die [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) -Funktion aufrufen, um bestimmte Abschnitte oder Eigenschaften des Ereignisses zu Rendering. Ein Beispiel für die Verwendung dieses Schemas beim Rendern von Ereignissen finden Sie unter [Rendern von Ereignissen](rendering-events.md).

Zusätzlich zum Ereignis Schema definiert das Windows-Ereignisprotokoll auch die folgenden Schemas:

-   [Eventmanifest-Schema](eventmanifestschema-schema.md)– definiert die Elemente und Typen, die zum Schreiben eines Instrumentierungs Manifests verwendet werden.
-   [Abfrage Schema](queryschema-schema.md)– definiert die Elemente und Typen, mit denen eine Abfrage zum Abrufen von Ereignissen von einem oder mehreren Kanälen geschrieben wird.

 

 




