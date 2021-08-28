---
title: EventManifest-Schema
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: Weitere Informationen finden Sie unter EventManifest-Schema.
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8b282a3570c7ddc510f55c012a13b9438108693a3b6abba06de08ce1da59d734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055848"
---
# <a name="eventmanifest-schema"></a>EventManifest-Schema

Das EventManifest-Schema definiert die folgenden Elemente und Typen, die Sie zum Schreiben eines Instrumentierungsmanifests verwenden:

-   [EventManifestSchema-Elemente](eventmanifestschema-elements.md)
-   [Einfache EventManifestSchema-Typen](eventmanifestschema-simple-types.md)
-   [Komplexe EventManifestSchema-Typen](eventmanifestschema-complex-types.md)

Der Abschnitt elements enthält die Namen der Elemente, die Sie in Ihrem Manifest verwenden. Um jedoch die Details für jedes Element zu erhalten, sehen Sie sich den komplexen Typ an, der das Element enthält.

Ein Instrumentierungsmanifest ist eine XML-Datei, die einen Ereignisanbieter definiert, die Kanäle, in die die Ereignisse geschrieben werden, die Ereignisse selbst, die Kriterien für die Ereignisfilterung wie Ebenen, Tasks und Opcodes sowie die lokalisierten Zeichenfolgen, die beim Rendern der Ereignisse verwendet werden. Die Konvention besteht in der Verwendung von .man als Erweiterung für Manifestdateien. Weitere Informationen zum Schreiben eines Manifests finden Sie unter [Schreiben eines Instrumentierungsmanifests.](writing-an-instrumentation-manifest.md)

Das Windows SDK enthält das Schema in der \\ Datei \\ Eventman.xsd enthalten. Sie können die XSD verwenden, um Ihr Manifest zu überprüfen.

Zusätzlich zum EventManifest-Schema definiert Windows Ereignisprotokoll auch die folgenden Schemas:

-   [Ereignisschema](eventschema-schema.md): Definiert die Elemente und Typen, die zum Rendern eines Ereignisses verwendet werden.
-   [Abfrageschema](queryschema-schema.md): Definiert die Elemente und Typen, die zum Schreiben einer Abfrage verwendet werden, um Ereignisse aus einem oder mehr Kanälen abzurufen.

 

 




