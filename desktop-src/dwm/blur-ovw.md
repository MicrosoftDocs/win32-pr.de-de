---
title: DWM-weich hinter Übersicht
description: Eine der DWM-Effekte (Signature Desktopfenster-Manager) ist ein durchlässiges und verschwommene nicht-Client-Bereich. Mithilfe der DWM-APIs können Anwendungen diese Effekte auf den Client Bereich ihrer Fenster der obersten Ebene anwenden.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Desktopfenster-Manager (DWM), weich/Behind-Effekt
- Dwm (Desktopfenster-Manager), weich-Behind-Effekt
- weich-Behind-Effekt
- durchlässiges wirken
- transparenter Glas Effekt
- Desktopfenster-Manager (DWM), durchlässigem Effekt
- Dwm (Desktopfenster-Manager), durchscheinend
- Desktopfenster-Manager (DWM), transparenter Glas Effekt
- Dwm (Desktopfenster-Manager), transparenter Glas Effekt
- Desktopfenster-Manager (DWM), Erweitern des Fensterrahmens in den Client Bereich
- Dwm (Desktopfenster-Manager), Erweitern des Fensterrahmens in den Client Bereich
- Erweitern des Fensterrahmens in den Client Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf7378cfcaff93aa9a54ce399890ec1bfd8cc1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039505"
---
# <a name="dwm-blur-behind-overview"></a>DWM-weich hinter Übersicht

Eine der DWM-Effekte (Signature Desktopfenster-Manager) ist ein durchlässiges und verschwommene nicht-Client-Bereich. Mithilfe der DWM-APIs können Anwendungen diese Effekte auf den Client Bereich ihrer Fenster der obersten Ebene anwenden.

> [!Note]  
> Windows Vista Home Basic Edition unterstützt den transparenten Glas Effekt nicht. Bereiche, die in der Regel mit dem transparenten Glas Effekt in anderen Windows-Editionen gerendert werden, werden als nicht transparent dargestellt.
> Beginnend mit Windows 8 führt das Aufrufen dieser Funktion nicht zu einem Weichzeichnereffekt aufgrund einer Stiländerung in der Art und Weise, in der Fenster gerendert werden.


 

In diesem Thema werden die folgenden Client-Behind-Behind-Szenarien erläutert, die die DWM ermöglicht.

-   [Hinzufügen von Unschärfe zu einem bestimmten Bereich des Client Bereichs](#adding-blur-to-a-specific-region-of-the-client-area)
-   [Erweitern des Fensterrahmens in den Client Bereich](#extending-the-window-frame-into-the-client-area)
-   [Zugehörige Themen](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a>Hinzufügen von Unschärfe zu einem bestimmten Bereich des Client Bereichs

Eine Anwendung kann den Weichzeichnereffekt hinter dem gesamten Client Bereich des Fensters oder auf eine bestimmte Unterregion anwenden. Dadurch können Anwendungen formatierte Pfade und Suchleisten hinzufügen, die visuell vom Rest der Anwendung getrennt sind.

Bei der in diesem Szenario verwendeten API handelt es sich um die [**dwmenableblurabledwindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) -Funktion, die die DWM-weich- [**hinter Konstanten**](dwm-bb-constants.md) und die [**DWM- \_ blurbehind**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) -Struktur nutzt.

Die folgende Beispiel Funktion, `EnableBlurBehind` , veranschaulicht, wie der weich-Behind-Effekt auf das gesamte Fenster angewendet wird.


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



Beachten Sie, dass **null** im *hRgnBlur* -Parameter angegeben wird. Dadurch wird der DWM mitgeteilt, dass der Weichzeichner hinter dem gesamten Fenster angewendet werden soll.

In der folgenden Abbildung wird der auf das gesamte Fenster angewendete weich-Behind-Effekt veranschaulicht.

![der auf ein Fenster angewendete weich-Behind-Effekt](images/dwm-blurbehindwindow.png)

Wenn Sie den weich Zeichen hinter einer Unterregion anwenden möchten, wenden Sie ein gültiges Regions handle (hrgn) auf den **hRgnBlur** -Member der [**DWM- \_ blurbehind**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) -Struktur an, und fügen Sie dem **dwFlags** -Member das Flag **DWM \_ BB \_ blurregion** hinzu.

Wenn Sie den weich-Behind-Effekt auf einen Teilbereich des Fensters anwenden, wird der Alphakanal des Fensters für den nicht unscharfen Bereich verwendet. Dies kann zu einer unerwarteten Transparenz im nicht unscharfen Bereich eines Fensters führen. Gehen Sie daher vorsichtig vor, wenn Sie einen Weichzeichnereffekt auf eine Unterregion anwenden.

## <a name="extending-the-window-frame-into-the-client-area"></a>Erweitern des Fensterrahmens in den Client Bereich

Eine Anwendung kann die weich Zeichnung des Fensterrahmens auf den Client Bereich ausdehnen. Dies ist hilfreich, wenn Sie den Weichzeichnereffekt hinter einem Fenster mit einer angedockten Symbolleiste oder visuell getrennte Steuerelemente vom Rest einer Anwendung anwenden. Diese Funktionalität wird von der Funktion " [**dwmextendframeinesclientarea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) " verfügbar gemacht.

Verwenden Sie zum Aktivieren von weich Zeichen mithilfe von [**dwmextendframeinesclientarea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea)die [**Ränder**](/windows/win32/api/uxtheme/ns-uxtheme-margins) -Struktur, um anzugeben, wie viel in den Client Bereich erweitert werden soll. Die folgende Beispiel Funktion, `ExtendIntoClientBottom` , schaltet die weichzeichnerweiterung unten im nicht-Client-Frame in den Client Bereich um.


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



In der folgenden Abbildung ist der weich-Behind-Effekt dargestellt, der auf den unteren Rand des Client Bereichs erweitert wurde.

![Bild, das den weich Zeichen-Behind-Effekt anzeigt, der zum unteren Rand eines Client Bereichs erweitert wurde](images/dwm-extendedbottom.png)

Auch über die [**dwmextendframeinesclientarea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) -Methode verfügbar, ist das "Sheet of Glass"-Effekt, bei dem der Weichzeichnereffekt auf die gesamte Oberfläche des Fensters ohne einen sichtbaren Fensterrahmen angewendet wird. Im folgenden Beispiel wird dieser Effekt veranschaulicht, bei dem der Client Bereich ohne Fensterrahmen gerendert wird.


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



In der folgenden Abbildung ist der weich-Behind im Fenster Stil "Sheet of Glass" dargestellt.

![Bild, das den weich Zeichnungs Effekt im Fenster Stil "Glas Blatt" veranschaulicht](images/dwm-sheetofglass.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Desktop Window Manager](dwm-overview.md)
</dt> <dt>

[Enable and Control DWM Composition (Aktivieren und Steuern der DWM-Komposition)](composition-ovw.md)
</dt> <dt>

[Überlegungen zur Leistung und bewährte Methoden](bestpractices-ovw.md)
</dt> </dl>

 

 