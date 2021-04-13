---
description: 'Es gibt eine Reihe von Formaten, in denen frei Hand Daten gespeichert werden können, einschließlich:'
ms.assetid: b08fba71-46cb-4419-9da5-a33a5b9a5ec0
title: Frei Hand Datenformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ccd0ab298e183867a9c4f8018727f22e51e7bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342819"
---
# <a name="ink-data-formats"></a>Frei Hand Datenformate

Es gibt eine Reihe von Formaten, in denen frei Hand Daten gespeichert werden können, einschließlich:

-   Ink-serialisiertes Format (ISF)
-   HTML
-   Rich-Text-Format (RTF)
-   Binärformat
-   Extensible Markup Language (XML)-basierte Formate

Verschiedene Formate sind unter verschiedenen Bedingungen anwendbar. Für eine optimale Interaktion mit der Zwischenablage sollten Anwendungen beliebig viele verschiedene Formate erkennen und generieren können.

Das wichtigste und einfachste Format, das zum Speichern von frei Hand Eingaben verwendet werden kann, ist das frei Hand Format (Ink Serialized Format, ISF). ISF bietet eine kompakte, aber komplette Darstellung eines einzelnen [**Ink**](inkdisp-class.md) -Objekts.

Ein gleichermaßen wichtiges Format ist HTML. Frei Hand Daten können in HTML so dargestellt werden, dass Sie als Bild von Anwendungen angezeigt werden können, die keine frei Hand Eingaben erkennen. Außerdem wird die vollständige Treue der frei Hand Eingaben beibehalten. Aus diesen Gründen und da es sich um ein häufig verwendetes Format handelt, das die Darstellung vieler unterschiedlicher Inhaltstypen ermöglicht, empfiehlt Microsoft HTML als Format für die Freigabe von frei Hand Eingaben.

Es ist auch möglich, frei Hand Eingaben in anderen Formaten zu speichern. Wenn Sie RTF als Format verwenden, können Sie frei Hand Eingaben in Anwendungen einfügen, die keine frei Hand Eingaben erkennen, wie z. b. Microsoft Word 2002. Dies erfolgt durch Einbetten von OLE-Objekten, die frei Hand Eingaben innerhalb von RTF enthalten. Es können weiterhin andere Formate verwendet werden, z. b. Binär-oder XML-basierte Formate.

Die Formate, die Sie für eine bestimmte Anwendung zum Kopieren, einfügen oder Serialisieren von frei Hand Eingaben auswählen, sollten auf diesen anwendungsspezifischen Anforderungen und Ressourcen basieren. Eine Anwendung sollte zumindest in der Lage sein, ISF zu kopieren und einzufügen, was die niedrigste Ebene der frei Hand Interoperabilität ermöglicht. Sowohl ISF als auch die Möglichkeit, ISF zu kopieren und einzufügen, sind in die Tablet PC-Plattform integriert. Viele Anwendungen müssen jedoch komplexere Inhalte darstellen, wie z. b. eine Auswahl, die mehrere frei Hand Objekte oder formatierten Text enthält. In einem solchen Fall kann eine Anwendung HTML kopieren und einfügen. Dies ermöglicht eine maximale Flexibilität. HTML ist weitgehend verständlich und leicht zu generieren. Und schließlich sollten Anwendungen, die bereits RTF oder eine starke Notwendigkeit haben, mit älteren Anwendungen zu kommunizieren, auch ein RTF-Format liefern.

> [!Note]  
> Während der Erörterung von frei Hand Interoperabilität, Bitmap, ISF und GIF handelt es sich um Bildformate. Das Text Ink-Objekt (Tink) und das Sketch Ink-Objekt (Senke) sind OLE-Objekte. Binary, HTML, XML und RTF sind Dokumentformate, in denen die Bilder verbraucht werden.

 

Die Tablet PC-Plattform bietet APIs, die Ihnen helfen, diese Formate zu generieren und zu interpretieren. Es gibt viele Optionen, die für die Interoperabilitäts-und persistenzanforderungen einer beliebigen Anwendung geeignet sind. Weitere Informationen zu frei Hand Formaten finden Sie unter [Persistenzformate](persistence-formats.md).

 

 



