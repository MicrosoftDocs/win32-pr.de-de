---
title: Aktivieren und Steuern der DWM-Komposition
description: Die Desktopfenster-Manager(DWM)-Kompositions-APIs bieten mehrere Funktionen zum Festlegen und Abfragen grundlegender Informationen, die vom DWM verwendet werden.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Desktopfenster-Manager (DWM), Komposition
- DWM (Desktopfenster-Manager),Composition
- Komposition
- Desktopkomposition
- Farbauftrag
- Rendering von Nicht-Client-Regionen
- Desktopfenster-Manager (DWM), Farbgebung
- DWM (Desktopfenster-Manager), Farbgebung
- Desktopfenster-Manager (DWM), Nicht-Clientbereichsrendering
- DWM (Desktopfenster-Manager), Rendering von Nicht-Client-Regionen
- Desktopfenster-Manager (DWM), Messaging
- DWM (Desktopfenster-Manager), Messaging
- messaging
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: e8c5df1778436e2cfe23df85483453b01fb80884adc9a6d8ff34955deb3e0c6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741580"
---
# <a name="enable-and-control-dwm-composition"></a>Aktivieren und Steuern der DWM-Komposition

Die Desktopfenster-Manager(DWM)-Kompositions-APIs bieten mehrere Funktionen zum Festlegen und Abfragen grundlegender Informationen, die vom DWM verwendet werden. Mit diesen APIs können Sie den Kompositionszustand abfragen und ändern. Darüber hinaus können Sie die Renderingrichtlinie für verschiedene DWM-Fensterattribute festlegen und abfragen.

## <a name="retrieving-colorization-information"></a>Abrufen von Farbgebungsinformationen

Die Farbe des Nicht-Clientbereichs eines Fensters wird durch das aktuelle Systemfarbdesign bestimmt. Der Farbgebungswert wird über die DWM-APIs bereitgestellt, damit Ihre Anwendung die Clientbenutzeroberfläche mit dem Systemfarbdesign ab finden kann.

Um auf diesen Farbwert zu zugreifen und die Farbänderung zu überwachen, verwenden Sie die [**DwmGetColorizationColor-Funktion**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) und die [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) Meldung.

In diesem Beispiel wird veranschaulicht, wie die Meldung "Farbänderung" behandelt und auf die neue Farbe zugreifen kann.

```cpp
...
case WM_DWMCOLORIZATIONCOLORCHANGED:
{
    DWORD newColorizationColor{ (DWORD)wParam };
    BOOL isBlendedWithOpacity{ (BOOL)lParam };
}
break;
...
```

## <a name="controlling-non-client-region-rendering"></a>Steuern des Renderns von nicht clientseitigen Regionen

Zwei der visuellen Effekte, die DWM ermöglicht, sind Transparenz des Nicht-Clientbereichs eines Fensters und Übergangseffekte. Ihre Anwendung muss diese Effekte möglicherweise aus Stil- oder Kompatibilitätsgründen deaktivieren oder erneut aktivieren. Die folgenden Funktionen werden verwendet, um Transparenz und Übergangseffektverhalten zu verwalten.

