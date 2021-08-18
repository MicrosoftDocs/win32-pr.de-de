---
description: Sie können einen Pinsel verwenden, um das Innere praktisch jeder Form mithilfe einer GDI-Funktion (Graphics Device Interface) zu zeichnen.
ms.assetid: 64cd6e82-7a0d-4b5e-b491-450f37eea43a
title: Verwenden von Pinseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42e09dc5731ceba7961dfd66b296df531897f2915cff53ccdacf1b5b5740160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037498"
---
# <a name="using-brushes"></a>Verwenden von Pinseln

Sie können einen Pinsel verwenden, um das Innere praktisch jeder Form mithilfe einer GDI-Funktion (Graphics Device Interface) zu zeichnen. Dies schließt das Innere von Rechtecke, Ellipsen, Polygonen und Pfaden ein. Abhängig von den Anforderungen Ihrer Anwendung können Sie einen Volltonpinsel mit einer angegebenen Farbe, einen Stockpinsel, einen Schraffierungspinsel oder einen Musterpinsel verwenden.

Dieser Abschnitt enthält Codebeispiele, die die Erstellung eines benutzerdefinierten Pinseldialogfelds veranschaulichen. Das Dialogfeld enthält ein Raster, das die Bitmap darstellt, die das System als Pinsel verwendet. Ein Benutzer kann dieses Raster verwenden, um eine Musterpinselbitmap zu erstellen und dann das benutzerdefinierte Muster durch Klicken auf die **Schaltfläche Testmuster** anzeigen.

Die folgende Abbildung zeigt ein Muster, das mithilfe des Dialogfelds **Benutzerdefinierter Pinsel** erstellt wurde.

![Screenshot des Dialogfelds "Benutzerdefinierter Pinsel"](images/custbrush.png)

Um ein Dialogfeld anzuzeigen, müssen Sie zunächst eine Dialogfeldvorlage erstellen. Die folgende Dialogfeldvorlage definiert das **Dialogfeld Benutzerdefinierter Pinsel.**


```C++
CustBrush DIALOG 6, 18, 160, 118 
STYLE WS_DLGFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Custom Brush" 
FONT 8, "MS Sans Serif" 
BEGIN 
    CONTROL         "", IDD_GRID, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 3, 2, 83, 79 
    CONTROL         "", IDD_RECT, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 96, 11, 57, 28 
    PUSHBUTTON      "Test Pattern", IDD_PAINTRECT, 96, 47, 57, 14 
    PUSHBUTTON      "OK", IDD_OK, 29, 98, 40, 14 
    PUSHBUTTON      "Cancel", IDD_CANCEL, 92, 98, 40, 14 
END 
```



Das **Dialogfeld Benutzerdefinierter** Pinsel enthält fünf Steuerelemente: ein Bitmaprasterfenster, ein Fenster zum Anzeigen von Mustern und drei Schaltflächen mit der Bezeichnung **Testmuster**, **OK** und **Abbrechen**. Mit **der Pushschaltfläche** Testmuster kann der Benutzer das Muster anzeigen. Die Dialogfeldvorlage gibt die Gesamtdimensionen des Dialogfeldfensters an, weist jedem Steuerelement einen Wert zu, gibt die Position jedes Steuerelements an usw. Weitere Informationen finden Sie unter [Dialogfelder](../dlgbox/dialog-boxes.md).

Die Steuerelementwerte in der Dialogfeldvorlage sind Konstanten, die wie folgt in der Headerdatei der Anwendung definiert wurden.


```C++
#define IDD_GRID      120 
#define IDD_RECT      121 
#define IDD_PAINTRECT 122 
#define IDD_OK        123 
#define IDD_CANCEL    124 
```



Nachdem Sie eine Dialogfeldvorlage erstellt und in die Ressourcendefinitionsdatei der Anwendung einfügen, müssen Sie eine Dialogprozedur schreiben. Diese Prozedur verarbeitet Nachrichten, die das System an das Dialogfeld sendet. Der folgende Auszug aus dem Quellcode einer Anwendung zeigt die Dialogfeldprozedur für das Dialogfeld Benutzerdefinierter **Pinsel** und die beiden anwendungsdefinierten Funktionen, die es aufruft.


