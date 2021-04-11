---
title: Verwenden visueller Stile mit benutzerdefinierten Steuerelementen und Owner-Drawn Steuerelementen
description: In diesem Thema wird beschrieben, wie die API für visuelle Stile verwendet wird, um visuelle Stile auf benutzerdefinierte Steuerelemente oder vom Besitzer gezeichnete Steuerelemente anzuwenden.
ms.assetid: 8b06f9ce-702c-48f8-8cf3-2718a09b8d77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7025bdf7c589649ac62bed7a4ea4f55c418940
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102435"
---
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a>Verwenden visueller Stile mit benutzerdefinierten Steuerelementen und Owner-Drawn Steuerelementen

In diesem Thema wird beschrieben, wie die API für visuelle Stile verwendet wird, um visuelle Stile auf benutzerdefinierte Steuerelemente oder vom Besitzer gezeichnete Steuerelemente anzuwenden.

-   [Zeichnen von Steuerelementen mit visuellen Stilen](#drawing-controls-with-visual-styles)
-   [Reagieren auf Designänderungen](#responding-to-theme-changes)
-   [Zugehörige Themen](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a>Zeichnen von Steuerelementen mit visuellen Stilen

Visuelle Stile werden von ComCtrl32.dll Version 6 und höher unterstützt. Wenn Ihre Anwendung für die Verwendung von ComCtrl32.dll Version 6 und höher konfiguriert ist und diese Version auf dem System verfügbar ist, werden die aktuellen visuellen Stile automatisch auf alle allgemeinen Steuerelemente in Ihrer Anwendung angewendet. Die aktuellen visuellen Stile werden jedoch nicht automatisch auf benutzerdefinierte Steuerelemente oder Steuerelemente angewendet, die vom Besitzer gezeichnet werden. Die Anwendung muss Code einschließen, mit dem überprüft wird, ob visuelle Stile verfügbar sind. wenn dies der Fall ist, wird die API für visuelle Stile verwendet, um die aktuell ausgewählten visuellen Stile auf die benutzerdefinierten und vom Besitzer gezeichneten Steuerelemente anzuwenden.

Um zu überprüfen, ob visuelle Stile verfügbar sind, rufen Sie die [**isapptheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) -Funktion auf. Wenn visuelle Stile nicht verfügbar sind, verwenden Sie den Fall Back Code, um das Steuerelement zu zeichnen.

Wenn visuelle Stile verfügbar sind, können Sie Funktionen mit visuellen Stilen wie [**drawdermetext**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) zum Rendering des Steuer Elements verwenden. Beachten Sie, dass mit [**drawdermetextex**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) die Darstellung von Text angepasst werden kann, wobei einige Eigenschaften der Design Schriftart beibehalten werden, während andere geändert werden.

**So zeichnen Sie ein Steuerelement im aktuellen visuellen Stil**

1.  Nennen Sie [**openfomedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), und übergeben Sie das *HWND* des Steuer Elements, auf das Sie visuelle Stile anwenden möchten, und eine Klassenliste, die den Typ des Steuer Elements beschreibt. Die Klassen werden in Vssym32. h definiert. **Opendermedata** gibt ein HTHEME-Handle zurück, aber wenn der Visual Styles-Manager deaktiviert ist oder der aktuelle visuelle Stil keine spezifischen Informationen für ein bestimmtes Steuerelement bereitstellt, gibt die Funktion **null** zurück. Wenn der Rückgabewert **null** ist, verwenden Sie nicht visuelle Stile für Zeichnungsfunktionen.
2.  Um den Hintergrund des Steuer Elements zu zeichnen, müssen Sie [**drawtemebackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) oder [**drawtemebackgroundex**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex)aufrufen.
3.  Um den Speicherort des Inhalts Rechtecks zu ermitteln, müssen Sie [**gettemebackgroundcontentrect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect)aufrufen.
4.  Verwenden Sie zum Rendering von Text entweder [**drawtemetext**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) oder [**drawtemetextex**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), und verwenden Sie dabei die Koordinaten des Rechtecks, das von [**gettemebackgroundcontentrect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect)zurückgegeben wurde. Diese Funktionen können den Text entweder in der Schriftart des Designs für einen angegebenen Steuerelement Teil und-Zustand oder in der derzeit im Gerätekontext (DC) ausgewählten Schriftart darstellen.
5.  Wenn das Steuerelement eine [**WM- \_ zerstörungsnachricht**](/windows/desktop/winmsg/wm-destroy) empfängt, können Sie [**closefomedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) aufrufen, um das Design Handle freizugeben, das beim Aufrufen von [**openfomedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata)zurückgegeben wurde.

Der folgende Beispielcode zeigt eine Möglichkeit, ein Schaltflächen-Steuerelement im aktuellen visuellen Stil zu zeichnen.


```C++
HTHEME hTheme = NULL;

hTheme = OpenThemeData(hwndButton, L"Button");
// ...
DrawMyControl(hDC, hwndButton, hTheme, iState);
// ...
if (hTheme)
{
    CloseThemeData(hTheme);
}


void DrawMyControl(HDC hDC, HWND hwndButton, HTHEME hTheme, int iState)
{
    RECT rc, rcContent;
    TCHAR szButtonText[255];
    HRESULT hr;
    size_t cch;

    GetWindowRect(hwndButton, &rc);
    GetWindowText(hwndButton, szButtonText,
                  (sizeof(szButtonText) / sizeof(szButtonText[0])+1));
    hr = StringCchLength(szButtonText,
         (sizeof(szButtonText) / sizeof(szButtonText[0])), &cch);
    if (hTheme)
    {
        hr = DrawThemeBackground(hTheme, hDC, BP_PUSHBUTTON, iState, &rc, 0);
        if (SUCCEEDED(hr))
        {
            hr = GetThemeBackgroundContentRect(hTheme, hDC, BP_PUSHBUTTON, 
                    iState, &rc, &rcContent);
        }

        if (SUCCEEDED(hr))
        {
            hr = DrawThemeText(hTheme, hDC, BP_PUSHBUTTON, iState, 
                    szButtonText, cch,
                    DT_CENTER | DT_VCENTER | DT_SINGLELINE,
                    0, &rcContent);
        }

    }
    else
    {
        // Draw the control without using visual styles.
    }
}
```





Der folgende Beispielcode befindet sich im [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldungs Handler für ein untergeordnetes Schaltflächen-Steuerelement. Der Text für das Steuerelement wird in der Schriftart der visuellen Stile gezeichnet, aber die Farbe ist abhängig vom Zustand des Steuer Elements Anwendungs definiert.


```C++
// textColor is a COLORREF whose value has been set according to whether the button is "hot".
// paint is the PAINTSTRUCT whose members are filled in by BeginPaint.
HTHEME theme = OpenThemeData(hWnd, L"button");
if (theme)
{
    DTTOPTS opts = { 0 };
    opts.dwSize = sizeof(opts);
    opts.crText = textColor;
    opts.dwFlags |= DTT_TEXTCOLOR;
    WCHAR caption[255];
    size_t cch;
    GetWindowText(hWnd, caption, 255);
    StringCchLength(caption, 255, &cch);
    DrawThemeTextEx(theme, paint.hdc, BP_PUSHBUTTON, CBS_UNCHECKEDNORMAL, 
        caption, cch, DT_CENTER | DT_VCENTER | DT_SINGLELINE, 
        &paint.rcPaint, &opts);
    CloseThemeData(theme);
}
else
{
    // Draw the control without using visual styles.
}
```



Sie können Teile aus anderen Steuerelementen verwenden und die einzelnen Teile separat darstellen. Beispielsweise können Sie für ein Kalender Steuerelement, das aus einem Raster besteht, jedes quadratische, das durch das Raster gebildet wird, als Symbolleisten-Schaltfläche behandeln, indem Sie das Design handle wie folgt abrufen:


```C++
OpenThemeData(hwnd, L"Toolbar");
```



Sie können Steuerelemente mischen und abgleichen, indem Sie [**opentemedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) mehrmals für ein bestimmtes Steuerelement aufrufen und den entsprechenden Design Handle verwenden, um verschiedene Teile zu zeichnen. In einigen visuellen Stilen sind bestimmte Teile jedoch möglicherweise nicht mit anderen Teilen kompatibel.

Ein weiterer Ansatz zum Rendern von Steuerelementen im aktiven visuellen Stil besteht darin, die Systemfarben zu verwenden. Sie können z. b. Systemfarben verwenden, um die Textfarbe beim Aufrufen der [**drawtemetextex**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) -Funktion festzulegen. Die meisten Systemfarben werden festgelegt, wenn eine visuelle Stil Datei angewendet wird.

## <a name="responding-to-theme-changes"></a>Reagieren auf Designänderungen

Wenn das Steuerelement eine [**WM \_**](/windows/desktop/winmsg/wm-themechanged) -Nachricht empfängt und ein globales Handle für das Design enthält, sollte es wie folgt vorgehen:

-   Ruft [**closedermedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) auf, um das vorhandene Design Handle zu schließen.
-   [**Öffnen Sie opentemedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) , um das Design Handle für den neu geladenen visuellen Stil abzurufen.

Im folgenden Beispiel werden die beiden-Aufrufe veranschaulicht.


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von visuellen Stilen](cookbook-overview.md)
</dt> <dt>

[Visuelle Stile](themes-overview.md)
</dt> </dl>

 

 