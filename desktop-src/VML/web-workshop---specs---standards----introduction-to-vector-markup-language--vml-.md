---
title: Vector Markup Language (VML)
description: Vector Markup Language (VML)
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Vector Markup Language (VML), Informationen
- VML (Vector Markup Language),Informationen
- Vektorgrafiken, Informationen
- Vektorgrafiken, Vector Markup Language (VML)
- Vector Markup Language (VML), World Wide Web Consortium (W3C)
- VML (Vector Markup Language),World Wide Web Consortium (W3C)
- Vektorgrafik, World Wide Web Consortium (W3C)
- Vektorgrafiken, VML-Vorteile
- Vector Markup Language (VML), Vorteile
- VML (Vector Markup Language),Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4637fff0550ce9c93e295c51fc529f62c370b8aa
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910258"
---
# <a name="vector-markup-language-vml"></a>Vector Markup Language (VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!NOTE]
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

Vector Markup Language (VML) ist ein XML-basiertes Austausch-, Bearbeitungs- und Übermittlungsformat für hochwertige Vektorgrafiken im Web, das die Anforderungen von Produktivitätsbenutzern und Grafikdesignexperten erfüllt. XML ist eine neue einfache, flexible und offene textbasierte Sprache, die HTML ergänzt. (Ausführliche Informationen zu XML finden Sie im [XML-Abschnitt](/documentation/?frame=true) der MSDN Library.)

VML wird derzeit von Microsoft Internet Explorer Version 5.0 oder höher unterstützt.

VML wurde dem W3C als Standard für Vektorgrafiken im Web vorgeschlagen (siehe [Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-VML)). Microsoft ist weiterhin für die Entwicklung und Implementierung von XML-basierten Technologien verantwortlich und arbeitet mit führenden Branchenpartnern (AutoDesk, Hewlett-Packard, Macromedia, Visio) und W3C zusammen, um webbasierte Standards zu fördern. Wir erwarten, dass wir mit dem W3C zusammenarbeiten, um letztendlich zu einem Standardformat für Vektorgrafiken im Web zu führen.

VML wird auch von Microsoft Office 2000 oder höher unterstützt. Microsoft Word, Microsoft Excel und Microsoft PowerPoint können zum Erstellen von VML-Grafiken verwendet werden.

### <a name="using-vml"></a>Verwenden von VML

Um VML in Ihren Webseiten zu verwenden, verwenden Sie ein Stilelement, um das VML-Verhalten zu importieren, wie im folgenden Code gezeigt.

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

Deklarieren Sie als Nächstes den VML-Namespace, wie im folgenden Codebeispiel gezeigt.

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

Fügen Sie abschließend VML-Elemente hinzu, um Visuelle Effekte zu definieren. Der folgende VML-Code erstellt z. B. ein rotes Oval.

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> Um optimale Ergebnisse bei der Verwendung von Dokumenten im strict-Modus zu erzielen, stellen Sie sicher, dass Ihr Markup gültig und wohlgeformt ist. Weitere Informationen finden Sie unter ! DOCTYPE-Referenzseite.


### <a name="benefits-of-vml"></a>Vorteile von VML

-   VML vereinfacht die Erstellung für Produktivitätsbenutzer und -autoren. Sie ermöglicht den Austausch (über Ausschneiden und Einfügen) und die nachfolgende Bearbeitung von Vektorgrafiken zwischen einer Vielzahl von Produktivitäts- und Entwurfsanwendungen.
-   VML bietet schnellere Grafikdownloads und eine bessere Benutzererfahrung. Sie ermöglicht die Übermittlung von qualitativ hochwertigen, vollständig integrierten, skalierbaren Vektorgrafiken im Web in einem offenen textbasierten Format. Anstatt auf Grafiken als externe Dateien zu verweisen, werden VML-Grafiken inline mit der HTML-Seite bereitgestellt, sodass sie mit der Benutzerinteraktion interagieren und skalieren können.
-   VML ist offen und standardbasiert. Es handelt sich um ein XML-basiertes Format. XML 1.0 ist eine offene, einfache, textbasierte Sprache zum Beschreiben strukturierter Daten im Web und ergänzt HTML für die Anzeige. VML unterstützt auch andere W3C-Standards, z. B. Cascading Stylesheets 2.0 (CSS), das Stilinformationen und 2D-Positionierung angibt, sowie das Dokumentobjektmodell (DOM), mit dem Entwickler konsistent mit Seitenelementen als Objekte interagieren können.

### <a name="for-additional-information"></a>Weitere Informationen

Weitere Informationen finden Sie unter den folgenden Links:

-   Antworten auf häufig gestellte Fragen zu VML finden Sie in den häufig gestellten Fragen zu [VML.](frequently-asked-questions-about-vml.yml)
-   Ein Tutorial zur Verwendung von VML auf Webseiten finden Sie unter [Verwenden von VML auf Webseiten,](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)das die an W3C übermittelte [VML-Spezifikation](https://www.w3.org/TR/NOTE-datetime.html) ergänzt.
-   Informationen zu VML-Datentypen finden Sie im Dokument [Grundlegende VML-Typen.](basic-vml-types.md)
-   Die vollständige Referenz zu VML, einschließlich Informationen zur Verwendung von VML mit Tags sowie zur Skripterstellung, finden Sie in der [VML-Referenz.](msdn-online-vml-introduction.md)