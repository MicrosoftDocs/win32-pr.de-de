---
title: Verarbeiten der DTN_FORMAT Benachrichtigung
description: In diesem Thema wird veranschaulicht, wie eine vom Steuerelement für die Datums-und Zeitauswahl (DTP) gesendete Format Benachrichtigung verarbeitet wird.
ms.assetid: 7B559846-FE52-4181-B25D-888BE90EB038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25271ff33ee6978ebcb0bc474492f884ed7faaa2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103858555"
---
# <a name="how-to-process-the-dtn_format-notification"></a>Verarbeiten der Dtn- \_ Format Benachrichtigung

In diesem Thema wird veranschaulicht, wie eine vom Steuerelement für die Datums-und Zeitauswahl (DTP) gesendete Format Benachrichtigung verarbeitet wird.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Ein DTP-Steuerelement sendet die [Dtn- \_ Format](dtn-format.md) Benachrichtigung an den Anforderungs Text, der in einem Rückruf Feld des Steuer Elements angezeigt wird. Diese Benachrichtigung muss von Ihrer Anwendung verarbeitet werden, damit das DTP-Steuerelement Informationen anzeigen kann, die nicht System intern unterstützt werden.

Das folgende C++-Codebeispiel ist eine Anwendungs definierte Funktion (**DoFormat**), die [Dtn- \_ Format](dtn-format.md) -Benachrichtigungs Codes verarbeitet, indem eine Text Zeichenfolge für ein Rückruf Feld bereitgestellt wird. Die Anwendung ruft die Anwendungs definierte **getdaynum** -Funktion auf, um die in der Rückruf Zeichenfolge zu verwendende Tagnummer anzufordern.


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



**Die Anwendungs definierte getdaynum-Funktion**

Die Anwendungs definierte Beispiel Funktion " **DoFormat** " Ruft die folgende, von der Anwendung definierte **getdaynum** -Funktion auf, um die Tagesnummer basierend auf dem aktuellen Datum anzufordern. **Getdaynum** gibt einen **int** -Wert zurück, der den aktuellen Tag des Jahres darstellt (von 0 bis 366). Diese Funktion ruft während der Verarbeitung eine andere Anwendungs definierte **isleapyr**-Funktion auf.


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



**Die Anwendungs definierte isleapyr-Funktion**

Die Anwendungs definierte Funktion **getdaynum** Ruft die **isleapyr** -Funktion auf, um zu bestimmen, ob das aktuelle Jahr ein Schaltjahr ist. **Isleapyr** gibt einen **booleschen** Wert zurück, der **true** ist, wenn es sich um ein Schaltjahr handelt, andernfalls **false** .


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

[Verwenden von Steuerelementen für Datums-und Zeitauswahl](using-date-and-time-picker.md)
</dt> <dt>

[Steuerelement Verweis für Datums-und Zeitauswahl](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Datums-und Zeitauswahl](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




