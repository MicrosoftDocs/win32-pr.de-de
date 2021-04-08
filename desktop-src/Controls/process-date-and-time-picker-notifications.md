---
title: Verarbeiten von Benachrichtigungen zu Datums-und Zeitauswahl
description: In diesem Abschnitt wird veranschaulicht, wie Benachrichtigungen für Datums-und Zeitauswahl verarbeitet werden.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b904c464677a81151b03e3ae89085847e4e8bdf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039873"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a><span data-ttu-id="759bf-103">Verarbeiten von Benachrichtigungen zu Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="759bf-103">How to Process Date and Time Picker Notifications</span></span>

<span data-ttu-id="759bf-104">In diesem Abschnitt wird veranschaulicht, wie Benachrichtigungen für Datums-und Zeitauswahl verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="759bf-104">This section demonstrates how to process date and time picker notifications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="759bf-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="759bf-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="759bf-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="759bf-106">Technologies</span></span>

-   [<span data-ttu-id="759bf-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="759bf-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="759bf-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="759bf-108">Prerequisites</span></span>

-   <span data-ttu-id="759bf-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="759bf-109">C/C++</span></span>
-   <span data-ttu-id="759bf-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="759bf-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="759bf-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="759bf-111">Instructions</span></span>


<span data-ttu-id="759bf-112">Ein DTP-Steuerelement (Datums-und Zeitauswahl) sendet Benachrichtigungs Meldungen an das übergeordnete Fenster, wenn Ereignisse, die normalerweise durch Eingabe des Benutzers ausgelöst werden, im-Steuerelement auftreten.</span><span class="sxs-lookup"><span data-stu-id="759bf-112">A date and time picker (DTP) control sends notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="759bf-113">Die Anwendung muss Code enthalten, um den Typ der Benachrichtigungs Meldung zu bestimmen und entsprechend zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="759bf-113">Your application must include code to determine the type of notification message and respond appropriately.</span></span>

<span data-ttu-id="759bf-114">Wenn Sie beabsichtigen, Rückruf Felder mit den DTP-Steuerelementen in der Anwendung zu verwenden, müssen Sie darauf vorbereitet sein, das [Dtn \_ formatQuery](dtn-formatquery.md)-, [Dtn- \_ Format](dtn-format.md)und [Dtn \_ wmKeyDown](dtn-wmkeydown.md) -Benachrichtigungs Codes zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="759bf-114">If you plan to use callback fields with the DTP controls in your application, you must be prepared to handle [DTN\_FORMATQUERY](dtn-formatquery.md), [DTN\_FORMAT](dtn-format.md), and [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification codes.</span></span> <span data-ttu-id="759bf-115">Weitere Informationen zu Rückruf Feldern finden Sie unter [Rückruf Felder](date-and-time-picker-controls.md).</span><span class="sxs-lookup"><span data-stu-id="759bf-115">For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).</span></span>

<span data-ttu-id="759bf-116">Im folgenden C++-Codebeispiel wird die von einem DTP-Steuerelement gesendete Benachrichtigungs Meldung identifiziert, und die entsprechende Anwendungs definierte Funktion wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="759bf-116">The following C++ code example identifies the notification message sent by a DTP control and calls the appropriate application-defined function.</span></span> <span data-ttu-id="759bf-117">In den folgenden Themen finden Sie Codebeispiele, die veranschaulichen, wie die in diesem Beispiel angezeigten Benachrichtigungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="759bf-117">Refer to the following topics for code examples that illustrate how to process the notifications that appear in this example.</span></span>

|                                                                                                        |
|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="759bf-118">Verarbeiten der Dtn \_ datetimechange-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="759bf-118">How to Process the DTN\_DATETIMECHANGE Notification</span></span>](process-the-dtn-datetimechange-notification.md) |
| [<span data-ttu-id="759bf-119">Verarbeiten der Dtn \_ formatQuery-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="759bf-119">How to Process the DTN\_FORMATQUERY Notification</span></span>](process-the-dtn-formatquery-notification.md)       |
| [<span data-ttu-id="759bf-120">Verarbeiten der Dtn- \_ Format Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="759bf-120">How to Process the DTN\_FORMAT Notification</span></span>](process-the-dtn-format-notfication.md)                  |
| [<span data-ttu-id="759bf-121">Verarbeiten der Dtn- \_ wmKeyDown-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="759bf-121">How to Process the DTN\_WMKEYDOWN Notification</span></span>](process-the-dtn-wmkeydown-notification.md)           |



 



```C++
BOOL WINAPI DoNotify(HWND hwnd, WPARAM wParam, LPARAM lParam)
{
    LPNMHDR hdr = (LPNMHDR)lParam;

    switch(hdr->code){

        case DTN_DATETIMECHANGE:{
            LPNMDATETIMECHANGE lpChange = (LPNMDATETIMECHANGE)lParam;
            DoDateTimeChange(lpChange);
        }
        break;

        case DTN_FORMATQUERY:{
            LPNMDATETIMEFORMATQUERY lpDTFQuery = (LPNMDATETIMEFORMATQUERY)lParam;

            // Process DTN_FORMATQUERY to ensure that the control
            // displays callback information properly.
            DoFormatQuery(hdr->hwndFrom, lpDTFQuery);
        }
        break;

        case DTN_FORMAT:{
            LPNMDATETIMEFORMAT lpNMFormat = (LPNMDATETIMEFORMAT) lParam;

            // Process DTN_FORMAT to supply information about callback
            // fields (fields) in the DTP control.
            DoFormat(hdr->hwndFrom, lpNMFormat);
        }
        break;

        case DTN_WMKEYDOWN:{
            LPNMDATETIMEWMKEYDOWN lpDTKeystroke = 
                            (LPNMDATETIMEWMKEYDOWN)lParam;

            // Process DTN_WMKEYDOWN to respond to a user's keystroke in
            // a callback field.
            DoWMKeydown(hdr->hwndFrom, lpDTKeystroke);
        }
        break;
    }

    // All of the above notifications require the owner to return zero.
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="759bf-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="759bf-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="759bf-123">Datums-und Zeitauswahl Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="759bf-123">Date and Time Picker Notifications</span></span>](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[<span data-ttu-id="759bf-124">Steuerelement Verweis für Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="759bf-124">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="759bf-125">Verwenden von Steuerelementen für Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="759bf-125">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="759bf-126">Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="759bf-126">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