```C++
BOOL CALLBACK BrushDlgProc( HWND hdlg, UINT message, LONG wParam, 
                            LONG lParam) 
{ 
    static HWND hwndGrid;       // grid-window control  
    static HWND hwndBrush;      // pattern-brush control  
    static RECT rctGrid;        // grid-window rectangle  
    static RECT rctBrush;       // pattern-brush rectangle  
    static UINT bBrushBits[8];  // bitmap bits  
    static RECT rect[64];       // grid-cell array  
    static HBITMAP hbm;         // bitmap handle  
    HBRUSH hbrush;              // current brush  
    HBRUSH hbrushOld;           // default brush  
    HRGN hrgnCell;              // test-region handle  
    HDC hdc;                    // device context (DC) handle  
    int x, y, deltaX, deltaY;   // drawing coordinates  
    POINTS ptlHit;              // mouse coordinates  
    int i;                      // count variable  
 
    switch (message) 
        { 
        case WM_INITDIALOG: 
 
            // Retrieve a window handle for the grid-window and  
            // pattern-brush controls.  
 
            hwndGrid = GetDlgItem(hdlg, IDD_GRID); 
            hwndBrush = GetDlgItem(hdlg, IDD_RECT); 
 
            // Initialize the array of bits that defines the  
            // custom brush pattern with the value 1 to produce a  
            // solid white brush.  

            for (i=0; i<8; i++) 
                bBrushBits[i] = 0xFF; 
 
            // Retrieve dimensions for the grid-window and pattern- 
            // brush controls.  
 
            GetClientRect(hwndGrid, &rctGrid); 
            GetClientRect(hwndBrush, &rctBrush); 
 
            // Determine the width and height of a single cell.  
 
            deltaX = (rctGrid.right - rctGrid.left)/8; 
            deltaY = (rctGrid.bottom - rctGrid.top)/8; 
 
            // Initialize the array of cell rectangles.  
 
            for (y=rctGrid.top, i=0; y < rctGrid.bottom; y += deltaY)
            { 
                for(x=rctGrid.left; x < (rctGrid.right - 8) && i < 64; 
                        x += deltaX, i++) 
                { 
                    rect[i].left = x; rect[i].top = y; 
                    rect[i].right = x + deltaX; 
                    rect[i].bottom = y + deltaY; 
                } 
            } 
            return FALSE; 
 
 
        case WM_PAINT: 

            // Draw the grid.  
 
            hdc = GetDC(hwndGrid); 
 
            for (i=rctGrid.left; i<rctGrid.right; 
                 i+=(rctGrid.right - rctGrid.left)/8)
            { 
                 MoveToEx(hdc, i, rctGrid.top, NULL); 
                 LineTo(hdc, i, rctGrid.bottom); 
            } 
            for (i=rctGrid.top; i<rctGrid.bottom; 
                 i+=(rctGrid.bottom - rctGrid.top)/8)
            { 
                 MoveToEx(hdc, rctGrid.left, i, NULL); 
                 LineTo(hdc, rctGrid.right, i); 
            } 
            ReleaseDC(hwndGrid, hdc); 
            return FALSE; 
 
 
        case WM_LBUTTONDOWN: 
 
            // Store the mouse coordinates in a POINT structure.  
 
            ptlHit = MAKEPOINTS((POINTS FAR *)lParam); 
 
            // Create a rectangular region with dimensions and  
            // coordinates that correspond to those of the grid  
            // window.  
 
            hrgnCell = CreateRectRgn(rctGrid.left, rctGrid.top, 
                        rctGrid.right, rctGrid.bottom); 
 
            // Retrieve a window DC for the grid window.  
 
            hdc = GetDC(hwndGrid); 
 
            // Select the region into the DC.  
 
            SelectObject(hdc, hrgnCell); 
 
            // Test for a button click in the grid-window rectangle.  
 
            if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
            { 
                // A button click occurred in the grid-window  
                // rectangle; isolate the cell in which it occurred.  
 
                for(i=0; i<64; i++)
                { 
                    DeleteObject(hrgnCell); 
 
                    hrgnCell = CreateRectRgn(rect[i].left,  
                               rect[i].top, 
                               rect[i].right, rect[i].bottom); 
 
                    if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
                    { 
                        InvertRgn(hdc, hrgnCell); 
 
                        // Set the appropriate brush bits.  
 
                         if (i % 8 == 0) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x80; 
                         else if (i % 8 == 1) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x40; 
                         else if (i % 8 == 2) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x20; 
                         else if (i % 8 == 3) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x10; 
                         else if (i % 8 == 4) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x08; 
                         else if (i % 8 == 5) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x04; 
                         else if (i % 8 == 6) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x02; 
                         else if (i % 8 == 7) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x01; 
 
                      // Exit the "for" loop after the bit is set.  
 
                         break; 
                    } // end if  
 
                } // end for  
 
            } // end if  
 
            // Release the DC for the control.  
 
            ReleaseDC(hwndGrid, hdc); 
            return TRUE; 
 
 
        case WM_COMMAND: 
            switch (wParam)
            { 
               case IDD_PAINTRECT: 
 
                    hdc = GetDC(hwndBrush); 
 
                    // Create a monochrome bitmap.  
 
                    hbm = CreateBitmap(8, 8, 1, 1, 
                          (LPBYTE)bBrushBits); 
 
                    // Select the custom brush into the DC.  
 
                    hbrush = CreatePatternBrush(hbm); 
 
                    hbrushOld = SelectObject(hdc, hbrush); 
 
                    // Use the custom brush to fill the rectangle.  
 
                    Rectangle(hdc, rctBrush.left, rctBrush.top, 
                              rctBrush.right, rctBrush.bottom); 
 
                    // Clean up memory.  
                    SelectObject(hdc, hbrushOld); 
                    DeleteObject(hbrush); 
                    DeleteObject(hbm); 
 
                    ReleaseDC(hwndBrush, hdc); 
                    return TRUE; 
 
                case IDD_OK: 
 
                case IDD_CANCEL: 
                    EndDialog(hdlg, TRUE); 
                    return TRUE; 
 
            } // end switch  
            break; 
        default: 
            return FALSE; 
        } 
} 
 
 
int GetStrLngth(LPTSTR cArray) 
{ 
    int i = 0; 
 
    while (cArray[i++] != 0); 
    return i-1; 
 
} 
 
DWORD RetrieveWidth(LPTSTR cArray, int iLength) 
{ 
    int i, iTmp; 
    double dVal, dCount; 
 
    dVal = 0.0; 
    dCount = (double)(iLength-1); 
    for (i=0; i<iLength; i++)
    { 
        iTmp = cArray[i] - 0x30; 
        dVal = dVal + (((double)iTmp) * pow(10.0, dCount--)); 
    } 
 
    return (DWORD)dVal; 
} 
```



