---
title: Erstellen statischer Steuerelemente
description: Das Beispiel in diesem Abschnitt veranschaulicht, wie ein animiertes statisches Steuerelement erstellt wird.
ms.assetid: D2DA38CB-360C-49EC-90BC-9AFA88C4B751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4bdb4cce808ab3f8f8133a731c7f4ef5638bb1fbf9fd45370e4304d0138d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826381"
---
# <a name="how-to-create-static-controls"></a>Erstellen statischer Steuerelemente

Das Beispiel in diesem Abschnitt veranschaulicht, wie ein animiertes statisches Steuerelement erstellt wird.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="create-a-static-control"></a>Erstellen eines statischen Steuerelements

Im folgenden Codebeispiel werden ein Timer und die [**STM \_ SETICON-Nachricht**](stm-seticon.md) verwendet, um ein statisches Symbolsteuerelement in einem Dialogfeld zu animieren.


```C++
#define MAXICONS 3 
#define HALF_SECOND 500

INT_PTR CALLBACK StaticDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam) 
{ 
    static HICON aIcons[MAXICONS]; 
    static UINT i = 0; 
    static UINT idTimer = 1; 

    switch (message) 
    { 
        case WM_INITDIALOG: 

            // Load the icon resources. g_hInst is the global instance handle.
            aIcons[i]   = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON1)); 
            aIcons[++i] = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON2)); 
            aIcons[++i] = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON3)); 
            
            // Reset the array index.
            i = 0;
 
            // Set a timer. 
            SetTimer(hDlg, idTimer, HALF_SECOND, (TIMERPROC) NULL); 
            return TRUE; 

        case WM_TIMER: 

            // Use STM_SETICON to associate a new icon with the static icon
            // control whenever a WM_TIMER message is received. 
            SendDlgItemMessage(hDlg, IDC_STATIC_ICON, STM_SETICON, 
                (WPARAM) aIcons[i], 0);                    

            // Reset the array index, if necessary.
            if (++i == MAXICONS)
                i = 0;

            return 0; 

        case WM_COMMAND: 
            if (wParam == IDOK 
                || wParam == IDCANCEL) 
            { 
                EndDialog(hDlg, TRUE); 
            } 
            return TRUE; 
 
        case WM_DESTROY: 
            KillTimer(hDlg, idTimer); 

            // Note that it is not necessary to call DestroyIcon here. LoadIcon
            // obtains a shared icon, which is valid as long as the module from 
            // which it was loaded is in memory. 
 
            return 0; 
    } 
    return FALSE; 

    UNREFERENCED_PARAMETER(lParam); 
} 
```



## <a name="remarks"></a>Hinweise

Der Bezeichner des statischen Symbolsteuerelements (IDI \_ STATIC \_ ICON) wird in einer globalen Headerdatei definiert, und die Symbole werden aus den Anwendungsressourcen geladen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden statischer Steuerelemente](using-static-controls.md)
</dt> <dt>

[Demo zu Windows allgemeinen Steuerelementen (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




