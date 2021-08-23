---
title: Drucken des Inhalts von Rich Edit-Steuerelementen
description: Dieser Abschnitt enthält Informationen zum Drucken des Inhalts von Rich-Edit-Steuerelementen.
ms.assetid: d61e2e11-d848-43fc-9622-b3b2032bda48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00c7a7287fc86e47e085cfacd7757a7e24b4a91a3a513e75dc4610b51606b36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575550"
---
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a>Drucken des Inhalts von Rich Edit-Steuerelementen

Dieser Abschnitt enthält Informationen zum Drucken des Inhalts von Rich-Edit-Steuerelementen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="use-print-preview"></a>Verwenden der Seitenansicht

Um Text in einem Rich-Edit-Steuerelement so zu formatieren, wie er auf einem Zielgerät (normalerweise auf der gedruckten Seite) angezeigt wird, senden Sie die [**EM \_ SETTARGETDEVICE-Nachricht,**](em-settargetdevice.md) und übergeben Sie das Handle an einen Gerätekontext (HDC) des Zielgeräts und die gewünschte Linienbreite. In der Regel erhalten Sie die Linienbreite, indem [**Sie GetDeviceCaps für**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) das HDC-Ziel aufrufen.

### <a name="format-print-for-a-specific-device"></a>Formatdruck für ein bestimmtes Gerät

Um einen Teil des Inhalts eines Rich-Edit-Steuerelements für ein bestimmtes Gerät zu formatieren, senden Sie die [**EM \_ FORMATRANGE-Nachricht.**](em-formatrange.md) Die [**FORMATRANGE-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-formatrange) die mit dieser Meldung verwendet wird, gibt den zu formatierten Textbereich sowie den HDC für das Zielgerät an. Optional sendet diese Nachricht auch den Text an den Drucker.

### <a name="use-banding"></a>Verwenden von Banding

Banding ist der Prozess, bei dem eine einzelne Seite der Ausgabe mit einem oder mehr separaten Rechtecke oder Bändern generiert wird. Wenn alle Bänder auf der Seite platziert werden, wird ein vollständiges Bild angezeigt. Dieser Ansatz wird häufig von Rasterdruckern verwendet, die nicht über genügend Arbeitsspeicher verfügen oder eine vollständige Seite gleichzeitig erstellen können.

Um banding zu implementieren, verwenden Sie die [**EM \_ DISPLAYBAND-Nachricht,**](em-displayband.md) um aufeinander folgende Teile des Rich Edit-Steuerelementinhalts an das Gerät zu senden. Diese Meldung wird auf dem Gerät gedruckt, das in einem vorherigen Aufruf von [**EM \_ FORMATRANGE angegeben wurde.**](em-formatrange.md) Natürlich sollte der *wParam-Parameter* der **EM \_ FORMATRANGE-Nachricht** 0 (null) sein, damit das Drucken nicht von dieser Nachricht initiiert wird.

## <a name="printrtf-code-example"></a>PrintRTF-Codebeispiel

Der folgende Beispielcode gibt den Inhalt eines Rich-Edit-Steuerelements auf dem angegebenen Drucker aus.


```C++
// hwnd is the HWND of the rich edit control.
// hdc is the HDC of the printer. This value can be obtained for the 
// default printer as follows:
//
//     PRINTDLG pd = { sizeof(pd) };
//     pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
//
//     if (PrintDlg(&pd))
//     {
//        HDC hdc = pd.hDC;
//        ...
//     }

BOOL PrintRTF(HWND hwnd, HDC hdc)
{
    DOCINFO di = { sizeof(di) };
    
    if (!StartDoc(hdc, &di))
    {
        return FALSE;
    }

    int cxPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETX);
    int cyPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETY);
    
    int cxPhys = GetDeviceCaps(hdc, PHYSICALWIDTH);
    int cyPhys = GetDeviceCaps(hdc, PHYSICALHEIGHT);

    // Create "print preview". 
    SendMessage(hwnd, EM_SETTARGETDEVICE, (WPARAM)hdc, cxPhys/2);

    FORMATRANGE fr;

    fr.hdc       = hdc;
    fr.hdcTarget = hdc;

    // Set page rect to physical page size in twips.
    fr.rcPage.top    = 0;  
    fr.rcPage.left   = 0;  
    fr.rcPage.right  = MulDiv(cxPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSX));  
    fr.rcPage.bottom = MulDiv(cyPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSY)); 

    // Set the rendering rectangle to the pintable area of the page.
    fr.rc.left   = cxPhysOffset;
    fr.rc.right  = cxPhysOffset + cxPhys;
    fr.rc.top    = cyPhysOffset;
    fr.rc.bottom = cyPhysOffset + cyPhys;

    SendMessage(hwnd, EM_SETSEL, 0, (LPARAM)-1);          // Select the entire contents.
    SendMessage(hwnd, EM_EXGETSEL, 0, (LPARAM)&fr.chrg);  // Get the selection into a CHARRANGE.

    BOOL fSuccess = TRUE;

    // Use GDI to print successive pages.
    while (fr.chrg.cpMin < fr.chrg.cpMax && fSuccess) 
    {
        fSuccess = StartPage(hdc) > 0;
        
        if (!fSuccess) break;
        
        int cpMin = SendMessage(hwnd, EM_FORMATRANGE, TRUE, (LPARAM)&fr);
        
        if (cpMin <= fr.chrg.cpMin) 
        {
            fSuccess = FALSE;
            break;
        }
        
        fr.chrg.cpMin = cpMin;
        fSuccess = EndPage(hdc) > 0;
    }
    
    SendMessage(hwnd, EM_FORMATRANGE, FALSE, 0);
    
    if (fSuccess)
    {
        EndDoc(hdc);
    } 
    
    else 
    
    {
        AbortDoc(hdc);
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

 

 