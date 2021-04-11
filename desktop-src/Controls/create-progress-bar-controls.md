---
title: Vorgehensweise beim Verwenden von Statusanzeige-Steuerelementen
description: In diesem Thema wird erläutert, wie Sie eine Statusanzeige verwenden, um den Fortschritt eines langen Datei Verarbeitungsvorgangs anzuzeigen.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c71ff33a14f2d2af5fa8735c5197c50acaa948b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949167"
---
# <a name="how-to-use-progress-bar-controls"></a>Vorgehensweise beim Verwenden von Statusanzeige-Steuerelementen

In diesem Thema wird erläutert, wie Sie eine Statusanzeige verwenden, um den Fortschritt eines langen Datei Verarbeitungsvorgangs anzuzeigen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="create-a-progress-bar-control"></a>Erstellen eines Statusanzeige-Steuer Elements

Der folgende Beispielcode erstellt eine Statusanzeige und positioniert Sie am unteren Rand des Client Bereichs des übergeordneten Fensters. Die Höhe der Statusanzeige basiert auf der Höhe der in einer Schiebe Leiste verwendeten Pfeil Bitmap. Der Bereich basiert auf der Größe der Datei dividiert durch 2.048, d. h. der Größe jedes "Blocks" der aus der Datei gelesenen Daten. Im Beispiel wird außerdem ein Inkrement festgelegt, und die aktuelle Position der Statusanzeige wird um das Inkrement erhöht, nachdem die einzelnen Blöcke verarbeitet wurden.


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



## <a name="remarks"></a>Bemerkungen

Sie müssen sicherstellen, dass die Funktion "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " ordnungsgemäß verwendet wird, um die Sicherheit Ihrer Anwendung zu gewährleisten. Im Beispielcode sollten Sie z. b. überprüfen, ob `ReadFile` alle angeforderten Daten tatsächlich von gelesen werden.

Beachten Sie auch, [**dass der vierte Parameter von "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)–" (lpsecurity- \_ Attribute)**null**– Standard Sicherheitswerte festlegt. Wenn Sie bestimmte Sicherheitseinstellungen benötigen, müssen Sie die entsprechenden Werte in den Elementen der-Struktur festlegen. Ruft **sizeof** auf, um die korrekte Größe der **lpsecurity- \_ Attribut** Struktur festzulegen.

Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Microsoft Windows](sec-comctls.md)-Steuerelemente.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Statusanzeige-Steuerelementen](using-progress-bar-controls.md)
</dt> <dt>

[Überlegungen zur Sicherheit: Microsoft Windows-Steuerelemente](sec-comctls.md)
</dt> </dl>

 

 