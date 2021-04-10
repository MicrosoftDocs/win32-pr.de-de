---
title: Verwenden von Streams
description: Sie können Datenströme verwenden, um Daten in ein oder aus einem Rich-Edit-Steuerelement zu übertragen. Ein Stream wird durch eine editstream-Struktur definiert, die einen Puffer und eine Anwendungs definierte Rückruffunktion angibt.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89a9cc2a8caa157f9c65220fc5cead7564bc555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104101383"
---
# <a name="how-to-use-streams"></a>Verwenden von Streams

Sie können Datenströme verwenden, um Daten in ein oder aus einem Rich-Edit-Steuerelement zu übertragen. Ein Stream wird durch eine [**editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream) -Struktur definiert, die einen Puffer und eine Anwendungs definierte Rückruffunktion angibt.

Verwenden Sie zum Lesen von Daten in ein Rich-Edit-Steuerelement (d. h. Stream in den Daten) die [**EM- \_ StreamIn**](em-streamin.md) -Nachricht. Das-Steuerelement ruft die Rückruffunktion der Anwendung wiederholt auf, die jedes Mal einen Teil der Daten in den Puffer überträgt.

Um den Inhalt eines Rich-Edit-Steuer Elements (d. h. das Streamen der Daten) zu speichern, können Sie die [**EM- \_ StreamOut**](em-streamout.md) -Nachricht verwenden. Das-Steuerelement schreibt wiederholt in den Puffer und ruft dann die Rückruffunktion der Anwendung auf. Für jeden-Befehl speichert die Rückruffunktion den Inhalt des Puffers.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-a-stream"></a>Verwenden eines Streams

Im folgenden Codebeispiel wird gezeigt, wie eine RTF-Datei in ein Rich-Edit-Steuerelement gelesen wird. Das Datei Handle wird über den **dwCookie** -Member der [**editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream) -Struktur an die Rückruffunktion übermittelt.


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

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




