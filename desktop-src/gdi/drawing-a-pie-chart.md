---
description: Sie können die Linien-und Kurven Funktionen zum Zeichnen eines Kreis Diagramms verwenden.
ms.assetid: 788d3bc2-1010-436c-a95f-6fe55daac88e
title: Zeichnen eines Kreis Diagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d14928c3f90c3222c2a01d6a063d46f109ad7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130793"
---
# <a name="drawing-a-pie-chart"></a>Zeichnen eines Kreis Diagramms

Sie können die Linien-und Kurven Funktionen zum Zeichnen eines Kreis Diagramms verwenden. Die primäre Funktion zum Zeichnen von Kreis Diagrammen ist die [**anglearc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) -Funktion, bei der Sie die Koordinaten der Mitte des Kreises, den Radius des Kreises, einen Start Winkel und einen Mittelpunktswinkel angeben müssen. Der folgende Screenshot zeigt ein Dialogfeld, mit dem der Benutzer diese Werte eingeben kann.

![Screenshot mit einem Dialogfeld zum Eingeben von Werten für ein Kreis Diagramm](images/pie.png)

Mit den oben gezeigten Werten wird das folgende Kreis Diagramm erzeugt.

![Screenshot des resultierenden Kreis Diagramms](images/sampleapp.png)

Die Dialogfeld Vorlage, die im Ressourcen Skript der Anwendung () gefunden wird. RC) gibt die Merkmale des vorangehenden Dialog Felds (die Höhe, die darin enthaltenen Steuerelemente und den Stil) wie folgt an.


```C++
AngleArc DIALOG 6, 18, 160, 100 
STYLE WS_DLGFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Pie Chart" 
FONT 8, "MS Sans Serif" 
BEGIN 
    EDITTEXT   IDD_X, 18, 22, 25, 12, ES_AUTOHSCROLL 
    LTEXT      "X", 102, 4, 24, 9, 8 
    EDITTEXT   IDD_Y, 18, 39, 25, 12, ES_AUTOHSCROLL 
    LTEXT      "Y", 104, 5, 42, 12, 8 
    LTEXT      "Center", 105, 19, 11, 23, 8 
    EDITTEXT   IDD_RADIUS, 103, 9, 32, 12, ES_AUTOHSCROLL 
    EDITTEXT   IDD_STARTANGLE, 103, 31, 32, 12, ES_AUTOHSCROLL 
    EDITTEXT   IDD_SWEEPANGLE, 103, 53, 32, 12, ES_AUTOHSCROLL 
    LTEXT      "Radius", 109, 73, 11, 25, 8 
    LTEXT      "Start Angle", 110, 59, 33, 42, 8 
    LTEXT      "Sweep Angle", 111, 55, 55, 43, 8 
    PUSHBUTTON "OK", IDD_OK, 9, 82, 40, 14 
    PUSHBUTTON "Cancel", IDD_CANCEL, 110, 82, 40, 14 
END 
```



Die in der Quelldatei der Anwendung gefundene Dialogfeld Prozedur ruft Daten (zentrierte Koordinaten, Bogen RADIUS und Start-und Sweep-Winkel) ab, indem Sie die folgenden Schritte ausführen:

1.  Die Anwendungs definierte clearbits-Funktion initialisiert das Array, das die Benutzereingaben an Null empfängt.
2.  Die von der Anwendung definierte getstraulngth-Funktion Ruft die Länge der vom Benutzer eingegebenen Zeichenfolge ab.
3.  Die von der Anwendung definierte "retrieveinput"-Funktion Ruft den vom Benutzer eingegebenen Wert ab.

Der folgende Beispielcode zeigt die-Dialogfeld Prozedur.


