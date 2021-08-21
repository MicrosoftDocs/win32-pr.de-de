---
title: Verarbeiten der DTN_FORMATQUERY benachrichtigung
description: In diesem Thema wird veranschaulicht, wie eine Formatabfragebenachrichtigung verarbeitet wird, die vom DTP-Steuerelement (Date and Time Picker) gesendet wird.
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c148332c36711e68b7c3b773fdb47acef202c5fd2a67f5620319f06c7fbc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696940"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a>Verarbeiten der \_ DTN-FORMATQUERY-Benachrichtigung

In diesem Thema wird veranschaulicht, wie eine Formatabfragebenachrichtigung verarbeitet wird, die vom DTP-Steuerelement (Date and Time Picker) gesendet wird.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Ein DTP-Steuerelement sendet einen [DTN \_ FORMATQUERY-Benachrichtigungscode,](dtn-formatquery.md) um Informationen zur maximal möglichen Größe eines Rückruffelds innerhalb des Steuerelements anzufordern. Ihre Anwendung muss diese Meldung verarbeiten, um sicherzustellen, dass alle Felder ordnungsgemäß angezeigt werden.

Das folgende C++-Codebeispiel ist eine anwendungsdefinierte Funktion, die den [DTN FORMATQUERY-Benachrichtigungscode \_ ](dtn-formatquery.md) verarbeitet, indem die Breite der größtmöglichen Zeichenfolge für ein bestimmtes Rückruffeld berechnet wird.

**Sicherheitswarnung:** Die falsche Verwendung von **lstrcmp** kann die Sicherheit Ihrer Anwendung gefährden. Bevor Sie beispielsweise **lstrcmp** im folgenden Codebeispiel aufrufen, sollten Sie sicherstellen, dass die beiden Zeichenfolgen NULL-terminiert sind. Lesen Sie [Sicherheitsüberlegungen: Microsoft Windows Controls,](sec-comctls.md) bevor Sie fortfahren.



```C++
//  DoFormatQuery processes DTN_FORMATQUERY messages to ensure that the
//  DTP control displays callback fields properly.
//

void WINAPI DoFormatQuery(
 HWND hwndDP, 
 LPNMDATETIMEFORMATQUERY lpDTFQuery)
{
    HDC hdc;
    HFONT hFont, hOrigFont;

    //  Prepare the device context for GetTextExtentPoint32 call.
    hdc = GetDC(hwndDP);

    hFont = (HFONT) SendMessage(hwndDP, WM_GETFONT, 0L, 0L); 

    if(!hFont)
        hFont = (HFONT)GetStockObject(DEFAULT_GUI_FONT);

    hOrigFont = (HFONT) SelectObject(hdc, hFont);

    // Check to see if this is the callback segment desired. If so,
    // use the longest text segment to determine the maximum 
    // width of the callback field, and then place the information into 
    // the NMDATETIMEFORMATQUERY structure.
    if(!lstrcmp(L"XX",lpDTFQuery->pszFormat))
        GetTextExtentPoint32 (hdc,
                          L"366",  // widest date string
                          3,
                          &lpDTFQuery->szMax);

    // Reset the font in the device context; then release the context.
    SelectObject(hdc,hOrigFont);
    ReleaseDC(hwndDP, hdc);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Steuerelementen für die Datums- und Uhrzeitauswahl](using-date-and-time-picker.md)
</dt> <dt>

[Datums- und Uhrzeitauswahl-Steuerelementreferenz](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Datums- und Uhrzeitauswahl](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




