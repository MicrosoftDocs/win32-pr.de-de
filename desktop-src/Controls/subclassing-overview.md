---
title: Steuerelemente für Unterklassen
description: Wenn ein Steuerelement fast alles macht, was Sie möchten, aber einige weitere Features benötigen, können Sie features ändern oder dem ursprünglichen Steuerelement hinzufügen, indem Sie es in Unterklassen untergliedern.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2e338deca61c4aac07fca431e77492f53f168540cfbbcf7596b8540ba5369f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168580"
---
# <a name="subclassing-controls"></a>Steuerelemente für Unterklassen

Wenn ein Steuerelement fast alles macht, was Sie möchten, aber einige weitere Features benötigen, können Sie features ändern oder dem ursprünglichen Steuerelement hinzufügen, indem Sie es in Unterklassen untergliedern. Eine Unterklasse kann alle Funktionen einer vorhandenen Klasse sowie alle zusätzlichen Features haben, die Sie ihr geben möchten.

In diesem Dokument wird erläutert, wie Unterklassen erstellt werden, und es werden die folgenden Themen behandelt.

-   [Unterklassensteuerelemente vor ComCtl32.dll Version 6](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [Speichern von Benutzerdaten](#storing-user-data)
    -   [Nachteile des Alten Unterklassenansatzes](#disadvantages-of-the-old-subclassing-approach)
-   [Unterklassen von Steuerelementen mit ComCtl32.dll Version 6](#subclassing-controls-using-comctl32dll-version-6)
    -   [SetWindowSubclass](#setwindowsubclass)
    -   [GetWindowSubclass](#getwindowsubclass)
    -   [RemoveWindowSubclass](#removewindowsubclass)
    -   [DefSubclassProc](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a>Unterklassensteuerelemente vor ComCtl32.dll Version 6

Sie können ein Steuerelement in einer Unterklasse speichern und Benutzerdaten in einem -Steuerelement speichern. Dies ist der Fall, wenn Sie Versionen von ComCtl32.dll Version 6 verwenden. Es gibt einige Nachteile beim Erstellen von Unterklassen mit früheren Versionen von ComCtl32.dll.

Um ein neues Steuerelement zu machen, ist es am besten, mit einem der Windows zu beginnen und es an eine bestimmte Anforderungen zu erweitern. Um ein Steuerelement zu erweitern, erstellen Sie ein Steuerelement, und ersetzen Sie die vorhandene Fensterprozedur durch eine neue Prozedur. Die neue Prozedur fängt die Nachrichten des Steuerelements ab und führt entweder aktionen oder übergibt sie zur Standardverarbeitung an die ursprüngliche Prozedur. Verwenden Sie [**die Funktion SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) oder [**SetWindowLongPtr,**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) um den WNDPROC des Steuerelements zu ersetzen. Das folgende Codebeispiel zeigt, wie WNDPROC ersetzt wird.


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a>Speichern von Benutzerdaten

Möglicherweise möchten Sie Benutzerdaten in einem einzelnen Fenster speichern. Diese Daten können von der neuen Fensterprozedur verwendet werden, um zu bestimmen, wie das Steuerelement ge zeichnen oder wohin bestimmte Nachrichten gesendet werden sollen. Beispielsweise können Sie Daten verwenden, um einen C++-Klassenzeiger auf die Klasse zu speichern, die das Steuerelement darstellt. Das folgende Codebeispiel zeigt, wie Sie [**SetProp verwenden,**](/windows/desktop/api/winuser/nf-winuser-setpropa) um Daten mit einem Fenster zu speichern.


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a>Nachteile des Alten Unterklassenansatzes

Die folgende Liste zeigt einige nachteile der Verwendung des zuvor beschriebenen Ansatzes zum Unterklassen eines Steuerelements.

-   Die Fensterprozedur kann nur einmal ersetzt werden.
-   Es ist schwierig, eine Unterklasse zu entfernen, nachdem sie erstellt wurde.
-   Das Zuordnen privater Daten zu einem Fenster ist ineffizient.
-   Zum Aufrufen der nächsten Prozedur in einer Unterklassenkette können Sie die alte Fensterprozedur nicht umschalten und aufrufen. Sie müssen sie mithilfe der [**CallWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) aufrufen.

## <a name="subclassing-controls-using-comctl32dll-version-6"></a>Unterklassen von Steuerelementen mit ComCtl32.dll Version 6

> [!Note]  
> ComCtl32.dll Version 6 ist nur Unicode. Die allgemeinen Steuerelemente, die von ComCtl32.dll 6 unterstützt werden, sollten nicht mit ANSI-Fensterverfahren als Unterklassen (oder Übergeordnetes) klassifiziert werden.

 

ComCtl32.dll Version 6 enthält vier Funktionen, die das Erstellen von Unterklassen vereinfachen und die zuvor erläuterten Nachteile beseitigen. Die neuen Funktionen kapseln die Verwaltung, die mit mehreren Sätzen von Verweisdaten verbunden ist, daher kann sich der Entwickler auf die Programmierung von Features und nicht auf die Verwaltung von Unterklassen konzentrieren. Die Unterklassenfunktionen sind:

-   [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a>SetWindowSubclass

Diese Funktion wird verwendet, um zunächst eine Unterklasse eines Fensters zu erstellen. Jede Unterklasse wird durch die Adresse der *pfnSubclass* und ihrer *uIdSubclass eindeutig identifiziert.* Beides sind Parameter der [**SetWindowSubclass-Funktion.**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) Mehrere Unterklassen können dieselbe Unterklassenprozedur gemeinsam verwenden, und die ID kann jeden Aufruf identifizieren. Um Verweisdaten zu ändern, können Sie nachfolgende Aufrufe von **SetWindowSubclass tätigen.** Der wichtige Vorteil ist, dass jede Unterklasseninstanz über eigene Verweisdaten verfügt.

Die Deklaration einer Unterklassenprozedur ist etwas anders als eine reguläre Fensterprozedur, da sie zwei zusätzliche Daten enthält: die Unterklassen-ID und die Verweisdaten. Die letzten beiden Parameter der folgenden Funktionsdeklaration zeigen dies.


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



Jedes Mal, wenn eine Nachricht von der neuen Fensterprozedur empfangen wird, werden eine Unterklassen-ID und Verweisdaten eingeschlossen.

> [!Note]  
> Alle an die Prozedur übergebenen Zeichenfolgen sind Unicode-Zeichenfolgen, auch wenn Unicode nicht als Präprozessordefinition angegeben ist.

 

Das folgende Beispiel zeigt eine Gerüstimplementierung einer Fensterprozedur für ein Steuerelement mit Unterklassen.


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



Die Fensterprozedur kann an das -Steuerelement im [**WM \_ INITDIALOG-Handler**](/windows/desktop/dlgbox/wm-initdialog) der Dialogprozedur angefügt werden, wie im folgenden Beispiel gezeigt.


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a>GetWindowSubclass

Diese Funktion ruft Informationen zu einer Unterklasse ab. Beispielsweise können Sie [**getWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) verwenden, um auf die Verweisdaten zu zugreifen.

### <a name="removewindowsubclass"></a>RemoveWindowSubclass

Diese Funktion entfernt Unterklassen. [**Mit RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in Kombination mit [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) können Sie Unterklassen dynamisch hinzufügen und entfernen.

### <a name="defsubclassproc"></a>DefSubclassProc

Die [**DefSubclassProc-Funktion**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) ruft den nächsten Handler in der Unterklassenkette auf. Die Funktion ruft auch die richtigen ID- und Verweisdaten ab und übergibt die Informationen an die Nächste Fensterprozedur.

 

 