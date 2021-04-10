---
title: Einführung in DirectWrite
description: Menschen kommunizieren mit Text in Ihrem täglichen Leben.
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite, Informationen
- DirectWrite, typografische Features
- Typografie
- DirectWrite, internationaler Text
- DirectWrite, OpenType-Schriftarten
- OpenType-Schriftarten
- DirectWrite, ClearType
- ClearType
- DirectWrite, API-Übersicht
- DirectWrite, idschreitefontface
- Idschreitefontface
- DirectWrite, Text Rendering
- DirectWrite, Renderingmodi
- DirectWrite, GDI-Interoperation
- DirectWrite, Interoperabilität
- Interoperabilität, DirectWrite
- Interoperabilität, Graphics Device Interface (GDI)
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858447"
---
# <a name="introducing-directwrite"></a>Einführung in DirectWrite

Menschen kommunizieren mit Text in Ihrem täglichen Leben. Dies ist die primäre Methode für Personen, eine zunehmende Menge an Informationen zu verbrauchen. In der Vergangenheit war die Verwendung von gedruckten Inhalten, hauptsächlich Dokumenten, Zeitungen, Büchern usw.,. Es handelt sich immer mehr um Online Inhalte auf Ihrem Windows-PC. Ein typischer Windows-Benutzer verbringt viel Zeit mit dem Lesen des Computerbildschirms. Sie können im Web Surfen, e-Mails scannen, einen Bericht verfassen, eine Kalkulations Tabelle ausfüllen oder Software schreiben, aber tatsächlich wird das Lesen durchgeführt. Obwohl Text und Schriftarten fast jeden Teil der Benutzer Darstellung in Windows durchdringen, ist das Lesen auf dem Bildschirm für die meisten Benutzer nicht so angenehm wie das Lesen der gedruckten Ausgabe.

Für Entwickler von Windows-Anwendungen ist das Schreiben von Text Behandlungs Code eine Herausforderung, da die Anforderungen für eine bessere Lesbarkeit, eine ausgereifte Formatierung und Layoutsteuerung sowie die Unterstützung für mehrere Sprachen, die von der Anwendung angezeigt werden müssen, erhöht werden. Selbst das grundlegendste Textverarbeitungssystem muss Texteingabe, Layout, Anzeige, Bearbeitung und kopieren und einfügen zulassen. Windows-Benutzer erwarten in der Regel sogar mehr als diese grundlegenden Features, sodass auch einfache Editoren mehrere Schriftarten, verschiedene Absatzformate, eingebettete Bilder, Rechtschreibprüfung und andere Features unterstützen müssen. Das moderne Design der Benutzeroberfläche ist auch nicht mehr auf das nur-Text-Format beschränkt, sondern muss auch eine bessere Oberfläche mit umfangreichen Schriftarten und Textlayouts bieten.

Dies ist eine Einführung in die Art und Weise, wie [DirectWrite](direct-write-portal.md) Windows-Anwendungen ermöglicht, den Text für die Benutzeroberfläche und Dokumente zu verbessern

## <a name="improving-the-text-experience"></a>Verbessern des Text Erlebnisses

Moderne Windows-Anwendungen haben anspruchsvolle Anforderungen an Text in der Benutzeroberfläche und in den Dokumenten. Diese umfassen eine bessere Lesbarkeit, Unterstützung für eine Vielzahl von Sprachen und Skripts sowie eine überlegene Renderingleistung. Außerdem erfordern die meisten vorhandenen Anwendungen eine Möglichkeit, vorhandene Investitionen in die WindowsWin32-Codebasis auszuführen.

[DirectWrite](direct-write-portal.md) bietet die folgenden drei Features, mit denen Entwickler von Windows-Anwendungen die Textdarstellung innerhalb Ihrer Anwendungen verbessern können: Unabhängigkeit vom Renderingsystem, hochwertige Typografie und mehrere Funktionsebenen.

## <a name="rendering-system-independence"></a>Rendering-System Unabhängigkeit

[DirectWrite](direct-write-portal.md) ist unabhängig von einer bestimmten Grafiktechnologie. Anwendungen können die renderingtechnologie verwenden, die für Ihre Anforderungen am besten geeignet ist. Dadurch haben Anwendungen die Flexibilität, einige Teile Ihrer Anwendung mithilfe von GDI und anderen Teilen über Direct3D oder [Direct2D](../direct2d/direct2d-portal.md)weiter zurendern. Tatsächlich kann eine Anwendung das Rendern von DirectWrite über einen proprietären renderingstapel auswählen.

