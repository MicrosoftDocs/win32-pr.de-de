---
description: Wenn Sie eine Vorschau bereitstellen, sollten die folgenden Richtlinien befolgt werden.
title: Richtlinien für Vorschauhandler
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2ed9250e06d2b970ba92bffd10bf80fc6495793b8a9b0237d257b45feb10a99a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719628"
---
# <a name="preview-handler-guidelines"></a>Richtlinien für Vorschauhandler

Wenn Sie eine Vorschau bereitstellen, sollten die folgenden Richtlinien befolgt werden.

-   Eine Vorschau sollte nur eine minimale Benutzeroberfläche enthalten– es handelt sich lediglich um eine Vorschauversion. Es sollte nur der Dateiinhalt angezeigt werden. Es sollten keine Dialogfelder, Begrüßungsbildschirme, Symbolleisten oder Aufgabenbereiche angezeigt werden. Der Lesebereich wird häufig zusammen mit der Suche verwendet, um eine Datei schnell zu identifizieren. Alles, was den Lesebereich überladen oder anderweitig von Dateiinhalten ablenkt oder Verzögerungen bei der Vorschauanzeige verursacht, sollte vermieden werden.
-   Die Vorschauversion sollte es dem Benutzer ermöglichen, im Dokument zu navigieren. Der Benutzer sollte auch in der Lage sein, Text auszuwählen und zu kopieren.
-   Die Vorschau sollte nicht speicherintensiv sein, nur minimale Ressourcen verbrauchen und eine schnelle Startzeit haben.
-   Die Ausführung aller Skripts und Makros in der Datei, für die die Vorschau angezeigt wird, sollte aus Sicherheits- und Datenschutzgründen blockiert werden.
-   Die Vorschauversion sollte Tastenkombinationen für die Navigation und Auswahl unterstützen, wie von der Anwendung unterstützt. Außerdem sollte ein Kontextmenü angezeigt werden, wenn mit der rechten Maustaste darauf geklickt wird.
-   Wenn eine Datei als Vorschau angezeigt wird, sollte die Vorschau die Datei selbst nicht sperren. Eine Datei kann gleichzeitig in der zugehörigen Anwendung in der Vorschau angezeigt und geöffnet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorschauhandler und Shell-Vorschauhost](preview-handlers.md)
</dt> <dt>

[Erstellen von Vorschauhandlern](building-preview-handlers.md)
</dt> </dl>

 

 



