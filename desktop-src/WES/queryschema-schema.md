---
title: Abfrage Schema
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 'Weitere Informationen finden Sie unter: Abfrage Schema'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aa9b6c842ff7acd874e8e467d07c31e298a63564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217416"
---
# <a name="query-schema"></a>Abfrage Schema

Das Abfrage Schema definiert die folgenden Elemente und Typen, die Sie verwenden können, um eine strukturierte XML-Abfrage zum Abrufen von Ereignissen aus einer Kanal-oder Protokolldatei zu schreiben:

-   [Queryschema-Elemente](queryschema-elements.md)
-   [Komplexe queryschema-Typen](queryschema-complex-types.md)

Der Abschnitt "Elemente" enthält die Namen der Elemente, die Sie in der Abfrage verwenden. Informationen zu den einzelnen Elementen finden Sie jedoch unter dem komplexen Typ, der das Element enthält.

Eine Abfrage kann einen oder mehrere XPath-Ausdrücke enthalten, die verwendet werden, um ein Ereignis in das Abfrageresultset einzuschließen oder auszuschließen. Sie können Ereignisse aus mehreren Kanälen oder Protokolldateien Abfragen, aber es ist nicht möglich, Kanäle und Protokolldateien zu mischen. Sie können eine Abfrage in jeder Funktion verwenden, die einen XPath annimmt (z. b. die Funktionen [**evtquery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) oder [**evtsubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) ). Jeder von Ihnen angegebene XPath ist auf 32-Ausdrücke beschränkt. Ein Beispiel finden Sie unter Verwenden von [Ereignissen](consuming-events.md).

Der Windows SDK enthält das Schema in der \\ include \\ Query. xsd-Datei.

Zusätzlich zum Abfrage Schema definiert das Windows-Ereignisprotokoll auch die folgenden Schemas:

-   [Eventmanifest-Schema](eventmanifestschema-schema.md)– definiert die Elemente und Typen, die zum Schreiben eines Instrumentierungs Manifests verwendet werden.
-   [Ereignis Schema](eventschema-schema.md)– definiert die Elemente und Typen, die zum Rendering eines Ereignisses verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verarbeiten von Ereignissen](consuming-events.md)
</dt> </dl>

 

 




