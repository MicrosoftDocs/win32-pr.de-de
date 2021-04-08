---
title: Verarbeiten der DTN_FORMATQUERY Benachrichtigung
description: In diesem Thema wird veranschaulicht, wie eine Formatierungs Abfrage Benachrichtigung verarbeitet wird, die vom Steuerelement für die Datums-und Uhrzeit Auswahl (DTP) gesendet wird.
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e8de1e1a80d04f9a7f9e9d0cfcda198118e67c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949252"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a>Verarbeiten der Dtn \_ formatQuery-Benachrichtigung

In diesem Thema wird veranschaulicht, wie eine Formatierungs Abfrage Benachrichtigung verarbeitet wird, die vom Steuerelement für die Datums-und Uhrzeit Auswahl (DTP) gesendet wird.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Ein DTP-Steuerelement sendet einen [Dtn \_ formatQuery](dtn-formatquery.md) -Benachrichtigungs Code, um Informationen über die maximal mögliche Größe eines Rückruf Felds im Steuerelement anzufordern. Diese Nachricht muss von Ihrer Anwendung verarbeitet werden, um sicherzustellen, dass alle Felder ordnungsgemäß angezeigt werden.

Das folgende C++-Codebeispiel ist eine Anwendungs definierte Funktion, die den [Dtn \_ formatQuery](dtn-formatquery.md) -Benachrichtigungs Code verarbeitet, indem die Breite der größtmöglichen Zeichenfolge für ein bestimmtes Rückruf Feld berechnet wird.

**Sicherheitswarnung:** Die falsche Verwendung von **lstrincmp** kann die Sicherheit Ihrer Anwendung beeinträchtigen. Bevor Sie z. b. **lstrcmp** im folgenden Codebeispiel aufrufen, sollten Sie sicherstellen, dass die beiden Zeichen folgen mit Null enden. Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.



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

[Verwenden von Steuerelementen für Datums-und Zeitauswahl](using-date-and-time-picker.md)
</dt> <dt>

[Steuerelement Verweis für Datums-und Zeitauswahl](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Datums-und Zeitauswahl](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




