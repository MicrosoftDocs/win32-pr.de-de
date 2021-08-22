---
title: Informationen zum Textobjektmodell
description: Dieses Thema bietet eine umfassende Übersicht über tom.
ms.assetid: e304ec18-ec2e-4ea7-91c6-6f6ab63b72ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ec5c2f4156e7afce8765626a475a9b922ec428826d90789752c86f51bd69513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079448"
---
# <a name="about-text-object-model"></a>Informationen zum Textobjektmodell

Das Textobjektmodell (Text Object Model, TOM) definiert eine Reihe von Textbearbeitungsschnittstellen, die von mehreren Microsoft-Textlösungen in unterschiedlichem Grad unterstützt werden, einschließlich des Rich-Edit-Steuerelements. Dieses Thema bietet eine umfassende Übersicht über tom. Es werden die folgenden Themen erläutert.

-   [TOM-Objekte der Version 2](#tom-version-2-objects)
-   [TOM-Schnittstellenkonventionen](#tom-interface-conventions)
-   [Der tomBool-Typ](#the-tombool-type)
-   [Mathematischer BuildUp und Build Down](#math-buildup-and-build-down)
-   [TOM RTF](#tom-rtf)
-   [Suchen von Rich Text](#finding-rich-text)
-   [TOM-Barrierefreiheit](#tom-accessibility)
    -   [Schnittstelle aus ausgeführter Objekttabelle](#interface-from-running-object-table)
    -   [Schnittstelle aus Fenstermeldungen](#interface-from-window-messages)
    -   [Barrierefreiheitsorientierte Methoden](#accessibility-oriented-methods)
-   [Zeichen-Übereinstimmungssätze](#character-match-sets)

## <a name="tom-version-2-objects"></a>TOM-Objekte der Version 2

TOM Version 2 (TOM 2) erweitert das ursprüngliche Textobjektmodell. die neuen Schnittstellen werden von den alten abgeleitet. Die aktualisierte TOM-API bietet Unterstützung für neue Zeichen- und Absatzformateigenschaften, ein Tabellenmodell, Mehrfachauswahl und Inlineobjektunterstützung für Mathematik und Ruby.

Das TOM 2-Objekt der obersten Ebene wird von der [**ITextDocument2-Schnittstelle**](/windows/desktop/api/Tom/nn-tom-itextdocument2) definiert, die Methoden zum Erstellen und Abrufen von Objekten weiter unten in der Objekthierarchie enthält. Für die einfache Nur-Text-Verarbeitung können Sie ein [**ITextRange2-Objekt**](/windows/desktop/api/Tom/nn-tom-itextrange2) aus einem **ITextDocument2-Objekt** abrufen und damit die meisten Schritte unternehmen. Wenn Sie Rich-Text-Formatierung hinzufügen müssen, können Sie [**ITextFont2-**](/windows/desktop/api/Tom/nn-tom-itextfont2) und [**ITextPara2-Objekte**](/windows/desktop/api/Tom/nn-tom-itextpara2) aus einem **ITextRange2-Objekt** abrufen. **ITextFont2 stellt** die Programmierentsprechung des Dialogfelds Microsoft Word Formatschriftart und **ITextPara2** das Äquivalent zum Dialogfeld "Word-Format-Absatz" zur Verfügung.

Zusätzlich zu diesen drei Objekten auf niedrigerer Ebene verfügt TOM 2 über ein Auswahlobjekt ([**ITextSelection2**](/windows/win32/api/tom/nn-tom-itextselection2)), bei dem es sich um ein [**ITextRange2-Objekt**](/windows/desktop/api/Tom/nn-tom-itextrange2) mit Auswahlhervorhebung und einigen uiorientierten Methoden handelt.

Die Bereichs- und Auswahlobjekte enthalten bildschirmorientierte Methoden, mit denen Programme Text auf dem Bildschirm oder Text untersuchen können, der auf den Bildschirm gescrollt werden kann. Diese Funktionen helfen z.B., Personen mit sehbehinderter Sehbehinderung Text zugänglich zu machen.

Jede Schnittstelle mit dem Suffix 2 erbt von der entsprechenden Schnittstelle ohne das Suffix 2. Beispielsweise erbt [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) von [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument).

Die TOM 2-Objekte verfügen über die folgende Hierarchie.

``` syntax
ITextDocument2         Top-level editing object
    ITextRange2        Primary text interface: a range of text
        ITextFont2     Character-attribute interface
        ITextPara2     Paragraph-attribute interface
        ITextRow       Table interface
    ITextSelection2    Screen highlighted text range
        ITextRange2    Selection inherits all range methods
    ITextDisplays      Displays collection (not yet defined)
    ITextStrings       Rich-text strings collection
    ITextStoryRanges2  Enumerator for stories in document
```

Ein [**ITextDocument2-Objekt**](/windows/desktop/api/Tom/nn-tom-itextdocument2) beschreibt einen oder mehrere zusammenhängende Textbereiche, die als Storys *bezeichnet werden.* Storys stellen verschiedene Teile eines Dokuments dar, z. B. den Haupttext des Dokuments, Kopf- und Fußzeilen, Fußnoten, Anmerkungen und Rich-Text-Scratchpads. Bei der Übersetzung zwischen linear formatierten mathematischen Ausdrücken und einer integrierten Form wird ein Scratchpad-Story verwendet. Ein Scratchpad-Story wird auch verwendet, wenn der Inhalt eines Bereichs, der die aktuelle Kopierquelle ist, beim Ändern des Inhalts speichern wird.

Ein [**ITextRange2-Objekt**](/windows/desktop/api/Tom/nn-tom-itextrange2) wird durch seine Offsets für Start- und Endzeichenposition und ein Story-Objekt definiert. Sie ist nicht unabhängig vom übergeordneten Storyobjekt vorhanden, obwohl ihr Text in die Zwischenablage oder in andere Ziele kopiert werden kann. Ein Textbereichsobjekt ist anders als tabellen- und andere Bereichsobjekte, die durch andere Arten von Offsets definiert werden. Beispiel: Zeile/Spalte oder Grafikposition (x, y). Ein Textbereichsobjekt kann sich auf verschiedene Weise selbst ändern, ein Duplikat von sich selbst zurückgeben, und es kann befehlet werden, seine Start- und Endzeichenpositionen und seinen Storyzeiger auf die aktuelle Auswahl zu kopieren.

Ein explizites Story-Objekt ist nicht erforderlich, da ein [**ITextRange-Objekt**](/windows/desktop/api/Tom/nn-tom-itextrange) immer erstellt werden kann, um eine bestimmte Geschichte zu repräsentieren. Insbesondere kann das [**ITextDocument-Objekt**](/windows/desktop/api/Tom/nn-tom-itextdocument) ein [**ITextStoryRanges-Objekt**](/windows/desktop/api/Tom/nn-tom-itextstoryranges) erstellen, um die Storys im Dokument in Bezug auf Bereiche mit Werten für die Start- und Endzeichenposition zu aufzählen, die vollständige Storys beschreiben (z. B. 0 und **tomForward).**

Bei einem [**ITextStoryRanges2-Objekt**](/windows/desktop/api/Tom/nn-tom-itextstoryranges2) ist kein explizites Story-Objekt erforderlich, da jede Story von einem [**ITextRange2-Objekt beschrieben**](/windows/desktop/api/Tom/nn-tom-itextrange2) wird. Insbesondere kann das [**ITextDocument2-Objekt**](/windows/desktop/api/tom/nn-tom-itextdocument2) ein [**ITextStoryRanges2-Objekt**](/windows/desktop/api/tom/nn-tom-itextstoryranges2) erstellen, um die Storys im Dokument in Bezug auf Bereiche mit Werten für die Start- und Endzeichenposition aufzählen zu können, die vollständige Storys beschreiben (z. B. 0 und **tomForward).**

Die [**ITextRow-Schnittstelle**](/windows/desktop/api/Tom/nn-tom-itextrow) bietet zusammen mit den [**Methoden ITextRange::Move**](/windows/desktop/api/Tom/nf-tom-itextrange-move) und [**ITextRange::Expand**](/windows/desktop/api/Tom/nf-tom-itextrange-expand) die Möglichkeit zum Einfügen, Abfragen und Ändern von Tabellen.

## <a name="tom-interface-conventions"></a>TOM-Schnittstellenkonventionen

Alle TOM-Methoden geben **HRESULT-Werte** zurück. Im Allgemeinen geben die TOM-Methoden die folgenden Standardwerte zurück.

-   E \_ OUTOFMEMORY
-   E \_ INVALIDARG
-   E \_ NOTIMPL
-   E \_ FILENOTFOUND
-   E \_ ACCESSDENIED
-   E \_ FAIL
-   CO \_ E \_ VERÖFFENTLICHT
-   NOERROR (identisch mit S \_ OK)
-   S \_ FALSE

Beachten Sie, dass das TOM-Objekt nicht mehr verwendet werden kann, wenn die bearbeitungsinstanz, die einem TOM-Objekt wie [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) zugeordnet ist, gelöscht wird und alle zugehörigen Methoden CO \_ E RELEASED \_ zurückgeben.

Zusätzlich zu den **HRESULT-Rückgabewerten** enthalten viele Methoden Out-Parameter, die Zeiger sind, die zum Zurückgeben von Werten verwendet werden. Für alle Schnittstellen sollten Sie alle Zeigerparameter überprüfen, um sicherzustellen, dass sie ungleich 0 (null) sind, bevor Sie sie verwenden. Wenn Sie einen NULL-Wert an eine Methode übergeben, die einen gültigen Zeiger erfordert, gibt die Methode E \_ INVALIDARG zurück. Optionale Out-Zeiger mit NULL-Werten werden ignoriert.

Verwenden Sie Methoden mit Get- und Set-Präfixen, um Eigenschaften zu erhalten und zu festlegen. Boolesche Variablen verwenden **tomFalse** (0) für **FALSE** und **tomTrue** (-1) für **TRUE.**

TOM-Konstanten werden im [**TomConstants-Enumerationstyp**](/windows/win32/api/tom/ne-tom-tomconstants) definiert und beginnen mit dem Präfix *tom*, z. B. **tomWord**.

## <a name="the-tombool-type"></a>Der tomBool-Typ

Viele TOM-Methoden verwenden einen speziellen Variablentyp namens "tomBool" für Rich-Text-Attribute, die binäre Zustände haben. Der tomBool-Typ ist  anders als der boolesche Typ, da er vier Werte verwenden kann: **tomTrue,** **tomFalse,** **tomToggle** und **tomUndefined.** Die **Werte tomTrue** und **tomFalse geben** true und false an. Der **tomToggle-Wert** wird verwendet, um eine Eigenschaft umzuschalten. Der **tomUndefined-Wert,** der eher als NINCH bezeichnet wird, ist ein spezieller Wert ohne Eingabe und ohne Änderung, der mit longs, floats und **COLORREF-s** funktioniert. Bei **Zeichenfolgen wird tomUndefined** (oder NINCH) durch die NULL-Zeichenfolge dargestellt. Bei Eigenschafteneinstellungsvorgängen ändert **die Verwendung von tomUndefined** nicht die Zieleigenschaft. Bei Vorgängen zum Abrufen von Eigenschaften bedeutet **tomUndefined,** dass die Zeichen im Bereich unterschiedliche Werte haben (das graue Kontrollkästchen wird in Eigenschaftendialogfeldern angezeigt).

## <a name="math-buildup-and-build-down"></a>Mathematischer BuildUp und Build Down

Sie können die [**ITextRange2::BuildUpMath-Methode**](/windows/desktop/api/Tom/nf-tom-itextrange2-buildupmath) verwenden, um linear formatierte mathematische Ausdrücke in integrierte Versionen zu konvertieren. Die [**ITextRange2::Linearize-Methode**](/windows/desktop/api/Tom/nf-tom-itextrange2-linearize) führt die umgekehrte Konvertierung aus, die als Linearisierung oder Build down bezeichnet wird, um integrierte Versionen von mathematischen Ausdrücken zurück in das lineare Format zu konvertieren. Die Mathematische Erstellungsfunktion ist nützlich, wenn Sie Nur-Text exportieren oder bestimmte Bearbeitungstypen aktivieren müssen.

## <a name="tom-rtf"></a>TOM RTF

In TOM kann der Rich-Text-Austausch durch Sätze von expliziten Methodenaufrufen oder durch Übertragungen von Rich-Text im Rich-Text-Format (RTF) erfolgen. Dieser Abschnitt enthält Tabellen mit RTF-Steuerwörtern für Absatzeigenschaften und Zeicheneigenschaften.

**TOM RTF Paragraph Control Words**

| Steuerwort   | Bedeutung                                                                                                                                                                                                                                                                        |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ fi *n*      | Einrückung in die erste Zeile (Der Standardwert ist 0 (null).                                                                                                                                                                                                                                       |
| \\ Halten        | Lassen Sie den Absatz intakt.                                                                                                                                                                                                                                                         |
| \\ keepn       | Behalten Sie den nächsten Absatz bei.                                                                                                                                                                                                                                                  |
| \\ li *n*      | Linker Einzug (Der Standardwert ist 0 (null).                                                                                                                                                                                                                                             |
| \\ noline      | Keine Zeilennummerierung.                                                                                                                                                                                                                                                             |
| \\ nowidctlpar | Deaktivieren Sie die Steuerung für verwaiste/verwaiste Daten.                                                                                                                                                                                                                                                 |
| \\ pagebb      | Seite vor Absatz umbrechen.                                                                                                                                                                                                                                                   |
| \\ Par         | Neuer Absatz.                                                                                                                                                                                                                                                                 |
| \\ pard        | Setzt auf standardmäßige Absatzeigenschaften zurück.                                                                                                                                                                                                                                        |
| \\ Ql          | Linksbündig ausgerichtet (Standard).                                                                                                                                                                                                                                                    |
| \\ Qr          | Rechtsbündig ausgerichtet.                                                                                                                                                                                                                                                                 |
| \\ Qj          | Blocksatz.                                                                                                                                                                                                                                                                     |
| \\ Qc          | Zentriert.                                                                                                                                                                                                                                                                      |
| \\ ri *n*      | Rechter Einzug (Der Standardwert ist 0 (null).                                                                                                                                                                                                                                            |
| \\ s *n*       | Format *n*.                                                                                                                                                                                                                                                                     |
| \\ sa *n*      | Leerzeichen nach (der Standardwert ist 0 (null).                                                                                                                                                                                                                                             |
| \\ sb *n*      | Leerzeichen vor (der Standardwert ist 0 (null).                                                                                                                                                                                                                                            |
| \\ sl *n*      | Wenn der Zeilenabstand fehlt oder *n*=1000, wird der Zeilenabstand durch das höchste Zeichen in der Zeile bestimmt (einzeiler Abstand). Wenn *n*> null ist, wird mindestens diese Größe verwendet. Wenn *n* gleich < null ist, wird genau \| *n* \| verwendet. Der Zeilenabstand ist ein mehrzeiler Abstand, wenn \\ slmult 1 folgt. |
| \\ slmult *m*  | Folgt \\ sl. *m* = null: Mindestens oder exakter Zeilenabstand, wie von \\ sl *n beschrieben.* *m* = 1: Zeilenabstand = *n*/240-mal einzeiler Abstand.                                                                                                                              |
| \\ TB *n*      | Position der Balkenregisterkarte in Twips vom linken Rand.                                                                                                                                                                                                                              |
| \\ tldot       | Registerkarten-Leaderpunkte.                                                                                                                                                                                                                                                               |
| \\ tleq        | Tabstopp-Leader: Gleichheitszeichen.                                                                                                                                                                                                                                                         |
| \\ tlhyph      | Bindestriche für Tabstopps.                                                                                                                                                                                                                                                            |
| \\ tlth        | Spitzenlinie der Tabulatoren.                                                                                                                                                                                                                                                         |
| \\ tlul        | Registerkartenleiter unterstrichen.                                                                                                                                                                                                                                                          |
| \\ Tqc         | Zentrierte Registerkarte.                                                                                                                                                                                                                                                                  |
| \\ tqdec       | Registerkarte "Dezimal".                                                                                                                                                                                                                                                                   |
| \\ tqr         | Registerkarte "Rechts leeren".                                                                                                                                                                                                                                                               |
| \\ tx *n*      | Tabstoppposition in Twips vom linken Rand.                                                                                                                                                                                                                                  |



 

**TOM RTF Character Format Control Words**

| Steuerwort     | Bedeutung                                                                                                                                                                                                                                  |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ Animation *n* | Legt den Animationstyp auf *n fest.*                                                                                                                                                                                                              |
| \\ B             | Fettdruck                                                                                                                                                                                                                                    |
| \\ Caps          | Alle Groß- und Groß-                                                                                                                                                                                                                            |
| \\ cf *n*        | Vordergrundfarbe (der Standardwert ist **tomAutocolor**).                                                                                                                                                                                      |
| \\ cs *n*        | Zeichenformat *n*.                                                                                                                                                                                                                     |
| \\ dn *n*        | Unterskriptposition in Halbpunkten (Der Standardwert ist 6).                                                                                                                                                                                    |
| \\ Embo          | Geprägt.                                                                                                                                                                                                                                |
| \\ f *n*         | Schriftartnummer, *n* bezieht sich auf einen Eintrag in der Schriftarttabelle.                                                                                                                                                                                   |
| \\ fs *n*        | Schriftgrad in Halbpunkten (Der Standardwert ist 24).                                                                                                                                                                                            |
| \\ Highlight *n* | Hintergrundfarbe (der Standardwert ist **tomAutocolor**).                                                                                                                                                                                      |
| \\ Ich             | Italic.                                                                                                                                                                                                                                  |
| \\ Impr          | Impressum.                                                                                                                                                                                                                                 |
| \\ lang *n*      | Wendet eine Sprache auf ein Zeichen an. *n* ist eine Zahl, die einer Sprache entspricht. Das einfache Steuerelementwort setzt die Spracheigenschaft auf die Sprache zurück, die durch \\ \\ deflang *n* in den Dokumenteigenschaften definiert wird.                             |
| \\ nosupersub    | Deaktiviert hoch- oder untergestellt.                                                                                                                                                                                                      |
| \\ outl          | Umriss.                                                                                                                                                                                                                                 |
| \\ einfach         | Setzt Zeichenformatierungseigenschaften auf einen standardwert zurück, der von der Anwendung definiert wird. Die zugeordneten Zeichenformatierungseigenschaften (beschrieben im Abschnitt Zugeordnete Zeicheneigenschaften in der RTF-Spezifikation) werden ebenfalls zurückgesetzt. |
| \\ SCAPS         | Kleine Groß- und Klein groß.                                                                                                                                                                                                                          |
| \\ Shad          | Schatten.                                                                                                                                                                                                                                  |
| \\ Schlag        | Durchgestrichen.                                                                                                                                                                                                                           |
| \\ Sub           | Wendet einen Inskript auf Text an und reduziert den Punktgröße entsprechend den Schriftartinformationen.                                                                                                                                                          |
| \\ Super         | Wendet hochgestellt auf Text an und reduziert den Punktgröße entsprechend den Schriftartinformationen.                                                                                                                                                        |
| \\ Ul            | Kontinuierliche Unterstreichung. \\ ul0 deaktiviert alle Unterstreichungen.                                                                                                                                                                                  |
| \\ Uld           | Gepunktete Unterstreichung.                                                                                                                                                                                                                        |
| \\ uldb          | Doppelte Unterstreichung.                                                                                                                                                                                                                        |
| \\ ulnone        | Beendet alle Unterlinings.                                                                                                                                                                                                                   |
| \\ ulw           | Wort unterstrichen.                                                                                                                                                                                                                          |
| \\ bis *n*        | Superscriptposition in Halbpunkten (Der Standardwert ist 6).                                                                                                                                                                                  |
| \\ V             | Ausgeblendeter Text.                                                                                                                                                                                                                             |



 

## <a name="finding-rich-text"></a>Suchen von Rich Text

Sie können TOM-Methoden verwenden, um Rich-Text zu finden, wie durch einen Textbereich definiert. Solche Umfangreichen Text zu finden, ist häufig bei der Textverarbeitung erforderlich, obwohl sie noch nie in einem WISIWYG-Textverarbeitungsprogramm (WHAT You See Is What You Get) erfüllt wurde. Es gibt eindeutig einen größeren Bereich des Rich-Text-Abgleichs, der es ermöglicht, einige Zeichenformatierungseigenschaften zu ignorieren (oder Absatzformatierung und/oder Objektinhalte einzubeziehen), aber solche Verallgemeinerungen gehen über den Rahmen dieses Abschnitts hinaus.

Ein Zweck dieser Funktionalität ist die  Verwendung eines Rich-Text-Suchdialogfelds, um den Rich-Text zu definieren, den Sie in einem Dokument suchen möchten. Das Dialogfeld wird mithilfe eines Rich-Edit-Steuerelements implementiert, und TOM-Methoden werden verwendet, um die Suche im Dokument durchzuführen. Sie können entweder den gewünschten Rich Text aus dem Dokument in das Dialogfeld **Suchen** kopieren oder ihn direkt im Dialogfeld **Suchen** eingeben und formatieren.

Im folgenden Beispiel wird gezeigt, wie Tom-Methoden verwendet werden, um Text zu suchen, der Kombinationen der genauen Zeichenformatierung enthält. Der Algorithmus sucht nach dem Nur-Text im Übereinstimmungsbereich mit dem Namen `pr1` . Wenn der Nur-Text gefunden wird, wird auf ihn durch einen Testbereich mit dem Namen `pr2` verwiesen. Anschließend werden zwei Einfügemarkebereiche ( `prip1` und `prip2` ) verwendet, um den Testbereich zu durchlaufen und dessen Zeichenformatierung mit der von zu `pr1` vergleichen. Wenn sie genau übereinstimmen, wird der Eingabebereich (angegeben von `ppr` ) aktualisiert, um auf den Text des Testbereichs zu verweisen, und die Funktion gibt die Anzahl der Zeichen im übereinstimmende Bereich zurück. Zwei [**ITextFont-Objekte,**](/windows/desktop/api/Tom/nn-tom-itextfont) `pf1` und , werden im `pf2` Zeichenformatierungsvergleich verwendet. Sie werden an die Einfügemarkebereiche `prip1` und `prip2` angefügt.


```
LONG FindRichText (
    ITextRange **ppr,             // Ptr to range to search
    ITextRange *pr1)              // Range with rich text to find
{
    BSTR        bstr;             // pr1 plain-text to search for
    LONG        cch;              // Text string count
    LONG        cch1, cch2;       // tomCharFormat run char counts
    LONG        cchMatch = 0;     // Nothing matched yet
    LONG        cp;               // Handy char position
    LONG        cpFirst1;         // pr1 cpFirst
    LONG        cpFirst2;         // pr2 cpFirst
    ITextFont  *    pf1, *pf      // Fonts corresponding to IPs prip1 and prip2
    ITextRange *pr2;              // Range duplicate to search with
    ITextRange *prip1, *prip      // Insertion points to walk pr1, pr2

    if (!ppr || !*ppr || !pr1)
        return E_INVALIDARG;

    // Initialize range and font objects used in search
    if ((*ppr)->GetDuplicate(&pr2)    != NOERROR ||
        pr1->GetDuplicate(&prip1)     != NOERROR ||
        pr2->GetDuplicate(&prip2)     != NOERROR ||
        prip1->GetFont(&pf1)          != NOERROR ||
        prip2->GetFont(&pf2)          != NOERROR ||
        pr1->GetText(&bstr)           != NOERROR )
    {
        return E_OUTOFMEMORY;
    }

    pr1->GetStart(&cpFirst1);

    // Keep searching till rich text is matched or no more plain-text hits
    while(!cchMatch && pr2->FindText(bstr, tomForward, 0, &cch) == NOERROR)
    {
        pr2->GetStart(&cpFirst2);                 // pr2 is a new trial range
        prip1->SetRange(cpFirst1, cpFirst1);      // Set up IPs to scan match
        prip2->SetRange(cpFirst2, cpFirst2);      //  and trial ranges

        while(cch > 0 &&
            pf1->IsEqual(pf2, NULL) == NOERROR)   // Walk match & trial ranges
        {                                         //  together comparing font
            prip1->GetStart(&cch1);               //  properties
            prip1->Move(tomCharFormat, 1, NULL);
            prip1->GetStart(&cp);
            cch1 = cp - cch1;                     // cch of next match font run

            prip2->GetStart(&cch2);
            prip2->Move(tomCharFormat, 1, NULL);
            prip2->GetStart(&cp);
            cch2 = cp - cch2;                      // cch of next trial font run

            if(cch1 < cch)                         // There is more to compare
            {
                if(cch1 != cch2)                   // Different run lengths:
                    break;                         //  no formatting match
                cch = cch - cch1;                  // Matched format run
            }
            else if(cch2 < cch)                    // Trial range format run too
                break;                             //  short

            else                                   // Both match and trial runs
            {                                      //  reach at least to match
                pr2->GetEnd(&cp);                  //  text end: rich-text match
                (*ppr)->SetRange(cpFirst2, cp)     // Set input range to hit
                cchMatch = cp - cpFirst2;          //  coordinates and return
                break;                             //  length of matched string
            }
        }
    }
    pr2->Release();
    prip1->Release();
    prip2->Release();
    pf1->Release();
    pf2->Release();
    SysFreeString(bstr);

    return cchMatch;
}
```



## <a name="tom-accessibility"></a>TOM-Barrierefreiheit

TOM bietet Barrierefreiheitsunterstützung über die Schnittstellen [**ITextSelection**](/windows/desktop/api/Tom/nn-tom-itextselection) und [**ITextRange.**](/windows/desktop/api/Tom/nn-tom-itextrange) In diesem Abschnitt werden Methoden beschrieben, die für die Barrierefreiheit nützlich sind, und wie ein Programm die *x-, y-Bildschirmposition* eines Objekts bestimmen kann. 

Da benutzeroberflächenbasierte Barrierefreiheitsprogramme in der Regel mit dem Bildschirm und der Maus funktionieren, besteht ein häufiges Problem darin, die entsprechende [**ITextDocument-Schnittstelle**](/windows/desktop/api/Tom/nn-tom-itextdocument) für die aktuelle Mausposition (in Bildschirmkoordinaten) zu finden. In den folgenden Abschnitten werden zwei Möglichkeiten zum Bestimmen der richtigen Schnittstelle beschrieben:

-   [Durch die Tabelle running-object](#interface-from-running-object-table)
-   Über die [**EM \_ GETOLEINTERFACE-Nachricht,**](em-getoleinterface.md) die für Rich Edit-Instanzen mit Fenstern funktioniert, vorausgesetzt, der Client befindet sich im selben Prozessbereich (es ist kein *Marshalling* erforderlich).

Weitere Informationen finden Sie in der Microsoft Active Accessibility-Spezifikation. Nachdem Sie ein Objekt von einer Bildschirmposition erhalten haben, können Sie für eine [**ITextDocument-Schnittstelle**](/windows/desktop/api/Tom/nn-tom-itextdocument) verwenden und die [**RangeFromPoint-Methode**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) aufrufen, um ein leeres Bereichsobjekt an der cp abzurufen, das der Bildschirmposition entspricht.

### <a name="interface-from-running-object-table"></a>Schnittstelle aus ausgeführter Objekttabelle

Eine ausgeführte Objekttabelle (ROT) gibt an, welche Objektinstanzen aktiv sind. Durch Abfragen dieser Tabelle können Sie den Vorgang zum Verbinden eines Clients mit einem Objekt beschleunigen, wenn das Objekt bereits ausgeführt wird. Bevor Programme über die ausgeführte Objekttabelle auf TOM-Schnittstellen zugreifen können, muss sich eine TOM-Instanz mit einem Fenster mithilfe eines Monikers im ROT registrieren. Sie erstellen den Moniker aus einer Zeichenfolge, die den Hexadezimalwert des [**HWND**](/windows/desktop/WinProg/windows-data-types)enthält. Im folgenden Codebeispiel wird dies veranschaulicht.


```
// This TOM implementation code is executed when a new windowed 
// instance starts up. 
// Variables with leading underscores are members of this class.

HRESULT hr;
OLECHAR szBuf[10];            // Place to put moniker
MONIKER *pmk;

hr = StringCchPrintf(szBuff, 10, "%x", _hwnd);
if (FAILED(hr))
{
    //
    // TODO: write error handler
    //
}
CreateFileMoniker(szBuf, &pmk);
OleStdRegisterAsRunning(this, pmk, &_dwROTcookie);
....................
 
// Accessibility Client: 
//    Find hwnd for window pointed to by mouse cursor.

GetCursorPos(&pt);
hwnd = WindowFromPoint(pt);

// Look in ROT (running object table) for an object attached to hwnd

hr = StringCchPrintf(szBuff, 10, "%x", hwnd);
if (FAILED(hr))
{
    //
    // TODO: write error handler
    //
}
CreateFileMoniker(szBuf, &pmk);
CreateBindContext(0, &pbc);
pmk->BindToObject(pbc, NULL, IID_ITextDocument, &pDoc);
pbc->Release();

if( pDoc )
{
    pDoc->RangeFromPoint(pt.x, pt.y, &pRange);
    // ...now do whatever with the range pRange
}
```



### <a name="interface-from-window-messages"></a>Schnittstelle aus Fenstermeldungen

Die [**EM \_ GETOLEINTERFACE-Nachricht**](em-getoleinterface.md) bietet eine weitere Möglichkeit, eine [**IUnknown-Schnittstelle**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) für ein Objekt an einer bestimmten Bildschirmposition abzurufen. Wie unter [Schnittstelle aus ausgeführter Objekttabelle](#interface-from-running-object-table)beschrieben, erhalten Sie einen [**HWND**](/windows/desktop/WinProg/windows-data-types) für die Bildschirmposition und senden diese Nachricht dann an das **HWND.** Die **EM \_ GETOLEINTERFACE-Nachricht** ist rich edit-specific und gibt einen Zeiger auf eine [**IRichEditOle-Schnittstelle**](/windows/desktop/api/Richole/nn-richole-iricheditole) in der Variablen zurück, die von *lParam* adressiert wird.

**Tipp** Wenn ein Zeiger zurückgegeben wird (achten Sie darauf, das Objekt festzulegen, auf das *lParam* vor dem Senden der Nachricht auf NULL zeigt), können Sie die [**IUnknown::QueryInterface-Methode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) aufrufen, um eine [**ITextDocument-Schnittstelle**](/windows/desktop/api/Tom/nn-tom-itextdocument) abzurufen. Das folgende Codebeispiel veranschaulicht diese Vorgehensweise.


```
    HWND    hwnd;
    ITextDocument *pDoc;
    ITextRange *pRange;
    POINT    pt;
    IUnknown *pUnk = NULL;
    
    GetCursorPos(&pt);
    hwnd = WindowFromPoint(pt);
    SendMessage(hwnd, EM_GETOLEINTERFACE, 0, (LPARAM)&pUnk);
    if(pUnk && 
        pUnk->QueryInterface(IID_ITextDocument, &pDoc) == NOERROR)
    {
        pDoc->RangeFromPoint(pt.x, pt.y, &pRange);
        //  ... continue with rest of program
    }
```



### <a name="accessibility-oriented-methods"></a>Barrierefreiheitsorientierte Methoden

Einige TOM-Methoden sind besonders nützlich für die Navigation auf dem Bildschirm, während andere TOM-Methoden die Möglichkeiten verbessern, wenn Sie an interessanten Orten eintreffen. In der folgenden Tabelle werden die nützlichsten Methoden beschrieben.



| Methode                                                 | Fördern der Barrierefreiheit                                                                                                                                                                 |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSelection**](/windows/desktop/api/Tom/nf-tom-itextdocument-getselection)     | Diese Methode ruft die aktive Auswahl ab, die für eine Vielzahl von ansichtsorientierten Zwecken verwendet werden kann, z. B. hervorheben von Text und Scrollen.                                                      |
| [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) | Bei Verwendung für eine aktive Auswahl erhält diese Methode garantiert einen Bereich, der einer bestimmten Ansicht zugeordnet ist.                                                                                 |
| [**Expand**](/windows/desktop/api/Tom/nf-tom-itextrange-expand)                    | Vergrößert einen Textbereich, sodass alle enthaltenen Teileinheiten vollständig enthalten sind. `Expand(tomWindow)`Beispielsweise erweitert den Bereich um den sichtbaren Teil der Geschichte des Bereichs. |
| [**GetDuplicate**](/windows/desktop/api/Tom/nf-tom-itextrange-getduplicate)        | Bei Verwendung für eine aktive Auswahl erhält diese Methode garantiert einen Bereich, der einer bestimmten Ansicht zugeordnet ist. Weitere Informationen finden Sie in der Beschreibung von [**RangeFromPoint.**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint)  |
| [**GetPoint**](/windows/desktop/api/Tom/nf-tom-itextrange-getpoint)                | Ruft die Bildschirmkoordinaten für die Anfangs- oder Endzeichenposition im Textbereich ab.                                                                                                        |
| [**ScrollIntoView**](/windows/desktop/api/Tom/nf-tom-itextrange-scrollintoview)    | Führt einen Bildlauf für einen Textbereich in die Ansicht durch.                                                                                                                                                               |
| [**Sollwert**](/windows/desktop/api/Tom/nf-tom-itextrange-setpoint)                | Wählt Text an oder nach oben bis zu einem angegebenen Punkt aus.                                                                                                                                              |



 

## <a name="character-match-sets"></a>Zeichen übereinstimmungssätze

Der *Variant-Parameter* der verschiedenen  \* Move-Methoden in [**ITextRange,**](/windows/desktop/api/Tom/nn-tom-itextrange)z. [**B. MoveWhile**](/windows/desktop/api/Tom/nf-tom-itextrange-movewhile) und [**MoveUntil,**](/windows/desktop/api/Tom/nf-tom-itextrange-moveuntil)kann eine explizite Zeichenfolge oder einen 32-Bit-Zeichensatz-Satz annehmen. Die Indizes werden entweder durch Unicode-Bereiche oder [**GetStringTypeEx-Zeichensätze**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) definiert. Der Unicode-Bereich ab *n* und der Länge *l* (< 32768) wird durch den Index *n* + (*l <*< 16) + 0x80000000 angegeben. Einfache griechisch-Buchstaben werden z. B. durch CR Griechisch = 0x805f0370 definiert, \_ und druckbare ASCII-Zeichen werden durch CR \_ ASCIIPrint = 0x805e0020 definiert. Darüber hinaus können Sie mit den Methoden **MoveWhile** und **MoveUntil** schnell eine Zeichenspanne in einem **beliebigen GetStringTypeEx-Zeichensatz** oder in einer Zeichenspanne umgehen, die sich nicht in einem dieser Zeichensätze befindet.

Die [**GetStringTypeEx-Mengen**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) werden durch die Werte für *Ctype1,* *Ctype2* und *Ctype3* angegeben und wie folgt definiert.



| Cset                 | Bedeutung                          |
|----------------------|----------------------------------|
| *Ctype1*             | Kombination von CT \_ CTYPE1-Typen. |
| *Ctype2* + tomCType2 | Beliebiger CT \_ CTYPE2-Typ.             |
| *Ctype3* + tomCType3 | Kombination von CT \_ CTYPE3-Typen. |



 

Insbesondere kann *Ctype1* eine beliebige Kombination der folgenden Sein.



| Ctype1-Name | Wert  | Bedeutung                                                           |
|-------------|--------|-------------------------------------------------------------------|
| C1 \_ UPPER   | 0x0001 | Großbuchstaben.                                                        |
| C1 \_ LOWER   | 0x0002 | Kleinbuchstaben.                                                        |
| C1 \_ DIGIT   | 0x0004 | Dezimalstellen.                                                   |
| C1 \_ SPACE   | 0x0008 | Leerzeichen.                                                 |
| C1 \_ PUNCT   | 0x0010 | Interpunktion.                                                      |
| C1 \_ CNTRL   | 0x0020 | Steuerzeichen.                                               |
| C1 \_ BLANK   | 0x0040 | Leere Zeichen.                                                 |
| C1 \_ XDIGIT  | 0x0080 | Hexadezimalziffern.                                               |
| C1 \_ ALPHA   | 0x0100 | Beliebiges linguistisches Zeichen (alphabetisch, syllabary oder ideographic). |
| C1 \_ DEFINIERT | 0x0200 | Ein definiertes Zeichen, aber keiner der anderen \_ \* C1-Typen.       |



 

Die *Ctype2-Typen* unterstützen das richtige Layout von Unicode-Text. Die Richtungsattribute werden zugewiesen, sodass der bidirektionale Layoutalgorithmus, der durch Unicode standardisiert ist, genaue Ergebnisse liefert. Diese Typen schließen sich gegenseitig aus. Weitere Informationen zur Verwendung dieser Attribute finden Sie unter *The Unicode Standard: Worldwide Character Encoding, Volumes 1 and 2*, Addison-Wesley Publishing Company: 1991, 1992.



| CType2-Name          | Wert | Bedeutung                          |
|----------------------|-------|----------------------------------|
| Stark:              |       |                                  |
| C2 \_ LEFTTORIGHT      | 0x1   | Von links nach rechts.                   |
| C2 \_ RIGHTTOLEFT      | 0x2   | Von rechts nach links.                   |
| Schwach:                |       |                                  |
| C2 \_ EUROPENUMBER     | 0x3   | Europäische Zahl, europäische Ziffer. |
| C2 \_ EUROPESEPARATOR  | 0x4   | Europäisches numerisches Trennzeichen.      |
| C2 \_ EUROPETERMINATOR | 0x5   | Europäisches numerisches Abschlusszeichen.     |
| C2 \_ ARABICNUMBER     | 0x6   | Arabische Zahl.                   |
| C2 \_ COMMONSEPARATOR  | 0x7   | Allgemeines numerisches Trennzeichen.        |
| Neutral:             |       |                                  |
| C2 \_ BLOCKSEPARATOR   | 0x8   | Blocktrennzeichen.                 |
| C2 \_ SEGMENTSEPARATOR | 0x9   | Segmenttrennzeichen.               |
| \_C2-LEERRAUM       | 0xA   | Leerraum.                     |
| C2 \_ OTHERNEUTRAL     | 0xB   | Andere Neutrale.                  |
| Nicht zutreffend:      |       |                                  |
| C2 \_ NOTAPPLICABLE    | 0x0   | Keine implizite Richtung.           |



 

Die *Ctype3-Typen* sollen Platzhalter für Erweiterungen der POSIX-Typen sein, die für die allgemeine Textverarbeitung oder für die C-Standardbibliotheksfunktionen erforderlich sind.



| CType3-Name       | Wert  | Bedeutung                                                             |
|-------------------|--------|---------------------------------------------------------------------|
| C3 \_ NONSPACING    | 0x1    | Nicht-Pacingmarkierung.                                                    |
| C3 \_ DIACRITIC     | 0x2    | Diakritische Nonspacingmarkierung.                                          |
| C3 \_ VOWELMARK     | 0x4    | Vokal-Nonspacingmarkierung.                                              |
| \_C3-SYMBOL        | 0x8    | Symbol.                                                             |
| C3 \_ KATAKANA      | 0x10   | Katakana-Zeichen.                                                 |
| C3 \_ HIRAGANA      | 0x20   | Hiragana-Zeichen.                                                 |
| C3 \_ HALFWIDTH     | 0x40   | Zeichen halber Breite.                                               |
| C3 \_ FULLWIDTH     | 0x80   | Zeichen mit voller Breite.                                               |
| \_C3-IDEOGRAMM     | 0x100  | Ideografisches Zeichen.                                              |
| C3 \_ KASHIDA       | 0x200  | Arabisches Kashida-Zeichen.                                           |
| C3 \_ ALPHA         | 0x8000 | Alle linguistischen Zeichen (alphabetisch, syllabary und ideographic). |
| C3 \_ NOTAPPLICABLE | 0x0    | Nicht zutreffend                                                     |



 

Ein Edit Development Kit (EDK) kann *pVar-Indexdefinitionen* für die folgenden Bereiche enthalten, die im Unicode-Standard beschrieben werden.



| Zeichensatz         | Unicode-Bereich | Zeichensatz             | Unicode-Bereich |
|-----------------------|---------------|---------------------------|---------------|
| ASCII                 | 0x0 – 0x7f      | ANSI                      | 0x0 – 0xff      |
| ASCIIPrint            | 0x20– 0x7e     | Latin1                    | 0x20 – 0xff     |
| Latin1Supp            | 0xa0 – 0xff     | LatinXA                   | 0x100 – 0x17f   |
| LatinXB               | 0x180 – 0x24f   | IPAX                      | 0x250 – 0x2af   |
| SpaceMod              | 0x2b0 – 0x2ff   | Kombination                 | 0x300 – 0x36f   |
| Griechisch                 | 0x370 – 0x3ff   | BasicGreek                | 0x370 – 0x3cf   |
| GriechischSymbole          | 0x3d0 – 0x3ff   | Kyrillisch                  | 0x400 – 0x4ff   |
| Armenisch              | 0x530 – 0x58f   | Hebräisch                    | 0x590 – 0x5ff   |
| BasicHebrew           | 0x5d0 – 0x5ea   | HebräischXA                  | 0x590 – 0x5cf   |
| HebräischXB              | 0x5eb – 0x5ff   | Arabisch                    | 0x600 – 0x6ff   |
| BasicArabic           | 0x600 – 0x652   | ArabischX                   | 0x653 – 0x6ff   |
| Devangari             | 0x900 – 0x97f   | Pausieren (vormals :) | 0x980 – 0x9ff   |
| Gurmukhi              | 0xa00 – 0xa7f   | Gujarati                  | 0xa80– 0xaff   |
| Odia (ehemals Oriya) | 0xb00 – 0xb7f   | Tamilisch                     | 0xb80 – 0xbff   |
| Teluga                | 0xc00 – 0xc7f   | Kannada                   | 0xc80 – 0xcff   |
| Malayalam             | 0xd00 – 0xd7f   | Thailändisch                      | 0xe00 – 0xe7f   |
| Laotisch                   | 0xe80 – 0xeff   | AtlantanX                 | 0x10a0 – 0xa0cf |
| BascGeoroan          | 0x10d0 – 0x10ff | Jamo                      | 0x1100 – 0x11ff |
| LatinXAdd             | 0x1e00 – 0x1eff | GriechischX                    | 0x1f00 – 0x1fff |
| GenPunct              | 0x2000 – 0x206f | Hochgestellt               | 0x2070 – 0x207f |
| Tiefgestellt             | 0x2080 – 0x208f | SuperSubscript            | 0x2070 – 0x209f |
| Währung              | 0x20a0 – 0x20cf | CombMarkSym               | 0x20d0 – 0x20ff |
| Letterlike            | 0x2100 – 0x214f | NumberForms               | 0x2150 – 0x218f |
| Pfeile                | 0x2190 – 0x21ff | MathOps                   | 0x2200 – 0x22ff |
| MiscTech              | 0x2300 – 0x23ff | STRGBild              | 0x2400 – 0x243f |
| OptCharRecog          | 0x2440 – 0x245f | EnclAlphaNum              | 0x2460 – x24ff  |
| BoxDrawing            | 0x2500 – 0x257f | BlockElement              | 0x2580 – 0x259f |
| GeometShapes          | 0x25a0 – 0x25ff | MiscSymbols               | 0x2600 – 0x26ff |
| Dingbats              | 0x2700 – 0x27bf | CJKSymPunct               | 0x3000 – 0x303f |
| Hiragana              | 0x3040 – 0x309f | Katakana                  | 0x30a0 – 0x30ff |
| Bopomofo              | 0x3100 – 0x312f | HangulJamo                | 0x3130 – 0x318f |
| CJLMisc               | 0x3190 – 0x319f | EnclCJK                   | 0x3200 – 0x32ff |
| CJKCompatibl          | 0x3300 – 0x33ff | Han                       | 0x3400 – 0xabff |
| Hangul                | 0xac00 – 0xd7ff | UTF16Lead                 | 0xd800 – 0xdbff |
| UTF16Trail            | 0xdc00 – 0xdfff | PrivateUse                | 0xe000 – 0xf800 |
| CJKCompIdeog          | 0xf900 – 0xfaff | AlphaPres                 | 0xfb00 – 0xfb4f |
| ArabicPresA           | 0xfb50 – 0xfdff | CombHalfMark              | 0xfe20 – 0xfe2f |
| CJKCompForm           | 0xfe30 – 0xfe4f | SmallFormVar              | 0xfe50 – 0xfe6f |
| ArabicPresB           | 0xfe70 – 0xfefe | HalfFullForm              | 0xff00 – 0xffef |
| Specials              | 0xfff0 – 0xfffd |                           |               |



 

 

 