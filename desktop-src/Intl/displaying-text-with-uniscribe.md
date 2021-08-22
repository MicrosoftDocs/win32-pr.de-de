---
description: Ihre Anwendungen können Uniscribe-API-Funktionen verwenden, um Typografie und die Anzeige und Bearbeitung von internationalem Text zu unterstützen. Uniscribe verwendet den Absatz als Einheit für die Textanzeige, und die Uniscribe-Funktionalität muss für den gesamten Absatz verwendet werden.
ms.assetid: e1adc567-0445-4deb-8634-25653f82127c
title: Anzeigen von Text mit Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17caf7e7880a61bdf9afbaf6db5b60065b01d3d3960f2ed5629a007aa304b7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949605"
---
# <a name="displaying-text-with-uniscribe"></a>Anzeigen von Text mit Uniscribe

Ihre Anwendungen können Uniscribe-API-Funktionen verwenden, um Typografie und die Anzeige und Bearbeitung von internationalem Text zu unterstützen. Uniscribe verwendet den Absatz als Einheit für die Textanzeige, und die Uniscribe-Funktionalität muss für den gesamten Absatz verwendet werden.

Wenn Sie Uniscribe für die Anzeige von Text verwenden, muss eine Anwendung einen Formatierungsprozess ("Layout") durchgehen, der in der Regel Uniscribe verwendet. Die Anwendung unterteilt einen Text absatz in Zeichenfolgen mit dem gleichen Stil, der als "Runs" bezeichnet wird. Der Stil wird durch die bestimmte Implementierung bestimmt, enthält jedoch in der Regel Attribute wie Schriftart, Größe und Farbe. Beim Definieren von Läufen kann die Anwendung auch andere Informationen anwenden, z. B. Sprach- und Locale-Daten, die für die Verwendung mit lexikalischen Tools verwaltet werden. Eine Anwendung kann z. B. als separate Ausführung eine Stellung in einem hauptsächlich englischsprachigen Text behandeln, der auf Französisch gerendert wird.

Nachdem die Ausführungen für alle Absätze bestimmt wurden, teilt die Anwendung jeden Absatz in Zeichenfolgen auf, die das gleiche Skript und dieselbe Richtung ("Elemente") haben. Die Anwendung wendet die Elementinformationen an, um Ausführungen zu erzeugen, die in Skript und Richtung eindeutig sind und vollständig in ein einzelnes Element ("Bereiche") fallen.

Die Aufschlüsselung eines Elements in Bereiche ist etwas willkürlich, obwohl ein Bereich aus einem oder mehreren aufeinander folgenden skriptdefinierten, unteilbaren Zeichengruppen bestehen sollte, die als "Cluster" bezeichnet werden. Bei europäischen Sprachen entspricht ein Cluster in der Regel einem einzelnen Codepagezeichen oder Unicode-Codepunkt und besteht aus einem [einzelnen Symbol.](uniscribe-glossary.md) In Sprachen wie thailändisch ist ein Cluster jedoch eine Gruppierung von Glyphen und entspricht mehreren aufeinander folgenden Zeichen oder Codepunkten. Beispielsweise kann ein thailändisch-Cluster einen Konsonanten, einen Vokal und eine Tonmarkung enthalten. Damit Cluster nicht unterbricht, sollte die Anwendung in der Regel entweder die längsten Bereiche verwenden, die sie haben kann, oder ihre eigenen lexikalischen Informationen verwenden, um zwischen Bereichen an Stellen zu unterbrechen, die sich nicht in der Mitte eines Clusters befinden.

Wenn die Cluster in jedem Bereich identifiziert wurden, muss die Anwendung die Größe der einzelnen Cluster bestimmen. Uniscribe wird verwendet, um die Cluster zu summieren, um die Größe jedes Bereichs zu bestimmen. Anschließend summiert die Anwendung die Größen der Bereiche, bis sie eine Linie überlaufen, d.&a; den Rand erreichen. Der Bereich, der die Linie überläuft, wird zwischen der aktuellen zeile und der nächsten Zeile aufgeteilt. Für jede Zeile erstellt die Anwendung eine Karte von der visuellen Position zur logischen Position für jeden Bereich. Anschließend formt die Anwendung die Codepunkte für jeden Bereich in Glyphen, die sie anschließend positionieren und rendern kann.

Eine Anwendung führt das Textlayout nur einmal aus. Anschließend werden die Glyphen und Positionen entweder zu Anzeigezwecken gespeichert oder jedes Mal generiert, wenn der Text angezeigt wird, und der Kompromiss ist Geschwindigkeit und Arbeitsspeicher. Eine typische Anwendung implementiert den Layoutprozess einmal und generiert dann jedes Mal die Glyphen und Positionen, wenn sie den Text anzeigt.

Eine Anwendung, die [komplexe Skripts verwendet,](uniscribe-glossary.md) hat die folgenden Probleme mit einem einfachen Ansatz für Layout und Anzeige.

