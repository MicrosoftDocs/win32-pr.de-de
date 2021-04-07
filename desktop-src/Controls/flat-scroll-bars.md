---
title: Flache Scrollleisten
description: Microsoft Internet Explorer 4,0 führte eine neue visuelle Technologie mit dem Namen "flatscrollleisten" ein.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fbbdb64aa9815cb56f5dc3bf55ffb17390db38
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730457"
---
# <a name="flat-scroll-bars"></a>Flache Scrollleisten

Microsoft Internet Explorer 4,0 führte eine neue visuelle Technologie mit dem Namen "flatscrollleisten" ein. Funktionale, flache Schiebe leisten Verhalten sich genau wie Standard Scrollleisten. Der Unterschied besteht darin, dass Sie Ihre Darstellung in größerem Umfang als Standard Scrollleisten anpassen können.

Die folgende Abbildung zeigt ein Fenster, das eine flache Bild Lauf Leiste enthält.

![Screenshot eines Fensters, das eine flatscrollleiste enthält](images/flatsb.jpg)

> [!Note]  
> Flache Schiebe leisten werden von Comctl32.dll Versionen 4,71 bis 5,82 unterstützt. In Comctl32.dll, Version 6,00 und höher, werden keine flachen Schiebe leisten unterstützt.

 

## <a name="using-flat-scroll-bars"></a>Verwenden von flachen Schiebe leisten

In diesem Abschnitt wird beschrieben, wie Sie flache Schiebe leisten in der Anwendung implementieren.

### <a name="before-you-begin"></a>Vorbereitungen

Wenn Sie die Funktionen der flatscrollleiste verwenden möchten, müssen Sie in den Quelldateien kommctrl. h einschließen und mit Comctl32. lib verknüpfen.

### <a name="adding-flat-scroll-bars-to-a-window"></a>Hinzufügen von flatscrollleisten zu einem Fenster

Wenn Sie einem Fenster flatscrollleisten hinzufügen möchten, führen Sie [**initializeflatsb**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb)aus, und übergeben Sie das Handle an das Fenster. Anstatt die Scrollleisten-Standardfunktionen zum Bearbeiten der Schiebe leisten zu verwenden, müssen Sie die entsprechende flatsb \_ xxx-Funktion verwenden. Es gibt flache Scrollleisten-Funktionen zum Festlegen und Abrufen der scrollinformationen, des Bereichs und der Position. Wenn für das Fenster keine flatscrollleisten initialisiert wurden, wird die API für die flatscrollleiste auf die entsprechenden Standardfunktionen zurückgestellt, sofern diese verwendet werden. Auf diese Weise können Sie flache Schiebe leisten ein-und ausschalten, ohne bedingten Code schreiben zu müssen.

Da eine Anwendung möglicherweise benutzerdefinierte Metriken für Ihre flachen Schiebe leisten festgelegt hat, werden Sie nicht automatisch aktualisiert, wenn sich Systemmetriken ändern. Wenn sich die Metriken der systemscrollleiste ändern, wird eine [**WM- \_ settingchange**](/windows/desktop/winmsg/wm-settingchange) -Nachricht gesendet, wobei *wParam* auf [**SPI \_ setnonclientmetrics**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)festgelegt ist. Zum Aktualisieren von flatscrollleisten auf die neuen Systemmetriken müssen Anwendungen diese Nachricht verarbeiten und die metrikabhängigen Eigenschaften der flatscrollleiste explizit ändern.

Verwenden Sie [**flatsb \_ setscrollprop**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop), um die ScrollBar-Eigenschaften zu aktualisieren. Mit dem folgenden Code Fragment werden die metrikabhängigen Eigenschaften einer flatscrollleiste auf die aktuellen System Werte geändert.


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



### <a name="enhancing-flat-scroll-bars"></a>Verbessern von flachen Schiebe leisten

[**Flatsb \_ Setscrollprop**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) ermöglicht es Ihnen, die flachen Schiebe leisten zu ändern, um das Aussehen des Fensters anzupassen. Bei vertikalen Schiebe leisten können Sie die Breite des Balkens und die Höhe der Pfeilrichtung ändern. Bei horizontalen Schiebe leisten können Sie die Höhe des Balkens und die Breite der Pfeilrichtung ändern. Sie können auch die Hintergrundfarbe der horizontalen und vertikalen Schiebe leisten ändern.

[**Flatsb \_ Mit setscrollprop**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) können Sie auch anpassen, wie die flachen Schiebe leisten angezeigt werden. Durch Ändern der Eigenschaften von WSB \_ Prop \_ Vstyle und WSB \_ Prop \_ hstyle können Sie den Typ der Scrollleiste festlegen, die Sie verwenden möchten. Es sind drei Stile verfügbar.



|                    |                                                                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FSB- \_ Encarta- \_ Modus | Eine standardmäßige flatscrollleiste wird angezeigt. Wenn die Maus über eine Richtungs Schaltfläche oder den Ziehpunkt bewegt wird, wird dieser Teil der Bild Lauf Leiste in 3D angezeigt.             |
| FSB \_ - \_ FlatMode    | Eine standardmäßige flatscrollleiste wird angezeigt. Wenn die Maus über eine Richtungs Schaltfläche oder den Ziehpunkt bewegt wird, wird dieser Teil der Bild Lauf Leiste in umgekehrten Farben angezeigt. |
| \_regulärer \_ Modus für FSB | Eine normale, nicht flache Bild Lauf Leiste wird angezeigt. Es werden keine besonderen visuellen Effekte angewendet.                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a>Entfernen von flachen Schiebe leisten

Wenn Sie flache Schiebe leisten aus dem Fenster entfernen möchten, können Sie die Funktion [**uninitializeflatsb**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) aufrufen und das Handle an das Fenster übergeben. Diese Funktion entfernt nur flatscrollleisten aus dem Fenster zur Laufzeit. Diese Funktion muss nicht aufgerufen werden, wenn das Fenster zerstört wird.

 

 