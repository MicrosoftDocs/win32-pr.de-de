---
title: Flache Bildlaufleisten
description: Microsoft Internet Explorer 4.0 hat eine neue visuelle Technologie eingeführt, die als flache Scrollleisten bezeichnet wird.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e56db4ee987a6d8cdc7b185f5db0f8d89540453
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423890"
---
# <a name="flat-scroll-bars"></a>Flache Bildlaufleisten

Microsoft Internet Explorer 4.0 hat eine neue visuelle Technologie eingeführt, die als flache Scrollleisten bezeichnet wird. Funktionell verhalten sich flache Bildlaufleisten genauso wie Standard-Scrollleisten. Der Unterschied besteht darin, dass Sie deren Darstellung in größerem Umfang als standard-Scrollleisten anpassen können.

Die folgende Abbildung zeigt ein Fenster, das eine flache Scrollleiste enthält.

![Screenshot eines Fensters, das eine flache Scrollleiste enthält](images/flatsb.jpg)

> [!Note]  
> Flache Scrollleisten werden von Comctl32.dll Versionen 4.71 bis 5.82 unterstützt. Comctl32.dll Versionen 6.00 und höher unterstützen keine flachen Bildlaufleisten.

 

## <a name="using-flat-scroll-bars"></a>Verwenden von flachen Bildlaufleisten

In diesem Abschnitt wird beschrieben, wie Sie flache Scrollleisten in Ihrer Anwendung implementieren.

### <a name="before-you-begin"></a>Vorbereitungen

Um die flachen Scrollleistenfunktionen zu verwenden, müssen Sie Commctrl.h in Ihre Quelldateien einschließen und eine Verknüpfung mit Comctl32.lib erstellen.

### <a name="adding-flat-scroll-bars-to-a-window"></a>Hinzufügen von flachen Bildlaufleisten zu einem Fenster

Um einem Fenster flache Scrollleisten hinzuzufügen, rufen [**Sie InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb)auf und übergeben das Handle an das Fenster. Anstatt die standardmäßigen Scrollleistenfunktionen zum Bearbeiten ihrer Scrollleisten zu verwenden, müssen Sie die entsprechende FlatSB \_ XXX-Funktion verwenden. Es gibt flache Scrollleistenfunktionen zum Festlegen und Abrufen der Scrollinformationen, des Bereichs und der Position. Wenn für Ihr Fenster keine flachen Bildlaufleisten initialisiert wurden, wird die API für flache Scrollleisten ggf. auf die entsprechenden Standardfunktionen zurückgeleitet. Dadurch können Sie flache Bildlaufleisten aktivieren und deaktivieren, ohne bedingten Code schreiben zu müssen.

Da eine Anwendung möglicherweise benutzerdefinierte Metriken für ihre flachen Scrollleisten festgelegt hat, werden sie nicht automatisch aktualisiert, wenn sich die Systemmetriken ändern. Wenn sich die Metriken der Scrollleiste des Systems ändern, wird eine [**WM \_ SETTINGCHANGE-Nachricht**](/windows/desktop/winmsg/wm-settingchange) übertragen, deren *wParam* auf [**SPI \_ SETNONCLIENTMETRICS festgelegt ist.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) Um flache Bildlaufleisten auf die neuen Systemmetriken zu aktualisieren, müssen Anwendungen diese Meldung verarbeiten und die metrikabhängigen Eigenschaften der flachen Scrollleiste explizit ändern.

Verwenden Sie [**FlatSB \_ SetScrollProp,**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop)um die Eigenschaften der Scrollleiste zu aktualisieren. Das folgende Codefragment ändert die metrikabhängigen Eigenschaften einer flachen Scrollleiste in die aktuellen Systemwerte.


```
void FlatSB_UpdateMetrics(HWND hWnd)
{
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXVSCROLL, GetSystemMetrics(SM_CXVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHSCROLL, GetSystemMetrics(SM_CXHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVSCROLL, GetSystemMetrics(SM_CYVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYHSCROLL, GetSystemMetrics(SM_CYHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHTHUMB, GetSystemMetrics(SM_CXHTHUMB), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVTHUMB, GetSystemMetrics(SM_CYVTHUMB), TRUE);
}
```



### <a name="enhancing-flat-scroll-bars"></a>Verbessern von flachen Bildlaufleisten

[**FlatSB \_ Mit SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) können Sie die flachen Scrollleisten ändern, um das Aussehen Ihres Fensters anzupassen. Bei vertikalen Bildlaufleisten können Sie die Breite des Balkens und die Höhe der Richtungspfeile ändern. Bei horizontalen Scrollleisten können Sie die Höhe des Balkens und die Breite der Richtungspfeile ändern. Sie können auch die Hintergrundfarbe der horizontalen und vertikalen Scrollleisten ändern.

[**FlatSB \_ Mit SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) können Sie auch anpassen, wie die flachen Scrollleisten angezeigt werden. Durch Ändern der Eigenschaften WSB PROP VSTYLE und WSB PROP HSTYLE können Sie den Typ der Bildlaufleiste \_ \_ \_ \_ festlegen, die Sie verwenden möchten. Es sind drei Stile verfügbar.



|   Style                 |   BESCHREIBUNG                                                                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_FSB-ENCARTA-MODUS \_ | Eine standardmäßige flache Bildlaufleiste wird angezeigt. Wenn der Mauszeiger über eine Richtungsschaltfläche oder den Strich bewegt wird, wird dieser Teil der Scrollleiste in 3D angezeigt.             |
| FSB \_ FLAT \_ MODE    | Eine standardmäßige flache Bildlaufleiste wird angezeigt. Wenn der Mauszeiger über eine Richtungsschaltfläche oder den Strich bewegt wird, wird dieser Teil der Scrollleiste in invertierten Farben angezeigt. |
| REGULÄRER \_ \_ FSB-MODUS | Eine normale, nichtflat-Scrollleiste wird angezeigt. Es werden keine speziellen visuellen Effekte angewendet.                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a>Entfernen von flachen Bildlaufleisten

Wenn Sie flache Bildlaufleisten aus Ihrem Fenster entfernen möchten, rufen Sie die [**UninitializeFlatSB-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) auf, und übergeben Sie das Handle an das Fenster. Diese Funktion entfernt nur zur Laufzeit flache Bildlaufleisten aus Ihrem Fenster. Sie müssen diese Funktion nicht aufrufen, wenn Ihr Fenster zerstört wird.

 

 