Die Dialogfeldprozedur für das **Dialogfeld Benutzerdefinierter Pinsel** verarbeitet vier Meldungen, wie in der folgenden Tabelle beschrieben.



| `Message`                                          | Aktion                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)   | Ruft ein Fensterhand handle und Dimensionen für die Rasterfenster- und Musterpinsel-Steuerelemente ab, berechnet die Dimensionen einer einzelnen Zelle im Rasterfenster-Steuerelement und initialisiert ein Array von Rasterzellenkoordinaten.                                                                                           |
| [**WM \_ PAINT**](wm-paint.md)                    | Zeichnet das Rastermuster im Rasterfenster-Steuerelement.                                                                                                                                                                                                                                                         |
| [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) | Bestimmt, ob sich der Cursor innerhalb des Rasterfenster-Steuerelements befindet, wenn der Benutzer die linke Maustaste drückt. Wenn dies der Ansicht ist, wird die entsprechende Rasterzelle von der Dialogfeldprozedur invertiert, und der Zustand dieser Zelle wird in einem Array von Bits erfasst, das zum Erstellen der Bitmap für den benutzerdefinierten Pinsel verwendet wird.              |
| [**\_WM-BEFEHL**](../menurc/wm-command.md)         | Verarbeitet Eingaben für die drei Steuerelemente der Schaltfläche "Push". Wenn der Benutzer auf die Schaltfläche **Testmuster** klickt, zeichnet die Dialogfeldprozedur das Testmuster-Steuerelement mit dem neuen benutzerdefinierten Pinselmuster. Wenn der Benutzer auf die Schaltfläche **OK oder** **Abbrechen** klickt, führt die Dialogfeldprozedur aktionen entsprechend aus. |



 

Weitere Informationen zur Nachrichten- und Nachrichtenverarbeitung finden Sie unter [Nachrichten und Nachrichtenwarteschlangen.](../winmsg/messages-and-message-queues.md)

Nachdem Sie die Dialogfeldprozedur geschrieben haben, schließen Sie die Funktionsdefinition für die Prozedur in die Headerdatei der Anwendung ein, und rufen Sie dann die Dialogfeldprozedur an der entsprechenden Stelle in der Anwendung auf.

Der folgende Auszug aus der Headerdatei der Anwendung zeigt die Funktionsdefinition für die Dialogfeldprozedur und die beiden funktionen, die sie aufruft.


```C++
BOOL CALLBACK BrushDlgProc(HWND, UINT, WPARAM, LPARAM); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveWidth(LPTSTR, int); 
```



Schließlich zeigt der folgende Code, wie die Dialogfeldprozedur aus der Quellcodedatei der Anwendung aufgerufen wird.


```C++
    DialogBox((HANDLE)GetModuleHandle(NULL), 
        (LPTSTR)"CustBrush", 
        hWnd, 
        (DLGPROC) BrushDlgProc); 
```



Dieser Aufruf erfolgt in der Regel als Reaktion auf den Benutzer, der im Menü der Anwendung eine Option auswählt.

 

 