-   Die Breite eines komplexen Skriptzeichens hängt von seinem Kontext ab. Es ist nicht möglich, die Breite in einfachen Tabellen zu speichern.
-   Das Aufbrechen von Wörtern in Skripts wie Thai erfordert Wörterbuchunterstützung. Beispielsweise wird kein Trennzeichen zwischen thailändisch-Wörtern verwendet.
-   Arabisch, Hebräisch, Hebräisch, Urdu und andere [bidirektionale](uniscribe-glossary.md) Textsprachen erfordern eine Neuanordnung vor der Anzeige.
-   Häufig ist eine Form der Schriftarten-Zuordnung erforderlich, um komplexe Skripts einfach verwenden zu können.

Die Tatsache, dass Uniscribe den Absatz als Anzeigeeinheit verwendet, hilft der Anwendung, diese komplexen Skriptprobleme angemessen zu behandeln.

> [!Note]  
> Uniscribe muss für einen gesamten Absatz verwendet werden, auch wenn Abschnitte des Absatzes keine komplexen Skripts sind.

 

Wie in der folgenden Tabelle gezeigt, unterstützt Die Uniscribe-Version 1.6 oder höher mehrere Funktionen, die OpenType-Tags nutzen. Sie können durch die entsprechenden regulären Uniscribe-Funktionen ersetzt werden. Im Allgemeinen sollten Ihre Anwendungen vollständig mit Funktionen aus einer Gruppe oder der anderen gruppe arbeiten und nicht versuchen, Funktionen zu "mischen und zu kombinieren".



| Reguläre Uniscribe-Funktion             | Äquivalente OpenType-Funktion                           |
|----------------------------------------|--------------------------------------------------------|
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) | [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)     | [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)     |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)     | [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)     |



 

## <a name="lay-out-text-using-uniscribe"></a>Auslegen von Text mithilfe von Uniscribe

Ihre Anwendung kann die folgenden Schritte ausführen, um einen Textabdruck mit Uniscribe zu erstellen. Bei diesem Verfahren wird davon ausgegangen, dass die Anwendung den Absatz bereits in Läufe unterteilt hat.

1.  Rufen [**Sie ScriptRecordDigitSubsinformation**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) nur auf, wenn eine WM [**\_ SETTINGCHANGE-Nachricht**](../winmsg/wm-settingchange.md) gestartet oder empfangen wird.
2.  (Optional) Rufen [**Sie ScriptIsComplex auf,**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex) um zu ermitteln, ob der Absatz eine komplexe Verarbeitung erfordert.
3.  (Optional) Wenn Sie Uniscribe verwenden, um bidirektionalen Text und/oder die Ziffernersetzung zu verarbeiten, rufen Sie [**ScriptApplyDigitSubs analog**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) auf, um die [**SCRIPT \_ CONTROL-**](/windows/win32/api/usp10/ns-usp10-script_control) und [**SCRIPT \_ STATE-Strukturen**](/windows/win32/api/usp10/ns-usp10-script_state) als Eingaben für [**ScriptItemize vorzubereiten.**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) Wenn Sie diesen Schritt überspringen, aber trotzdem eine Ziffernersetzung erfordern, ersetzen Sie unicode U+0030 bis U+0039 (europäische Ziffern) durch nationale Ziffern. Informationen zur Ziffernersetzung finden Sie unter [Ziffernformen.](digit-shapes.md)
4.  Rufen Sie [**ScriptItemize auf,**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) um den Absatz in Elemente zu unterteilen. Wenn Uniscribe nicht für die Ziffernersetzung verwendet wird und die bidirektionale Reihenfolge bekannt ist, z. B. aufgrund des Tastaturlayouts, das zum Eingeben des Zeichens verwendet wird, rufen Sie **ScriptItemize auf.** Geben Sie im -Aufruf NULL-Zeiger für die [**SCRIPT \_ CONTROL- und**](/windows/win32/api/usp10/ns-usp10-script_control) SCRIPT [**\_ STATE-Strukturen**](/windows/win32/api/usp10/ns-usp10-script_state) an. Bei dieser Technik werden Elemente nur mithilfe der -Engine generiert, und die Elemente können mithilfe der Engine-Informationen neu angeordnet werden.
    > [!Note]  
    > In der Regel sollten Anwendungen, die nur mit Links-nach-Rechts-Skripts und ohne Ziffernersetzung arbeiten, NULL-Zeiger für die [**SCRIPT \_ CONTROL-**](/windows/win32/api/usp10/ns-usp10-script_control) und [**SCRIPT \_ STATE-Strukturen**](/windows/win32/api/usp10/ns-usp10-script_state) übergeben.

     

