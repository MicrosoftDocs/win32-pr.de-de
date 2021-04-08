---
title: Verarbeiten von Benachrichtigungs Meldungen
description: Ein Eigenschaften Blatt sendet WM \_ -Benachrichtigungs Meldungen, um Informationen von den Seiten abzurufen und die Seiten mit Benutzeraktionen zu benachrichtigen.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724276"
---
# <a name="how-to-process-notification-messages"></a><span data-ttu-id="3c675-103">Verarbeiten von Benachrichtigungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="3c675-103">How to Process Notification Messages</span></span>

<span data-ttu-id="3c675-104">Ein Eigenschaften Blatt sendet [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldungen, um Informationen von den Seiten abzurufen und die Seiten mit Benutzeraktionen zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="3c675-104">A property sheet sends [**WM\_NOTIFY**](wm-notify.md) messages to retrieve information from the pages and to notify the pages of user actions.</span></span>

<span data-ttu-id="3c675-105">Der *LPARAM* -Parameter der Nachricht ist die Adresse einer [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die das Handle für das Eigenschaften Blatt-Dialogfeld, das Handle für das Dialogfeld der Seite und einen Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="3c675-105">The *lParam* parameter of the message is the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, which contains the handle to the property sheet dialog box, the handle to the page dialog box, and a notification code.</span></span> <span data-ttu-id="3c675-106">Die Seite muss auf einige Benachrichtigungs Meldungen reagieren, indem der DWL- \_ msgresult-Wert der Seite auf " **true** " oder " **false**" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3c675-106">The page must respond to some notification messages by setting the DWL\_MSGRESULT value of the page to either **TRUE** or **FALSE**.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3c675-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="3c675-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3c675-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="3c675-108">Technologies</span></span>

-   [<span data-ttu-id="3c675-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3c675-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3c675-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3c675-110">Prerequisites</span></span>

-   <span data-ttu-id="3c675-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="3c675-111">C/C++</span></span>
-   <span data-ttu-id="3c675-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="3c675-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3c675-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="3c675-113">Instructions</span></span>

### <a name="process-notification-messages"></a><span data-ttu-id="3c675-114">Verarbeiten von Benachrichtigungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="3c675-114">Process Notification Messages</span></span>

<span data-ttu-id="3c675-115">Das folgende Beispiel ist ein Code Fragment aus der Dialogfeld Prozedur für eine Seite.</span><span class="sxs-lookup"><span data-stu-id="3c675-115">The following example is a code fragment from the dialog box procedure for a page.</span></span> <span data-ttu-id="3c675-116">Es zeigt, wie der [PSN- \_ Hilfe](psn-help.md) -Benachrichtigungs Code verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="3c675-116">It shows how to process the [PSN\_HELP](psn-help.md) notification code.</span></span>


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a><span data-ttu-id="3c675-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c675-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c675-118">Verwenden von Eigenschaften Blättern</span><span class="sxs-lookup"><span data-stu-id="3c675-118">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

<span data-ttu-id="3c675-119">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="3c675-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




