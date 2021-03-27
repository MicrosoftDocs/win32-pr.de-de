---
description: Wenn Sie eine Vorschauversion bereitstellen, sollten die folgenden Richtlinien befolgt werden.
title: Vorschau der handlerrichtlinien
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e725d561056e78a88bd9eeabd00d90abda1f0343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866152"
---
# <a name="preview-handler-guidelines"></a>Vorschau der handlerrichtlinien

Wenn Sie eine Vorschauversion bereitstellen, sollten die folgenden Richtlinien befolgt werden.

-   Eine Vorschauversion sollte eine minimale Benutzeroberfläche enthalten – es handelt sich einfach um eine Vorschauversion. Es sollte nur der Inhalt der Datei angezeigt werden. Es sollten keine Dialogfelder, Begrüßungs Bildschirme, Symbolleisten oder Aufgabenbereiche angezeigt werden. Der Lesebereich wird in der Regel zusammen mit der Suche verwendet, um eine Datei schnell zu identifizieren. Alle Elemente, die den Lesebereich gruppieren oder anderweitig aus Dateiinhalten entfernt oder Verzögerungen in der Vorschau Anzeige verursachen, sollten vermieden werden.
-   Die Vorschau sollte dem Benutzer ermöglichen, im Dokument zu navigieren. Der Benutzer sollte außerdem in der Lage sein, Text auszuwählen und zu kopieren.
-   Die Vorschau sollte nicht Arbeitsspeicher intensiv sein, sollte nur minimale Ressourcen beanspruchen und sollte über eine schnelle Startzeit verfügen.
-   Alle Skripts und Makros in der Datei, die in der Vorschau angezeigt werden, sollten aus Sicherheits-und Datenschutzgründen nicht ausgeführt werden.
-   Die Vorschauversion sollte die von der Anwendung unterstützten Tastaturbeschleuniger für Navigation und Auswahl unterstützen. Es sollte auch ein Kontextmenü angezeigt werden, wenn mit der rechten Maustaste geklickt wird.
-   Wenn eine Datei als Vorschau angezeigt wird, sollte die Vorschau der Datei nicht gesperrt werden. Eine Datei kann in der zugehörigen Anwendung in der Vorschau angezeigt und geöffnet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorschau Handler und Shell-Vorschau Host](preview-handlers.md)
</dt> <dt>

[Entwickeln von Vorschau Handlern](building-preview-handlers.md)
</dt> </dl>

 

 



