---
description: Sie können das Dialogfeld Schriftart allgemein verwenden, um verfügbare Schriftarten anzuzeigen.
ms.assetid: 317ea311-0592-432a-87b5-58296de003aa
title: Erstellen einer logischen Schriftart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb491a1af055963053e8b0247ecaa212547a750a7bd0a35db0ae983695a2420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887470"
---
# <a name="creating-a-logical-font"></a>Erstellen einer logischen Schriftart

Sie können das Dialogfeld **Schriftart** allgemein verwenden, um verfügbare Schriftarten anzuzeigen. Das Dialogfeld **ChooseFont** wird angezeigt, nachdem eine Anwendung die Member einer [**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) initialisiert und die [**CHOOSEFONT-Funktion aufruft.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) Nachdem der Benutzer eine der verfügbaren Schriftarten ausgewählt und die Schaltfläche **OK** gedrückt hat, initialisiert die **ChooseFont-Funktion** eine [**LOGFONT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logfonta) mit den relevanten Daten. Ihre Anwendung kann dann die [**CreateFontIndirect-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta) aufrufen und basierend auf der Anforderung des Benutzers eine logische Schriftart erstellen. Im folgenden Beispiel wird veranschaulicht, wie dies erfolgt.


```C++
HFONT FAR PASCAL MyCreateFont( void ) 
{ 
    CHOOSEFONT cf; 
    LOGFONT lf; 
    HFONT hfont; 
 
    // Initialize members of the CHOOSEFONT structure.  
 
    cf.lStructSize = sizeof(CHOOSEFONT); 
    cf.hwndOwner = (HWND)NULL; 
    cf.hDC = (HDC)NULL; 
    cf.lpLogFont = &lf; 
    cf.iPointSize = 0; 
    cf.Flags = CF_SCREENFONTS; 
    cf.rgbColors = RGB(0,0,0); 
    cf.lCustData = 0L; 
    cf.lpfnHook = (LPCFHOOKPROC)NULL; 
    cf.lpTemplateName = (LPSTR)NULL; 
    cf.hInstance = (HINSTANCE) NULL; 
    cf.lpszStyle = (LPSTR)NULL; 
    cf.nFontType = SCREEN_FONTTYPE; 
    cf.nSizeMin = 0; 
    cf.nSizeMax = 0; 
 
    // Display the CHOOSEFONT common-dialog box.  
 
    ChooseFont(&cf); 
 
    // Create a logical font based on the user's  
    // selection and return a handle identifying  
    // that font.  
 
    hfont = CreateFontIndirect(cf.lpLogFont); 
    return (hfont); 
} 
```



 

 
