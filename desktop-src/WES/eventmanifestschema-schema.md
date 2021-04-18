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
# <a name="eventmanifest-schema"></a>Event Manifest-Schema

Das eventmanifest-Schema definiert die folgenden Elemente und Typen, mit denen Sie ein Instrumentations Manifest schreiben können:

-   [EventManifestSchema-Elemente](eventmanifestschema-elements.md)
-   [EventManifestSchema einfache Typen](eventmanifestschema-simple-types.md)
-   [Komplexe EventManifestSchema-Typen](eventmanifestschema-complex-types.md)

Der Abschnitt "Elemente" enthält die Namen der Elemente, die Sie im Manifest verwenden. Informationen zu den einzelnen Elementen finden Sie jedoch unter dem komplexen Typ, der das Element enthält.

Ein Instrumentations Manifest ist eine XML-Datei, die einen Ereignis Anbieter definiert, die Kanäle, auf die die Ereignisse geschrieben werden, die Ereignisse selbst, die Ereignis Filterkriterien, wie z. b. Ebenen, Tasks und Opcodes, und die lokalisierten Zeichen folgen, die beim Rendern der Ereignisse verwendet werden. Die Konvention besteht darin, ". man" als Erweiterung für Manifest-Dateien zu verwenden. Ausführliche Informationen zum Schreiben eines Manifests finden Sie unter [Schreiben eines Instrumentierungs Manifests](writing-an-instrumentation-manifest.md).

Die Windows SDK enthält das Schema in der \\ include- \\ Datei "eventman. xsd". Sie können das Manifest mit XSD validieren.

Zusätzlich zum eventmanifest-Schema definiert das Windows-Ereignisprotokoll auch die folgenden Schemas:

-   [Ereignis Schema](eventschema-schema.md)– definiert die Elemente und Typen, die zum Rendering eines Ereignisses verwendet werden.
-   [Abfrage Schema](queryschema-schema.md)– definiert die Elemente und Typen, mit denen eine Abfrage zum Abrufen von Ereignissen von einem oder mehreren Kanälen geschrieben wird.

 

 