```C++
void ClearBits(LPTSTR, int); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveInput(LPTSTR, int); 

BOOL CALLBACK ArcDlgProc(HWND hdlg, UINT uMsg, WPARAM wParam, 
LPARAM lParam) 
{ 
    CHAR chInput[4];    // receives control-window input  
    int cch;            // array-size and count variable  
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
            return FALSE; 
 
        case WM_COMMAND: 
            switch (wParam)
            { 
                // If the user pressed the OK button, retrieve the  
                // data that was entered in the various AngleArc  
                // controls.  
 
                case IDD_OK: 
                    // Retrieve the x-coordinate of the arc's center.  
 
                    ClearBits(chInput, sizeof(chInput)); 
                    GetDlgItemText(hdlg, IDD_X, chInput, 
                        sizeof(chInput)); 
                    cch = GetStrLngth(chInput); 
                    nX = (int)RetrieveInput(chInput, cch); 
 
                    // Retrieve the y-coordinate of the arc's center.  
 
                    ClearBits(chInput, sizeof(chInput)); 
                    GetDlgItemText(hdlg, IDD_Y, chInput, 
                        sizeof(chInput)); 
                    cch = GetStrLngth(chInput); 
                    nY = (int)RetrieveInput(chInput, cch); 
 
                    // Retrieve the radius of the arc.  
 
                    ClearBits(chInput, sizeof(chInput)); 
                    GetDlgItemText(hdlg, IDD_RADIUS, chInput, 
                        sizeof(chInput)); 
                    cch = GetStrLngth(chInput); 
                    dwRadius = (DWORD) RetrieveInput(chInput, cch); 
 
                    // Retrieve the start angle.  
 
                    ClearBits(chInput, sizeof(chInput)); 
                    GetDlgItemText(hdlg, IDD_STARTANGLE, chInput, 
                        sizeof(chInput)); 
                    cch = GetStrLngth(chInput); 
                    xStartAngle = (float) RetrieveInput(chInput, cch); 
 
                    // Retrieve the sweep angle.  
 
                    ClearBits(chInput, sizeof(chInput)); 
                    GetDlgItemText(hdlg, IDD_SWEEPANGLE, chInput, 
                        sizeof(chInput)); 
                    cch = GetStrLngth(chInput); 
                    xSweepAngle = (float) RetrieveInput(chInput, cch); 
 
                    EndDialog(hdlg, FALSE); 
                    return TRUE; 
 
                // If user presses the CANCEL button, close the  
                // dialog box.  
 
                case IDD_CANCEL: 
                    EndDialog(hdlg, FALSE); 
                    return TRUE; 
            } // end switch (wParam)  
 
            break; 
 
        default: 
            return FALSE; 
    } // end switch (message)  
 
    UNREFERENCED_PARAMETER(lParam); 
} 
 
 
void ClearBits(LPTSTR cArray, int iLength) 
{ 
    int i; 
 
    for (i = 0; i < iLength; i++) 
        cArray[i] = 0; 
} 
 
int GetStrLngth(LPTSTR cArray) 
{ 
    int i = 0; 
 
    while (cArray[i++] != 0); 
        return i - 1; 
} 
 
DWORD RetrieveInput(LPTSTR cArray, int iLength) 
{ 
    int i, iTmp; 
    double dVal, dCount; 
 
    dVal = 0.0; 
    dCount = (double) (iLength - 1); 
 
    // Convert ASCII input to a floating-point value.  
 
    for (i = 0; i < iLength; i++) 
    { 
        iTmp = cArray[i] - 0x30; 
        dVal = dVal + (((double)iTmp) * pow(10.0, dCount--)); 
    } 
 
    return (DWORD) dVal; 
} 
```



Um jeden Abschnitt des Kreis Diagramms zu zeichnen, übergeben Sie die vom Benutzer eingegebenen Werte an die [**anglearc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) -Funktion. Um das Kreis Diagramm mit dem aktuellen Pinsel auszufüllen, Betten Sie den aufzurufenden **aufrufungsend** in eine Pfad Klammer ein. Das folgende Codebeispiel zeigt die definierte Pfad Klammer und den aufzurufenden aufzurufenden **.**


```C++
    int nX; 
    int nY; 
    DWORD dwRadius; 
    float xStartAngle; 
    float xSweepAngle; 
 
    hdc = GetDC(hwnd); 
    BeginPath(hdc); 
    SelectObject(hdc, GetStockObject(GRAY_BRUSH)); 
    MoveToEx(hdc, nX, nY, (LPPOINT) NULL); 
    AngleArc(hdc, nX, nY, dwRadius, xStartAngle, xSweepAngle); 
    LineTo(hdc, nX, nY); 
    EndPath(hdc); 
    StrokeAndFillPath(hdc); 
    ReleaseDC(hwnd, hdc); 
```



 

 



