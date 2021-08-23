---
description: In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben ausgeführt werden, die Fenstereigenschaften zugeordnet sind.
ms.assetid: cdf196ec-300c-4c7b-8a4f-68088c4a2507
title: Verwenden von Fenstereigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fcb4cb0346554ee2df5c1b2fc92df7675cd61d11799b891156b13f26fb213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028268"
---
# <a name="using-window-properties"></a>Verwenden von Fenstereigenschaften

In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben ausgeführt werden, die Fenstereigenschaften zugeordnet sind.

-   [Hinzufügen einer Fenstereigenschaft](#adding-a-window-property)
-   [Abrufen einer Fenstereigenschaft](#retrieving-a-window-property)
-   [Auflisten von Fenstereigenschaften für ein bestimmtes Fenster](#listing-window-properties-for-a-given-window)
-   [Löschen einer Fenstereigenschaft](#deleting-a-window-property)

## <a name="adding-a-window-property"></a>Hinzufügen einer Fenstereigenschaft

Im folgenden Beispiel werden ein Symbol und dann ein Cursor geladen und Arbeitsspeicher für einen Puffer belegt. Im Beispiel wird dann die [**SetProp-Funktion**](/windows/win32/api/winuser/nf-winuser-setpropa) verwendet, um die resultierenden Symbol-, Cursor- und Arbeitsspeicherhandles als Fenstereigenschaften für das Fenster zuzuweisen, das durch die anwendungsdefinierte Variable hwndSubclass identifiziert wird. Die Eigenschaften werden durch die Zeichenfolgen PROP \_ ICON, PROP \_ CURSOR und PROP \_ BUFFER identifiziert.


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



## <a name="retrieving-a-window-property"></a>Abrufen einer Fenstereigenschaft

Ein Fenster kann Handles für seine Fenstereigenschaftsdaten erstellen und die Daten für beliebige Zwecke verwenden. Im folgenden Beispiel wird [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) verwendet, um Handles für die Fenstereigenschaften abzurufen, die durch PROP ICON, PROP CURSOR und PROP BUFFER identifiziert \_ \_ \_ werden. Im Beispiel werden dann der Inhalt des neu abgerufenen Speicherpuffers, des Cursors und des Symbols im Clientbereich des Fensters angezeigt.


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



## <a name="listing-window-properties-for-a-given-window"></a>Auflisten von Fenstereigenschaften für ein bestimmtes Fenster

Im folgenden Beispiel listet die [**EnumPropsEx-Funktion**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) die Zeichenfolgenbezeichner der Fenstereigenschaften für das Fenster auf, das durch die anwendungsdefinierte Variable hwndSubclass identifiziert wird. Diese Funktion verwendet die anwendungsdefinierte Rückruffunktion WinPropProc, um die Zeichenfolgen im Clientbereich des Fensters anzuzeigen.


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



## <a name="deleting-a-window-property"></a>Löschen einer Fenstereigenschaft

Wenn ein Fenster zerstört wird, muss es alle von ihm festgelegten Fenstereigenschaften zerstören. Im folgenden Beispiel werden die [**EnumPropsEx-Funktion**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) und die anwendungsdefinierte Rückruffunktion DelPropProc verwendet, um die Eigenschaften zu zerstören, die dem von der anwendungsdefinierten hwndSubclass-Variablen identifizierten Fenster zugeordnet sind. Die Rückruffunktion, die die [**RemoveProp-Funktion**](/windows/win32/api/winuser/nf-winuser-removepropa) verwendet, wird ebenfalls angezeigt.


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



 

 
