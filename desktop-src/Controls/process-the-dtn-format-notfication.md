---
title: Verarbeiten der DTN_FORMAT Benachrichtigung
description: In diesem Thema wird veranschaulicht, wie Sie eine Formatbenachrichtigung verarbeiten, die vom DTP-Steuerelement (Date and Time Picker) gesendet wird.
ms.assetid: 7B559846-FE52-4181-B25D-888BE90EB038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070d1234dbd9d09159335539309deec86e2d3e1e05547d933cd18f16b9d7162d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829911"
---
# <a name="how-to-process-the-dtn_format-notification"></a>Verarbeiten der \_ DTN-FORMATbenachrichtigung

In diesem Thema wird veranschaulicht, wie Sie eine Formatbenachrichtigung verarbeiten, die vom DTP-Steuerelement (Date and Time Picker) gesendet wird.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Ein DTP-Steuerelement sendet die [DTN \_ FORMAT-Benachrichtigung](dtn-format.md) an den Anforderungstext, der in einem Rückruffeld des Steuerelements angezeigt wird. Ihre Anwendung muss diese Benachrichtigung verarbeiten, damit das DTP-Steuerelement Informationen anzeigen kann, die nicht nativ unterstützt werden.

Das folgende C++-Codebeispiel ist eine anwendungsdefinierte Funktion (**DoFormat**), die [DTN FORMAT-Benachrichtigungscodes \_](dtn-format.md) verarbeitet, indem eine Textzeichenfolge für ein Rückruffeld zur Verfügung steht. Die Anwendung ruft die **anwendungsdefinierte GetDayNum-Funktion** auf, um die Tagnummer an fordern, die in der Rückrufzeichenfolge verwendet werden soll.


```C++
//  DoFormat processes DTN_FORMAT to provide the text for a callback
//  field in a DTP control. In this example, the callback field
//  contains a value for the day of year. The function calls the 
//  application-defined function GetDayNum (below) to retrieve
//  the correct value. StringCchPrintf truncates the formatted string if
//  the entire string will not fit into the destination buffer. 

void WINAPI DoFormat(HWND hwndDP, LPNMDATETIMEFORMAT lpDTFormat)
{
HRESULT hr = StringCchPrintf(lpDTFormat->szDisplay,
                sizeof(lpDTFormat->szDisplay)/sizeof(lpDTFormat->szDisplay[0]),
                L"%d",GetDayNum(&lpDTFormat->st));
if(SUCCEEDED(hr))
 {
   // Insert code here to handle the case when the function succeeds.      
 }
else
 {
   // Insert code here to handle the case when the function fails or the string 
   // is truncated.
 }
}
```



**Die anwendungsdefinierte GetDayNum-Funktion**

Die anwendungsdefinierte Beispielfunktion **DoFormat** ruft die folgende **anwendungsdefinierte GetDayNum-Funktion** auf, um die Tagesnummer basierend auf dem aktuellen Datum an fordern. **GetDayNum gibt** einen **INT-Wert** zurück, der den aktuellen Tag des Jahres von 0 bis 366 darstellt. Diese Funktion ruft während der Verarbeitung eine andere anwendungsdefinierte Funktion auf, **IsLeapYr.**


```C++
//  GetDayNum is an application-defined function that retrieves the 
//  correct day of year value based on the contents of a given 
//  SYSTEMTIME structure. This function calls the IsLeapYr function to 
//  check if the current year is a leap year. The function returns an 
//  integer value that represents the day of year.

int WINAPI GetDayNum(SYSTEMTIME *st)
{
    int iNormYearAccum[ ] = {31,59,90,120,151,181,
                            212,243,273,304,334,365};
    int iLeapYearAccum[ ] = {31,60,91,121,152,182,
                            213,244,274,305,335,366};
    int iDayNum;

    if(IsLeapYr(st->wYear))
        iDayNum=iLeapYearAccum[st->wMonth-2]+st->wDay;
    else
        iDayNum=iNormYearAccum[st->wMonth-2]+st->wDay;

    return (iDayNum);
}        
```



**Die anwendungsdefinierte IsLeapYr-Funktion**

Die anwendungsdefinierte **Funktion GetDayNum ruft** die **IsLeapYr-Funktion** auf, um zu bestimmen, ob das aktuelle Jahr ein Schaltjahr ist. **IsLeapYr gibt** einen **BOOL-Wert** zurück, der **TRUE ist,** wenn es sich um ein Schaltjahr handelt, andernfalls **FALSE.**


```C++
//  IsLeapYr determines if a given year value is a leap year. The
//  function returns TRUE if the current year is a leap year, and 
//  FALSE otherwise.

BOOL WINAPI IsLeapYr(int iYear)
{
    BOOL fLeapYr = FALSE;

    // If the year is evenly divisible by 4 and not by 100, but is 
    // divisible by 400, it is a leap year.
    if ((!(iYear % 4))             // each even fourth year
            && ((iYear % 100)      // not each even 100 year
            || (!(iYear % 400))))  // but each even 400 year
        fLeapYr = TRUE;

    return (fLeapYr);
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

 

 




