---
title: Ereignisschema
ms.assetid: 36037697-b777-4e5c-99af-77964200a3e4
description: Weitere Informationen finden Sie unter Ereignisschema.
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c08e22ad44cb1eec461ebe70361a8ee4640a7fdf5a7eb7040b2774a520be7a05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904360"
---
# <a name="event-schema"></a>Ereignisschema

Das Ereignisschema definiert die folgenden Elemente und Typen, die die Elemente und Attribute eines protokollierten Ereignisses identifizieren:

-   [EventSchema-Elemente](eventschema-elements.md)
-   [Einfache EventSchema-Typen](eventschema-simple-types.md)
-   [Komplexe EventSchema-Typen](eventschema-complex-types.md)

Der Abschnitt elements enthält die Namen der Elemente, die Sie in protokollierten Ereignissen finden würden. Um jedoch die Details für jedes Element zu erhalten, sehen Sie sich den komplexen Typ an, der das Element enthält.

Das Windows SDK enthält das Schema in der \\ Include \\ Event.xsd-Datei.

Sie können dieses Schema verwenden, um die Elemente und Attribute zu identifizieren, wenn Sie die [**EvtRender-Funktion**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) aufrufen, um bestimmte Abschnitte oder Eigenschaften des Ereignisses zu rendern. Ein Beispiel, das zeigt, wie dieses Schema beim Rendern von Ereignissen verwendet wird, finden Sie unter [Renderingereignisse](rendering-events.md).

Zusätzlich zum Ereignisschema definiert Windows Ereignisprotokoll auch die folgenden Schemas:

-   [EventManifest-Schema](eventmanifestschema-schema.md): Definiert die Elemente und Typen, die zum Schreiben eines Instrumentierungsmanifests verwendet werden.
-   [Abfrageschema](queryschema-schema.md): Definiert die Elemente und Typen, die zum Schreiben einer Abfrage verwendet werden, um Ereignisse aus einem oder mehr Kanälen abzurufen.

 

 