## <a name="high-quality-typography"></a>TypografieHigh-Quality

[DirectWrite](direct-write-portal.md) nutzt die Verbesserungen in der [OpenType](../intl/opentype-font-format.md) -Schriftart Technologie, um qualitativ hochwertige Typografie innerhalb einer Windows-Anwendung zu ermöglichen. Das Schriftart System von DirectWrite bietet Dienste für den Umgang mit Schriftart Enumeration, Schriftart fallback und Schriftart Caching, die alle von Anwendungen zum Verarbeiten von Schriftarten benötigt werden.

Die von [DirectWrite](direct-write-portal.md) bereitgestellte [OpenType](../intl/opentype-font-format.md) -Unterstützung ermöglicht es Entwicklern, Ihren Anwendungen Erweiterte typografische Features und Unterstützung für internationalen Text hinzuzufügen.

## <a name="support-for-advanced-typographic-features"></a>Unterstützung für erweiterte typografische Features

Mithilfe von [DirectWrite](direct-write-portal.md) können Anwendungsentwickler die Features von OpenType-Schriftarten entsperren, die Sie in WinForms oder GDI nicht verwenden können. Das "DirectWrite [**idwrite tetypografie**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) "-Objekt macht viele erweiterte Features von OpenType-Schriftarten verfügbar, wie z. b. Stilvarianten und Swashes. Das Microsoft Windows Software Development Kit (SDK) bietet eine Reihe von [OpenType](../intl/opentype-font-format.md) -Beispiel Schriftarten, die mit umfangreichen Funktionen wie den Schriftarten "Pericles" und "Pescadero" entworfen wurden. Weitere Informationen zu OpenType-Funktionen finden Sie unter [OpenType-Schriftart Features](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).

## <a name="support-for-international-text"></a>Unterstützung für internationalen Text

[DirectWrite](direct-write-portal.md) verwendet [OpenType](../intl/opentype-font-format.md) -Schriftarten, um eine umfassende Unterstützung für internationalen Text zu ermöglichen. Unicode-Features, wie z. b. Surrogates, Bidi, Zeilenumbruch und UVS, werden unterstützt. Durch sprachgesteuerte Skripterstellung, Zahlen Ersetzung und Symbol Strukturierung wird sichergestellt, dass der Text in jedem Skript über das richtige Layout und Rendering verfügt.

Die folgenden Skripts werden zurzeit unterstützt:

> [!Note]  
> Bei Skripts, die mit einem gekennzeichnet \* sind, gibt es keine standardmäßigen System Schriftarten. Anwendungen müssen Schriftarten installieren, die diese Skripts unterstützen.

 

-   Arabisch
-   Armenisch
-   Bengala
-   Bopomofo
-   Braille\*
-   Kanadische Aborigines-Silben
-   Cherokee
-   Chinesisch (vereinfacht & traditionell)
-   Kyrillisch
-   Koptisch\*
-   Devanagari
-   Ethiopic
-   Georgisch
-   Glagolitisch\*
-   Griechisch
-   Gujarati
-   Gurmukhi
-   Hebräisch
-   Japanisch
-   Kannada
-   Khmer
-   Koreanisch
-   Laotisch
-   Lateinisch
-   Malayalam
-   Mongolisch
-   Myanmar
-   Neue Tai-Lue
-   Ogam\*
-   Odia
-   "Phags-pa"
-   Runisch\*
-   Singhalesisch
-   Syrisch
-   Tai-Le
-   Tamilisch
-   Telugu
-   Thaana
-   Thailändisch
-   Tibetisch
-   Yi

## <a name="multiple-layers-of-functionality"></a>Mehrere Funktionsebenen

[DirectWrite](direct-write-portal.md) bietet faktorisierte Funktionsebenen, wobei jede Ebene nahtlos mit der nächsten interagiert. Der API-Entwurf bietet Anwendungsentwicklern die Freiheit und Flexibilität, individuelle Schichten abhängig von Ihren Anforderungen und dem Zeitplan zu übernehmen. Das folgende Diagramm zeigt die Beziehung zwischen diesen Ebenen.

![Diagramm der DirectWrite-Ebenen und ihrer Kommunikation mit einer Anwendung oder einem UI-Framework und der Grafik-API](images/intro-01.png)

