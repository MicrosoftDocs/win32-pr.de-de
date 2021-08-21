---
description: 'Es gibt eine Reihe von Formaten, in denen Ink-Daten gespeichert werden können, einschließlich:'
ms.assetid: b08fba71-46cb-4419-9da5-a33a5b9a5ec0
title: Ink-Datenformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 088483400f6e4452f888793dd7b0ce78966050b65c35db9baf6e79c2f00061c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032308"
---
# <a name="ink-data-formats"></a>Ink-Datenformate

Es gibt eine Reihe von Formaten, in denen Ink-Daten gespeichert werden können, einschließlich:

-   Serialisiertes Ink-Format (ISF)
-   HTML
-   Rich-Text-Format (RTF)
-   Binärformat
-   Extensible Markup Language (XML)-basierte Formate

Verschiedene Formate sind unter verschiedenen Umständen anwendbar. Um am besten mit der Zwischenablage zu interagieren, sollten Anwendungen in der Lage sein, so viele verschiedene Formate wie möglich zu erkennen und zu generieren.

Das wichtigste und grundlegendste Format, das zum Speichern von Ink verwendet werden kann, ist serialisiertes Freihandformat (ISF). ISF bietet eine kompakte, aber vollständige Darstellung eines einzelnen [**Ink-Objekts.**](inkdisp-class.md)

Ein ebenso wichtiges Format ist HTML. Ink-Daten können in HTML so dargestellt werden, dass sie von Anwendungen, die Ink nicht erkennen, als Bild angezeigt werden können. Darüber hinaus wird die vollständige Genauigkeit der Ink-Datei beibehalten. Aus diesen Gründen und da es sich um ein allgemein verständliches Format handelt, das die Darstellung vieler verschiedener Inhaltstypen ermöglicht, empfiehlt Microsoft HTML als Format für die Freigabe von Ink.

Es ist auch möglich, Ink in anderen Formaten zu speichern. Wenn Sie RTF als Format verwenden, können Sie Ink in Anwendungen einfügen, die keine Ink-Daten erkennen, z. B. Microsoft Word 2002. Dies erfolgt durch Einbetten von OLE-Objekten, die Ink innerhalb der RTF enthalten. Es können auch andere Formate wie binäre oder XML-basierte Formate verwendet werden.

Die Formate, die Sie für eine bestimmte Anwendung zum Kopieren, Einfügen oder Serialisieren von Freiwesen auswählen, sollten auf den anwendungsspezifischen Anforderungen und Ressourcen basieren. Eine Anwendung sollte mindestens in der Lage sein, ISF zu kopieren und einfüge, was die niedrigste Interoperabilität der Ink-Funktion ermöglicht. Sowohl ISF als auch die Möglichkeit zum Kopieren und Einfügen von ISF sind in die Tablet PC-Plattform integriert. Viele Anwendungen müssen jedoch komplexere Inhalte darstellen, z. B. eine Auswahl, die mehrere Freitextobjekte oder formatierten Text enthält. In einem solchen Fall kann eine Anwendung HTML kopieren und einfügen. Dies ermöglicht ein Maximum an Flexibilität. HTML ist allgemein verständlich und einfach zu generieren. Schließlich sollten Anwendungen, die bereits RTF erzeugen oder stark mit älteren Anwendungen kommunizieren müssen, auch ein RTF-Format erzeugen.

> [!Note]  
> Während der gesamten Diskussion über ink-Interoperabilität sind Bitmap, ISF und GIF Bildformate. Das Text-Ink-Objekt (tInk) und das Sketch-Ink-Objekt (sInk) sind OLE-Objekte. Binär, HTML, XML und RTF sind Dokumentformate, in denen die Bilder verwendet werden.

 

Die Tablet PC-Plattform bietet APIs, mit deren Hilfe Sie diese Formate generieren und interpretieren können. Es gibt viele Optionen, die zusammen den Interoperabilitäts- und Persistenzanforderungen jeder Anwendung entsprechen sollten. Weitere Informationen zu Ink-Formaten finden Sie unter [Persistenzformate.](persistence-formats.md)

 

 



