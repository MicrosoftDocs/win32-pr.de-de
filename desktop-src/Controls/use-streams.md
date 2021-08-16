---
title: Verwenden von Streams
description: Sie können Datenströme verwenden, um Daten in ein oder aus einem Rich-Edit-Steuerelement zu übertragen. Ein Stream wird durch eine EDITSTREAM-Struktur definiert, die einen Puffer und eine anwendungsdefinierte Rückruffunktion angibt.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae620d123ad983cd150bf78d27d99de137ec61eea8c5a32c9fcc9698cb262a63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828622"
---
# <a name="how-to-use-streams"></a>Verwenden von Streams

Sie können Datenströme verwenden, um Daten in ein oder aus einem Rich-Edit-Steuerelement zu übertragen. Ein Stream wird durch eine [**EDITSTREAM-Struktur**](/windows/desktop/api/Richedit/ns-richedit-editstream) definiert, die einen Puffer und eine anwendungsdefinierte Rückruffunktion angibt.

Verwenden Sie die EM STREAMIN-Nachricht, um Daten in ein umfangreiches Bearbeitungssteuersteuersystem einlesen zu können (d. h. in die [**\_ Daten streamen).**](em-streamin.md) Das -Steuerelement ruft wiederholt die Rückruffunktion der Anwendung auf, die jedes Mal einen Teil der Daten in den Puffer überträgt.

Sie können die [**EM \_ STREAMOUT-Nachricht**](em-streamout.md) verwenden, um den Inhalt eines Rich-Edit-Steuerelements (d. h. das Streamen der Daten) zu speichern. Das Steuerelement schreibt wiederholt in den Puffer und ruft dann die Rückruffunktion der Anwendung auf. Für jeden Aufruf speichert die Rückruffunktion den Inhalt des Puffers.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="use-a-stream"></a>Verwenden eines Streams

Das folgende Codebeispiel zeigt, wie Sie eine RTF-Datei in ein Rich-Edit-Steuerelement lesen. Das Dateihandling wird über den **dwCookie-Member** der [**EDITSTREAM-Struktur**](/windows/desktop/api/Richedit/ns-richedit-editstream) an die Rückruffunktion übergeben.


```C++
DWORD CALLBACK EditStreamCallback(DWORD_PTR dwCookie, 
                                  LPBYTE lpBuff,
                                  LONG cb, 
                                  PLONG pcb)
{
    HANDLE hFile = (HANDLE)dwCookie;
    
    if (ReadFile(hFile, lpBuff, cb, (DWORD *)pcb, NULL)) 
    {
        return 0;
    }
    
    return -1;
}

BOOL FillRichEditFromFile(HWND hwnd, LPCTSTR pszFile)
{
    BOOL fSuccess = FALSE;
    
    HANDLE hFile = CreateFile(pszFile, GENERIC_READ, 
                              FILE_SHARE_READ, 0, OPEN_EXISTING,
                              FILE_FLAG_SEQUENTIAL_SCAN, NULL);
        
    if (hFile != INVALID_HANDLE_VALUE) 
    {
        EDITSTREAM es = { 0 };
        
        es.pfnCallback = EditStreamCallback;
        es.dwCookie    = (DWORD_PTR)hFile;
        
        if (SendMessage(hwnd, EM_STREAMIN, SF_RTF, (LPARAM)&es) && es.dwError == 0) 
        {
                fSuccess = TRUE;
        }
        
        CloseHandle(hFile);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




