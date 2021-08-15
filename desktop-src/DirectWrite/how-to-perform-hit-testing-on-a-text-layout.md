---
title: Ausführen von Treffertests für ein Textlayout
description: Enthält ein kurzes Tutorial zum Hinzufügen von Treffertests zu einer DirectWrite Anwendung, die Text mithilfe der IDWriteTextLayout-Schnittstelle anzeigt.
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d42967b069a7a5008de75c1cecb453a6158857eb2b05d2dd0298584a67cef69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816569"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a>Ausführen von Treffertests für ein Textlayout

Enthält ein kurzes Tutorial zum Hinzufügen [](direct-write-portal.md) von Treffertests zu einer DirectWrite Anwendung, die Text mithilfe der [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) anzeigt.

Das Ergebnis dieses Tutorials ist eine Anwendung, die das Zeichen unterstreicht, auf das mit der linken Maustaste geklickt wird, wie im folgenden Screenshot gezeigt.

![Screenshot von "Auf diesen Text klicken"](images/hittest.png)

Dies enthält die folgenden Teile:

- [Schritt 1: Erstellen eines Textlayouts.](#step-1-create-a-text-layout)
- [Schritt 2: Hinzufügen einer OnClick-Methode.](#step-2-add-an-onclick-method)
- [Schritt 3: Ausführen von Treffertests.](#step-3-perform-hit-testing)
- [Schritt 4: Unterstrichen Sie den angeklickten Text.](#step-4-underline-the-clicked-text)
- [Schritt 5: Behandeln der \_ WM-LBUTTONDOWN-Nachricht.](/windows)

## <a name="step-1-create-a-text-layout"></a>Schritt 1: Erstellen eines Textlayouts.

Zunächst benötigen Sie eine Anwendung, die ein [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) verwendet. Wenn Sie bereits über eine Anwendung verfügen, die Text mit einem Textlayout anzeigt, fahren Sie mit Schritt 2 fort.

Gehen Sie wie folgt vor, um ein Textlayout hinzuzufügen:

1. Deklarieren Sie einen Zeiger auf eine [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) als Member der -Klasse.

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. Erstellen Sie am Ende der **CreateDeviceIndependentResources-Methode** ein [**IDWriteTextLayout-Schnittstellenobjekt,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) indem Sie die [**CreateTextLayout-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) aufrufen.

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

3. Anschließend müssen Sie den Aufruf der [**ID2D1RenderTarget::D rawText-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) in [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) ändern, wie im folgenden Code gezeigt.

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a>Schritt 2: Hinzufügen einer OnClick-Methode.

Fügen Sie nun der -Klasse eine -Methode hinzu, die die Treffertestfunktion des Textlayouts verwendet.

1. Deklarieren **Sie eine OnClick-Methode** in der Klassenheaderdatei.

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. Definieren Sie eine **OnClick-Methode** in der Klassenimplementierungsdatei.

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a>Schritt 3: Ausführen von Treffertests.

Um zu bestimmen, wo der Benutzer auf das Textlayout geklickt hat, verwenden wir die [**IDWriteTextLayout::HitTestPoint-Methode.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)

Fügen Sie der **OnClick-Methode,** die Sie in Schritt 2 definiert haben, Folgendes hinzu.

1. Deklarieren Sie die Variablen, die wir als Parameter an die -Methode übergeben.

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    Die [**HitTestPoint-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) gibt die folgenden Parameter aus.

    | Variable         | BESCHREIBUNG                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | *hitTestMetrics* | Die Geometrie, die die Treffertestposition vollständig umschließt.                                                                                     |
    | *isInside*       | Gibt an, ob sich die Treffertestposition innerhalb der Textzeichenfolge befindet oder nicht. Bei FALSE wird die Position zurückgegeben, die dem Rand des Texts am nächsten liegt. |
    | *isTrailingHit*  | Gibt an, ob sich die Treffertestposition an der führenden oder der nachseitigen Seite des Zeichens befindet.                                        |

2. Rufen Sie die [**HitTestPoint-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) des [**IDWriteTextLayout-Objekts**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) auf.

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    Der Code in diesem Beispiel übergibt die *x-* und *y-Variablen* für die Position ohne Änderungen. Dies kann in diesem Beispiel erfolgen, da das Textlayout die gleiche Größe wie das Fenster hat und aus der linken oberen Ecke des Fensters stammt. Wenn dies nicht der Fall wäre, müssten Sie die Koordinaten in Bezug auf den Ursprung des Textlayouts bestimmen.

## <a name="step-4-underline-the-clicked-text"></a>Schritt 4: Unterstrichen Sie den angeklickten Text.

Fügen Sie dem **OnClick-Befehl,** den Sie in Schritt 2 definiert haben, nach dem Aufruf der [**HitTestPoint-Methode Folgendes**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) hinzu.

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

Dieser Code führt Folgendes aus.

1. Überprüft mithilfe der *IsInside-Variablen,* ob sich der Treffertestpunkt im Text befindet.
2. Das **textPosition-Member** der *hitTestMetrics-Struktur* enthält den nullbasierten Index des angeklickten Zeichens.

    Ruft den Unterstrich für dieses Zeichen ab, indem dieser Wert an die [**IDWriteTextLayout::GetUnderline-Methode übergeben**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) wird.

3. Deklariert eine [**DWRITE \_ TEXT \_ RANGE-Variable,**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) bei der die Startposition auf **hitTestMetrics.textPosition** und eine Länge von 1 festgelegt ist.
4. Umschaltet die Unterstreichung mithilfe der [**IDWriteTextLayout::SetUnderline-Methode.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline)

Zeichnen Sie nach dem Festlegen der Unterstreichung den Text neu, indem Sie die **DrawD2DContent-Methode** der -Klasse aufrufen.

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a>Schritt 5: Behandeln der \_ WM-LBUTTONDOWN-Nachricht.

Fügen Sie abschließend die **\_ WM-LBUTTONDOWN-Nachricht** dem Meldungshandler für Ihre Anwendung hinzu, und rufen Sie die **OnClick-Methode** der -Klasse auf.

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

**GET \_ X \_ LPARAM-** und **GET \_ \_ X-LPARAM-Makros** werden in der Headerdatei windowsx.h deklariert. Sie können die x- und y-Position des Mausklicks leicht abrufen.
