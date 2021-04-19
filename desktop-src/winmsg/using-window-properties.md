---
description: In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben im Zusammenhang mit Fenster Eigenschaften ausgeführt werden.
ms.assetid: cdf196ec-300c-4c7b-8a4f-68088c4a2507
title: Verwenden von Fenster Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 736682eb34191a061aa9753ef9d5e8c7e366fbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349240"
---
# <a name="using-window-properties"></a>Verwenden von Fenster Eigenschaften

In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben im Zusammenhang mit Fenster Eigenschaften ausgeführt werden.

-   [Hinzufügen einer Fenster Eigenschaft](#adding-a-window-property)
-   [Abrufen einer Fenster Eigenschaft](#retrieving-a-window-property)
-   [Auflisten von Fenster Eigenschaften für ein bestimmtes Fenster](#listing-window-properties-for-a-given-window)
-   [Löschen einer Fenster Eigenschaft](#deleting-a-window-property)

## <a name="adding-a-window-property"></a>Hinzufügen einer Fenster Eigenschaft

Im folgenden Beispiel wird ein Symbol und dann ein Cursor geladen, und es wird Speicher für einen Puffer zugewiesen. Das Beispiel verwendet dann die [**setprop**](/windows/win32/api/winuser/nf-winuser-setpropa) -Funktion, um die resultierenden Symbole, Cursor und Speicher Handles als Fenster Eigenschaften für das Fenster zuzuweisen, das durch die Anwendungs definierte Variable hwndsubclass identifiziert wird. Die Eigenschaften werden durch das Zeichen folgen \_ Symbol, den Prop \_ -Cursor und den Prop- \_ Puffer identifiziert.


```
#define BUFFER 4096 
 
HINSTANCE hinst;       // handle of current instance 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIcon, hCursor; 
HGLOBAL hMem; 
char *lpMem; 
TCHAR tchPath[] = "c:\\winnt\\samples\\winprop.c";
HRESULT hResult; 
 
// Load resources. 
 
hIcon = LoadIcon(hinst, MAKEINTRESOURCE(400)); 
hCursor = LoadCursor(hinst, MAKEINTRESOURCE(220)); 
 
// Allocate and fill a memory buffer. 
 
hMem = GlobalAlloc(GPTR, BUFFER); 
lpMem = GlobalLock(hMem);
if (lpMem == NULL)
{
// TODO: write error handler
}
hResult = StringCchCopy(lpMem, STRSAFE_MAX_CCH, tchPath);
if (FAILED(hResult))
{
// TO DO: write error handler if function fails.
} 
GlobalUnlock(hMem); 
 
// Set the window properties for hwndSubclass. 
 
SetProp(hwndSubclass, "PROP_ICON", hIcon); 
SetProp(hwndSubclass, "PROP_CURSOR", hCursor); 
SetProp(hwndSubclass, "PROP_BUFFER", hMem); 
```



## <a name="retrieving-a-window-property"></a>Abrufen einer Fenster Eigenschaft

Ein Fenster kann Handles für seine Fenster Eigenschaften Daten erstellen und die Daten für jeden beliebigen Zweck verwenden. Im folgenden Beispiel wird [**getprop**](/windows/win32/api/winuser/nf-winuser-getpropa) verwendet, um Handles für die durch das Prop \_ -Symbol, den Prop \_ -Cursor und den Prop-Puffer identifizierten Fenster Eigenschaften abzurufen \_ . Im Beispiel wird dann der Inhalt des neu erhaltenen Speicherpuffers, Cursors und Symbols im Client Bereich des Fensters angezeigt.


```
#define PATHLENGTH 256 
 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIconProp, hCursProp; 
HGLOBAL hMemProp; 
char *lpFilename; 
TCHAR tchBuffer[PATHLENGTH]; 
size_t * nSize; 
HDC hdc;
HRESULT hResult; 
 
// Get the window properties, then use the data. 
 
hIconProp = (HICON) GetProp(hwndSubclass, "PROP_ICON"); 
TextOut(hdc, 10, 40, "PROP_ICON", 9); 
DrawIcon(hdc, 90, 40, hIconProp); 
 
hCursProp = (HCURSOR) GetProp(hwndSubclass, "PROP_CURSOR"); 
TextOut(hdc, 10, 85, "PROP_CURSOR", 9); 
DrawIcon(hdc, 110, 85, hCursProp); 
 
hMemProp = (HGLOBAL) GetProp(hwndSubclass, "PROP_BUFFER"); 
lpFilename = GlobalLock(hMemProp);
hResult = StringCchPrintf(tchBuffer, PATHLENGTH, 
    "Path to file:  %s", lpFilename);
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
hResult = StringCchLength(tchBuffer, PATHLENGTH, nSize)
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
TextOut(hdc, 10, 10, tchBuffer, *nSize); 
```



## <a name="listing-window-properties-for-a-given-window"></a>Auflisten von Fenster Eigenschaften für ein bestimmtes Fenster

Im folgenden Beispiel listet die [**enumpropsex**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) -Funktion die Zeichen folgen Bezeichner der Fenster Eigenschaften für das Fenster auf, das durch die Anwendungs definierte Variable hwndsubclass identifiziert wird. Diese Funktion basiert auf der Anwendungs definierten Rückruffunktion winpropproc, um die Zeichen folgen im Client Bereich des Fensters anzuzeigen.


```
EnumPropsEx(hwndSubclass, WinPropProc, NULL); 
 
// WinPropProc is an application-defined callback function 
// that lists a window property. 
 
BOOL CALLBACK WinPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    static int nProp = 1;    // property counter 
    TCHAR tchBuffer[BUFFER]; // expanded-string buffer 
    size_t * nSize;          // size of string in buffer 
    HDC hdc;                 // device-context handle
    HRESULT hResult; 
 
    hdc = GetDC(hwndSubclass); 
 
    // Display window property string in client area.
    hResult = StringCchPrintf(tchBuffer, BUFFER, "WinProp %d:  %s", nProp++, lpszString);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    }
    hResult = StringCchLength(tchBuffer, BUFFER, nSize);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    } 
    TextOut(hdc, 10, nProp * 20, tchBuffer, *nSize); 
 
    ReleaseDC(hwndSubclass, hdc); 
 
    return TRUE; 
} 
```



## <a name="deleting-a-window-property"></a>Löschen einer Fenster Eigenschaft

Wenn ein Fenster zerstört wird, muss es alle festgelegten Fenster Eigenschaften zerstören. Im folgenden Beispiel werden die [**enumpropsex**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) -Funktion und die Anwendungs definierte Rückruffunktion Delta verwendet, um die Eigenschaften zu zerstören, die dem durch die Anwendungs definierten hwndsubclass-Variablen identifizierten Fenster zugeordnet sind. Die Rückruffunktion, die die [**removeprop**](/windows/win32/api/winuser/nf-winuser-removepropa) -Funktion verwendet, wird ebenfalls angezeigt.


```
case WM_DESTROY: 
 
    EnumPropsEx(hwndSubclass, DelPropProc, NULL); 
 
    PostQuitMessage(0); 
    break; 
 
// DelPropProc is an application-defined callback function 
// that deletes a window property. 
 
BOOL CALLBACK DelPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    hData = RemoveProp(hwndSubclass, lpszString); 
//
// if appropriate, free the handle hData
//
 
    return TRUE; 
}
```



 

 
