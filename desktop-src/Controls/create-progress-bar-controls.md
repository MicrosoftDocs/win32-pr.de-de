---
title: Verwenden von Statusleisten-Steuerelementen
description: In diesem Thema wird erläutert, wie Sie mithilfe einer Statusleiste den Fortschritt eines längeren Dateiparsing-Vorgangs angeben.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e65d47d6b41422853d401a1fb2686e03e3d3f5bc378b78b7ba762b86fc7ffe30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826420"
---
# <a name="how-to-use-progress-bar-controls"></a>Verwenden von Statusleisten-Steuerelementen

In diesem Thema wird erläutert, wie Sie mithilfe einer Statusleiste den Fortschritt eines längeren Dateiparsing-Vorgangs angeben.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="create-a-progress-bar-control"></a>Erstellen eines Statusleisten-Steuerelements

Der folgende Beispielcode erstellt eine Statusleiste und positioniert sie am unteren Rand des Clientbereichs des übergeordneten Fensters. Die Höhe der Statusleiste basiert auf der Höhe der Pfeilbitmap, die in einer Bildlaufleiste verwendet wird. Der Bereich basiert auf der Größe der Datei geteilt durch 2.048. Dies ist die Größe jedes "Daten chunks", der aus der Datei gelesen wird. Das Beispiel legt auch ein Inkrement fest und erhöht die aktuelle Position der Statusleiste um das Inkrement, nachdem die einzelnen Blocke analyset wurden.


```C++
// ParseALargeFile - uses a progress bar to indicate the progress of a parsing operation.
//
// Returns TRUE if successful, or FALSE otherwise.
//
// hwndParent - parent window of the progress bar.
//
// lpszFileName - name of the file to parse. 
// 
// Global variable 
//     g_hinst - instance handle.
//

extern HINSTANCE g_hinst; 

BOOL ParseALargeFile(HWND hwndParent, LPTSTR lpszFileName) 
{ 
    RECT rcClient;  // Client area of parent window.
    int cyVScroll;  // Height of scroll bar arrow.
    HWND hwndPB;    // Handle of progress bar.
    HANDLE hFile;   // Handle of file.
    DWORD cb;       // Size of file and count of bytes read.
    LPCH pch;       // Address of data read from file.
    LPCH pchTmp;    // Temporary pointer.

    // Ensure that the common control DLL is loaded, and create a progress bar 
    // along the bottom of the client area of the parent window. 
    //
    // Base the height of the progress bar on the height of a scroll bar arrow.
    
    InitCommonControls(); 
    
    GetClientRect(hwndParent, &rcClient); 
    
    cyVScroll = GetSystemMetrics(SM_CYVSCROLL); 

    hwndPB = CreateWindowEx(0, PROGRESS_CLASS, (LPTSTR) NULL, 
                            WS_CHILD | WS_VISIBLE, rcClient.left, 
                            rcClient.bottom - cyVScroll, 
                            rcClient.right, cyVScroll, 
                            hwndParent, (HMENU) 0, g_hinst, NULL);

    // Open the file for reading, and retrieve the size of the file. 

    hFile = CreateFile(lpszFileName, GENERIC_READ, FILE_SHARE_READ, 
                       (LPSECURITY_ATTRIBUTES) NULL, OPEN_EXISTING, 
                       FILE_ATTRIBUTE_NORMAL, (HANDLE) NULL); 

    if (hFile == (HANDLE) INVALID_HANDLE_VALUE)
        return FALSE; 

    cb = GetFileSize(hFile, (LPDWORD) NULL); 

    // Set the range and increment of the progress bar. 

    SendMessage(hwndPB, PBM_SETRANGE, 0, MAKELPARAM(0, cb / 2048));
    
    SendMessage(hwndPB, PBM_SETSTEP, (WPARAM) 1, 0); 

    // Parse the file. 
    pch = (LPCH) LocalAlloc(LPTR, sizeof(char) * 2048); 
    
    pchTmp = pch; 
    
    do { 
        ReadFile(hFile, pchTmp, sizeof(char) * 2048, &cb, (LPOVERLAPPED) NULL);
        
        // TODO: Write an error handler to check that all the
        // requested data was read.
        //
        // Include here any code that parses the
        // file. 
        //  
        //  
        //  
        // Advance the current position of the progress bar by the increment.
        
        SendMessage(hwndPB, PBM_STEPIT, 0, 0); 
        
    } while (cb); 

    CloseHandle((HANDLE) hFile);
    
    DestroyWindow(hwndPB);

    return TRUE; 
}
```



## <a name="remarks"></a>Hinweise

Sie müssen sicherstellen, dass Die [**ReadFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ordnungsgemäß verwendet wird, um die Sicherheit Ihrer Anwendung sicherzustellen. Im Beispielcode sollten Sie beispielsweise überprüfen, ob tatsächlich alle `ReadFile` angeforderten Daten gelesen werden.

Beachten Sie auch, dass der vierte Parameter von [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)–(LPSECURITY \_ ATTRIBUTES)**NULL**– Standardwerte für die Sicherheit legt. Wenn Sie bestimmte Sicherheitseinstellungen benötigen, müssen Sie die entsprechenden Werte in den -Membern der -Struktur festlegen. Rufen **Sie sizeof** auf, um die richtige Größe der **LPSECURITY \_ ATTRIBUTES-Struktur** fest.

Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Microsoft Windows Controls](sec-comctls.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Statusleisten-Steuerelementen](using-progress-bar-controls.md)
</dt> <dt>

[Sicherheitsüberlegungen: Microsoft Windows Controls](sec-comctls.md)
</dt> </dl>

 

 