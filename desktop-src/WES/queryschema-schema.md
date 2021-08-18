---
title: Abfrageschema
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 'Weitere Informationen zu: Abfrageschema'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 14beeaf8c4d739e490de972107fedf279e16e75b5401f63a709d43b03c338c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005170"
---
# <a name="query-schema"></a>Abfrageschema

Das Abfrageschema definiert die folgenden Elemente und Typen, mit denen Sie eine strukturierte XML-Abfrage schreiben können, um Ereignisse aus einem Kanal oder einer Protokolldatei abzurufen:

-   [QuerySchema-Elemente](queryschema-elements.md)
-   [Komplexe QuerySchema-Typen](queryschema-complex-types.md)

Der Abschnitt elements enthält die Namen der Elemente, die Sie in Ihrer Abfrage verwenden. Um jedoch die Details für jedes Element abzurufen, sehen Sie sich den komplexen Typ an, der das Element enthält.

Eine Abfrage kann einen oder mehrere XPath-Ausdrücke enthalten, die verwendet werden, um Ereignisse in das Abfrageresultset einzuschließen oder auszuschließen. Sie können Ereignisse aus mehreren Kanälen oder Protokolldateien abfragen, aber Sie können keine Kanäle und Protokolldateien mischen. Sie können eine Abfrage in jeder Funktion verwenden, die einen XPath verwendet (z. B. die [**Funktionen EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) oder [**EvtSubscribe).**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) Jeder angegebene XPath ist auf 32 Ausdrücke beschränkt. Ein Beispiel finden Sie unter [Nutzen von Ereignissen.](consuming-events.md)

Das Windows SDK enthält das Schema in der \\ \\ Include Query.xsd-Datei.

Zusätzlich zum Abfrageschema definiert Windows Ereignisprotokoll auch die folgenden Schemas:

-   [EventManifest-Schema](eventmanifestschema-schema.md): Definiert die Elemente und Typen, die zum Schreiben eines Instrumentierungsmanifests verwendet werden.
-   [Ereignisschema](eventschema-schema.md): Definiert die Elemente und Typen, die zum Rendern eines Ereignisses verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nutzen von Ereignissen](consuming-events.md)
</dt> </dl>

 

 