Die textlayoutapi bietet die Funktionen der höchsten Ebene, die in [DirectWrite](direct-write-portal.md)verfügbar sind. Es stellt Dienste für die Anwendung bereit, mit denen umfangreich formatierte Text Zeichenfolgen gemessen, angezeigt und mit ihnen interagieren können. Diese Text-API kann in Anwendungen verwendet werden, die derzeit Win32's DrawText verwenden, um eine moderne Benutzeroberfläche mit Umfang reichformatiertem Text zu erstellen.

Text intensive Anwendungen, die ihre eigene LayoutEngine implementieren, können die nächste Ebene nach unten verwenden: der Skript Prozessor. Der Skript Prozessor teilt einen Text Block in Skriptblöcke auf und behandelt die Zuordnung zwischen Unicode-Darstellungen und der entsprechenden Symboldarstellung in der Schriftart, damit der Text des Skripts ordnungsgemäß in der richtigen Sprache angezeigt werden kann. Das Layoutsystem, das von der textlayoutapi-Ebene verwendet wird, basiert auf dem Schriftart-und Skript Verarbeitungssystem.

Die Glyphe-renderingschicht ist die niedrigste Funktionalitäts Ebene und bietet Funktionen zum Rendern von Symbolen für Anwendungen, die ihre eigene Textlayoutengine implementieren. Die Symbol Rendering-Ebene ist auch nützlich für Anwendungen, die einen benutzerdefinierten Renderer implementieren, um das Symbol zum Zeichnen von Symbolen durch die Rückruffunktion in der [DirectWrite](direct-write-portal.md) -Text Formatierungs-API zu ändern.

Das Schriftart System von [DirectWrite](direct-write-portal.md) ist für alle DirectWrite-Funktionsebenen verfügbar und ermöglicht es einer Anwendung, auf Schriftart-und Symbol Informationen zuzugreifen. Es wurde entwickelt, um allgemeine Schriftart Technologien und Datenformate zu verarbeiten. Das DirectWrite-Schrift Modell folgt der allgemeinen typografischen Praxis, bei der eine beliebige Anzahl von Gewichtungen, Stilen und Strecken in derselben Schriftfamilie unterstützt wird. Dieses Modell, das gleiche Modell, gefolgt von WPF und CSS, gibt an, dass Schriftarten, die sich nur in Gewichtung (Fett, hell usw.), Style (AUFSTEIG, kursiv oder schräg) oder Streckung (schmal, komprimiert, breit usw.) unterscheiden, als Member einer einzelnen Schriftfamilie betrachtet werden.

### <a name="improved-text-rendering-with-cleartype"></a>Verbessertes Text Rendering mit ClearType