5.  Führen Sie die Elementinformationen mit den Ausführungsinformationen zusammen, um Bereiche zu erzeugen.
6.  Rufen [**Sie ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) auf, um Cluster zu identifizieren und Glyphen zu generieren.
7.  Wenn [**ScriptShape den**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) Code USP E SCRIPT NOT IN FONT oder S OK mit der Ausgabe mit fehlenden \_ \_ \_ \_ \_ \_ Glyphen zurückgibt, wählen Sie Zeichen aus einer anderen Schriftart aus. Ersetzen Sie entweder eine andere Schriftart, oder deaktivieren Sie die Strukturierung, indem Sie das **eScript-Member** der [**SCRIPT \_ ANALYSIS-Struktur,**](/windows/win32/api/usp10/ns-usp10-script_analysis) das an **ScriptShape** übergeben wird, auf SCRIPT \_ UNDEFINED festlegen. Weitere Informationen finden Sie unter [Verwenden des Schriftartfallbacks.](using-font-fallback.md)
8.  Rufen [**Sie ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) auf, um [höhere Breiten und](uniscribe-glossary.md) x- und y-Positionen für die Glyphen in jedem nachfolgenden Bereich zu generieren. Dies ist der erste Schritt, bei dem die Textgröße berücksichtigt wird.
9.  Summiert die Bereichsgrößen, bis die Zeile überläuft.
10. Unterbricht den Bereich an einer Wortgrenze mithilfe der **Elemente fSoftBreak** und **fWhiteSpace** in den logischen Attributen. Um einen Cluster mit nur einem Zeichen von der Ausführung abzubrechen, verwenden Sie die Informationen, die durch Aufrufen von [**ScriptBreak zurückgegeben werden.**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)
    > [!Note]  
    > Entscheiden Sie, ob der erste Codepunkt eines Bereichs ein Wortbruchpunkt sein soll, da es für das letzte Zeichen des vorherigen Bereichs erforderlich ist. Wenn ein Bereich beispielsweise mit einem Komma endet, betrachten Sie das erste Zeichen des nächsten Bereichs als Wortbruchpunkt.

     

11. Wiederholen Sie die Schritte 6 bis 10 für jede Zeile im Absatz. Wenn sie jedoch die letzte Ausführung in der Zeile durchbrechen, rufen Sie [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) auf, um den verbleibenden Teil der Ausführung bei der ersten Ausführung in der nächsten Zeile umzugestalten.

## <a name="display-text-using-uniscribe"></a>Anzeigen von Text mithilfe von Uniscribe

Ihre Anwendung kann die folgenden Schritte ausführen, um einen Text absatz anzuzeigen. Bei diesem Verfahren wird davon ausgegangen, dass die Anwendung den Text bereits festgelegt und die Glyphen und Positionen aus dem Layoutprozess nicht gespeichert hat. Wenn die Geschwindigkeit ein Problem ist, kann die Anwendung die Glyphen und Positionen aus der Layoutprozedur speichern und bei Schritt 2 in der Anzeigeprozedur beginnen.

> [!Note]  
> Die Anwendung kann Schritt 2 weglassen, wenn der Text keine Zeichen aus Skripts von rechts nach links enthält, keine bidirektionalen Steuerzeichen enthält und eine Basis-Einbettungsebene von links nach rechts verwendet.

 

1.  Führen Sie für jede Ausführung folgende Schritte aus:
    1.  Wenn sich der Stil seit der letzten Ausführung geändert hat, aktualisieren Sie das Handle auf den Gerätekontext, indem Sie es freigeben und erneut abrufen.
    2.  Rufen [**Sie ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) auf, um Glyphen für die Ausführung zu generieren.
    3.  Rufen [**Sie ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) auf, um eine höhere Breite und einen x,y-Offset für jedes Glyphen zu generieren.
2.  Gehen Sie wie folgt vor, um die richtige visuelle Reihenfolge für die In der Zeile zu erstellen:
    1.  Extrahieren Sie ein Array von bidirektionalen [Einbettungsebenen](uniscribe-glossary.md), eine pro Bereich. Die Einbettungsebene wird durch (SCRIPT \_ ITEM) si. ( \_SKRIPTANALYSE) a. (SCRIPT \_ STATE) s.uBidiLevel.
    2.  Übergeben Sie dieses Array an [**ScriptLayout,**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout) um eine Zuordnung visueller Positionen zu logischen Positionen zu generieren.
3.  (Optional) Um den Text zu rechtfertigen, rufen Sie [**entweder ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify) auf, oder verwenden Sie spezielle Kenntnisse des Texts.
4.  Verwenden Sie die visual-zu-logical-Zuordnung, um die Läufe in visueller Reihenfolge anzuzeigen. Rufen Sie am linken Ende der Zeile [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) auf, um die Ausführung anzuzeigen, die durch den ersten Eintrag in der Karte angegeben wird. Rufen Sie für jeden nachfolgenden Eintrag in der Zuordnung **ScriptTextOut** auf, um die angegebene Ausführung rechts neben der zuvor angezeigten Ausführung anzuzeigen.

    Wenn Sie Schritt 2 weglassen, beginnen Sie am linken Ende der Zeile, und rufen Sie [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) auf, um die erste logische Ausführung anzuzeigen und dann jede logische Ausführung rechts von der vorherigen Ausführung anzuzeigen.

5.  Wiederholen Sie die obigen Schritte für alle Zeilen im Absatz.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
