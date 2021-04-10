---
title: Informationen zum Text Objektmodell
description: Dieses Thema enthält eine allgemeine Übersicht über das Tom.
ms.assetid: e304ec18-ec2e-4ea7-91c6-6f6ab63b72ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b934aab1cbd3dca932b58e4aa99498843cb8cc97
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039720"
---
# <a name="about-text-object-model"></a>Informationen zum Text Objektmodell

Das Textobjekt Modell (Tom) definiert einen Satz von Text Bearbeitungs Schnittstellen, die von mehreren Microsoft-Textlösungen, einschließlich des Rich Edit-Steuer Elements, unterschiedlich unterstützt werden. Dieses Thema enthält eine allgemeine Übersicht über das Tom. In diesem Thema werden die folgenden Themen behandelt.

-   [Tom-Version 2-Objekte](#tom-version-2-objects)
-   [Tom-Schnittstellen Konventionen](#tom-interface-conventions)
-   [Der tombool-Typ](#the-tombool-type)
-   [Mathematische Erstellung und Buildvorgang](#math-buildup-and-build-down)
-   [Tom RTF](#tom-rtf)
-   [Suchen von reichem Text](#finding-rich-text)
-   [Tom-Barrierefreiheit](#tom-accessibility)
    -   [Schnittstelle aus der Ausführung der Objekttabelle](#interface-from-running-object-table)
    -   [Schnittstelle von Fenster Meldungen](#interface-from-window-messages)
    -   [Barrierefreiheits orientierte Methoden](#accessibility-oriented-methods)
-   [Zeichen Übereinstimmungs Sätze](#character-match-sets)

## <a name="tom-version-2-objects"></a>Tom-Version 2-Objekte

Tom Version 2 (Tom 2) erweitert das ursprüngliche Textobjekt Modell. die neuen Schnittstellen werden von den alten abgeleitet. Die aktualisierte Tom-API umfasst Unterstützung für neue Zeichen-und Absatzformat Eigenschaften, ein Tabellen Modell, Mehrfachauswahl und Unterstützung von Inline Objekten für Math und Ruby.

Das Tom 2-Objekt der obersten Ebene wird von der [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) -Schnittstelle definiert, die über Methoden zum Erstellen und Abrufen von Objekten in der Objekthierarchie verfügt. Für die einfache Textverarbeitung können Sie ein [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) -Objekt aus einem **ITextDocument2** -Objekt abrufen und die meisten Aufgaben mit diesem ausführen. Wenn Sie Rich-Text-Formatierung hinzufügen müssen, können Sie [**ITextFont2**](/windows/desktop/api/Tom/nn-tom-itextfont2) -und [**ITextPara2**](/windows/desktop/api/Tom/nn-tom-itextpara2) -Objekte von einem **ITextRange2** -Objekt abrufen. **ITextFont2** stellt das Programmier Äquivalent des Dialog Felds "Format-Schriftart" von Microsoft Word bereit, und **ITextPara2** stellt die Entsprechung des Dialog Felds "Word-Format-Absatz" bereit.

Zusätzlich zu diesen drei Objekten auf niedrigerer Ebene hat Tom 2 ein Selection-Objekt ([**ITextSelection2**](/windows/win32/api/tom/nn-tom-itextselection2)), bei dem es sich um ein [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) -Objekt mit Auswahl Hervorhebung und einigen Benutzeroberflächen orientierten Methoden handelt.

Die Bereich-und Auswahl Objekte enthalten Bildschirm orientierte Methoden, mit denen Programme Text auf dem Bildschirm oder Text untersuchen können, der auf dem Bildschirm angezeigt werden kann. Diese Funktionen helfen dem Zugriff auf Text für Personen mit eingeschränkter Sehfähigkeit, z. b..

Jede Schnittstelle mit dem Suffix 2 erbt von der entsprechenden Schnittstelle ohne das Suffix 2. [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) erbt z. b. von [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument).

Die Tom 2-Objekte haben die folgende Hierarchie.

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

Ein [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) -Objekt beschreibt einen oder mehrere zusammenhängende Textbereiche, die als *Stories* bezeichnet werden. Stories stellen verschiedene Teile eines Dokuments dar, z. b. den Haupttext des Dokuments, Kopf-und Fußzeilen, Fußnoten, Anmerkungen und Rich-Text-Ablage Pads. Bei der Übersetzung zwischen Inline formatierten mathematischen Ausdrücken und einem integrierten Formular wird ein Scratch-Pad verwendet. Beim Speichern des Inhalts eines Bereichs, bei dem es sich um die aktuelle Kopier Quelle handelt, wird auch eine Scratch-Pad-Story verwendet, wenn der Inhalt geändert wird.

Ein [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) -Objekt wird durch seine Start-und End-Zeichen Positions Offsets und ein Story-Objekt definiert. Er ist nicht unabhängig von seinem übergeordneten Story-Objekt vorhanden, obwohl der Text in die Zwischenablage oder andere Ziele kopiert werden kann. Ein Text Bereichs Objekt unterscheidet sich von der Kalkulations Tabelle und anderen Bereichs Objekten, die durch andere Arten von Offsets definiert werden. beispielsweise Zeilen-/Spalten-oder Grafik Position (x, y). Ein Text Bereichs Objekt kann sich auf verschiedene Weise ändern, kann ein Duplikat von sich selbst zurückgeben, und es kann befohlen werden, seine Start-und Endzeichen Positionen und den Story-Zeiger auf die aktuelle Auswahl zu kopieren.

Ein explizites Story-Objekt ist nicht erforderlich, da ein [**itextrange**](/windows/desktop/api/Tom/nn-tom-itextrange) -Objekt immer erstellt werden kann, um eine bestimmte Story darzustellen. Insbesondere das [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) -Objekt kann ein [**itextstoryranges**](/windows/desktop/api/Tom/nn-tom-itextstoryranges) -Objekt erstellen, um die Textabschnitte im Dokument in Bezug auf Bereiche mit Anfangs-und Endzeichen-Positions Werten aufzulisten, die komplette Textabschnitte (z. b. 0 und **tomforward**) beschreiben.

Bei einem [**ITextStoryRanges2**](/windows/desktop/api/Tom/nn-tom-itextstoryranges2) -Objekt wird kein explizites Story-Objekt benötigt, da jede Story von einem [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) -Objekt beschrieben wird. Insbesondere kann das [**ITextDocument2**](/windows/desktop/api/tom/nn-tom-itextdocument2) -Objekt ein [**ITextStoryRanges2**](/windows/desktop/api/tom/nn-tom-itextstoryranges2) -Objekt erstellen, um die Textabschnitte im Dokument in Bezug auf Bereiche mit Anfangs-und Endzeichen-Positions Werten aufzulisten, die komplette Storys beschreiben (z. b. 0 und **tomforward**).

Die [**itextrow**](/windows/desktop/api/Tom/nn-tom-itextrow) -Schnittstelle in Verbindung mit den Methoden [**itextrange:: Move**](/windows/desktop/api/Tom/nf-tom-itextrange-move) und [**itextrange:: Expand**](/windows/desktop/api/Tom/nf-tom-itextrange-expand) bietet die Möglichkeit, Tabellen einzufügen, abzufragen und zu ändern.

## <a name="tom-interface-conventions"></a>Tom-Schnittstellen Konventionen

Alle Tom-Methoden geben **HRESULT** -Werte zurück. Im Allgemeinen geben die Tom-Methoden die folgenden Standardwerte zurück.

-   E \_ outo-Memory
-   E \_ invalidArg
-   E \_ notimpl
-   E file \_ Topics
-   E \_ AccessDenied
-   E \_ fehlschlagen
-   Co \_ E \_ veröffentlicht
-   NoError (identisch mit S \_ OK)
-   S \_ false

Beachten Sie, dass das Tom-Objekt nutzlos ist, wenn die einem Tom-Objekt zugeordnete Bearbeitungs Instanz, z. b. [**itextrange**](/windows/desktop/api/Tom/nn-tom-itextrange) , gelöscht wird \_ \_ .

Zusätzlich zu den **HRESULT** -Rückgabe Werten enthalten viele Methoden out-Parameter, bei denen es sich um Zeiger handelt, die zum Zurückgeben von Werten verwendet werden. Für alle Schnittstellen sollten Sie alle Zeiger Parameter überprüfen, um sicherzustellen, dass Sie nicht NULL sind, bevor Sie Sie verwenden. Wenn Sie einen NULL-Wert an eine Methode übergeben, die einen gültigen Zeiger erfordert, gibt die Methode E \_ invalidArg zurück. Optionale out-Zeiger mit NULL-Werten werden ignoriert.

Verwenden Sie Methoden mit Get-und Set-Präfixen, um Eigenschaften zu erhalten und festzulegen. Boolesche Variablen verwenden **tomfalse** (0) für **false** und **tomtrue** (-1) für **true**.

Tom-Konstanten werden im [**tomconstants**](/windows/win32/api/tom/ne-tom-tomconstants) -Enumerationstyp definiert und beginnen mit dem Präfix *Tom*(z. b. **tomword**).

## <a name="the-tombool-type"></a>Der tombool-Typ

Viele Tom-Methoden verwenden eine besondere Art von Variable namens "tombool" für Rich-Text-Attribute, die über binäre Zustände verfügen. Der tombool-Typ unterscheidet sich vom **booleschen** Typ, da er vier Werte annehmen kann: **tomtrue**, **tomfalse**, **tomtoggle** und **tomunundefiniert**. Die Werte **tomtrue** und **tomfalse** geben "true" und "false" an. Der **tomtoggle** -Wert wird verwendet, um eine Eigenschaft zu wechseln. Der **tomunundefinierte** Wert, der üblicherweise als ninch bezeichnet wird, ist ein spezieller No-Input-und No-Change-Wert, der mit Longs, float und **COLORREF** s funktioniert. Für Zeichen folgen wird **tomundefiniert** (oder ninch) durch die NULL-Zeichenfolge dargestellt. Bei Eigenschafts Einstellungs Vorgängen wird durch die Verwendung von **tomundefinierter** die Ziel Eigenschaft nicht geändert. Bei Eigenschafts Einfügevorgängen bedeutet **tomundefiniert** , dass die Zeichen im Bereich unterschiedliche Werte aufweisen (das Kontrollkästchen wird in den Eigenschaften Dialogfeldern angezeigt).

## <a name="math-buildup-and-build-down"></a>Mathematische Erstellung und Buildvorgang

Sie können die [**ITextRange2:: buildupmath**](/windows/desktop/api/Tom/nf-tom-itextrange2-buildupmath) -Methode verwenden, um linear formatierte mathematische Ausdrücke in integrierte Versionen zu konvertieren. Die [**ITextRange2:: Linearize**](/windows/desktop/api/Tom/nf-tom-itextrange2-linearize) -Methode führt die umgekehrte Konvertierung, die sogenannte Linearisierung oder den Buildvorgang, aus, um integrierte Versionen von mathematischen Ausdrücken zurück in das lineare Format zu konvertieren. Die mathematische Funktion "Build downdown" ist nützlich, wenn Sie nur-Text exportieren oder bestimmte Bearbeitungs Typen aktivieren müssen.

## <a name="tom-rtf"></a>Tom RTF

In Tom kann Rich-Text-Austausch durch Sätze expliziter Methodenaufrufe oder durch Übertragungen von Rich-Text im RTF-Format (Rich Text Format) erreicht werden. Dieser Abschnitt enthält Tabellen mit RTF-Steuer Wörtern für Absatz Eigenschaften und für Zeichen Eigenschaften.

**Tom RTF-Absatz Steuer Wörter**

| Steuerwort   | Bedeutung                                                                                                                                                                                                                                                                        |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ fi *n*      | Einzug in der ersten Zeile (der Standardwert ist 0 (null)).                                                                                                                                                                                                                                       |
| \\ halten        | Speichern Sie den Absatz unverändert.                                                                                                                                                                                                                                                         |
| \\ keepn       | Behalten Sie den nächsten Absatz bei.                                                                                                                                                                                                                                                  |
| \\ Li *n*      | Linker Einzug (der Standardwert ist 0 (null)).                                                                                                                                                                                                                                             |
| \\ NoLine      | Keine Zeilennummerierung.                                                                                                                                                                                                                                                             |
| \\ nowidctlpar | Deaktivieren Sie das Steuerelement für das Witwen-/verwaisten                                                                                                                                                                                                                                                 |
| \\ Rück Belastung      | Seitenumbruch vor Absatz.                                                                                                                                                                                                                                                   |
| \\ Durchschnittlicher         | Neuer Absatz.                                                                                                                                                                                                                                                                 |
| \\ par        | Setzt auf Standard Absatz Eigenschaften zurück.                                                                                                                                                                                                                                        |
| \\ zuzugreifen          | Linksbündig (Standard).                                                                                                                                                                                                                                                    |
| \\ QR-          | Rechtsbündig ausgerichtet.                                                                                                                                                                                                                                                                 |
| \\ QJ          | Blocksatz.                                                                                                                                                                                                                                                                     |
| \\ anzubieten          | Zentriert.                                                                                                                                                                                                                                                                      |
| \\ RI *n*      | Rechter Einzug (der Standardwert ist 0 (null)).                                                                                                                                                                                                                                            |
| \\ s *n*       | Stil *n*.                                                                                                                                                                                                                                                                     |
| \\ Sa *n*      | Leerzeichen nach (der Standardwert ist 0 (null)).                                                                                                                                                                                                                                             |
| \\ SB *n*      | Leerzeichen vor (der Standardwert ist 0 (null)).                                                                                                                                                                                                                                            |
| \\ SL *n*      | Wenn der Wert fehlt oder wenn *n*= 1000, wird der Zeilenabstand durch das höchste Zeichen in der Zeile (einzeiligen Abstand) bestimmt. Wenn *n*> NULL ist, wird mindestens diese Größe verwendet. Wenn *n* < NULL ist, wird genau \| *n* \| verwendet. Der Zeilenabstand ist ein mehrzeiligen Abstand, wenn \\ slmult 1 folgt. |
| \\ slmult *m*  | Folgt auf \\ SL. *m* = NULL: mindestens oder genau der Zeilenabstand, wie von \\ SL *n* beschrieben. *m* = 1: Zeilenabstand = *n*/240 mal einzeilige Abstände.                                                                                                                              |
| \\ TB *n*      | Position der Balken Registerkarte, in Twips, vom linken Rand.                                                                                                                                                                                                                              |
| \\ tldot       | Registerkarten-Spitzen Punkte.                                                                                                                                                                                                                                                               |
| \\ f        | Registerkarten-gleich Zeichen.                                                                                                                                                                                                                                                         |
| \\ tlhyph      | Registerkarten-Bindestriche.                                                                                                                                                                                                                                                            |
| \\ tlth        | Linie mit fester Linie für die Registerkarte                                                                                                                                                                                                                                                         |
| \\ tlul        | Tab-Taste unterstrichen.                                                                                                                                                                                                                                                          |
| \\ TQC         | Registerkarte zentriert.                                                                                                                                                                                                                                                                  |
| \\ tqdec       | Dezimaltrennzeichen.                                                                                                                                                                                                                                                                   |
| \\ tqr         | Registerkarte "leeren".                                                                                                                                                                                                                                                               |
| \\ TX *n*      | Registerkarten Position in Twips vom linken Rand.                                                                                                                                                                                                                                  |



 

**Zeichen Format-Steuer Wörter für Tom RTF**

| Steuerwort     | Bedeutung                                                                                                                                                                                                                                  |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ Animation *n* | Legt den Animationstyp auf *n* fest.                                                                                                                                                                                                              |
| \\ b             | Fettdruck                                                                                                                                                                                                                                    |
| \\ Deck          | Alle Großbuchstaben.                                                                                                                                                                                                                            |
| \\ CF *n*        | Vordergrundfarbe (Standardwert ist **tomautocolor**).                                                                                                                                                                                      |
| \\ CS *n*        | Zeichenstil *n*.                                                                                                                                                                                                                     |
| \\ DN *n*        | Die Indexposition in halben Punkten (der Standardwert ist 6).                                                                                                                                                                                    |
| \\ EMBO          | Geprägt.                                                                                                                                                                                                                                |
| \\ f *n*         | Schriftart Nummer, *n* bezieht sich auf einen Eintrag in der Schriftart Tabelle.                                                                                                                                                                                   |
| \\ FS *n*        | Schrift Grad in halben Punkten (der Standardwert ist 24).                                                                                                                                                                                            |
| \\ Hervorhebung von *n* | Hintergrundfarbe (Standardwert ist **tomautocolor**).                                                                                                                                                                                      |
| \\ Ich             | Kursiv.                                                                                                                                                                                                                                  |
| \\ Impr          | Lösch.                                                                                                                                                                                                                                 |
| \\ lang *n*      | Wendet eine Sprache auf ein Zeichen an. *n* ist eine Zahl, die einer Sprache entspricht. Das \\ einfache Steuerwort setzt die Language-Eigenschaft auf die Sprache zurück, die \\ in den Dokumenteigenschaften von deflang *n* definiert wurde.                             |
| \\ nosupersub    | Deaktiviert das hoch gestellt-oder-Abonnement.                                                                                                                                                                                                      |
| \\ Outl          | Risses.                                                                                                                                                                                                                                 |
| \\ Lin         | Setzt Zeichen Formatierungs Eigenschaften auf einen Standardwert zurück, der von der Anwendung definiert wird. Die zugehörigen Zeichen Formatierungs Eigenschaften (die im Abschnitt zugehörige Zeichen Eigenschaften in der RTF-Spezifikation beschrieben werden) werden ebenfalls zurückgesetzt. |
| \\ scaps         | Kleine Hauptstädte.                                                                                                                                                                                                                          |
| \\ Shad          | Schattet.                                                                                                                                                                                                                                  |
| \\ Tag        | Durchgestrichen.                                                                                                                                                                                                                           |
| \\ nationale           | Wendet den Index auf Text an und reduziert die Größe des Punkts entsprechend der Schriftart Informationen.                                                                                                                                                          |
| \\ Super         | Wendet hoch gestellt auf Text an und reduziert die Größe des Punkts gemäß den Schriftart Informationen.                                                                                                                                                        |
| \\ nützlichen            | Fortlaufender unterstrich. \\ ul0 deaktiviert alle Unterstreichung.                                                                                                                                                                                  |
| \\ ULD           | Gepunktete Unterstreichung                                                                                                                                                                                                                        |
| \\ ULDB          | Doppelter unterstrich.                                                                                                                                                                                                                        |
| \\ ulnone        | Beendet alle Unterstreichung.                                                                                                                                                                                                                   |
| \\ ulW           | Word-Unterstreichung.                                                                                                                                                                                                                          |
| \\ aufwärts *n*        | Superscript-Position in halb Punkten (der Standardwert ist 6).                                                                                                                                                                                  |
| \\ Ramelow             | Versteckter Text.                                                                                                                                                                                                                             |



 

## <a name="finding-rich-text"></a>Suchen von reichem Text

Sie können Tom-Methoden verwenden, um Rich-Text zu finden, wie durch einen Textbereich definiert. Das Auffinden eines solchen umfangreichen Texts ist häufig bei der Verarbeitung von Wörtern erforderlich, obwohl er nie in einem "was Sie sehen, was Sie sehen" (WYSIWYG) Word-Prozessor ist. Es gibt deutlich eine größere Domäne der Rich-Text-Übereinstimmung, mit der einige Zeichen Formatierungs Eigenschaften ignoriert werden können (oder um die Absatz Formatierung und/oder den Objekt Inhalt einzuschließen). solche Verallgemeinerungen gehen jedoch über den Rahmen dieses Abschnitts hinaus.

Ein Zweck für diese Funktionalität ist die Verwendung eines Rich-Text-Such Dialogfelds, um den Rich **-Text zu** definieren, den Sie in einem Dokument suchen möchten. Das Dialogfeld wird mithilfe eines Rich-Edit-Steuer Elements implementiert, und Tom-Methoden werden verwendet, um die Suche durch das Dokument durchzuführen. Sie können entweder den gewünschten Rich-Text aus dem Dokument in das Dialogfeld **Suchen** kopieren oder direkt im Dialogfeld **Suchen** eingeben und formatieren.

Im folgenden Beispiel wird gezeigt, wie Sie mithilfe von Tom-Methoden nach Text suchen, der Kombinationen aus der exakten Zeichen Formatierung enthält. Der Algorithmus sucht nach dem reinen Text im Übereinstimmungs Bereich mit dem Namen `pr1` . Wenn der Klartext gefunden wird, wird auf einen Testbereich mit dem Namen verwiesen `pr2` . Anschließend werden zwei einfügepunktbereiche ( `prip1` und `prip2` ) verwendet, um den Testbereich zu durchlaufen, der die Zeichen Formatierung mit der von vergleicht `pr1` . Wenn Sie genau übereinstimmen, wird der Eingabebereich (angegeben durch `ppr` ) aktualisiert, um auf den Text des Testbereichs zu verweisen, und die Funktion gibt die Anzahl der Zeichen im übereinstimmenden Bereich zurück. Zwei [**itextfont**](/windows/desktop/api/Tom/nn-tom-itextfont) -Objekte, `pf1` und `pf2` , werden beim Zeichen Formatierungs Vergleich verwendet. Sie werden an die einfügepunktbereiche `prip1` und angefügt `prip2` .


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



## <a name="tom-accessibility"></a>Tom-Barrierefreiheit

Tom bietet Barrierefreiheits Unterstützung über die Schnittstellen [**itextselection**](/windows/desktop/api/Tom/nn-tom-itextselection) und [**itextrange**](/windows/desktop/api/Tom/nn-tom-itextrange) . In diesem Abschnitt werden Methoden beschrieben, die für die Barrierefreiheit nützlich sind, und wie ein Programm die *x*-, *y* -Bildschirmposition eines Objekts bestimmen kann.

Da Benutzeroberflächen basierte Barrierefreiheits Programme in der Regel mit dem Bildschirm und der Maus funktionieren, ist es häufig von Bedeutung, die entsprechende [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) -Schnittstelle für die aktuelle Mausposition (in Bildschirm Koordinaten) zu finden. In den folgenden Abschnitten finden Sie zwei Möglichkeiten, die richtige Schnittstelle zu bestimmen:

-   [Durch die Tabelle "Running-Object"](#interface-from-running-object-table)
-   Durch die [**EM \_ getoleinterface**](em-getoleinterface.md) -Nachricht, die für Fenster reiche Bearbeitungs Instanzen funktioniert, vorausgesetzt, der Client befindet sich im gleichen Prozessbereich *(kein* Marshalling erforderlich)

Weitere Informationen finden Sie in der Microsoft Active Accessibility-Spezifikation. Nachdem Sie ein Objekt von einer Bildschirmposition abgerufen haben, können Sie für eine [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) -Schnittstelle verwenden und die [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) -Methode aufrufen, um ein leeres Bereichs Objekt auf dem CP abzurufen, das der Bildschirmposition entspricht.

### <a name="interface-from-running-object-table"></a>Schnittstelle aus der Ausführung der Objekttabelle

Eine aktive Objekttabelle (rot) teilt mit, welche Objektinstanzen aktiv sind. Wenn Sie diese Tabelle Abfragen, können Sie den Prozess der Verbindungs Herstellung eines Clients mit einem Objekt beschleunigen, wenn das Objekt bereits ausgeführt wird. Bevor Programme über die laufende Objekttabelle auf Tom-Schnittstellen zugreifen können, muss sich eine Tom-Instanz mit einem Fenster mithilfe eines Monikers in der rot registrieren. Sie erstellen den Moniker aus einer Zeichenfolge, die den Hexadezimalwert des [**HWND**](/windows/desktop/WinProg/windows-data-types)enthält. Das folgende Codebeispiel zeigt, wie dies geschieht.


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



### <a name="interface-from-window-messages"></a>Schnittstelle von Fenster Meldungen

Die [**\_ getoleinterface**](em-getoleinterface.md) -Nachricht von EM bietet eine weitere Möglichkeit zum Abrufen einer [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle für ein Objekt an einer bestimmten Bildschirmposition. Wie unter [Interface from Running Object Table](#interface-from-running-object-table)beschrieben, erhalten Sie ein [**HWND**](/windows/desktop/WinProg/windows-data-types) für die Bildschirmposition und senden diese Nachricht dann an dieses **HWND**. Die **\_ getoleinterface** -Nachricht von EM ist umfangreich bearbeitet und gibt einen Zeiger auf eine [**iricheditole**](/windows/desktop/api/Richole/nn-richole-iricheditole) -Schnittstelle in der von *LPARAM* adressierten Variablen zurück.

**Tipp** Wenn ein Zeiger zurückgegeben wird (stellen Sie sicher, dass das Objekt, auf das *LPARAM* verweist, vor dem Senden der Nachricht auf NULL festgelegt wird), können Sie die [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode zum Abrufen einer [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) -Schnittstelle abrufen. Das folgende Codebeispiel veranschaulicht diese Vorgehensweise.


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



### <a name="accessibility-oriented-methods"></a>Barrierefreiheits orientierte Methoden

Einige Tom-Methoden sind besonders nützlich, um auf dem Bildschirm zu navigieren, während andere Tom-Methoden das tun, was Sie tun können, wenn Sie zu interessanten Orten gelangen. In der folgenden Tabelle werden die nützlichsten Methoden beschrieben.



| Methode                                                 | Herauf Stufen der Barrierefreiheit                                                                                                                                                                 |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSelection**](/windows/desktop/api/Tom/nf-tom-itextdocument-getselection)     | Diese Methode ruft die aktive Auswahl ab, die für eine Vielzahl von Ansichts orientierten Zwecken verwendet werden kann, z. b. zum Markieren von Text und scrollen.                                                      |
| [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) | Bei Verwendung für eine aktive Auswahl wird sichergestellt, dass diese Methode einen Bereich erhält, der einer bestimmten Ansicht zugeordnet ist.                                                                                 |
| [**Expand**](/windows/desktop/api/Tom/nf-tom-itextrange-expand)                    | Vergrößert einen Textbereich, sodass alle darin enthaltenen partiellen Einheiten vollständig enthalten sind. Beispielsweise `Expand(tomWindow)` erweitert den Bereich, um den sichtbaren Teil der Story des Bereichs einzubeziehen. |
| [**Getduplicate**](/windows/desktop/api/Tom/nf-tom-itextrange-getduplicate)        | Bei Verwendung für eine aktive Auswahl wird sichergestellt, dass diese Methode einen Bereich erhält, der einer bestimmten Ansicht zugeordnet ist. Weitere Informationen finden Sie in der Beschreibung von [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint).  |
| [**GetPoint**](/windows/desktop/api/Tom/nf-tom-itextrange-getpoint)                | Ruft die Bildschirm Koordinaten für die Position des Anfangs-oder Endzeichens im Textbereich ab.                                                                                                        |
| [**ScrollIntoView**](/windows/desktop/api/Tom/nf-tom-itextrange-scrollintoview)    | Scrollt einen Textbereich in die Ansicht.                                                                                                                                                               |
| [**SetPoint**](/windows/desktop/api/Tom/nf-tom-itextrange-setpoint)                | Wählt Text von bis zu einem angegebenen Punkt aus.                                                                                                                                              |



 

## <a name="character-match-sets"></a>Zeichen Übereinstimmungs Sätze

Der *Variant* -Parameter **der verschiedenen Verschiebungs** \* Methoden in [**itextrange**](/windows/desktop/api/Tom/nn-tom-itextrange)(z. b. [**MoveWhile**](/windows/desktop/api/Tom/nf-tom-itextrange-movewhile) und [**MoveUntil**](/windows/desktop/api/Tom/nf-tom-itextrange-moveuntil)) kann eine explizite Zeichenfolge oder einen Zeichen-Match-Satz mit 32-Bit-Index annehmen. Die Indizes werden entweder durch Unicode-Bereiche oder [**getstringtypeex**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) -Zeichensätze definiert. Der Unicode-Bereich, beginnend bei *n* und der Länge *l* (< 32768), wird durch den Index *n* + (*l <*< 16) + 0x80000000 angegeben. Beispielsweise werden die grundlegenden griechischen Buchstaben durch CR \_ Greek = 0x805f0370 definiert, und druckbare ASCII-Zeichen werden durch CR \_ asciiprint = 0x805e0020 definiert. Darüber hinaus können Sie mit den Methoden " **muvewhile** " und " **muveuntil** " schnell eine Spanne von Zeichen in einem beliebigen **getstringtypeex** -Zeichensatz oder in einer Spanne von Zeichen, die sich nicht in einem dieser Zeichensätze befindet, umgehen.

Die [**getstringtypeex**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) -Sätze werden durch die Werte für *Ctype1*, *Ctype2* und *Ctype3* angegeben und wie folgt definiert.



| Cset                 | Bedeutung                          |
|----------------------|----------------------------------|
| *Ctype1*             | Kombination von CT- \_ CTYPE1-Typen. |
| *Ctype2* + tomCType2 | Beliebiger CT- \_ CTYPE2-Typ.             |
| *Ctype3* + tomCType3 | Kombination von CT- \_ CTYPE3-Typen. |



 

*Ctype1* kann eine beliebige Kombination der folgenden sein.



| Ctype1 | Wert  | Bedeutung                                                           |
|-------------|--------|-------------------------------------------------------------------|
| C1 ( \_ oben)   | 0x0001 | Großbuchstaben.                                                        |
| C1 ( \_ niedriger)   | 0x0002 | Kleinbuchstaben.                                                        |
| C1- \_ Ziffer   | 0x0004 | Dezimalziffern.                                                   |
| C1- \_ Speicherplatz   | 0x0008 | Leerzeichen.                                                 |
| C1- \_ punct   | 0x0010 | Interpunktions.                                                      |
| C1- \_ CNTRL   | 0x0020 | Steuerzeichen.                                               |
| C1 \_ leer   | 0x0040 | Leerzeichen.                                                 |
| C1- \_ xdigit  | 0x0080 | Hexadezimale Ziffern.                                               |
| C1- \_ Alpha   | 0x0100 | Beliebiges linguistisches Zeichen (alphabetisch, silabär oder ideografisch). |
| C1 \_ definiert | 0x0200 | Ein definiertes Zeichen, aber nicht einer der anderen C1- \_ \* Typen.       |



 

Die *Ctype2* -Typen unterstützen das ordnungsgemäße Layout von Unicode-Text. Die Direction-Attribute werden zugewiesen, sodass der von Unicode standardisierte bidirektionale layouthmus genaue Ergebnisse liefert. Diese Typen schließen sich gegenseitig aus. Weitere Informationen zur Verwendung dieser Attribute finden Sie unter Unicode- *Standard: weltweite Zeichencodierung, Volumes 1 und 2*, Addison-Wesley Publishing Company: 1991, 1992.



| CType2          | Wert | Bedeutung                          |
|----------------------|-------|----------------------------------|
| Starke              |       |                                  |
| C2 \_ LeftToRight      | 0x1   | Von links nach rechts.                   |
| C2 \_ RightToLeft      | 0x2   | Von rechts nach links.                   |
| Weak                |       |                                  |
| C2- \_ europenumber     | 0x3   | Europäische Zahl, Europäische Ziffer. |
| C2- \_ europeseparser  | 0x4   | Europäisches numerisches Trennzeichen.      |
| C2-Abschluss Zeichen \_ | 0x5   | Europäisches numerisches Terminator.     |
| C2 \_ arabicnumber     | 0x6   | Arabische Zahl.                   |
| C2 \_ commonseparator  | 0x7   | Gängiges numerisches Trennzeichen.        |
| Neutrale             |       |                                  |
| C2- \_ blockseparator   | 0x8   | Block Trennzeichen.                 |
| C2 \_ segmentseparator | 0x9   | Segment Trennzeichen.               |
| C2- \_ Whitespace       | 0xa   | Leerraum.                     |
| C2 \_ otherneutral     | 0xB   | Andere neutrale.                  |
| Nicht zutreffend:      |       |                                  |
| C2 \_ NotApplicable    | 0x0   | Keine implizite Richtung.           |



 

Die *Ctype3* -Typen dienen als Platzhalter für Erweiterungen der POSIX-Typen, die für die allgemeine Textverarbeitung oder für die Standard-C-Bibliotheksfunktionen erforderlich sind.



| CType3       | Wert  | Bedeutung                                                             |
|-------------------|--------|---------------------------------------------------------------------|
| \_Nicht Abstände von C3    | 0x1    | Nicht-Abstands Markierung.                                                    |
| C3- \_ diakritisch     | 0x2    | Zeichen für diakritische nicht Abstände.                                          |
| C3- \_ vowelmark     | 0x4    | Zeichen für die nicht-Abstände-vowel.                                              |
| C3- \_ Symbol        | 0x8    | Tick.                                                             |
| C3 \_ Katakana      | 0x10   | Katakana-Zeichen.                                                 |
| C3- \_ Hiragana      | 0x20   | Hiragana-Zeichen.                                                 |
| C3 \_ Halfwidth     | 0x40   | Zeichen halber Breite.                                               |
| C3 \_ Fullwidth     | 0x80   | Zeichen mit voller Breite.                                               |
| C3 \_ ideograph     | 0x100  | Ideografisches Zeichen.                                              |
| C3 \_ Kashida       | 0x200  | Arabisches Kashida-Zeichen.                                           |
| C3 \_ Alpha         | 0x8000 | Alle linguistischen Zeichen (alphabetisch, silabär und ideografisch). |
| C3 \_ NotApplicable | 0x0    | Nicht zutreffend                                                     |



 

Ein Edit Development Kit (EDK) kann *pvar* -Index Definitionen für die folgenden Bereiche enthalten, die im Unicode-Standard beschrieben werden.



| Zeichensatz         | Unicode-Bereich | Zeichensatz             | Unicode-Bereich |
|-----------------------|---------------|---------------------------|---------------|
| ASCII                 | 0x0 – 0x7F      | ANSI                      | 0x0 – 0xFF      |
| Asciiprint            | 0x20 – 0x7E     | Latin1                    | 0x20 – 0xFF     |
| Latin1Supp            | 0xa0 – 0xFF     | Latinxa                   | 0x100 – 0x17f   |
| Latinxb               | 0x180 – 0x24f   | Ipax                      | 0x250 – 0x2af   |
| Spacemod              | 0x2b0 – 0x2ff   | Kombinierte                 | 0x300 – 0x36f   |
| Griechisch                 | 0x370 – 0x3ff   | Basicgreek                | 0x370 – 0x3cf   |
| Greeksymbols          | 0x3d0 – 0x3ff   | Kyrillisch                  | 0x400 – 0x4ff   |
| Armenisch              | 0x530 – 0x58f   | Hebräisch                    | 0x590 – 0x5ff   |
| Basichebrew           | 0x5d0 – 0x5ea   | Hebrewxa                  | 0x590 – 0x5cf   |
| Hebrewxb              | 0x5eb – 0x5ff   | Arabisch                    | 0x600 – 0x6ff   |
| Basicarabic           | 0x600 – 0x652   | Arabicx                   | 0x653 – 0x6ff   |
| "De vangari"             | 0x900 – 0x97f   | Bangla (ehemals Bengalisch) | 0x980 – 0x9ff   |
| Gurmukhi              | 0xa00 – 0xa7f   | Gujarati                  | 0xa80 – 0xaff   |
| Odia (früher Oriya) | 0xb00 – 0xb7f   | Tamilisch                     | 0xb80 – 0xbff   |
| Teluga                | 0xc00 – 0xc7f   | Kannada                   | 0xc80 – 0xcff   |
| Malayalam             | 0xd00 – 0xd7f   | Thailändisch                      | 0xe00 – 0xe7f   |
| Laotisch                   | 0xe80 – 0xeff   | Georgianx                 | 0x10a0 – 0xa0cf |
| Bascgeorgian          | 0x10d0 – 0x10ff | Jamo                      | 0x1100 – 0x11ff |
| Latinxadd             | 0x1E00 – 0x1EFF | Greekx                    | 0x1f00 – 0x1fff |
| Genpunct              | 0x2000 – 0x206f | Hochgestellt               | 0x2070 – 0x207f |
| Tiefgestellt             | 0x2080 – 0x208f | Superabonniert            | 0x2070 – 0x209f |
| Währung              | 0x20a0 – 0x20cf | Combmarksym               | 0x20d0 – 0x20ff |
| Letterlike            | 0x2100 – 0x214f | Anzahlformulare               | 0x2150 – 0x218 f |
| Pfeile                | 0x2190 – 0x21ff | Mathops                   | 0x2200 – 0x22ff |
| Falsch Tech              | 0x2300 – 0x23ff | Ctrlpictures              | 0x2400 – 0x243f |
| Optcharrecog          | 0x2440 – 0x245f | Umclalpha-Anum              | 0x2460 – x24ff  |
| Boxdrawing            | 0x2.500 – 0x257f | Block Element              | 0x2580 – 0x259f |
| Geometshapes          | 0x25a0 – 0x25ff | Falsch Symbole               | 0x2600 – 0x26ff |
| Dingbats              | 0x2700 – 0x27bf | Cjksympunct               | 0x3000 – 0x303f |
| Hiragana              | 0x3040 – 0x309f | Katakana                  | 0x30a0 – 0x30ff |
| Bopomofo              | 0x3100 – 0x312f | Hanguljamo                | 0x3130 – 0x318f |
| Cjlmisc               | 0x3190 – 0x319f | Umclcjk                   | 0x3200 – 0x32ff |
| Cjkcompatibl          | 0x3300 – 0x33ff | Nachrichten                       | 0x3400 – 0xabff |
| Hangul                | 0xac00 – 0xd7ff | UTF16Lead                 | 0xD800 – 0xDBFF |
| UTF16Trail            | 0xDC00 – 0xDFFF | Privateuse                | 0xE000 – 0xF 800 |
| Cjkcompideog          | 0xF 900 – 0xF. | Alphapres                 | 0xF B00 – 0xF b4f |
| Arabicpresa           | 0xF B50 – 0xbdff | Combhalfmark              | 0xfe20 – 0xfe2f |
| Cjkcompform           | 0xfe30 – 0xfe4f | Smallformvar              | 0xfe50 – 0xfe6f |
| Arabicpresb           | 0xfe70 – 0xfefe | Halffullform              | 0xFF00 – 0xffef |
| Spezi              | 0xfff0 – 0xFFFD |                           |               |



 

 

 