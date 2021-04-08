---
title: Ausführen von Treffer Tests für ein Text Layout
description: Bietet ein kurzes Tutorial zum Hinzufügen von Treffer Tests zu einer DirectWrite-Anwendung, die Text mithilfe der idwrite-Textlayout-Schnittstelle anzeigt.
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca80ac641920c4e63c08f4cbb0fd9e24eb7b2d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103961234"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a>Ausführen von Treffer Tests für ein Text Layout

Bietet ein kurzes Tutorial zum Hinzufügen von Treffer Tests zu einer [DirectWrite](direct-write-portal.md) -Anwendung, die Text mithilfe der [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle anzeigt.

Das Ergebnis dieses Tutorials ist eine Anwendung, die das Zeichen, auf das mit der linken Maustaste geklickt wird, unterstreicht, wie im folgenden Screenshot gezeigt.

![Screenshot von "klicken Sie auf diesen Text"](images/hittest.png)

Diese Vorgehensweise enthält die folgenden Teile:

- [Schritt 1: Erstellen eines Text Layouts](#step-1-create-a-text-layout)
- [Schritt 2: Fügen Sie eine OnClick-Methode hinzu.](#step-2-add-an-onclick-method)
- [Schritt 3: Ausführen von Treffer Tests.](#step-3-perform-hit-testing)
- [Schritt 4: unterstreichen des angeklickten Texts.](#step-4-underline-the-clicked-text)
- [Schritt 5: Behandeln der WM- \_ lbuttondown-Nachricht.](/windows)

## <a name="step-1-create-a-text-layout"></a>Schritt 1: Erstellen eines Text Layouts

Zunächst benötigen Sie eine Anwendung, die ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt verwendet. Wenn Sie bereits über eine Anwendung verfügen, in der Text mit einem Text Layout angezeigt wird, fahren Sie mit Schritt 2 fort.

Zum Hinzufügen eines Textlayouts müssen Sie die folgenden Schritte ausführen:

1. Deklarieren Sie einen Zeiger auf eine [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle als Member der-Klasse.

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. Erstellen Sie am Ende der **createdeviceindependentresources** -Methode ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstellen Objekt, indem Sie die [**createtextlayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) -Methode aufrufen.

    ```cpp
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

3. Anschließend müssen Sie den aufzurufenden [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode in [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) ändern, wie im folgenden Code gezeigt.

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a>Schritt 2: Fügen Sie eine OnClick-Methode hinzu.

Fügen Sie nun der-Klasse eine Methode hinzu, die die Treffer Test Funktionalität des Textlayouts verwendet.

1. Deklarieren **Sie eine OnClick** -Methode in der Klassen Header Datei.

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. Definieren **Sie eine OnClick** -Methode in der Klassen Implementierungs Datei.

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a>Schritt 3: Ausführen von Treffer Tests.

Um zu ermitteln, wo der Benutzer auf das Text Layout geklickt hat, verwenden wir die [**idschreitetextlayout:: hitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) -Methode.

Fügen Sie der **OnClick** -Methode Folgendes hinzu, die Sie in Schritt 2 definiert haben.

1. Deklarieren Sie die Variablen, die als Parameter an die Methode übergeben werden.

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    Die [**hitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) -Methode gibt die folgenden Parameter aus.

    | Variable         | BESCHREIBUNG                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | *hittestmetrics* | Die Geometrie, die den Treffer Test Speicherort vollständig einschließt.                                                                                     |
    | *isInside*       | Gibt an, ob sich die Position des Treffer Tests in der Text Zeichenfolge befindet oder nicht. Bei "false" wird die Position zurückgegeben, die dem Rand des Texts am nächsten liegt. |
    | *istrailinghit*  | Gibt an, ob sich die Position des Treffer Tests auf der führenden oder der nachfolgenden Seite des Zeichens befindet.                                        |

2. Ruft die [**hitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) -Methode des [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts auf.

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    Der Code in diesem Beispiel übergibt die *x* -und *y* -Variablen für die Position ohne Änderungen. Dies kann in diesem Beispiel der Fall sein, da das Text Layout die gleiche Größe wie das Fenster hat und in der oberen linken Ecke des Fensters angezeigt wird. Wenn dies nicht der Fall wäre, müssten Sie die Koordinaten im Verhältnis zum Ursprung des Textlayouts bestimmen.

## <a name="step-4-underline-the-clicked-text"></a>Schritt 4: unterstreichen des angeklickten Texts.

Fügen Sie Folgendes zu dem **OnClick** hinzu, den Sie in Schritt 2 nach dem aufzurufen der [**hitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) -Methode definiert haben.

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

Mit diesem Code wird Folgendes durchführt:

1. Überprüft, ob sich der Treffer Test Punkt im Text mithilfe der *isInside* -Variablen befand.
2. Der **Textposition** -Member der *hittestmetrics* -Struktur enthält den NULL basierten Index des angeklickten Zeichens.

    Ruft die Unterstreichung für dieses Zeichen ab, indem dieser Wert an die [**idschreitetextlayout:: getstrichen**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) -Methode übergeben wird.

3. Deklariert eine [**dwrite- \_ Text \_ Bereichs**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) Variable, bei der die Startposition auf " **hittestmetrics. Textposition** " und eine Länge von 1 festgelegt ist.
4. Schaltet die Unterstreichung mithilfe der [**idwrite-Textlayout:: setstreicht**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) -Methode um.

Nachdem Sie die Unterstreichung festgelegt haben, zeichnen Sie den Text neu, indem Sie die **DrawD2DContent** -Methode der Klasse aufrufen.

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a>Schritt 5: Behandeln der WM- \_ lbuttondown-Nachricht.

Fügen Sie schließlich dem Meldungs Handler für Ihre Anwendung die **WM- \_ lbuttondown** -Nachricht hinzu, und nennen Sie die **OnClick** -Methode der-Klasse.

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

**Get \_ X \_ LPARAM** -und **get \_ X \_ LPARAM** -Makros werden in der Header Datei "WINDOWSX. h" deklariert. Sie können die x-und y-Position des Mausklicks problemlos abrufen.
