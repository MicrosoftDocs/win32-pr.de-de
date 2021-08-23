---
title: Texteinheiten für Benutzeroberflächenautomatisierung
description: In diesem Thema werden die Vom Microsoft-Benutzeroberflächenautomatisierung \ 32; unterstützten Texteinheiten beschrieben. TextRange-Steuerelementmuster. Benutzeroberflächenautomatisierung und Clients verwenden Texteinheiten, um den Betrag anzugeben, um den die Größe eines Textbereichs bewegt oder geändert werden soll.
ms.assetid: 3ec43a81-c4f1-4c73-865f-a60c751fc3fb
keywords:
- Benutzeroberflächenautomatisierung,Texteinheiten
- Texteinheiten,About
- Benutzeroberflächenautomatisierung,Liste der Texteinheiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5c40604f3c524c1e9f3bcdb36458e099563eb7279fa61133dcfa7ea3fde90b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118824163"
---
# <a name="ui-automation-text-units"></a>Benutzeroberflächenautomatisierung Texteinheiten

In diesem Thema werden die Texteinheiten beschrieben, die vom Microsoft Benutzeroberflächenautomatisierung [TextRange-Steuerelementmuster](uiauto-implementingtextandtextrange.md) unterstützt werden. Benutzeroberflächenautomatisierung und Clients verwenden Texteinheiten, um den Betrag anzugeben, um den die Größe eines Textbereichs bewegt oder geändert werden soll.

