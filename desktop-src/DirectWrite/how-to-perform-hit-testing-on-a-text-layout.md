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
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a><span data-ttu-id="3bd50-103">Ausführen von Treffer Tests für ein Text Layout</span><span class="sxs-lookup"><span data-stu-id="3bd50-103">How to Perform Hit Testing on a Text Layout</span></span>

<span data-ttu-id="3bd50-104">Bietet ein kurzes Tutorial zum Hinzufügen von Treffer Tests zu einer [DirectWrite](direct-write-portal.md) -Anwendung, die Text mithilfe der [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle anzeigt.</span><span class="sxs-lookup"><span data-stu-id="3bd50-104">Provides a short tutorial about how to add hit testing to a [DirectWrite](direct-write-portal.md) application that displays text by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="3bd50-105">Das Ergebnis dieses Tutorials ist eine Anwendung, die das Zeichen, auf das mit der linken Maustaste geklickt wird, unterstreicht, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3bd50-105">The result of this tutorial is an application that underlines the character that is clicked on by the left mouse button, as shown in the following screen shot.</span></span>

![Screenshot von "klicken Sie auf diesen Text"](images/hittest.png)

<span data-ttu-id="3bd50-107">Diese Vorgehensweise enthält die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="3bd50-107">This how to contains the following parts:</span></span>

- [<span data-ttu-id="3bd50-108">Schritt 1: Erstellen eines Text Layouts</span><span class="sxs-lookup"><span data-stu-id="3bd50-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
- [<span data-ttu-id="3bd50-109">Schritt 2: Fügen Sie eine OnClick-Methode hinzu.</span><span class="sxs-lookup"><span data-stu-id="3bd50-109">Step 2: Add an OnClick method.</span></span>](#step-2-add-an-onclick-method)
- [<span data-ttu-id="3bd50-110">Schritt 3: Ausführen von Treffer Tests.</span><span class="sxs-lookup"><span data-stu-id="3bd50-110">Step 3: Perform Hit Testing.</span></span>](#step-3-perform-hit-testing)
- [<span data-ttu-id="3bd50-111">Schritt 4: unterstreichen des angeklickten Texts.</span><span class="sxs-lookup"><span data-stu-id="3bd50-111">Step 4: Underline the Clicked Text.</span></span>](#step-4-underline-the-clicked-text)
- [<span data-ttu-id="3bd50-112">Schritt 5: Behandeln der WM- \_ lbuttondown-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3bd50-112">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>](/windows)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="3bd50-113">Schritt 1: Erstellen eines Text Layouts</span><span class="sxs-lookup"><span data-stu-id="3bd50-113">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="3bd50-114">Zunächst benötigen Sie eine Anwendung, die ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="3bd50-114">To begin, you will need an application that uses an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="3bd50-115">Wenn Sie bereits über eine Anwendung verfügen, in der Text mit einem Text Layout angezeigt wird, fahren Sie mit Schritt 2 fort.</span><span class="sxs-lookup"><span data-stu-id="3bd50-115">If you already have an application that displays text with a text layout, go to Step 2.</span></span>

<span data-ttu-id="3bd50-116">Zum Hinzufügen eines Textlayouts müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="3bd50-116">To add a text layout you must do the following:</span></span>

1. <span data-ttu-id="3bd50-117">Deklarieren Sie einen Zeiger auf eine [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle als Member der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="3bd50-117">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. <span data-ttu-id="3bd50-118">Erstellen Sie am Ende der **createdeviceindependentresources** -Methode ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstellen Objekt, indem Sie die [**createtextlayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3bd50-118">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>

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

3. <span data-ttu-id="3bd50-119">Anschließend müssen Sie den aufzurufenden [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode in [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) ändern, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3bd50-119">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) as shown in the following code.</span></span>

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a><span data-ttu-id="3bd50-120">Schritt 2: Fügen Sie eine OnClick-Methode hinzu.</span><span class="sxs-lookup"><span data-stu-id="3bd50-120">Step 2: Add an OnClick method.</span></span>

<span data-ttu-id="3bd50-121">Fügen Sie nun der-Klasse eine Methode hinzu, die die Treffer Test Funktionalität des Textlayouts verwendet.</span><span class="sxs-lookup"><span data-stu-id="3bd50-121">Now add a method to the class that will use the hit testing functionality of the text layout.</span></span>

1. <span data-ttu-id="3bd50-122">Deklarieren **Sie eine OnClick** -Methode in der Klassen Header Datei.</span><span class="sxs-lookup"><span data-stu-id="3bd50-122">Declare an **OnClick** method in the class header file.</span></span>

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. <span data-ttu-id="3bd50-123">Definieren **Sie eine OnClick** -Methode in der Klassen Implementierungs Datei.</span><span class="sxs-lookup"><span data-stu-id="3bd50-123">Define an **OnClick** method in the class implementation file.</span></span>

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a><span data-ttu-id="3bd50-124">Schritt 3: Ausführen von Treffer Tests.</span><span class="sxs-lookup"><span data-stu-id="3bd50-124">Step 3: Perform Hit Testing.</span></span>

<span data-ttu-id="3bd50-125">Um zu ermitteln, wo der Benutzer auf das Text Layout geklickt hat, verwenden wir die [**idschreitetextlayout:: hitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3bd50-125">To determine where the user has clicked the text layout we will use the [**IDWriteTextLayout::HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

<span data-ttu-id="3bd50-126">Fügen Sie der **OnClick** -Methode Folgendes hinzu, die Sie in Schritt 2 definiert haben.</span><span class="sxs-lookup"><span data-stu-id="3bd50-126">Add the following to the **OnClick** method that you defined in Step 2.</span></span>

1. <span data-ttu-id="3bd50-127">Deklarieren Sie die Variablen, die als Parameter an die Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="3bd50-127">Declare the variables we will pass as parameters to the method.</span></span>

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    <span data-ttu-id="3bd50-128">Die [**hitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) -Methode gibt die folgenden Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="3bd50-128">The [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method outputs the following parameters.</span></span>

    | <span data-ttu-id="3bd50-129">Variable</span><span class="sxs-lookup"><span data-stu-id="3bd50-129">Variable</span></span>         | <span data-ttu-id="3bd50-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3bd50-130">Description</span></span>                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="3bd50-131">*hittestmetrics*</span><span class="sxs-lookup"><span data-stu-id="3bd50-131">*hitTestMetrics*</span></span> | <span data-ttu-id="3bd50-132">Die Geometrie, die den Treffer Test Speicherort vollständig einschließt.</span><span class="sxs-lookup"><span data-stu-id="3bd50-132">The geometry fully enclosing the hit-test location.</span></span>                                                                                     |
    | <span data-ttu-id="3bd50-133">*isInside*</span><span class="sxs-lookup"><span data-stu-id="3bd50-133">*isInside*</span></span>       | <span data-ttu-id="3bd50-134">Gibt an, ob sich die Position des Treffer Tests in der Text Zeichenfolge befindet oder nicht.</span><span class="sxs-lookup"><span data-stu-id="3bd50-134">Indicates whether the hit-test location is inside the text string or not.</span></span> <span data-ttu-id="3bd50-135">Bei "false" wird die Position zurückgegeben, die dem Rand des Texts am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="3bd50-135">When FALSE, the position nearest the text's edge is returned.</span></span> |
    | <span data-ttu-id="3bd50-136">*istrailinghit*</span><span class="sxs-lookup"><span data-stu-id="3bd50-136">*isTrailingHit*</span></span>  | <span data-ttu-id="3bd50-137">Gibt an, ob sich die Position des Treffer Tests auf der führenden oder der nachfolgenden Seite des Zeichens befindet.</span><span class="sxs-lookup"><span data-stu-id="3bd50-137">Indicates whether the hit-test location is at the leading or the trailing side of the character.</span></span>                                        |

2. <span data-ttu-id="3bd50-138">Ruft die [**hitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) -Methode des [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="3bd50-138">Call the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method of the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    <span data-ttu-id="3bd50-139">Der Code in diesem Beispiel übergibt die *x* -und *y* -Variablen für die Position ohne Änderungen.</span><span class="sxs-lookup"><span data-stu-id="3bd50-139">The code in this example passes the *x* and *y* variables for the position without any modification.</span></span> <span data-ttu-id="3bd50-140">Dies kann in diesem Beispiel der Fall sein, da das Text Layout die gleiche Größe wie das Fenster hat und in der oberen linken Ecke des Fensters angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3bd50-140">This can be done in this example because the text layout is the same size as the window and originates in the upper-left corner of the window.</span></span> <span data-ttu-id="3bd50-141">Wenn dies nicht der Fall wäre, müssten Sie die Koordinaten im Verhältnis zum Ursprung des Textlayouts bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3bd50-141">If this was not the case, you would have to determine the coordinates in relation to the origin of the text layout.</span></span>

## <a name="step-4-underline-the-clicked-text"></a><span data-ttu-id="3bd50-142">Schritt 4: unterstreichen des angeklickten Texts.</span><span class="sxs-lookup"><span data-stu-id="3bd50-142">Step 4: Underline the Clicked Text.</span></span>

<span data-ttu-id="3bd50-143">Fügen Sie Folgendes zu dem **OnClick** hinzu, den Sie in Schritt 2 nach dem aufzurufen der [**hitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) -Methode definiert haben.</span><span class="sxs-lookup"><span data-stu-id="3bd50-143">Add the following to the **OnClick** you defined in Step 2, after the call to the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

<span data-ttu-id="3bd50-144">Mit diesem Code wird Folgendes durchführt:</span><span class="sxs-lookup"><span data-stu-id="3bd50-144">This code does the following.</span></span>

1. <span data-ttu-id="3bd50-145">Überprüft, ob sich der Treffer Test Punkt im Text mithilfe der *isInside* -Variablen befand.</span><span class="sxs-lookup"><span data-stu-id="3bd50-145">Checks if the hit-test point was inside the text using the *isInside* variable.</span></span>
2. <span data-ttu-id="3bd50-146">Der **Textposition** -Member der *hittestmetrics* -Struktur enthält den NULL basierten Index des angeklickten Zeichens.</span><span class="sxs-lookup"><span data-stu-id="3bd50-146">The **textPosition** member of the *hitTestMetrics* structure contains the zero-based index of the character clicked.</span></span>

    <span data-ttu-id="3bd50-147">Ruft die Unterstreichung für dieses Zeichen ab, indem dieser Wert an die [**idschreitetextlayout:: getstrichen**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) -Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3bd50-147">Gets the underline for this character by passing this value to the [**IDWriteTextLayout::GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) method.</span></span>

3. <span data-ttu-id="3bd50-148">Deklariert eine [**dwrite- \_ Text \_ Bereichs**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) Variable, bei der die Startposition auf " **hittestmetrics. Textposition** " und eine Länge von 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3bd50-148">Declares a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable with the start position set to **hitTestMetrics.textPosition** and a length of 1.</span></span>
4. <span data-ttu-id="3bd50-149">Schaltet die Unterstreichung mithilfe der [**idwrite-Textlayout:: setstreicht**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) -Methode um.</span><span class="sxs-lookup"><span data-stu-id="3bd50-149">Toggles the underline by using the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>

<span data-ttu-id="3bd50-150">Nachdem Sie die Unterstreichung festgelegt haben, zeichnen Sie den Text neu, indem Sie die **DrawD2DContent** -Methode der Klasse aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3bd50-150">After setting the underline, redraw the text by calling the **DrawD2DContent** method of the class.</span></span>

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a><span data-ttu-id="3bd50-151">Schritt 5: Behandeln der WM- \_ lbuttondown-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3bd50-151">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>

<span data-ttu-id="3bd50-152">Fügen Sie schließlich dem Meldungs Handler für Ihre Anwendung die **WM- \_ lbuttondown** -Nachricht hinzu, und nennen Sie die **OnClick** -Methode der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="3bd50-152">Finally, add the **WM\_LBUTTONDOWN** message to the message handler for your application and call the **OnClick** method of the class.</span></span>

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

<span data-ttu-id="3bd50-153">**Get \_ X \_ LPARAM** -und **get \_ X \_ LPARAM** -Makros werden in der Header Datei "WINDOWSX. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="3bd50-153">**GET\_X\_LPARAM** and **GET\_X\_LPARAM** macros are declared in the windowsx.h header file.</span></span> <span data-ttu-id="3bd50-154">Sie können die x-und y-Position des Mausklicks problemlos abrufen.</span><span class="sxs-lookup"><span data-stu-id="3bd50-154">They easily retrieve the x and y position of the mouse click.</span></span>