Das verbessern der Lesbarkeit auf dem Bildschirm ist eine wichtige Voraussetzung für alle Windows-Anwendungen. Der Beweis der Forschung in Cognitive Psychologie deutet darauf hin, dass wir in der Lage sein müssen, jeden Buchstaben genau zu erkennen, und dass sogar der Abstand zwischen Buchstaben für die schnelle Verarbeitung entscheidend ist. Buchstaben und Wörter, die nicht symmetrisch sind, werden als hässlich empfunden und beeinträchtigen das Leseverhalten. Kevin Larson, Microsoft Advanced Reading Technologies Group, hat einen Artikel zu dem Thema verfasst, das in "Spektrum IEEE" veröffentlicht wurde. Der Artikel wird als "die Technologie von Text" bezeichnet ( https://www.spectrum.ieee.org/print/5049) .

Der Text in [DirectWrite](direct-write-portal.md) wird mithilfe von Microsoft ClearType gerendert, wodurch die Übersichtlichkeit und Lesbarkeit von Text verbessert wird. ClearType nutzt die Tatsache, dass moderne LCD-Fenster RGB-Streifen für jedes Pixel aufweisen, das einzeln gesteuert werden kann. DirectWrite verwendet die neuesten Erweiterungen von ClearType, die zuerst in Windows Vista mit Windows Presentation Foundation enthalten waren, sodass es nicht nur die einzelnen Buchstaben, sondern auch den Abstand zwischen Buchstaben auswerten kann. Vor diesen ClearType-Erweiterungen war es schwierig, Text mit einer "Lese"-Größe von 10 oder 12 Punkten anzuzeigen: Wir konnten entweder 1 Pixel zwischen Buchstaben platzieren, was oft zu wenig war, oder 2 Pixel, was oft zu viel war. Die Verwendung der zusätzlichen Auflösung in den Subpixeln stellt uns einen Bruch Bruch dar, der die Gleichmäßigkeit und Symmetrie der gesamten Seite verbessert.

In der folgenden Abbildung wird gezeigt, wie Symbole bei der Positionierung von Subpixeln an einer beliebigen Subpixelgrenze beginnen können.

Die folgende Abbildung wird mithilfe der GDI-Version des ClearType-Renderers gerendert, der keine unter Pixel Positionierung verwendet hat.

![Darstellung der "Technologie", die ohne unter Pixel Positionierung gerendert wird](images/intro-03.png)

Die folgende Abbildung wird mithilfe der [DirectWrite](direct-write-portal.md) -Version des ClearType-Renderers gerendert, der die unter Pixel Positionierung verwendet.

![Abbildung der "Technologie", die mit der unter Pixel Positionierung gerendert wird](images/intro-04.png)

Beachten Sie, dass der Abstand zwischen den Buchstaben h und n mehr ist, auch im zweiten Bild, und der Buchstabe o wird weiter von dem Buchstaben n entfernt. Dies gilt auch für den Buchstaben l. Beachten Sie auch, dass die Stämme auf den Buchstaben l natürlicher aussehen.

Die Positionierung von subpixelcleartype bietet den genauesten Abstand von Zeichen auf dem Bildschirm, insbesondere bei kleinen Größen, bei denen der Unterschied zwischen einem Subpixel und einem ganzen Pixel einen signifikanten Anteil der Glyphe darstellt. Sie ermöglicht die Messung von Text im idealen Auflösungs Bereich und wird an seiner natürlichen Position im LCD-Farbstreifen mit der Granularität des Subpixels gerendert. Text, der mit dieser Technologie gemessen und gerendert wird, ist Definitions unabhängig, d. h., dass genau dasselbe Layout von Text über den Bereich verschiedener Anzeige Auflösungen hinweg erreicht wird.

Im Unterschied zu einem Typ des GDI-ClearType-Renderings bietet Sub-Pixel ClearType die präzisere Breite von Zeichen.

Die Text Zeichenfolgen-API übernimmt standardmäßig das Rendern von subpixeltext, d. h., Sie misst Text in seiner idealen Auflösung unabhängig von der aktuellen Bildschirmauflösung und erzeugt das Ergebnis der Symbol Positionierung basierend auf den wirklich skalierten Symbol Vorgängen und der Positions Offsets.

Bei umfangreichen Text ermöglicht [DirectWrite](direct-write-portal.md) auch das Antialiasing entlang der y-Achse, um die Ränder zu vereinfachen und Buchstaben als den Schriftart-Designer zu erzeugen. In der folgenden Abbildung ist das Antialiasing in y-Richtung dargestellt.

![Abbildung von "ClearType", die als GDI-Text und als DirectWrite-Text mit y-Richtung-Antialiasing gerendert wird](images/intro-05.png)

Obwohl [DirectWrite](direct-write-portal.md) -Text standardmäßig mithilfe des untergeordneten Pixels ClearType positioniert und gerendert wird, sind andere Renderingoptionen verfügbar. Viele vorhandene Anwendungen verwenden GDI zum Rendern der meisten Benutzeroberflächen, und einige Anwendungen verwenden die Steuerelemente für die System Bearbeitung, die GDI weiterhin für das Text Rendering verwenden. Wenn Sie diesen Anwendungen DirectWrite-Text hinzufügen, kann es notwendig sein, die Verbesserungen der Lesevorgänge zu Opfern, die von Sub-Pixel ClearType bereitgestellt werden, damit der Text in der gesamten Anwendung einheitlich dargestellt wird.

Um diese Anforderungen zu erfüllen, unterstützt [DirectWrite](direct-write-portal.md) auch die folgenden Renderingoptionen:

-   Sub-Pixel ClearType (Standard).
-   Unter Pixel-ClearType mit Antialiasing in horizontalen und vertikalen Dimensionen.
-   Alias Text.
-   GDI mit natürlicher Breite (z. b. von Microsoft Word Leseansicht).
-   GDI-kompatibel-Breite (einschließlich ostasiatischen eingebetteten Bitmap).

Jeder dieser Renderingmodi kann mithilfe der DirectWrite-API und über den neuen Windows 7-Posteingangs-ClearType-Tuner optimiert werden.

> [!Note]  
> Ab Windows 8 sollten Sie in den meisten Fällen das Antialiasing für Graustufen Text verwenden. Weitere Informationen finden Sie im nächsten Abschnitt.

 

### <a name="support-for-natural-layout"></a>Unterstützung für natürliches Layout

Das natürliche Layout ist auflösungsunabhängig, sodass sich der Abstand von Zeichen nicht ändert, wenn Sie vergrößern oder verkleinern oder abhängig vom dpi-Wert der Anzeige. Ein sekundärer Vorteil besteht darin, dass der Abstand für den Entwurf der Schriftart true ist. Das natürliche Layout wird durch die Unterstützung natürlicher Rendering durch DirectWrite ermöglicht, d. h., einzelne Symbole können auf einen Bruchteil eines Pixels positioniert werden.

Während das natürliche Layout der Standard ist, müssen einige Anwendungen den Text mit dem gleichen Abstand und der gleichen Darstellung wie GDI Rendering. Für solche Anwendungen stellt DirectWrite den klassischen GDI-und GDI-Mess Modus und die entsprechenden Renderingmodi bereit.

Jeder der obigen Renderingmodi kann mit einem der beiden Antialiasing Modi kombiniert werden: ClearType oder Grayscale. ClearType-Antialiasing Simulationen eine höhere Auflösung durch die individuelle Bearbeitung der roten, grünen und blauen Farbwerte jedes Pixels. Graustufen-Antialiasing berechnet nur einen deckwert (oder einen Alpha Wert) für jedes Pixel. ClearType ist die Standardeinstellung, aber Graustufen-Antialiasing wird für Windows Store-Apps empfohlen, da es schneller ist und mit standardantialiasing kompatibel ist, während es immer noch hoch lesbar ist.

## <a name="api-overview"></a>API-Übersicht

Die [**idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Schnittstelle ist der Ausgangspunkt für die Verwendung von DirectWrite-Funktionen. Die Factory ist das Stamm Objekt, das eine Gruppe von Objekten erstellt, die gleichzeitig verwendet werden können.

Der Formatierungs-und Layoutvorgang ist eine Voraussetzung für die Vorgänge, da Text ordnungsgemäß formatiert und für einen bestimmten Satz von Einschränkungen festgelegt werden muss, bevor er gezeichnet oder auf einen Treffer getestet werden kann. Zwei wichtige Objekte, die Sie zu diesem Zweck mit [**idwrite tefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) erstellen können, sind [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). Ein **idwrite-Textformat** -Objekt stellt die Formatierungsinformationen für einen Textabschnitt dar. Die [**idwrite Team Factory:: foratetextlayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) -Funktion nimmt die Eingabe Zeichenfolge, die zugeordneten Einschränkungen, z. b. die Dimension des zu füllenden Speicherplatzes, und das **idwrite-Textformat** -Objekt, und fügt das vollständig analysierte und formatierte Ergebnis in **idschreitetextlayout** ein, das in nachfolgenden Vorgängen verwendet wird.

Die Anwendung kann dann den Text mithilfe der von [Direct2D](../direct2d/direct2d-portal.md) bereitgestellten [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Funktion oder durch Implementieren einer Rückruffunktion, die GDI, Direct2D oder andere Grafik Systeme verwenden kann, um die Symbole zu renderhen. Bei einem einzelnen Formatierungs Text bietet die [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Funktion auf Direct2D eine einfachere Möglichkeit, Text zu zeichnen, ohne zuerst ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt erstellen zu müssen.

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a>Formatieren und Zeichnen von "Hallo Welt" mithilfe von DirectWrite

Im folgenden Codebeispiel wird veranschaulicht, wie eine Anwendung einen einzelnen Absatz mithilfe von [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) formatieren und mithilfe der [Direct2D](../direct2d/direct2d-portal.md)[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Funktion zeichnen kann.


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a>Zugreifen auf das Schriftart System

Zusätzlich zur Angabe eines Schriftart Familiennamens für die Text Zeichenfolge mithilfe der [**idwrite tetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle im obigen Beispiel bietet [DirectWrite](direct-write-portal.md) Anwendungen mehr Kontrolle über die Schriftart Auswahl durch die Schriftart Enumeration und die Möglichkeit, eine benutzerdefinierte Schriftart Auflistung auf der Grundlage von eingebetteten Dokument Schriftarten zu erstellen.

Das [**idwrite-FontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) -Objekt ist eine Sammlung von Schriftfamilien. DirectWrite ermöglicht den Zugriff auf die auf dem System installierten Schriftarten über eine spezielle Schriftart Sammlung, die als System Schriftart Auflistung bezeichnet wird. Dies wird durch Aufrufen der [**getsystemfontcollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) -Methode des [**idwrite-Factory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Objekts abgerufen. Eine Anwendung kann auch eine benutzerdefinierte Schriftart Auflistung aus einem Satz von Schriftarten erstellen, die durch einen Anwendungs definierten Rückruf, d. h. private Schriftarten, die von einer Anwendung installiert wurden, oder in ein Dokument eingebettete Schriftarten aufgelistet sind.

Die Anwendung kann dann [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) aufrufen, um ein bestimmtes FontFamily-Objekt innerhalb der Auflistung zu erhalten, und dann [**idschreitefontfamily:: getfirstmatchingfont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) aufrufen, um zu einem bestimmten [**idschreitefont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) -Objekt zu gelangen. Das **idwrite-Font** -Objekt stellt eine Schriftart in einer Schriftart Auflistung dar und macht Eigenschaften und einige grundlegende Schriftart Metriken verfügbar.

[**Idwrite tefontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) ist ein anderes Objekt, das eine Schriftart darstellt und einen vollständigen Satz von Metriken für eine Schriftart verfügbar macht. Das **idwrite-fontface** -Element kann direkt über einen Schriftart Namen erstellt werden. eine Anwendung muss keine Schriftart Auflistung abrufen, um darauf zugreifen zu können. Dies ist nützlich für eine Textlayoutanwendung wie z. b. Microsoft Word, die die Details für eine bestimmte Schriftart Abfragen muss.

Im folgenden Diagramm wird die Beziehung zwischen diesen Objekten veranschaulicht.

![Diagramm der Beziehung zwischen einer Schriftart Auflistung, einer Schriftfamilie und einer Schriftart](images/fontcollection.png)

### <a name="idwritefontface"></a>Idschreitefontface

Das [**idwrite-fontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) -Objekt stellt eine Schriftart dar und stellt ausführlichere Informationen über die Schriftart bereit als das [**idwrite-Font**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) -Objekt. Die Schriftart-und Glyphe-Metriken aus **idschreitefontface** sind für Anwendungen nützlich, die Text Layout implementieren.

Die meisten gängigen Anwendungen verwenden diese APIs nicht direkt, sondern verwenden stattdessen [**idwrite-Font**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) oder geben den Namen der Schriftfamilie direkt an.

In der folgenden Tabelle werden die Verwendungs Szenarien für die beiden-Objekte zusammengefasst.



| Category                                                                                                         | [**Idschreiteschriftart**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [**Idschreitefontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| APIs zur Unterstützung von Benutzerinteraktionen, z. b. eine Benutzeroberfläche zur Schriftart Auswahl: Beschreibung und andere informative APIs | Ja                                        | Nein                                                 |
| APIs zur Unterstützung der Schriftart Zuordnung: Familie, Stil, Gewichtung, Streckung, Zeichen Abdeckung                                 | Ja                                        | Nein                                                 |
| DrawText-API                                                                                                     | Ja                                        | Nein                                                 |
| Zum Rendering verwendete APIs                                                                                          | Nein                                         | Ja                                                |
| APIs, die für das Text Layout verwendet werden: Glyphe Metriken usw.                                                              | Nein                                         | Ja                                                |
| APIs für UI-Steuerelement und Text Layout: Schriftart weite Metriken                                                           | Ja                                        | Ja                                                |



 

Im folgenden finden Sie eine Beispielanwendung, die die Schriftarten in der System Schriftart Auflistung auflistet.


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a>Rendering von Text

Die Text Rendering-APIs ermöglichen das Rendern von Symbolen in einer [DirectWrite](direct-write-portal.md) -Schriftart an eine [Direct2D](../direct2d/direct2d-portal.md) -Oberfläche oder eine unabhängige GDI-Geräte Bitmap oder die Konvertierung in-oder-Bitmaps. Das ClearType-Rendering in DirectWrite unterstützt die unter Pixel Positionierung mit verbesserter Schärfe und Kontrast im Vergleich zu vorherigen Implementierungen unter Windows. DirectWrite unterstützt auch einen schwarz-und weißem Text mit Alias, um Szenarien mit ostasiatischen Schriftarten mit eingebetteten Bitmaps zu unterstützen, oder wenn der Benutzer die Schriftart Glättung eines beliebigen Typs deaktiviert hat.

Alle Optionen sind für alle verfügbaren ClearType-Knoten, auf die über die [DirectWrite](direct-write-portal.md) -APIs zugegriffen werden kann, anpassbar und werden auch über das neue System Steuerungs Applet Windows 7 ClearType-Tuner verfügbar gemacht.

Es stehen zwei APIs für das Rendern von Symbolen zur Verfügung, von denen eine Hardware beschleunigtes Rendering über [Direct2D](../direct2d/direct2d-portal.md) und die andere das Software Rendering für eine GDI-Bitmap bereitstellt. Eine Anwendung, die [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) verwendet und den [**idwrite-TextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) -Rückruf implementiert, kann eine dieser Funktionen als Reaktion auf einen [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Rückruf aufrufen. Außerdem können Anwendungen, die ein eigenes Layout implementieren oder mit Daten auf Symbolebene umgehen, diese APIs verwenden.

1.  [**ID2DRenderTarget::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    Anwendungen können mit der [Direct2D](../direct2d/direct2d-portal.md) [**-API DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) Hardwarebeschleunigung für das Text Rendering mithilfe der GPU bereitstellen. Die Hardware Beschleunigung wirkt sich auf alle Phasen der Textrenderingpipeline aus – von der Zusammenführung von Symbolen in Glyphe und dem Filtern der Glyphe-Run-Bitmap bis zum Anwenden des ClearType-Mischungs Algorithmus auf die endgültige angezeigte Ausgabe. Dies ist die empfohlene API, um die beste Renderingleistung zu erzielen.

2.  [**Idschreitebitmaprendertarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    Anwendungen können die [**idschreitebitmaprendertarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) -Methode verwenden, um ein Software Rendering einer Ausführung von Symbolen in eine 32-bpp-Bitmap auszuführen. Das [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Objekt kapselt eine Bitmap und einen Speichergeräte Kontext, der zum Rendern von Glyphen verwendet werden kann. Diese API ist nützlich, wenn Sie GDI beibehalten möchten, da Sie über eine vorhandene Codebasis verfügen, die in GDI gerendert wird.

Wenn Sie über eine Anwendung mit vorhandenem textlayoutcode verfügen, der GDI verwendet, und Sie den vorhandenen Layoutcode beibehalten möchten, aber [DirectWrite](direct-write-portal.md) nur für den letzten Schritt des Renderings von Symbolen verwenden, stellt [**idschreitegdiinterop:: anatefontfacefromhdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) die Brücke zwischen den beiden APIs bereit. Vor dem Aufrufen dieser Funktion verwendet die Anwendung die **idschreitegdiinterop:: createfontfakefromhdc** -Funktion, um einen Schriftart Verweis aus einem Gerätekontext abzurufen.

> [!Note]  
> In den meisten Szenarien müssen Anwendungen diese Glyphe-Rendering-APIs möglicherweise nicht verwenden. Nachdem eine Anwendung ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt erstellt hat, kann Sie die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode verwenden, um den Text zu erzeugen.

 

## <a name="custom-rendering-modes"></a>Benutzerdefinierte Rendermodi

Eine Reihe von Parametern wirkt sich auf das Text Rendering aus, z. b. Gamma, ClearType-Ebene, Pixelgeometrie und erweiterter Kontrast. Renderingparameter werden von einem Objekt gekapselt, das die öffentliche [**idschreiterenderingparameterschnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) implementiert. Das renderparametern-Objekt wird automatisch basierend auf Hardware Eigenschaften und/oder Benutzereinstellungen initialisiert, die über das System Steuerungs Applet "ClearType" in Windows 7 angegeben werden. Wenn ein Client die [DirectWrite](direct-write-portal.md) -layoutapi verwendet, wählt DirectWrite im allgemeinen automatisch einen Renderingmodus aus, der dem angegebenen Mess Modus entspricht.

Anwendungen, die mehr Kontrolle wünschen, können " [**idwrite tefactory:: kreatecustomrenderingpara**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) " verwenden, um die verschiedenen Renderingoptionen zu implementieren. Diese Funktion kann auch zum Festlegen von Gamma, Pixelgeometrie und erweiterter Kontrast verwendet werden.

Im folgenden sind die verschiedenen verfügbaren Renderingoptionen aufgeführt:

-   Subpixel-Antialiasing

    Die Anwendung legt den *renderingmode* -Parameter auf "Natural" fest, um das \_ \_ \_ Rendering mit Antialiasing nur in der horizontalen Dimension anzugeben.

-   Subpixel-Antialiasing in horizontalen und vertikalen Dimensionen.

    Die Anwendung legt den *renderingmode* -Parameter auf " \_ Natural Symmetric" im dwrite-Renderingmodus fest \_ \_ \_ , um das RENDERING mit Antialiasing in horizontalen und vertikalen Dimensionen anzugeben. Dadurch werden Kurven und diagonales Linien auf Kosten einer Weichheit und in der Regel in Größen oberhalb von 16 ppem zu einem reibungsloseren Bild angezeigt.

-   Alias Text

    Die Anwendung legt den *renderingmode* -Parameter auf den dwrite- \_ Renderingmodus \_ \_ Aliasing fest, um einen Alias Text anzugeben.

-   Graustufen Text

    Die Anwendung legt den *Pixel Geometry* -Parameter auf dwrite \_ Pixel \_ Geometry \_ Flat fest, um Graustufen Text anzugeben.

-   GDI-kompatibel-Breite (einschließlich ostasiatischen eingebetteten Bitmap)

    Die Anwendung legt den *renderingmode* -Parameter auf den dwrite \_ -Renderingmodus \_ \_ GDI \_ Classic fest, um ein GDI-kompatibles Antialiasing anzugeben.

-   GDI mit natürlicher Breite

    Die Anwendung legt den *renderingmode* -Parameter auf den dwrite- \_ Renderingmodus \_ \_ GDI \_ Natural fest, um ein GDI-kompatibles Antialiasing mit natürlicher Breite anzugeben.

-   Umriss Text

    Zum Rendern in großem Umfang kann es vorkommen, dass ein Anwendungsentwickler das Rendering mithilfe der Schriftart Gliederung anstatt durch rasterierung in eine Bitmap ausstellt. Die Anwendung legt den *renderingmode* -Parameter auf den dwrite-renderingmodusumriss fest, um anzugeben, dass das RENDERING den Raster umgehen und die **\_ \_ \_ Kontur** direkt verwenden soll.

## <a name="gdi-interoperability"></a>GDI-Interoperabilität

Die [**idschreitegdiinterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) -Schnittstelle bietet Interoperabilität mit GDI. Dadurch können Anwendungen Ihre vorhandenen Investitionen in GDI-Codebasen fortsetzen und [DirectWrite](direct-write-portal.md) selektiv zum Rendern oder Layout verwenden.

Im folgenden finden Sie die APIs, mit denen eine Anwendung zum bzw. aus dem GDI-Schriftart System migriert werden kann:

-   [**"Kreatefontfromlogfont"**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    Erstellt ein [**idwrite-Font**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) -Objekt, das mit den von der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur angegebenen Eigenschaften übereinstimmt.

-   [**Convertfonttologfont**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    Initialisiert eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur auf Grundlage der GDI-kompatiblen Eigenschaften der angegebenen [**idwrite-Schriftart**](/windows/win32/api/dwrite/nn-dwrite-idwritefont).

-   [**Convertfontfaketologfont**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    Initialisiert eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur auf Grundlage der GDI-kompatiblen Eigenschaften des angegebenen [**idwrite-fontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface).

-   [**"Kreatefontfakefromhdc"**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    Erstellt ein [**idwrite-fontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) -Objekt, das dem aktuell ausgewählten **hFont** entspricht.

## <a name="conclusion"></a>Zusammenfassung

Das verbessern der Lesevorgänge ist für Benutzer ein großartiger Wert, egal ob es sich um einen Bildschirm oder ein Papier handelt. [DirectWrite](direct-write-portal.md) bietet die einfache Verwendung und das geschichtete Programmiermodell für Anwendungsentwickler, um die Textdarstellung für Ihre Windows-Anwendungen zu verbessern. Anwendungen können mithilfe von DirectWrite umfangreicher formatierten Text für Ihre Benutzeroberfläche und Dokumente mit der Layout-API Rendering. Für komplexere Szenarien kann eine Anwendung direkt mit Symbolen, Zugriffs Schriftarten usw. arbeiten und die Leistungsfähigkeit von DirectWrite nutzen, um qualitativ hochwertige typografiken bereitzustellen.

Mit den Interoperabilitäts Funktionen von [DirectWrite](direct-write-portal.md) können Anwendungsentwickler ihre vorhandenen Win32-Codebasen weiterleiten und DirectWrite selektiv innerhalb Ihrer Anwendungen übernehmen.

 

 