-   [Text Unit API Elements](#text-unit-api-elements)
-   [Beschreibungen von Texteinheiten](#text-unit-descriptions)
    -   [Zeichen](#character)
    -   [Format](#format)
    -   [Word](#word)
    -   [Linie](#line)
    -   [Paragraph](#paragraph)
    -   [Seite](#page)
    -   [Dokument](#document)
-   [Andere potenzielle Bereiche](#other-potential-ranges)
-   [Zugehörige Themen](#related-topics)

## <a name="text-unit-api-elements"></a>TEXT UNIT-API-Elemente

Die Benutzeroberflächenautomatisierung-API enthält die folgenden Methoden, für die eine Texteinheit angegeben werden muss:

-   [**ITextRangeProvider::Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)
-   [**ITextRangeProvider::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)
-   [**ITextRangeProvider::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)
-   [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)
-   [**IUIAutomationTextRange::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit)
-   [**IUIAutomationTextRange::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)

Die [**TextUnit-Enumeration**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) definiert die Texteinheiten, die von Benutzeroberflächenautomatisierung unterstützt werden. Um die Texteinheit anzugeben, wird ein Member der [**TextUnit-Enumeration**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) in einem Aufruf einer [**ITextRangeProvider-**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) oder [**IUIAutomationTextRange-Methode**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) angegeben. Die Texteinheiten vom kleinsten zum größten sind wie folgt:

-   [**\_TextUnit-Zeichen**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_TextUnit-Format**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit \_ Line**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_TextUnit-Absatz**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_TextUnit-Seite**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_TextUnit-Dokument**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

Wenn ein bestimmtes textbasiertes Steuerelement die angegebene Texteinheit nicht unterstützt, sollte der Anbieter antworten, indem er die nächste größere Texteinheit, die vom -Steuerelement unterstützt wird, durch die nächste größere Texteinheit substituiert. Wenn beispielsweise [**TextUnit \_ Paragraph**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) angegeben, aber nicht unterstützt wird, kann die -Methode [**TextUnit \_ Page**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) oder [**TextUnit Document \_ ersetzen.**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

Die linguistischen Merkmale des Quelltexts können es einem Anbieter erschweren, Textgrenzen basierend auf der angegebenen Texteinheit zu bestimmen. Um Hilfe beim Bestimmen von Textgrenzen zu erhalten, kann ein Anbieter Uniscribe-API-Funktionen wie [**ScriptBreak verwenden.**](/windows/desktop/api/usp10/nf-usp10-scriptbreak) Weitere Informationen finden Sie auf der [MSDN-Website unter Uniscribe.](/windows/desktop/Intl/uniscribe)

## <a name="endpoint-inclusivity"></a>Endpunktneigung

Ein Texteinheitsendpunkt [](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) kann sowohl als Startendpunkt als auch als [Endendpunkt](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) für angrenzende Textbereiche desselben Typs dienen. Wenn das Ende einer Texteinheit auch der Anfang einer anderen [](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) Texteinheit ist, teilt der Bereich, der den Endpunkt End enthält, keine Attribute oder Objekte des angrenzenden Bereichs, der den [Startendpunkt](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) enthält.

Beispielsweise enthält der Textstream "Hello **world"** zwei Worteinheiten mit unterschiedlichen Schriftgewichtungsattributen (normal und fett). In diesem Fall sind der [Endpunkt](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) End der Worteinheit "Hello" und der [Startendpunkt](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) der Worteinheit **"world"** identisch, was folgende Ergebnisse ergibt:

- Der Bereich von "Hello" teilt sich nicht das Fettdruckattribut der Worteinheit "world" und gibt nicht den wert des gemischten Attributs für das Textattribut der Schriftgewichtung zurück.
- Der Bereich von **"world"** hat eine einzelne Schriftgradung (fett) und teilt nicht die Schriftgewichtung der vorherigen Worteinheit "Hello".

Hier ist ein weiteres Beispiel, in dem ein Textstream zwei Worteinheiten enthält, von denen eine ein Link ist: `[Foo]() Bar` . In diesem Fall sind der [Endpunkt](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) End der Worteinheit und der Startendpunkt der Worteinheit "Bar" identisch. Dies führt `[Foo]()` zu [](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) Folgendem:

- Der Link gehört zum Textbereich, der "Foo" enthält.
- Der Link ist ein untergeordnetes Objekt des Textbereichs "Foo" und wird vom [ITextProvider eingeschlossen.](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider)
- Der Textbereich "Bar" hat keine unteren Und und wird vom [ITextProvider eingeschlossen.](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider)

**Zusätzliche Hinweise:**

> Ein degeneriertes (leeres) Feld an einer Texteinheitsgrenze mit einem Textbereich desselben Typs setzt Eigenschaften der unmittelbar angrenzenden Texteinheit voraus.
>
> Durch Aufrufen von [IUIAutomationTextRange::ExpandToEnclosingUnit](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit
) für einen degenerierten Bereich an einer Texteinheitsgrenze mit einem Textbereich desselben Typs wird der degenerierte Bereich auf die folgende Texteinheit erweitert.

## <a name="text-unit-descriptions"></a>Beschreibungen von Texteinheiten

In diesem Abschnitt werden die einzelnen Texteinheiten beschrieben, die von der Benutzeroberflächenautomatisierung.

### <a name="character"></a>Zeichen

[**TextUnit \_ Character**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) ist eine linguistische Texteinheit, die ein einzelnes Zeichen darstellt. Die linguistische Definition eines Zeichens variiert je nach Sprache. Für ENGLISCH (USA) wird ein Zeichen in der Regel durch ein Leerzeichen oder ein anderes Zeichen umgrenzt, z. B. ein Interpunktionszeichen, eine Zahl oder ein Buchstabe.

Steuerzeichen wie Wagenrücklauf und die Unicode-Links-nach-Rechts-Markierung (LTM) sollten nicht als Zeichen betrachtet werden, sondern können in einem Textbereich enthalten sein, der basierend auf der Zeichentexteinheit normalisiert wird.

Interpunktionszeichen und Wörterbruchzeichen wie Leerzeichen sollten als Zeichen betrachtet werden.

### <a name="format"></a>Format

[**TextUnit \_ Das Format**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) wird verwendet, um die Begrenzung eines Textbereichs basierend auf den Formatierungsattributen des Texts zu positionieren. Wenn beispielsweise ein Textbereich derzeit auf einem einzelnen Zeichen eines Worts positioniert ist, wird der Textbereich durch Angabe von **TextUnit \_ Format** in einem Aufruf von [**IUIAutomationTextRange::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) erweitert, um den text-Bereich zu erweitern, der dieselben Attribute wie das einzelne Zeichen enthält. Der resultierende Textbereich kann das gesamte Wort enthalten oder nicht. Außerdem erweitert die Verwendung der Formattexteinheit keinen Textbereich über die Grenzen eines eingebetteten Objekts, z. B. eines Bilds oder Links.

Im Gegensatz zu den anderen Texteinheiten, die die kleineren Texteinheiten als sie selbst enthalten, kann [**TextUnit \_ Format**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) kleiner oder größer als die anderen Einheiten sein. Wenn beispielsweise ein gesamtes Dokument die gleichen Textattribute hat und keine eingebetteten Objekte enthält, würde das Erweitern eines Textbereichs um **das \_ TextUnit-Format** einen neuen Bereich erstellen, der das gesamte Dokument umfasst, während das Erweitern des Textbereichs um [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) einen kleineren Bereich erzeugen würde.

### <a name="word"></a>Word

[**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) ist eine linguistische Texteinheit, die ein einzelnes ganzes Wort darstellt. Die linguistische Definition eines Worts variiert je nach Sprache. Für englisch (USA) werden Wörter in der Regel durch Leerzeichen oder Interpunktionszeichen umgrenzt.

Wenn [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) zum Festlegen der Begrenzung eines Textbereichs verwendet wird, sollte der resultierende Textbereich alle Wörterbruchzeichen enthalten, die am Ende des Worts, aber vor dem Anfang des nächsten Worts vorhanden sind.

### <a name="line"></a>Linie

[**TextUnit \_ Zeile**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) ist eine Texteinheit, die eine einzelne Textzeile darstellt, wie sie im Viewport des Steuerelements dargestellt wird. Wenn **TextUnit \_ Line** zum Festlegen der Begrenzung eines Textbereichs verwendet wird, sollte ein Anbieter die Grenze unmittelbar nach dem Punkt festlegen, an dem ein Steuerzeichen die Zeile unterbricht, oder an dem der Viewport des Steuerelements den Text in eine neue Zeile umbricht. Die Grenze sollte an der Stelle festgelegt werden, an der eine neue Zeile beginnt.

### <a name="paragraph"></a>Paragraph

[**TextUnit \_ Absatz**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) ist eine linguistische Texteinheit, die einen vollständigen Absatz darstellt. Ein Absatz sollte direkt vor dem ersten Zeichen eines Absatzes beginnen und in der Regel direkt nach dem letzten Zeichen enden. Alle leeren Zeilen nach einem Absatz sollten mit dem Absatz zusammengeführt werden, es sei denn, etwas in der Textquelle gibt etwas anderes an. In der Regel markiert die Endgrenze eines Absatzes auch die Endgrenze einer [**Texteinheit von TextUnit \_ Line.**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

### <a name="page"></a>Seite

[**TextUnit \_ Die Seite**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) stellt eine vollständige Textseite eines Dokuments dar. Die Grenzen einer Seite sollten an den unmittelbaren Punkten festgelegt werden, an denen eine Seite beginnt und endet.

### <a name="document"></a>Dokument

[**TextUnit \_ Das**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) Dokument stellt den gesamten Inhalt eines Dokuments dar, wie vom [Text-Steuerelementmuster](uiauto-implementingtextandtextrange.md) unterstützt. Außerhalb eines Textbereichs, der ein Dokument enthält, darf kein Text vorhanden sein. Alle Objekte, die in ein Dokument eingefügt werden, z. B. Anmerkungshinweise, die eine Seitengrenze überschreiten, sollten als eingebettete Objekte des Dokuments und nicht als Teil des Textinhalts des Dokuments behandelt werden.

## <a name="other-potential-ranges"></a>Andere potenzielle Bereiche

Die [](uiauto-implementingtextandtextrange.md) aktuelle TextRange-Steuerelementmusterspezifikation lässt nicht zu, dass der [**TextUnit-Enumeration**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) neue Texteinheitswerte hinzugefügt werden, und die vorhandenen Texteinheitswerte können nicht neu definiert werden. Um andere potenzielle Bereiche verfügbar zu machen, z. B. Header und Anmerkungen, sollte ein Anbieter diese Bereiche als eingebettete Objekte mit einem zugeordneten Textbereich verfügbar machen. Auf diese Weise können Sie auch Unterstützung für die entsprechenden Steuerelementmuster hinzufügen. Diese Lösung ist flexibler und erweiterbarer als das Definieren neuer Texteinheiten.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Verweis

[TextPatternRangeEndpoint](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

[ITextRangeProvider::GetChildren](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getchildren)





### <a name="conceptual"></a>Konzept

[Benutzeroberflächenautomatisierung-Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)

[Arbeiten mit textbasierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)