- [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

Rufen Sie [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) auf, und legen Sie *dwAttribute* auf [**DWMWA_NCRENDERING_ENABLED.**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) Wie Sie in der Dokumentation für DWMWA_NCRENDERING_ENABLED sehen [**können,**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute)ist der abgerufene Attributwert vom Typ **BOOL,** wenn Sie dieses Flag an **DwmGetWindowAttribute** übergeben. Verschiedene Flags bewirken, **dass DwmGetWindowAttribute** Werte verschiedener Typen zurück gibt. Hier sehen Sie ein Codebeispiel.

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

Im nächsten Beispiel wird gezeigt, wie das [**DWMWA_EXTENDED_FRAME_BOUNDS-Flag**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) mit **DwmGetWindowAttribute** verwendet wird, um das erweiterte Rahmengrenzerechteck eines Fensters abzurufen. Die Dokumentation für dieses Flag teilt uns mit, dass der abgerufene Attributwert vom Typ **RECT ist.**

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> Befolgen Sie das oben gezeigte Programmiermuster, wenn Sie [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) mit Flags für verschiedene Attribute aufrufen. Das [**DwMWINDOWATTRIBUTE-Enumerationsthema**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) gibt in der Zeile für jedes Flag an, auf welchen Werttyp Sie im *pvAttribute-Parameter* für **DwmGetWindowAttribute** einen Zeiger übergeben sollten. Der *cbAttribute-Parameter* enthält die Größe dieses Objekts in Bytes.

[**Mit DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) kann Ihre Anwendung die Richtlinie zum Rendern von Nicht-Clientbereich festlegen. Diese Funktion bestimmt auch, wie Ihre Anwendung DWM-Übergangseffekte behandeln soll.

Im nächsten Beispiel wird das Rendern von Nicht-Clientbereich deaktiviert. Dadurch werden alle vorherigen Aufrufe von [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) oder [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) deaktiviert.

```
HRESULT DisableNCRendering(HWND hWnd)
{
    HRESULT hr = S_OK;

    DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

    // Disable non-client area rendering on the window.
    hr = ::DwmSetWindowAttribute(hWnd,
        DWMWA_NCRENDERING_POLICY,
        &ncrp,
        sizeof(ncrp));

    if (SUCCEEDED(hr))
    {
        // ...
    }

    return hr;
}
```

Zusätzlich zum Steuern des Nicht-Clientbereichsrenderings kann [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) auch DWM-Übergangseffekte steuern. Sie können das Übergangsverhalten festlegen, indem Sie **DWMWA \_ TRANSITIONS \_ FORCEDISABLED** als *dwAttribute-Parameter* verwenden.

## <a name="messages"></a>Meldungen

Die folgenden Meldungen stellen eine Benachrichtigung über DWM-Ereignisse zur Verfügung. Diese Meldungen können verwendet werden, um Änderungen wie Änderungen am Kompositionszustand und Änderungen des Systemfarbdesigns zu überwachen.

- [**WM \_ DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md)
- [**WM \_ DWMCOMPOSITIONCHANGED**](wm-dwmcompositionchanged.md)
- [**WM \_ DWMNCRENDERINGCHANGED**](wm-dwmncrenderingchanged.md)
- [**WM \_ DWMWINDOWMAXIMIZEDCHANGE**](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows-7-and-earlier"></a>Deaktivieren der DWM-Komposition (Windows 7 und früher)

> [!WARNING]
> Die Informationen in diesem Abschnitt gelten nur für Windows 7 und frühere Systeme.

Da DWM die Grafikprozessor (GRAPHICS Processing Unit, GPU) für die Desktopkomposition verwendet, muss Ihre Anwendung DWM möglicherweise aus Kompatibilitäts- bzw. Kompatibilitätsproblemen deaktivieren. Anwendungen, die die vollständige Kontrolle über den Desktop haben, z. B. Spiele, die im Vollbildmodus ausgeführt werden, müssen bestimmen, ob das DWM aktiviert ist, und, falls dies der Status ist, es deaktivieren. Dazu sind zwei Funktionen erforderlich.

- [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

Ein Aufruf von [**DwmEnableComposition,**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) bei dem *fEnable* auf **DWM \_ EC \_ DISABLECOMPOSITION** festgelegt ist, deaktiviert die DWM-Komposition, bis entweder der aufrufende Prozess heruntergefahren wurde oder die Komposition durch Aufrufen von **DwmEnableComposition** mit fEnable erneut aktiviert wurde, wenn *fEnable* auf **DWM EC \_ \_ ENABLECOMPOSITION festgelegt** ist. Die DWM-Komposition wird automatisch neu gestartet, sobald alle Anwendungen, die die Komposition deaktiviert haben, entweder heruntergefahren oder die Komposition manuell durch Aufrufen von **DwmEnableComposition erneut aktiviert haben.**

> [!NOTE]  
> Das DWM deaktiviert die Komposition automatisch, wenn eine Anwendung versucht, direkt auf die primäre Anzeigeoberfläche zu zeichnen. Die Komposition wird deaktiviert, bis die primäre Geräteoberfläche von dieser Anwendung freigegeben wird.
