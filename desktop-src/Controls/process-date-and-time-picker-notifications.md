---
title: Verarbeiten von Datums- und Uhrzeitauswahlbenachrichtigungen
description: In diesem Abschnitt wird veranschaulicht, wie Sie Datums- und Uhrzeitauswahlbenachrichtigungen verarbeiten.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa1214ebd671b4ae222990bde4b44586e6d7b11
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424180"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a><span data-ttu-id="3c821-103">Verarbeiten von Datums- und Uhrzeitauswahlbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="3c821-103">How to Process Date and Time Picker Notifications</span></span>

<span data-ttu-id="3c821-104">In diesem Abschnitt wird veranschaulicht, wie Sie Datums- und Uhrzeitauswahlbenachrichtigungen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3c821-104">This section demonstrates how to process date and time picker notifications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3c821-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="3c821-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3c821-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="3c821-106">Technologies</span></span>

-   [<span data-ttu-id="3c821-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3c821-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3c821-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3c821-108">Prerequisites</span></span>

-   <span data-ttu-id="3c821-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="3c821-109">C/C++</span></span>
-   <span data-ttu-id="3c821-110">Windows Benutzeroberfläche Programmierung</span><span class="sxs-lookup"><span data-stu-id="3c821-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3c821-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="3c821-111">Instructions</span></span>


<span data-ttu-id="3c821-112">Ein DTP-Steuerelement (Datums- und Uhrzeitauswahl) sendet Benachrichtigungsmeldungen an das übergeordnete Fenster, wenn Ereignisse, die normalerweise durch Eingabe des Benutzers ausgelöst werden, im Steuerelement auftreten.</span><span class="sxs-lookup"><span data-stu-id="3c821-112">A date and time picker (DTP) control sends notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="3c821-113">Ihre Anwendung muss Code enthalten, um den Typ der Benachrichtigungsnachricht zu bestimmen und entsprechend zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="3c821-113">Your application must include code to determine the type of notification message and respond appropriately.</span></span>

<span data-ttu-id="3c821-114">Wenn Sie Rückruffelder mit den DTP-Steuerelementen in Ihrer Anwendung verwenden möchten, müssen Sie darauf vorbereitet sein, DIE Benachrichtigungscodes [DTN \_ FORMATQUERY,](dtn-formatquery.md) [DTN \_ FORMAT](dtn-format.md)und [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3c821-114">If you plan to use callback fields with the DTP controls in your application, you must be prepared to handle [DTN\_FORMATQUERY](dtn-formatquery.md), [DTN\_FORMAT](dtn-format.md), and [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification codes.</span></span> <span data-ttu-id="3c821-115">Weitere Informationen zu Rückruffeldern finden Sie unter [Rückruffelder.](date-and-time-picker-controls.md)</span><span class="sxs-lookup"><span data-stu-id="3c821-115">For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).</span></span>

<span data-ttu-id="3c821-116">Im folgenden C++-Codebeispiel wird die von einem DTP-Steuerelement gesendete Benachrichtigungsnachricht identifiziert und die entsprechende anwendungsdefinierte Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="3c821-116">The following C++ code example identifies the notification message sent by a DTP control and calls the appropriate application-defined function.</span></span> <span data-ttu-id="3c821-117">In den folgenden Themen finden Sie Codebeispiele, die veranschaulichen, wie die in diesem Beispiel angezeigten Benachrichtigungen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="3c821-117">Refer to the following topics for code examples that illustrate how to process the notifications that appear in this example.</span></span>

|   <span data-ttu-id="3c821-118">Themen</span><span class="sxs-lookup"><span data-stu-id="3c821-118">Topics</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c821-119">Verarbeiten der \_ DTN-DATETIMECHANGE-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="3c821-119">How to Process the DTN\_DATETIMECHANGE Notification</span></span>](process-the-dtn-datetimechange-notification.md) |
| [<span data-ttu-id="3c821-120">Verarbeiten der \_ DTN-FORMATQUERY-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="3c821-120">How to Process the DTN\_FORMATQUERY Notification</span></span>](process-the-dtn-formatquery-notification.md)       |
| [<span data-ttu-id="3c821-121">Verarbeiten der \_ DTN-FORMATbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="3c821-121">How to Process the DTN\_FORMAT Notification</span></span>](process-the-dtn-format-notfication.md)                  |
| [<span data-ttu-id="3c821-122">Verarbeiten der \_ DTN-WMKEYDOWN-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="3c821-122">How to Process the DTN\_WMKEYDOWN Notification</span></span>](process-the-dtn-wmkeydown-notification.md)           |



 



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



## <a name="related-topics"></a><span data-ttu-id="3c821-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c821-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c821-124">Datums- und Uhrzeitauswahlbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="3c821-124">Date and Time Picker Notifications</span></span>](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[<span data-ttu-id="3c821-125">Datums- und Uhrzeitauswahl-Steuerelementreferenz</span><span class="sxs-lookup"><span data-stu-id="3c821-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="3c821-126">Verwenden von Steuerelementen für die Datums- und Uhrzeitauswahl</span><span class="sxs-lookup"><span data-stu-id="3c821-126">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="3c821-127">Datums- und Uhrzeitauswahl</span><span class="sxs-lookup"><span data-stu-id="3c821-127">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




