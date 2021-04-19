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
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a><span data-ttu-id="5d5fe-103">Drucken des Inhalts der Rich Edit-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="5d5fe-103">How to Print the Contents of Rich Edit Controls</span></span>

<span data-ttu-id="5d5fe-104">Dieser Abschnitt enthält Informationen zum Drucken der Inhalte der Rich Edit-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-104">This section contains information about how to print the contents of rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5d5fe-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="5d5fe-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5d5fe-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="5d5fe-106">Technologies</span></span>

-   [<span data-ttu-id="5d5fe-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="5d5fe-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5d5fe-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5d5fe-108">Prerequisites</span></span>

-   <span data-ttu-id="5d5fe-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="5d5fe-109">C/C++</span></span>
-   <span data-ttu-id="5d5fe-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="5d5fe-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5d5fe-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="5d5fe-111">Instructions</span></span>

### <a name="use-print-preview"></a><span data-ttu-id="5d5fe-112">Verwenden der Seitenansicht</span><span class="sxs-lookup"><span data-stu-id="5d5fe-112">Use Print Preview</span></span>

<span data-ttu-id="5d5fe-113">Zum Formatieren von Text in einem Rich-Edit-Steuerelement, das auf einem Zielgerät angezeigt wird (in der Regel die gedruckte Seite), senden Sie die Nachricht [**EM \_ SetTargetDevice**](em-settargetdevice.md) , und übergeben Sie das Handle an einen Gerätekontext (HDC) des Zielgeräts und die gewünschte Linienbreite.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-113">To format text in a rich edit control as it will appear on a target device (usually the printed page), send the [**EM\_SETTARGETDEVICE**](em-settargetdevice.md) message, passing in the handle to a device context (HDC) of the target device and the desired line width.</span></span> <span data-ttu-id="5d5fe-114">Normalerweise erhalten Sie die Linienbreite, indem Sie [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) für den Ziel-HDC aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-114">Usually you will obtain the line width by calling [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) for the target HDC.</span></span>

### <a name="format-print-for-a-specific-device"></a><span data-ttu-id="5d5fe-115">Formatieren von Drucken für ein bestimmtes Gerät</span><span class="sxs-lookup"><span data-stu-id="5d5fe-115">Format Print for a Specific Device</span></span>

<span data-ttu-id="5d5fe-116">Um einen Teil des Inhalts eines Rich-Edit-Steuer Elements für ein bestimmtes Gerät zu formatieren, senden Sie die [**EM- \_ Format Bereichs**](em-formatrange.md) Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-116">To format part of a rich edit control's contents for a specific device, send the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span> <span data-ttu-id="5d5fe-117">Die [**FormatRange**](/windows/desktop/api/Richedit/ns-richedit-formatrange) -Struktur, die mit dieser Meldung verwendet wird, gibt den Textbereich an, der formatiert werden soll, sowie den hdc für das Zielgerät.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-117">The [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure that is used with this message specifies the range of text to format as well as the HDC for the target device.</span></span> <span data-ttu-id="5d5fe-118">Optional sendet diese Nachricht den Text auch an den Drucker.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-118">Optionally, this message also sends the text to the printer.</span></span>

### <a name="use-banding"></a><span data-ttu-id="5d5fe-119">Verwenden von Bändern</span><span class="sxs-lookup"><span data-stu-id="5d5fe-119">Use Banding</span></span>

<span data-ttu-id="5d5fe-120">Die Bandbreite ist der Prozess, mit dem eine einzelne Seite der Ausgabe mit einem oder mehreren separaten Rechtecke oder Bändern generiert wird.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-120">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="5d5fe-121">Wenn alle Bänder auf der Seite platziert werden, ergibt sich ein vollständiges Bild.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-121">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="5d5fe-122">Diese Vorgehensweise wird häufig von Raster Druckern verwendet, die nicht über genügend Arbeitsspeicher oder die Möglichkeit verfügen, eine vollständige Seite gleichzeitig zu Abbildern.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-122">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span>

<span data-ttu-id="5d5fe-123">Um die Bandbreite zu implementieren, verwenden Sie die [**EM \_ DisplayBand**](em-displayband.md) -Nachricht, um aufeinander folgende Teile des Inhalts des Rich Edit-Steuer Elements an das Gerät zu senden.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-123">To implement banding, use the [**EM\_DISPLAYBAND**](em-displayband.md) message to send successive portions of the rich edit control's content to the device.</span></span> <span data-ttu-id="5d5fe-124">Diese Meldung wird auf das Gerät gedruckt, das in einem vorherigen Befehl von [**EM \_ FormatRange**](em-formatrange.md)angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-124">This message prints to the device that was specified in a previous call to [**EM\_FORMATRANGE**](em-formatrange.md).</span></span> <span data-ttu-id="5d5fe-125">Natürlich sollte der *wParam* -Parameter der **EM \_ FormatRange** -Nachricht NULL sein, damit das Drucken nicht durch diese Nachricht initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-125">Of course, the *wParam* parameter of the **EM\_FORMATRANGE** message should be zero, so that printing is not initiated by that message.</span></span>

## <a name="printrtf-code-example"></a><span data-ttu-id="5d5fe-126">Printrtf-Code Beispiel</span><span class="sxs-lookup"><span data-stu-id="5d5fe-126">PrintRTF Code Example</span></span>

<span data-ttu-id="5d5fe-127">Im folgenden Beispielcode wird der Inhalt eines Rich-Edit-Steuer Elements auf den angegebenen Drucker gedruckt.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-127">The following example code prints the contents of a rich edit control to the specified printer.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5d5fe-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d5fe-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d5fe-129">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="5d5fe-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="5d5fe-130">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="5d5fe-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 