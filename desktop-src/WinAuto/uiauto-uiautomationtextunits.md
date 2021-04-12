---
title: Texteinheiten für Benutzeroberflächenautomatisierung
description: In diesem Thema werden die von Microsoft UI Automation \ 32; unterstützten Text Einheiten beschrieben. TextRange-Steuerelement Muster. Benutzeroberflächenautomatisierungs-Anbieter und-Clients verwenden Text Einheiten, um den Betrag anzugeben, um den der Textbereich verschoben oder geändert werden soll.
ms.assetid: 3ec43a81-c4f1-4c73-865f-a60c751fc3fb
keywords:
- Benutzeroberflächen Automatisierung, Text Einheiten
- Text Einheiten, Informationen
- Benutzeroberflächen Automatisierung, Liste von Text Einheiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff4257c70b34cea01a149b30dff2bf2fbe691a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315267"
---
# <a name="ui-automation-text-units"></a>Benutzeroberflächenautomatisierungs-Text Einheiten

In diesem Thema werden die vom Microsoft UI Automation [TextRange](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützten Text Einheiten beschrieben. Benutzeroberflächenautomatisierungs-Anbieter und-Clients verwenden Text Einheiten, um den Betrag anzugeben, um den der Textbereich verschoben oder geändert werden soll.

-   [Text Unit-API-Elemente](#text-unit-api-elements)
-   [Beschreibungen von Text Einheiten](#text-unit-descriptions)
    -   [Zeichen](#character)
    -   [Format](#format)
    -   [Word](#word)
    -   [Line](#line)
    -   [Paragraph](#paragraph)
    -   [Seite](#page)
    -   [Dokument](#document)
-   [Andere potenzielle Bereiche](#other-potential-ranges)
-   [Zugehörige Themen](#related-topics)

## <a name="text-unit-api-elements"></a>Text Unit-API-Elemente

Die Benutzeroberflächenautomatisierungs-API umfasst die folgenden Methoden, die eine angegebene Text Einheit erfordern:

-   [**ITextRangeProvider:: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)
-   [**ITextRangeProvider:: expandumenclosingunit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)
-   [**ITextRangeProvider:: "muveendpointbyunit"**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)
-   [**Iuiautomationtextrange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)
-   [**Iuiautomationtextrange:: expandumgarclosingunit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit)
-   [**Iuiautomationtextrange:: roveendpointbyunit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)

Die [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) -Enumeration definiert die Text Einheiten, die von Benutzeroberflächenautomatisierungs-Textbereichen unterstützt werden. Um die Text Einheit anzugeben, wird ein Member der [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) -Enumeration in einem Aufruf einer [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) -oder [**iuiautomationtextrange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) -Methode angegeben. Die Text Einheiten, von der kleinsten zum größten, lauten wie folgt:

-   [**TextUnit- \_ Zeichen**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit- \_ Format**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit- \_ Wort**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit- \_ Zeile**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit- \_ Absatz**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit- \_ Seite**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit- \_ Dokument**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

Wenn ein bestimmtes textbasiertes Steuerelement die angegebene Text Einheit nicht unterstützt, sollte der Anbieter reagieren, indem er die nächste größere Text Einheit ersetzt, die vom-Steuerelement unterstützt wird. Wenn z. b. [**TextUnit- \_ Absatz**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) angegeben, aber nicht unterstützt wird, kann die Methode die [**TextUnit- \_ Seite**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) oder das [**TextUnit- \_ Dokument**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)ersetzen.

Die linguistischen Merkmale des Quell Texts können es einem Anbieter erschweren, Text Begrenzungen basierend auf der angegebenen Text Einheit zu bestimmen. Zur Unterstützung der Bestimmung von Text Begrenzungen kann ein Anbieter uniwriter-API-Funktionen wie z. [**b. scriptbreak**](/windows/desktop/api/usp10/nf-usp10-scriptbreak)verwenden. Weitere Informationen finden Sie auf der MSDN-Website unter [uniscri.](/windows/desktop/Intl/uniscribe)

## <a name="endpoint-inclusivity"></a>Endpunkt-Inklusivität

Ein Text Einheiten-Endpunkt kann sowohl als [Start](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) Endpunkt als auch als [endendpunkt](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) für angrenzende Textbereiche desselben Typs fungieren. Wenn das Ende einer Text Einheit auch der Anfang einer anderen Text Einheit ist, gibt der Bereich, der den [endendpunkt](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) enthält, keine Attribute oder Objekte des angrenzenden Bereichs mit dem [Start](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) Endpunkt frei.

Beispielsweise enthält der Textstream "Hello **World**" zwei Word-Einheiten mit unterschiedlichen Schrift Gewichtungs Attributen (normal und Fett). In diesem Fall sind der [endendpunkt](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) der Word-Einheit "Hello" und der [Start](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) Endpunkt der Word-Einheit "**World**" identisch. Dies führt zu folgendem:

- Der Bereich von "Hello" weist nicht das Attribut "Bold" der Word-Einheit "World" auf und gibt den Wert des gemischten Attributs für das Attribut "Schriftart Weight Text" nicht zurück.
- Der Bereich "**World**" hat eine einzelne Schrift Breite (Fett) und gibt nicht die Schrift Breite der vorangehenden Word-Einheit "Hello" frei.

Im folgenden finden Sie ein weiteres Beispiel, in dem ein Textstream zwei Word-Einheiten enthält, von denen einer ein Link ist: `[Foo]() Bar` . In diesem Fall sind der [endendpunkt](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) der Word-Einheit `[Foo]()` und der [Start](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) Endpunkt der Word-Einheit "Bar" identisch. Dies führt zu folgendem:

- Der Link gehört zum Textbereich, der "foo" enthält.
- Der Link ist ein untergeordnetes Element des Text Bereichs "foo" und wird von [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider)eingeschlossen.
- Der Textbereich "Bar" weist keine untergeordneten Elemente auf und wird von [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider)eingeschlossen.

**Weitere Hinweise:**

> Ein degenerierter (leerer) Bereich an einer Text Einheiten Grenze mit einem Textbereich desselben Typs nimmt die Eigenschaften der unmittelbar angrenzenden Text Einheit an.
>
> Durch Aufrufen von [iuiautomationtextrange:: expandtotenclosingunit](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit
) für einen degenerierten Bereich an einer Text Einheiten Grenze mit einem Textbereich desselben Typs wird der degenerierte Bereich auf die folgende Text Einheit erweitert.

## <a name="text-unit-descriptions"></a>Beschreibungen von Text Einheiten

In diesem Abschnitt werden die einzelnen von der Benutzeroberflächen Automatisierung unterstützten Text Einheiten beschrieben.

### <a name="character"></a>Zeichen

[**TextUnit \_ Das Zeichen**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) ist eine linguistische Text Einheit, die ein einzelnes Zeichen darstellt. Die linguistische Definition eines Zeichens variiert je nach Sprache. Bei US-Englisch wird ein Zeichen in der Regel durch ein Leerzeichen oder ein anderes Zeichen, z. b. ein Satzzeichen, eine Zahl oder einen Buchstaben, begrenzt.

Steuerzeichen, wie z. b. Wagen Rückläufe und Unicode-Zeichen von links nach rechts (LTM), sollten nicht als Zeichen betrachtet werden, können jedoch in einen Textbereich eingeschlossen werden, der auf der Grundlage der Zeichen Text Einheit normalisiert wird.

Interpunktions Zeichen und Wort Umbruch Zeichen, wie z. b. Leerzeichen, sollten als Zeichen betrachtet werden.

### <a name="format"></a>Format

[**TextUnit \_ Das Format**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) wird verwendet, um die Begrenzung eines Text Bereichs basierend auf den Formatierungs Attributen des Texts zu positionieren. Wenn ein Textbereich z. b. aktuell auf einem einzelnen Zeichen eines Worts positioniert ist, wird der Textbereich durch Angeben des **TextUnit- \_ Formats** in einem Aufruf von [**iuiautomationtextrange:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) erweitert, sodass der gesamte Text, der alle gleichen Attribute wie das einzelne Zeichen enthält, eingeschlossen wird. Der resultierende Textbereich kann das gesamte Wort enthalten. Außerdem wird bei Verwendung der Formatierungs Text Einheit ein Textbereich nicht über die Grenze eines eingebetteten Objekts, wie z. b. ein Bild oder einen Hyperlink, erweitert.

Im Gegensatz zu anderen Text Einheiten, die die Text Einheiten enthalten, die kleiner als sich selbst sind, kann das [**TextUnit- \_ Format**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) kleiner oder größer als die anderen Einheiten sein. Wenn z. b. ein gesamtes Dokument die gleichen Text Attribute aufweist und keine eingebetteten Objekte enthält, würde durch das Erweitern eines Text Bereichs im **TextUnit- \_ Format** ein neuer Bereich erstellt werden, der das gesamte Dokument umfasst, während beim Erweitern des Text Bereichs durch [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) ein kleinerer Bereich erstellt wird.

### <a name="word"></a>Word

[**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) ist eine linguistische Text Einheit, die ein einzelnes ganzes Wort darstellt. Die linguistische Definition eines Worts variiert je nach Sprache. Für Englisch (USA) werden Wörter in der Regel von Leerzeichen oder Interpunktions Zeichen begrenzt.

Wenn [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) verwendet wird, um die Begrenzung eines Text Bereichs festzulegen, sollte der resultierende Textbereich alle Wort Umbruch Zeichen enthalten, die am Ende des Worts vorhanden sind, aber vor dem Anfang des nächsten Worts.

### <a name="line"></a>Zeile

[**TextUnit \_ "Line**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) " ist eine Textzeile, die eine einzelne Textzeile darstellt, wie im Viewport des Steuer Elements dargestellt. Bei der Verwendung der **TextUnit- \_ Linie** zum Festlegen der Grenze eines Text Bereichs sollte ein Anbieter die Grenze unmittelbar nach dem Punkt festlegen, an dem ein Steuerzeichen die Linie umbricht, oder wenn der Viewport des Steuer Elements den Text in eine neue Zeile umschließt. Die Grenze sollte festgelegt werden, wenn eine neue Zeile beginnt.

### <a name="paragraph"></a>Paragraph

[**TextUnit \_ Paragraph**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) ist eine linguistische Text Einheit, die einen vollständigen Absatz darstellt. Ein Absatz sollte direkt vor dem ersten Zeichen eines Absatzes beginnen und in der Regel unmittelbar nach dem letzten Zeichen enden. Alle leeren Zeilen, die auf einen Absatz folgen, sollten in den Absatz eingefügt werden, es sei denn, etwas in der Text Quelle zeigt andernfalls an. In der Regel markiert die Endgrenze eines Absatzes auch die endbegrenzung einer [**TextUnit- \_ Zeilen**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) Text Einheit.

### <a name="page"></a>Seite

[**TextUnit \_ Die Seite**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) stellt eine vollständige Textseite eines Dokuments dar. Die Begrenzungen einer Seite sollten an den unmittelbaren Stellen festgelegt werden, an denen eine Seite beginnt und endet.

### <a name="document"></a>Dokument

[**TextUnit \_ Dokument**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) stellt den gesamten Inhalt eines Dokuments dar, wie vom [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützt. Außerhalb eines Text Bereichs, der ein Dokument enthält, sollte kein Text vorhanden sein. Alle Objekte, die in ein Dokument eingefügt werden, z. b. Anmerkungen zu einer Seite, die eine Seiten Grenze überschreiten, sollten als eingebettete Objekte des Dokuments behandelt werden und sind nicht Teil des Text Inhalts des Dokuments.

## <a name="other-potential-ranges"></a>Andere potenzielle Bereiche

Die aktuelle [TextRange](uiauto-implementingtextandtextrange.md) -Steuerelement Muster Spezifikation lässt nicht zu, dass neue Text Einheiten Werte der [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) -Enumeration hinzugefügt werden, und es ist auch nicht möglich, die vorhandenen Text Einheiten Werte neu zu definieren. Um andere potenzielle Bereiche (z. b. Header und Anmerkungen) verfügbar zu machen, sollte ein Anbieter diese Bereiche als eingebettete Objekte mit einem zugeordneten Textbereich verfügbar machen. Auf diese Weise können Sie auch Unterstützung für die entsprechenden Steuerelement Muster hinzufügen. Diese Lösung ist flexibler und erweiterbar als das Definieren neuer Text Einheiten.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Referenz

[TextPatternRangeEndpoint](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

[ITextRangeProvider:: GetChildren](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getchildren)





### <a name="conceptual"></a>Konzept

[Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)

[Arbeiten mit Text basierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)