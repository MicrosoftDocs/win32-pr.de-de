---
title: Subclassingsteuerelemente
description: Wenn ein Steuerelement fast alles hat, was Sie möchten, aber Sie benötigen noch ein paar weitere Features, können Sie Funktionen zum ursprünglichen Steuerelement ändern oder hinzufügen, indem Sie es Unterklassen.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039706"
---
# <a name="subclassing-controls"></a>Subclassingsteuerelemente

Wenn ein Steuerelement fast alles hat, was Sie möchten, aber Sie benötigen noch ein paar weitere Features, können Sie Funktionen zum ursprünglichen Steuerelement ändern oder hinzufügen, indem Sie es Unterklassen. Eine Unterklasse kann über alle Funktionen einer vorhandenen Klasse sowie über alle zusätzlichen Features verfügen, die Sie erhalten möchten.

In diesem Dokument wird erläutert, wie Unterklassen erstellt werden und wie die folgenden Themen enthalten sind.

-   [Unterklassen-Steuerelemente vor ComCtl32.dll Version 6](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [Speichern von Benutzerdaten](#storing-user-data)
    -   [Nachteile des alten Unterklassen Ansatzes](#disadvantages-of-the-old-subclassing-approach)
-   [Unterklassen-Steuerelemente mit ComCtl32.dll Version 6](#subclassing-controls-using-comctl32dll-version-6)
    -   [Setwindowsubclass](#setwindowsubclass)
    -   [Getwindowsubclass](#getwindowsubclass)
    -   [Removewindowsubclass](#removewindowsubclass)
    -   [Defsubclassproc](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a>Unterklassen-Steuerelemente vor ComCtl32.dll Version 6

Sie können ein-Steuerelement in einer Unterklasse platzieren und Benutzerdaten in einem-Steuerelement speichern. Dies geschieht, wenn Sie Versionen von ComCtl32.dll vor Version 6 verwenden. Es gibt einige Nachteile beim Erstellen von Unterklassen mit früheren Versionen von ComCtl32.dll.

Um ein neues Steuerelement zu erstellen, ist es am besten, mit einem der allgemeinen Windows-Steuerelemente zu beginnen und es an einen bestimmten Bedarf anzupassen. Um ein Steuerelement zu erweitern, erstellen Sie ein-Steuerelement, und ersetzen Sie dessen vorhandene Fenster Prozedur durch eine neue. Die neue Prozedur fängt die Meldungen des Steuer Elements ab und führt Sie entweder aus oder übergibt sie zur Standard Verarbeitung an die ursprüngliche Prozedur. Verwenden Sie die Funktion " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) " oder " [**setwindowlongptr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) ", um das WndProc-Element des Steuer Elements zu ersetzen. Im folgenden Codebeispiel wird gezeigt, wie ein WndProc ersetzt wird.


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a>Speichern von Benutzerdaten

Möglicherweise möchten Sie Benutzerdaten mit einem einzelnen Fenster speichern. Diese Daten können von der neuen Fenster Prozedur verwendet werden, um zu bestimmen, wie das Steuerelement gezeichnet werden soll oder wohin bestimmte Nachrichten gesendet werden sollen. Beispielsweise können Sie Daten zum Speichern eines C++-Klassen Zeigers auf die Klasse verwenden, die das Steuerelement darstellt. Im folgenden Codebeispiel wird gezeigt, wie [**setprop**](/windows/desktop/api/winuser/nf-winuser-setpropa) zum Speichern von Daten mit einem-Fenster verwendet wird.


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a>Nachteile des alten Unterklassen Ansatzes

In der folgenden Liste werden einige Nachteile der Verwendung des zuvor beschriebenen Ansatzes zum Unterklassen eines-Steuer Elements aufgeführt.

-   Die Fenster Prozedur kann nur einmal ersetzt werden.
-   Es ist schwierig, eine Unterklasse zu entfernen, nachdem Sie erstellt wurde.
-   Das Zuordnen privater Daten zu einem Fenster ist ineffizient.
-   Um die nächste Prozedur in einer Unterklassen Kette aufzurufen, können Sie die alte Fenster Prozedur nicht umwandeln und aufrufen, sondern Sie müssen Sie mithilfe der [**callwindowproc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) -Funktion aufrufen.

## <a name="subclassing-controls-using-comctl32dll-version-6"></a>Unterklassen-Steuerelemente mit ComCtl32.dll Version 6

> [!Note]  
> ComCtl32.dll Version 6 ist nur Unicode. Die von ComCtl32.dll Version 6 unterstützten allgemeinen Steuerelemente dürfen nicht mit ANSI-Fenster Prozeduren untergeordnet (oder übergeordnet) werden.

 

ComCtl32.dll Version 6 enthält vier Funktionen, die das Erstellen von Unterklassen vereinfachen und die zuvor erörterten Nachteile vermeiden. Die neuen Funktionen kapseln die Verwaltung, die mit mehreren Sätzen von Verweis Daten verbunden ist. Daher kann sich der Entwickler auf die Programmierfunktionen konzentrieren, nicht auf die Verwaltung von Unterklassen. Die Unterklassen Funktionen sind:

-   [**Setwindowsubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [**Getwindowsubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [**Removewindowsubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [**Defsubclassproc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a>Setwindowsubclass

Diese Funktion wird verwendet, um anfänglich ein Fenster zu Unterklassen. Jede Unterklasse wird durch die Adresse der *pfnsubclass* und ihrer *uidsubclass* eindeutig identifiziert. Beide sind Parameter der Funktion [**setwindowsubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) . Mehrere Unterklassen können dieselbe Unterklassen Prozedur gemeinsam verwenden, und die ID kann jeden-Rückruf identifizieren. Um Verweis Daten zu ändern, können Sie nachfolgende Aufrufe an **setwindowsubclass** durchführen. Der wichtige Vorteil besteht darin, dass jede Unterklassen Instanz über eigene Verweis Daten verfügt.

Die Deklaration einer Unterklassen Prozedur unterscheidet sich geringfügig von einer regulären Fenster Prozedur, da Sie über zwei zusätzliche Datenelemente verfügt: die Unterklassen-ID und die Verweis Daten. Dies wird in den letzten beiden Parametern der folgenden Funktionsdeklaration veranschaulicht.


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



Jedes Mal, wenn eine Nachricht von der neuen Fenster Prozedur empfangen wird, sind eine Unterklassen-ID und Verweis Daten enthalten.

> [!Note]  
> Alle an die Prozedur weiter gegebenen Zeichen folgen sind Unicode-Zeichen folgen, auch wenn Unicode nicht als Präprozessordefinition angegeben ist.

 

Das folgende Beispiel zeigt eine Skeleton-Implementierung einer Fenster Prozedur für ein untergeordnetes Steuerelement.


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



Die Fenster Prozedur kann an das-Steuerelement im " [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog) "-Handler der Dialogfeld Prozedur angefügt werden, wie im folgenden Beispiel gezeigt.


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a>Getwindowsubclass

Diese Funktion Ruft Informationen zu einer Unterklasse ab. Beispielsweise können Sie [**getwindowsubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) verwenden, um auf die Verweis Daten zuzugreifen.

### <a name="removewindowsubclass"></a>Removewindowsubclass

Diese Funktion entfernt Unterklassen. [**Removewindowsubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in Kombination mit [**setwindowsubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) ermöglicht das dynamische Hinzufügen und Entfernen von Unterklassen.

### <a name="defsubclassproc"></a>Defsubclassproc

Die [**defsubclassproc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) -Funktion Ruft den nächsten Handler in der Unterklassen Kette auf. Die-Funktion ruft auch die richtige ID und Verweis Daten ab und übergibt die Informationen an die nächste Fenster Prozedur.

 

 