---
title: Tutorial für den Einstieg in DirectWrite
description: In diesem Dokument erfahren Sie, wie Sie mithilfe von DirectWrite und Direct2D einfachen Text erstellen, der ein einzelnes Format enthält, und dann Text mit mehreren Formaten.
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite, Tutorial
- Tutorial zu den ersten Schritten mit DirectWrite
- DirectWrite, Direct2D
- Direct2D
- DirectWrite, idschreitetextlayout-Schnittstelle
- Idschreitetextlayout-Schnittstelle
- DirectWrite, idschreitetypografie-Schnittstelle
- Idschreitetypografieschnittstelle
- DirectWrite, idschreitetextformat-Schnittstelle
- Idschreitetextformat-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb385ff78650a16599a32d76d7c51ba575de47
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315861"
---
# <a name="tutorial-getting-started-with-directwrite"></a>Tutorial: Einstieg in DirectWrite

In diesem Dokument erfahren Sie, wie Sie mithilfe von [DirectWrite](direct-write-portal.md) und [Direct2D](rendering-by-using-direct2d.md) einfachen Text erstellen, der ein einzelnes Format enthält, und dann Text mit mehreren Formaten.

Dieses Tutorial enthält die folgenden Teile:

-   [Quellcode](#source-code)
-   [Zeichnen von einfachem Text](#drawing-simple-text)
    -   [Teil 1: Deklarieren von DirectWrite-und Direct2D-Ressourcen.](#part-1-declare-directwrite-and-direct2d-resources)
    -   [Teil 2: Erstellen von geräteunabhängigen Ressourcen.](#part-2-create-device-independent-resources)
    -   [Teil 3: Erstellen von Device-Dependent Ressourcen.](#part-3-create-device-dependent-resources)
    -   [Teil 4: Zeichnen von Text mithilfe der Direct2D DrawText-Methode.](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [Teil 5: Rendering der Fenster Inhalte mithilfe von Direct2D](#part-5-render-the-window-contents-using-direct2d)
-   [Zeichnen von Text mit mehreren Formaten.](#drawing-text-with-multiple-formats)
    -   [Teil 1: Erstellen einer idschreitetextlayout-Schnittstelle.](#part-1-create-an-idwritetextlayout-interface)
    -   [Teil 2: Anwenden der Formatierung mit idbeschreib tetextlayout.](#part-2-applying-formatting-with-idwritetextlayout)
    -   [Teil 3: Hinzufügen von typografischen Features mit idbeschreib tetypografie.](#part-3-adding-typographic-features-with-idwritetypography)
    -   [Teil 4: Zeichnen von Text mithilfe der Direct2D drawtextlayout-Methode.](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a>Quellcode

Der in dieser Übersicht angezeigte Quellcode stammt aus dem [DirectWrite-Hallo Welt Beispiel](/samples/browse/?redirectedfrom=MSDN-samples). Jeder Teil ist in einer separaten Klasse (SimpleText und multiformattedtext) implementiert und wird in einem separaten untergeordneten Fenster angezeigt. Jede Klasse stellt ein Microsoft Win32-Fenster dar. Neben der *WndProc* -Methode enthält jede Klasse die folgenden Methoden:



| Funktion                              | BESCHREIBUNG                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| **CreateDeviceIndependentResources**  | Erstellt Ressourcen, die Geräte unabhängig sind, sodass Sie überall wieder verwendet werden können.                      |
| **Verwerfen von "Verwerfen von Ressourcen"** | Gibt die geräteunabhängigen Ressourcen frei, wenn Sie nicht mehr benötigt werden.                          |
| **CreateDeviceResources**             | Erstellt Ressourcen, z. b. Pinsel und Renderziele, die an ein bestimmtes Gerät gebunden sind.        |
| **Verwerfen von Datenquellen**            | Gibt die geräteabhängigen Ressourcen frei, wenn Sie nicht mehr benötigt werden.                            |
| **DrawD2DContent**                    | Verwendet [Direct2D](../direct2d/direct2d-portal.md) zum Rendering auf dem Bildschirm.                              |
| **DrawText**                          | Zeichnet die Text Zeichenfolge mithilfe von [Direct2D](../direct2d/direct2d-portal.md).                            |
| **OnResize**                          | Ändert die Größe des [Direct2D](../direct2d/direct2d-portal.md) -Renderziels, wenn die Fenstergröße geändert wird. |



 

Sie können das bereitgestellte Beispiel verwenden oder die folgenden Anweisungen befolgen, um [DirectWrite](direct-write-portal.md) und [Direct2D](rendering-by-using-direct2d.md) ihrer eigenen Win32-Anwendung hinzuzufügen. Weitere Informationen zum Beispiel und den zugehörigen Projektdateien finden Sie im [DirectWrite-HelloWorld-Beispiel](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="drawing-simple-text"></a>Zeichnen von einfachem Text

In diesem Abschnitt wird gezeigt, wie Sie mithilfe von [DirectWrite](direct-write-portal.md) und [Direct2D](../direct2d/direct2d-portal.md) einfachen Text mit einem einzelnen Format renderz, wie im folgenden Screenshot gezeigt.

![Screenshot von "Hello World using DirectWrite!" in einem einzelnen Format](images/simplecropped.png)

Zum Zeichnen von einfachem Text auf dem Bildschirm sind vier Komponenten erforderlich:

-   Eine Zeichenfolge, die dargestellt werden soll.
-   Eine Instanz von [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).
-   Die Abmessungen des Bereichs, in dem der Text enthalten sein soll.
-   Ein Objekt, das den Text erzeugen kann. In diesem Tutorial. Sie verwenden ein [Direct2D](../direct2d/direct2d-portal.md) -Renderziel.

Die [**idwrite Test Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle beschreibt den Schriftfamilien Namen, die Größe, die Gewichtung, den Stil und die Streckung, die zum Formatieren von Text verwendet werden, und beschreibt Gebiets Schema Informationen. **Idbeschreib tetextformat** definiert auch Methoden zum Festlegen und erhalten der folgenden Eigenschaften:

-   Der Zeilenabstand.
-   Die Textausrichtung relativ zum linken und rechten Rand des layoutfelds.
-   Die Absatz Ausrichtung relativ zum oberen und unteren Rand des layoutfelds.
-   Die Leserichtung.
-   Der Text, der die Granularität für Text beschneidet, der das layoutfeld überschreitet.
-   Der inkrementelle Tabstopp.
-   Die Absatz Fluss Richtung.

Die [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle ist zum Zeichnen von Text erforderlich, der beide in diesem Dokument beschriebenen Prozesse verwendet.

Bevor Sie ein [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt oder ein anderes [DirectWrite](direct-write-portal.md) -Objekt erstellen können, benötigen Sie eine [**idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Instanz. Sie verwenden eine **idwrite-Factory** , um **idschreitetextformat** -Instanzen und andere DirectWrite-Objekte zu erstellen. Verwenden Sie zum Abrufen einer Factory-Instanz die [**dschreitekreatefactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) -Funktion.

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a>Teil 1: Deklarieren von DirectWrite-und Direct2D-Ressourcen.

In diesem Teil deklarieren Sie die Objekte, die Sie später zum Erstellen und Anzeigen von Text als private Datenmember ihrer Klasse verwenden werden. Alle Schnittstellen, Funktionen und Datentypen für [DirectWrite](direct-write-portal.md) werden in der *dwrite. h* -Header Datei deklariert, und die für [Direct2D](../direct2d/direct2d-portal.md) sind in *d2d1. h deklariert.* Wenn Sie dies noch nicht getan haben, schließen Sie diese Header in Ihr Projekt ein.

1.  Deklarieren Sie in der Klassen Header Datei (SimpleText. h) Zeiger auf die Schnittstellen [**idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) und [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) als private Member.
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  Deklarieren Sie Member, um die zu Rendering Ende Text Zeichenfolge und die Länge der Zeichenfolge zu speichern.
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  Deklarieren Sie Zeiger auf [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)-, [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)-und [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Schnittstellen zum Rendern des Texts mit [Direct2D](../direct2d/direct2d-portal.md).
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a>Teil 2: Erstellen von geräteunabhängigen Ressourcen.

[Direct2D](rendering-by-using-direct2d.md) bietet zwei Arten von Ressourcen: Geräte abhängige Ressourcen und geräteunabhängige Ressourcen. Geräte abhängige Ressourcen sind einem renderinggerät zugeordnet und funktionieren nicht mehr, wenn das Gerät entfernt wird. Geräteunabhängige Ressourcen können auf der anderen Seite den Geltungsbereich ihrer Anwendung überdauern.

[DirectWrite](direct-write-portal.md) -Ressourcen sind Geräte unabhängig.

In diesem Abschnitt erstellen Sie die geräteunabhängigen Ressourcen, die von Ihrer Anwendung verwendet werden. Diese Ressourcen müssen durch einen Aufrufder **releasemethode** der-Schnittstelle freigegeben werden.

Einige der verwendeten Ressourcen müssen nur einmal erstellt werden und sind nicht an ein Gerät gebunden. Die Initialisierung für diese Ressourcen wird in der *SimpleText:: createdeviceindependentresources* -Methode abgelegt, die beim Initialisieren der-Klasse aufgerufen wird.

1.  Rufen Sie innerhalb der *SimpleText:: createdeviceindependentresources* -Methode in der Klassen Implementierungs Datei (SimpleText. cpp) die [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) -Funktion auf, um eine [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Schnittstelle zu erstellen, die die Stamm-factoryschnittstelle für alle [Direct2D](../direct2d/direct2d-portal.md) -Objekte ist. Sie verwenden dieselbe Factory, um andere Direct2D-Ressourcen zu instanziieren.
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  Rufen Sie die [**dbeschreib tekreatefactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) -Funktion auf, um eine [**idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Schnittstelle zu erstellen, die die stammfactoringschnittstelle für alle [DirectWrite](direct-write-portal.md) -Objekte ist. Sie verwenden dieselbe Factory, um andere DirectWrite-Ressourcen zu instanziieren.
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  Initialisieren Sie die Text Zeichenfolge, und speichern Sie Ihre Länge.

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  Erstellen Sie ein [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstellen Objekt, indem Sie die [**idschreitefactory::**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) -Methode zum Erstellen von Textformaten verwenden. Das **idwrite-Textformat** gibt die Schriftart, die Gewichtung, die Streckung, den Stil und das Gebiets Schema an, die zum renderingtext der Zeichenfolge verwendet werden.
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  Zentrieren Sie den Text horizontal und vertikal, indem Sie die Methoden [**idschreitetextformat:: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) und [**idschreitetextformat:: setparagraphalignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) aufrufen.
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

In diesem Teil haben Sie die geräteunabhängigen Ressourcen initialisiert, die von Ihrer Anwendung verwendet werden. Im nächsten Teil initialisieren Sie die geräteabhängigen Ressourcen.

### <a name="part-3-create-device-dependent-resources"></a>Teil 3: Erstellen von Device-Dependent Ressourcen.

In diesem Teil erstellen Sie eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -und eine [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Datei zum Rendern des Texts.

Ein Renderziel ist ein Direct2D-Objekt, das Zeichnungs Ressourcen erstellt und Zeichnungs Befehle auf einem renderinggerät rendert. Ein [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) ist ein Renderziel, das in ein **HWND** gerendert wird.

Eine der Zeichnungs Ressourcen, die von einem Renderziel erstellt werden kann, ist ein Pinsel zum Zeichnen von umrissen, Füllungen und Text. Ein [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) zeichnet mit einer voll Tonfarbe.

Die [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Schnittstelle und die [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Schnittstelle sind an ein renderinggerät gebunden, wenn Sie erstellt werden, und müssen freigegeben und neu erstellt werden, wenn das Gerät ungültig wird.

1.  Überprüfen Sie in der SimpleText:: deatedeviceresources-Methode, ob der renderzielzeiger **null** ist. Wenn dies der Fall ist, rufen Sie die Größe des Rendering-Bereichs ab, und erstellen Sie eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) dieser Größe. Verwenden Sie **ID2D1HwndRenderTarget** , um eine [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)zu erstellen.
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  Geben Sie in der SimpleText::D iscarddeviceresources-Methode sowohl den Pinsel als auch das Renderziel frei.
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

Nachdem Sie nun ein Renderziel und einen Pinsel erstellt haben, können Sie diese verwenden, um den Text zu renderzielen.

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a>Teil 4: Zeichnen von Text mithilfe der Direct2D DrawText-Methode.

1.  Definieren Sie in der SimpleText::D rawtext-Methode der Klasse den Bereich für das Text Layout, indem Sie die Dimensionen des Renderingbereichs abrufen, und erstellen Sie ein [Direct2D](../direct2d/direct2d-portal.md) -Rechteck, das die gleichen Dimensionen aufweist.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Verwenden Sie die [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode und das [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt, um Text auf dem Bildschirm zu Rendering. Die **ID2D1RenderTarget::D rawtext** -Methode übernimmt die folgenden Parameter:
    -   Eine zu Rendering-Zeichenfolge.
    -   Ein Zeiger auf eine [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle.
    -   Ein [Direct2D](../direct2d/direct2d-portal.md) -Layoutrechteck.
    -   Ein Zeiger auf eine-Schnittstelle, die [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)verfügbar macht.

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a>Teil 5: Rendering der Fenster Inhalte mithilfe von Direct2D

Gehen Sie folgendermaßen vor, um den Inhalt des Fensters mithilfe von [Direct2D](../direct2d/direct2d-portal.md) zu Rendering, wenn eine Paint-Meldung empfangen wird:

1.  Erstellen Sie die geräteabhängigen Ressourcen, indem Sie die SimpleText:: CreateDeviceResources-Methode aufrufen, die in Teil 3 implementiert ist.
2.  Aufrufen der [**ID2D1HwndRenderTarget:: beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode des Renderziels.
3.  Löschen Sie das Renderziel durch Aufrufen der [**ID2D1HwndRenderTarget:: Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) -Methode.
4.  Nennen Sie die in Teil 4 implementierte Methode SimpleText::D rawtext.
5.  Aufrufen der [**ID2D1HwndRenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode des Renderziels.
6.  Wenn dies erforderlich ist, verwerfen Sie die geräteabhängigen Ressourcen, damit Sie neu erstellt werden können, wenn das Fenster neu gezeichnet wird.


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



Die SimpleText-Klasse wird in SimpleText. h und SimpleText. cpp implementiert.

## <a name="drawing-text-with-multiple-formats"></a>Zeichnen von Text mit mehreren Formaten.

In diesem Abschnitt wird gezeigt, wie Sie mithilfe von [DirectWrite](direct-write-portal.md) und [Direct2D](../direct2d/direct2d-portal.md) Text mit mehreren Formaten Renderen, wie im folgenden Screenshot gezeigt.

![Screenshot von "Hello World using DirectWrite!" mit einigen Teilen in verschiedenen Formaten, Größen und Formaten](images/multiformattedcropped.png)

Der Code für diesen Abschnitt wird als multiformattedtext-Klasse im [dwrite-HelloWorld-Beispiel](/samples/browse/?redirectedfrom=MSDN-samples)implementiert. Es basiert auf den Schritten aus dem vorherigen Abschnitt.

Zum Erstellen von mehr formatiertem Text verwenden Sie die [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle zusätzlich zur [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle, die im vorherigen Abschnitt vorgestellt wurde. Die **idschreitetextlayout** -Schnittstelle beschreibt die Formatierung und das Layout eines Textblocks. Zusätzlich zur Standard Formatierung, die durch ein **idschreitetextformat** -Objekt angegeben wird, kann die Formatierung für bestimmte Textbereiche mithilfe von **idschreitetextlayout** geändert werden. Dazu zählen Schriftfamilien Name, Größe, Gewichtung, Stil, Streckung, durchgestrichen und Unterstreichung.

[**Idwrite tetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) bietet auch Treffer Testmethoden. Die von diesen Methoden zurückgegebenen Treffer Testmetriken sind relativ zum layoutfeld, das angegeben wird, wenn das **idschreitetextlayout** -Schnittstellen Objekt mithilfe der Methode " [**kreatetextlayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) " der [**idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Schnittstelle erstellt wird.

Die [**idwrite-Typografie**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) -Schnittstelle wird verwendet, um optionale [OpenType](../intl/opentype-font-format.md) -Typografiefunktionen zu einem Text Layout hinzuzufügen, z. b. Schwung Schrift und alternative Stil Text Sätze. Typografische Funktionen können einem bestimmten Textbereich in einem Text Layout hinzugefügt werden, indem die [**addfontfeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) -Methode der **idschreitetypografie** -Schnittstelle aufgerufen wird. Diese Methode empfängt eine [**dwrite- \_ Schriftart \_ Funktions**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) Struktur als Parameter, der die Enumerationskonstante des **dwrite- \_ Schriftart \_ Features \_** und einen **UInt32** Execution-Parameter enthält. Eine Liste der registrierten OpenType-Features finden Sie in der [OpenType-layouttagregistrierung](https://www.microsoft.com/typography/otspec/features_ae.htm) auf Microsoft.com. Informationen zu den entsprechenden DirectWrite-Enumerationskonstanten finden Sie unter **dwrite \_ Font \_ Feature \_ Tag**.

### <a name="part-1-create-an-idwritetextlayout-interface"></a>Teil 1: Erstellen einer idschreitetextlayout-Schnittstelle.

1.  Deklarieren Sie einen Zeiger auf eine [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle als Member der multiformattedtext-Klasse.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  Erstellen Sie am Ende der multiformattedtext:: createdeviceindependentresources-Methode ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstellen Objekt, indem Sie die [**createtextlayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) -Methode aufrufen. Die **idwrite-Textlayout** -Schnittstelle stellt zusätzliche Formatierungsfunktionen bereit, z. b. die Möglichkeit, unterschiedliche Formate auf ausgewählte Teile von Text anzuwenden.
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a>Teil 2: Anwenden der Formatierung mit idbeschreib tetextlayout.

Die Formatierung, wie z. b. Schriftart Größe, Gewichtung und Unterstreichung, kann auf Teil Zeichenfolgen des Texts angewendet werden, der mithilfe der [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle angezeigt werden soll.

1.  Legen Sie den Schrift Grad für die Teil Zeichenfolge "di" von "DirectWrite" auf "100" fest, indem Sie einen [**dwrite- \_ Text \_ Bereich**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) deklarieren und die [**idschreitetextlayout:: SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) -Methode aufrufen.
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  Unterstreichen Sie die Teil Zeichenfolge "DirectWrite", indem Sie die [**idwrite-Textlayout:: setstreicht**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) -Methode aufrufen.
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  Legen Sie die Schrift Breite für die Teil Zeichenfolge "DirectWrite" auf "Fett" fest, indem Sie die [**idschreitetextlayout:: SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) -Methode aufrufen.
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a>Teil 3: Hinzufügen von typografischen Features mit idbeschreib tetypografie.

1.  Deklarieren und erstellen Sie ein [**idwrite-Typografie**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) -Schnittstellen Objekt, indem Sie die [**idschreitefactory:: createtypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) -Methode aufrufen.
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  Fügen Sie eine Schriftart Funktion hinzu, indem Sie ein [**dwrite- \_ Schriftart \_ Funktions**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) Objekt deklarieren, das die angegebene stilmenge 7 hat, und die [**idschreitetypo:: addfontfeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) -Methode aufrufen.
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  Legen Sie das Text Layout so fest, dass die Typografie für die gesamte Zeichenfolge verwendet wird, indem Sie eine [**dwrite- \_ Text \_ Bereichs**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) Variable deklarieren und die [**idwrite tetextlayout:: settypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) -Methode aufrufen und den Textbereich übergeben.
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  Legen Sie die neue Breite und Höhe für das textlayoutobjekt in der multiformattedtext:: OnResize-Methode fest.
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a>Teil 4: Zeichnen von Text mithilfe der Direct2D drawtextlayout-Methode.

Ändern Sie den Code in der multiformattedtext::D rawtext-Methode, um [**idschreitetextlayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)zu verwenden, um den Text mit den textlayouteinstellungen zu zeichnen, die vom [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt angegeben werden.

1.  Sie müssen eine [**D2D1 \_ Point \_ 2F**](../direct2d/d2d1-point-2f.md) -Variable und die Variable auf den oberen linken Punkt des Fensters festlegen.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  Zeichnen Sie den Text auf dem Bildschirm, indem Sie die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode des [Direct2D](../direct2d/direct2d-portal.md) -Renderziels aufrufen und den [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Zeiger übergeben.
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

Die multiformattedtext-Klasse wird in multiformattedtext. h und multiformattedtext. cpp implementiert.

 

 