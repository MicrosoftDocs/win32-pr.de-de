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
# <a name="how-to-process-the-dtn_formatquery-notification"></a><span data-ttu-id="f0430-103">Verarbeiten der Dtn \_ formatQuery-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="f0430-103">How to Process the DTN\_FORMATQUERY Notification</span></span>

<span data-ttu-id="f0430-104">In diesem Thema wird veranschaulicht, wie eine Formatierungs Abfrage Benachrichtigung verarbeitet wird, die vom Steuerelement für die Datums-und Uhrzeit Auswahl (DTP) gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="f0430-104">This topic demonstrates how to process a Format Query notification that is sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f0430-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="f0430-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f0430-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="f0430-106">Technologies</span></span>

-   [<span data-ttu-id="f0430-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="f0430-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f0430-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="f0430-108">Prerequisites</span></span>

-   <span data-ttu-id="f0430-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="f0430-109">C/C++</span></span>
-   <span data-ttu-id="f0430-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="f0430-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f0430-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="f0430-111">Instructions</span></span>


<span data-ttu-id="f0430-112">Ein DTP-Steuerelement sendet einen [Dtn \_ formatQuery](dtn-formatquery.md) -Benachrichtigungs Code, um Informationen über die maximal mögliche Größe eines Rückruf Felds im Steuerelement anzufordern.</span><span class="sxs-lookup"><span data-stu-id="f0430-112">A DTP control sends a [DTN\_FORMATQUERY](dtn-formatquery.md) notification code to request information about the maximum possible size of a callback field within the control.</span></span> <span data-ttu-id="f0430-113">Diese Nachricht muss von Ihrer Anwendung verarbeitet werden, um sicherzustellen, dass alle Felder ordnungsgemäß angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f0430-113">Your application must handle this message to ensure that all fields are displayed properly.</span></span>

<span data-ttu-id="f0430-114">Das folgende C++-Codebeispiel ist eine Anwendungs definierte Funktion, die den [Dtn \_ formatQuery](dtn-formatquery.md) -Benachrichtigungs Code verarbeitet, indem die Breite der größtmöglichen Zeichenfolge für ein bestimmtes Rückruf Feld berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="f0430-114">The following C++ code example is an application-defined function that processes the [DTN\_FORMATQUERY](dtn-formatquery.md) notification code by calculating the width of the widest possible string for a given callback field.</span></span>

<span data-ttu-id="f0430-115">**Sicherheitswarnung:** Die falsche Verwendung von **lstrincmp** kann die Sicherheit Ihrer Anwendung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="f0430-115">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="f0430-116">Bevor Sie z. b. **lstrcmp** im folgenden Codebeispiel aufrufen, sollten Sie sicherstellen, dass die beiden Zeichen folgen mit Null enden.</span><span class="sxs-lookup"><span data-stu-id="f0430-116">For example, before calling **lstrcmp** in the following code example you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="f0430-117">Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="f0430-117">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="f0430-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0430-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0430-119">Verwenden von Steuerelementen für Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="f0430-119">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="f0430-120">Steuerelement Verweis für Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="f0430-120">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f0430-121">Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="f0430-121">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




