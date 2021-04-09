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
# <a name="how-to-process-the-dtn_format-notification"></a><span data-ttu-id="730ce-103">Verarbeiten der Dtn- \_ Format Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="730ce-103">How to Process the DTN\_FORMAT Notification</span></span>

<span data-ttu-id="730ce-104">In diesem Thema wird veranschaulicht, wie eine vom Steuerelement für die Datums-und Zeitauswahl (DTP) gesendete Format Benachrichtigung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="730ce-104">This topic demonstrates how to process a format notification sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="730ce-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="730ce-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="730ce-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="730ce-106">Technologies</span></span>

-   [<span data-ttu-id="730ce-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="730ce-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="730ce-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="730ce-108">Prerequisites</span></span>

-   <span data-ttu-id="730ce-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="730ce-109">C/C++</span></span>
-   <span data-ttu-id="730ce-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="730ce-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="730ce-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="730ce-111">Instructions</span></span>


<span data-ttu-id="730ce-112">Ein DTP-Steuerelement sendet die [Dtn- \_ Format](dtn-format.md) Benachrichtigung an den Anforderungs Text, der in einem Rückruf Feld des Steuer Elements angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="730ce-112">A DTP control sends the [DTN\_FORMAT](dtn-format.md) notification to request text that will be displayed in a callback field of the control.</span></span> <span data-ttu-id="730ce-113">Diese Benachrichtigung muss von Ihrer Anwendung verarbeitet werden, damit das DTP-Steuerelement Informationen anzeigen kann, die nicht System intern unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="730ce-113">Your application must handle this notification to enable the DTP control to display information that it does not natively support.</span></span>

<span data-ttu-id="730ce-114">Das folgende C++-Codebeispiel ist eine Anwendungs definierte Funktion (**DoFormat**), die [Dtn- \_ Format](dtn-format.md) -Benachrichtigungs Codes verarbeitet, indem eine Text Zeichenfolge für ein Rückruf Feld bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="730ce-114">The following C++ code example is an application-defined function (**DoFormat**) that processes [DTN\_FORMAT](dtn-format.md) notification codes by providing a text string for a callback field.</span></span> <span data-ttu-id="730ce-115">Die Anwendung ruft die Anwendungs definierte **getdaynum** -Funktion auf, um die in der Rückruf Zeichenfolge zu verwendende Tagnummer anzufordern.</span><span class="sxs-lookup"><span data-stu-id="730ce-115">The application calls the **GetDayNum** application-defined function to request the day number to be used in the callback string.</span></span>


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



<span data-ttu-id="730ce-116">**Die Anwendungs definierte getdaynum-Funktion**</span><span class="sxs-lookup"><span data-stu-id="730ce-116">**The GetDayNum application-defined function**</span></span>

<span data-ttu-id="730ce-117">Die Anwendungs definierte Beispiel Funktion " **DoFormat** " Ruft die folgende, von der Anwendung definierte **getdaynum** -Funktion auf, um die Tagesnummer basierend auf dem aktuellen Datum anzufordern.</span><span class="sxs-lookup"><span data-stu-id="730ce-117">The application-defined sample function **DoFormat** calls the following **GetDayNum** application-defined function to request the day number based on the current date.</span></span> <span data-ttu-id="730ce-118">**Getdaynum** gibt einen **int** -Wert zurück, der den aktuellen Tag des Jahres darstellt (von 0 bis 366).</span><span class="sxs-lookup"><span data-stu-id="730ce-118">**GetDayNum** returns an **INT** value that represents the current day of the year, from 0 to 366.</span></span> <span data-ttu-id="730ce-119">Diese Funktion ruft während der Verarbeitung eine andere Anwendungs definierte **isleapyr**-Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="730ce-119">This function calls another application-defined function, **IsLeapYr**, during processing.</span></span>


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



<span data-ttu-id="730ce-120">**Die Anwendungs definierte isleapyr-Funktion**</span><span class="sxs-lookup"><span data-stu-id="730ce-120">**The IsLeapYr application-defined function**</span></span>

<span data-ttu-id="730ce-121">Die Anwendungs definierte Funktion **getdaynum** Ruft die **isleapyr** -Funktion auf, um zu bestimmen, ob das aktuelle Jahr ein Schaltjahr ist.</span><span class="sxs-lookup"><span data-stu-id="730ce-121">The application-defined function **GetDayNum** calls the **IsLeapYr** function to determine whether the current year is a leap year.</span></span> <span data-ttu-id="730ce-122">**Isleapyr** gibt einen **booleschen** Wert zurück, der **true** ist, wenn es sich um ein Schaltjahr handelt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="730ce-122">**IsLeapYr** returns a **BOOL** value that is **TRUE** if it is a leap year and **FALSE** otherwise.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="730ce-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="730ce-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="730ce-124">Verwenden von Steuerelementen für Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="730ce-124">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="730ce-125">Steuerelement Verweis für Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="730ce-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="730ce-126">Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="730ce-126">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




