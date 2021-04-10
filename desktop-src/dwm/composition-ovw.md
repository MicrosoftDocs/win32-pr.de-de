---
title: Aktivieren und Steuern der DWM-Komposition
description: Die Desktopfenster-Manager (DWM)-Kompositions-APIs bieten verschiedene Funktionen zum Festlegen und Abfragen grundlegender Informationen, die von der DWM verwendet werden.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Desktopfenster-Manager (DWM), Komposition
- Dwm (Desktopfenster-Manager), Komposition
- Komposition
- Desktop Komposition
- farbliche Kennzeichnung
- Rendering außerhalb der Client Region
- Desktopfenster-Manager (DWM), farbige Farbgebung
- Dwm (Desktopfenster-Manager), farbige Farbgebung
- Desktopfenster-Manager (DWM), Rendering außerhalb der Client Region
- Dwm (Desktopfenster-Manager), Rendering außerhalb der Client Region
- Desktopfenster-Manager (DWM), Messaging
- Dwm (Desktopfenster-Manager), Messaging
- messaging
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: 8d7654f479896002b4bc65df613fab9506caf2a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856760"
---
# <a name="enable-and-control-dwm-composition"></a>Aktivieren und Steuern der DWM-Komposition

Die Desktopfenster-Manager (DWM)-Kompositions-APIs bieten verschiedene Funktionen zum Festlegen und Abfragen grundlegender Informationen, die von der DWM verwendet werden. Mit diesen APIs können Sie den Kompositions Statusabfragen und ändern. Außerdem können Sie die renderinganricht Linie für verschiedene DWM-Fenster Attribute festlegen und Abfragen.

## <a name="retrieving-colorization-information"></a>Informationen zur Farbgebung werden abgerufen.

Die Farbe des nicht-Client Bereichs eines Fensters wird durch das aktuelle System Farbschema bestimmt. Der Wert für die farbliche Kennzeichnung wird über die DWM-APIs bereitgestellt, damit die Anwendung die Client Benutzeroberfläche mit dem System Farbschema abgleichen kann.

Um auf diesen Wert für die Farbgebung zuzugreifen und die Farbänderung zu überwachen, verwenden Sie die Funktion [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) und die [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) Nachricht.

In diesem Beispiel wird veranschaulicht, wie Sie die geänderte Farbe der Farbe behandeln und auf die neue Farbe zugreifen.

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

## <a name="controlling-non-client-region-rendering"></a>Steuern des Renderings außerhalb der Client Region

Zwei der visuellen Effekte, die DWM ermöglicht, sind Transparenz des nicht-Client Bereichs eines Fensters und Übergangseffekte. Möglicherweise muss Ihre Anwendung diese Effekte aus Formatierungs-oder Kompatibilitätsgründen deaktivieren oder erneut aktivieren. Die folgenden Funktionen werden verwendet, um Transparenz und das Verhalten des Übergangs Effekts zu verwalten.

- [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

Rufen Sie zum Abrufen des aktuellen nicht-Client-Renderingzustands für das Fenster einer Anwendung [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) auf, wobei *dwattribute* auf [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute)festgelegt ist. Wie Sie in der Dokumentation für [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute)sehen können, ist der abgerufene Attribut Wert, wenn Sie dieses Flag an **DwmGetWindowAttribute** übergeben, vom Typ **bool**. Verschiedene Flags bewirken, dass **DwmGetWindowAttribute** Werte unterschiedlicher Typen zurückgibt. Hier sehen Sie ein Codebeispiel.

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

Im nächsten Beispiel wird gezeigt, wie das [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) -Flag mit **DwmGetWindowAttribute** verwendet wird, um das erweiterte Rahmen Rahmen-Rechteck eines Fensters abzurufen. Die Dokumentation für dieses Flag gibt an, dass der abgerufene Attribut Wert vom Typ " **Rect**" ist.

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> Befolgen Sie das oben gezeigte Programmier Muster, wenn Sie [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) mit Flags für verschiedene Attribute aufrufen. Das Thema [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) -Enumeration gibt an, welcher Werttyp, auf den Sie einen Zeiger im *pvattribute* -Parameter für **DwmGetWindowAttribute** übergeben sollten, in der Zeile für jedes Flag. Der *cbattribute* -Parameter enthält die Größe dieses Objekts in Bytes.

[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) ermöglicht der Anwendung das Festlegen der nicht-Client Bereichs-renderinganricht Linie. Diese Funktion bestimmt auch, wie die Anwendung DWM-Übergangseffekte behandeln soll.

Im nächsten Beispiel wird das Rendering außerhalb des Client Bereichs deaktiviert. Dies bewirkt, dass alle vorherigen Aufrufe von [dwmenableblurabledwindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) oder [dwmextendframeindeclientarea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) deaktiviert werden.

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

Neben der Steuerung des nicht-Client Bereichs Rendering kann [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) auch DWM-Übergangseffekte steuern. Sie können das Übergangs Verhalten mithilfe von **dwmwa-über \_ Gängen \_ forcedeaktiviert** als *dwattribute* -Parameter festlegen.

## <a name="messages"></a>Meldungen

Die folgenden Meldungen enthalten eine Benachrichtigung über DWM-Ereignisse. Diese Nachrichten können zum Überwachen von Änderungen verwendet werden, z. b. Änderungen des Kompositions Status und Änderungen am System Farbdesign.

- [**WM \_ dwmcolorizationcolorchanged**](wm-dwmcolorizationcolorchanged.md)
- [**WM \_ dwmcompositionchanged**](wm-dwmcompositionchanged.md)
- [**WM \_ dwmncrenderingchanged**](wm-dwmncrenderingchanged.md)
- [**WM \_ dwmwindowmaximizedchange**](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a>Deaktivieren der DWM-Komposition (Windows 7 und früher)

> [!WARNING]
> Die Informationen in diesem Abschnitt gelten nur für Windows 7 und frühere Systeme.

Da DWM die GPU (Graphics Processing Unit) für die Desktop Komposition verwendet, muss Ihre Anwendung DWM möglicherweise auf Kompatibilität deaktivieren. Anwendungen, die die vollständige Kontrolle über den Desktop übernehmen, z. b. Spiele, die im Vollbildmodus ausgeführt werden, müssen bestimmen, ob die DWM aktiviert ist. ist dies der Fall, deaktivieren Sie Sie. Zu diesem Zweck werden zwei Funktionen benötigt.

- [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

Ein Aufruf von [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) , bei dem " *fEnable* " auf **DWM \_ EC " \_ disablecomposition** " festgelegt ist, deaktiviert die DWM-Komposition, bis der aufrufende Prozess beendet wurde oder die Komposition durch Aufrufen von " **DwmEnableComposition** " mit " *fEnable* " auf " **DWM \_ EC \_ enablecomposition**" erneut aktiviert wurde. Die DWM-Komposition wird automatisch neu gestartet, sobald alle Anwendungen, die die Komposition deaktiviert haben, die Komposition durch Aufrufen von **DwmEnableComposition** entweder heruntergefahren oder manuell erneut aktiviert haben.

> [!NOTE]  
> Die DWM deaktiviert die Komposition automatisch, wenn eine Anwendung versucht, direkt zur primären Anzeige Oberfläche zu zeichnen. Die Komposition wird deaktiviert, bis die primäre Geräteoberfläche von der Anwendung freigegeben wird.
