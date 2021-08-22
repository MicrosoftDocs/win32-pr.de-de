---
title: Übersicht über DWM-Weichzeichner
description: Einer der DwM-Effekte (Signature Desktopfenster-Manager) ist ein durchscheinender und unscharfer Nicht-Clientbereich. Mit den DWM-APIs können Anwendungen diese Effekte auf den Clientbereich ihrer Fenster der obersten Ebene anwenden.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Desktopfenster-Manager (DWM),Blur-Behind-Effekt
- DWM (Desktopfenster-Manager),Blur-Behind-Effekt
- Blur-Behind-Effekt
- Durchscheinender Effekt
- Transparent Glass-Effekt
- Desktopfenster-Manager (DWM), durchscheinender Effekt
- DWM (Desktopfenster-Manager),durchscheinender Effekt
- Desktopfenster-Manager (DWM), transparenter Glass-Effekt
- DWM (Desktopfenster-Manager), transparenter Glass-Effekt
- Desktopfenster-Manager (DWM), Erweitern des Fensterrahmens in den Clientbereich
- DWM (Desktopfenster-Manager),Erweitern des Fensterrahmens in den Clientbereich
- Erweitern des Fensterrahmens in den Clientbereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7b357719ea3aa5a4853a933350ee2dda417842777354e2bbf1711e1cbeff1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456082"
---
# <a name="dwm-blur-behind-overview"></a>Übersicht über DWM-Weichzeichner

Einer der DwM-Effekte (Signature Desktopfenster-Manager) ist ein durchscheinender und unscharfer Nicht-Clientbereich. Mit den DWM-APIs können Anwendungen diese Effekte auf den Clientbereich ihrer Fenster der obersten Ebene anwenden.

> [!Note]  
> Windows Vista Home Basic Edition unterstützt den Transparent Glass-Effekt nicht. Bereiche, die in der Regel mit dem Transparent Glass-Effekt auf anderen Windows Editionen gerendert werden, werden als nicht transparent gerendert.
> Ab Windows 8 führt das Aufrufen dieser Funktion nicht zu einem Weichzeichnereffekt, da die Art und Weise geändert wird, wie Fenster gerendert werden.


 

In diesem Thema werden die folgenden Client-BlurBehind-Szenarien erläutert, die dwm aktiviert.

-   [Hinzufügen von Weichzeichner zu einem bestimmten Bereich des Clientbereichs](#adding-blur-to-a-specific-region-of-the-client-area)
-   [Erweitern des Fensterrahmens in den Clientbereich](#extending-the-window-frame-into-the-client-area)
-   [Zugehörige Themen](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a>Hinzufügen von Weichzeichner zu einem bestimmten Bereich des Clientbereichs

Eine Anwendung kann den Weichzeichnereffekt hinter dem gesamten Clientbereich des Fensters oder auf eine bestimmte Unterregion anwenden. Dadurch können Anwendungen formatierte Pfad- und Suchleisten hinzufügen, die visuell vom Rest der Anwendung getrennt sind.

Die in diesem Szenario verwendete API ist die [**DwmEnableBlurBehindWindow-Funktion,**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) die die [**DWM-Blur Hinter Konstanten**](dwm-bb-constants.md) und die [**\_ DWM-BLURBEHIND-Struktur**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) verwendet.

Die folgende `EnableBlurBehind` Beispielfunktion, , veranschaulicht, wie der Weichzeichner-Behind-Effekt auf das gesamte Fenster angewendet wird.


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



Beachten Sie, dass **NULL** im *hRgnBlur-Parameter* angegeben ist. Dies weist den DWM an, den Weichzeichner hinter dem gesamten Fenster anzuwenden.

Die folgende Abbildung veranschaulicht den Weichzeichnereffekt, der auf das gesamte Fenster angewendet wird.

![Der auf ein Fenster angewendete Weichzeichner-Behind-Effekt](images/dwm-blurbehindwindow.png)

Um die Weichzeichner hinter einer Unterregion anzuwenden, wenden Sie ein gültiges Regionshandle (HRGN) auf den **hRgnBlur-Member** der [**DWM \_ BLURBEHIND-Struktur**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) an, und fügen Sie dem **dwFlags-Member** das **DWM \_ BB \_ BLURREGION-Flag** hinzu.

Wenn Sie den Weichzeichnereffekt auf einen Unterbereich des Fensters anwenden, wird der Alphakanal des Fensters für den nichtblurrierten Bereich verwendet. Dies kann zu einer unerwarteten Transparenz im nichtblurrierten Bereich eines Fensters führen. Seien Sie daher vorsichtig, wenn Sie einen Weichzeichnereffekt auf eine Unterregion anwenden.

## <a name="extending-the-window-frame-into-the-client-area"></a>Erweitern des Fensterrahmens in den Clientbereich

Eine Anwendung kann die Weichzeichner des Fensterrahmens auf den Clientbereich erweitern. Dies ist nützlich, wenn Sie den Weichzeichnereffekt hinter einem Fenster mit einer angedockten Symbolleiste anwenden oder Steuerelemente visuell vom Rest einer Anwendung trennen. Diese Funktionalität wird von der [**DwmExtendFrameIntoClientArea-Funktion**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) verfügbar gemacht.

Verwenden Sie zum Aktivieren von Weichzeichnern mithilfe von [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea)die [**MARGINS-Struktur,**](/windows/win32/api/uxtheme/ns-uxtheme-margins) um anzugeben, wie viel in den Clientbereich erweitert werden soll. Die folgende Beispielfunktion `ExtendIntoClientBottom` schaltet die Weichzeichnererweiterung am unteren Rand des Nicht-Clientframes in den Clientbereich um.


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



Die folgende Abbildung veranschaulicht den Weichzeichner-Hinter-Effekt, der auf den unteren Rand des Clientbereichs erweitert wurde.

![Abbildung, die den Weichzeichner-Hinter-Effekt zeigt, der in den unteren Bereich eines Clientbereichs erweitert wurde](images/dwm-extendedbottom.png)

Auch über die [**DwmExtendFrameIntoClientArea-Methode**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) ist der Effekt "Sheet of Glass" verfügbar, bei dem der Weichzeichnereffekt auf die gesamte Oberfläche des Fensters ohne sichtbaren Fensterrahmen angewendet wird. Im folgenden Beispiel wird dieser Effekt veranschaulicht, bei dem der Clientbereich ohne Fensterrahmen gerendert wird.


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



Die folgende Abbildung veranschaulicht das Weichzeichnen im Fensterstil "Brille".

![Abbildung zur Veranschaulichung des Weichzeichnereffekts im Fensterstil "Brille"](images/dwm-sheetofglass.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Desktop Window Manager](dwm-overview.md)
</dt> <dt>

[Enable and Control DWM Composition (Aktivieren und Steuern der DWM-Komposition)](composition-ovw.md)
</dt> <dt>

[Überlegungen zur Leistung und bewährte Methoden](bestpractices-ovw.md)
</dt> </dl>

 

 