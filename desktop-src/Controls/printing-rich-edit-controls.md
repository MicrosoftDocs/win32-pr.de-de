---
title: Drucken des Inhalts der Rich Edit-Steuerelemente
description: Dieser Abschnitt enthält Informationen zum Drucken der Inhalte der Rich Edit-Steuerelemente.
ms.assetid: d61e2e11-d848-43fc-9622-b3b2032bda48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a304e5c09b5f8ea934c90873c3d915179295964e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106338690"
---
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a>Drucken des Inhalts der Rich Edit-Steuerelemente

Dieser Abschnitt enthält Informationen zum Drucken der Inhalte der Rich Edit-Steuerelemente.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-print-preview"></a>Verwenden der Seitenansicht

Zum Formatieren von Text in einem Rich-Edit-Steuerelement, das auf einem Zielgerät angezeigt wird (in der Regel die gedruckte Seite), senden Sie die Nachricht [**EM \_ SetTargetDevice**](em-settargetdevice.md) , und übergeben Sie das Handle an einen Gerätekontext (HDC) des Zielgeräts und die gewünschte Linienbreite. Normalerweise erhalten Sie die Linienbreite, indem Sie [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) für den Ziel-HDC aufrufen.

### <a name="format-print-for-a-specific-device"></a>Formatieren von Drucken für ein bestimmtes Gerät

Um einen Teil des Inhalts eines Rich-Edit-Steuer Elements für ein bestimmtes Gerät zu formatieren, senden Sie die [**EM- \_ Format Bereichs**](em-formatrange.md) Nachricht. Die [**FormatRange**](/windows/desktop/api/Richedit/ns-richedit-formatrange) -Struktur, die mit dieser Meldung verwendet wird, gibt den Textbereich an, der formatiert werden soll, sowie den hdc für das Zielgerät. Optional sendet diese Nachricht den Text auch an den Drucker.

### <a name="use-banding"></a>Verwenden von Bändern

Die Bandbreite ist der Prozess, mit dem eine einzelne Seite der Ausgabe mit einem oder mehreren separaten Rechtecke oder Bändern generiert wird. Wenn alle Bänder auf der Seite platziert werden, ergibt sich ein vollständiges Bild. Diese Vorgehensweise wird häufig von Raster Druckern verwendet, die nicht über genügend Arbeitsspeicher oder die Möglichkeit verfügen, eine vollständige Seite gleichzeitig zu Abbildern.

Um die Bandbreite zu implementieren, verwenden Sie die [**EM \_ DisplayBand**](em-displayband.md) -Nachricht, um aufeinander folgende Teile des Inhalts des Rich Edit-Steuer Elements an das Gerät zu senden. Diese Meldung wird auf das Gerät gedruckt, das in einem vorherigen Befehl von [**EM \_ FormatRange**](em-formatrange.md)angegeben wurde. Natürlich sollte der *wParam* -Parameter der **EM \_ FormatRange** -Nachricht NULL sein, damit das Drucken nicht durch diese Nachricht initiiert wird.

## <a name="printrtf-code-example"></a>Printrtf-Code Beispiel

Im folgenden Beispielcode wird der Inhalt eines Rich-Edit-Steuer Elements auf den angegebenen Drucker gedruckt.


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

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 