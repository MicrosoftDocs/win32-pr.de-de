---
title: Verarbeiten der DTN_DATETIMECHANGE Benachrichtigung
description: In diesem Thema wird veranschaulicht, wie Benachrichtigungen von Änderungen, die vom Benutzer vorgenommen wurden, an das Steuerelement für die Datums-und Zeitauswahl (DTP) verarbeitet werden.
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434c7ebbda673f76a757375e9a3d23504483d42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949261"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a><span data-ttu-id="324b1-103">Verarbeiten der Dtn \_ datetimechange-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="324b1-103">How to Process the DTN\_DATETIMECHANGE Notification</span></span>

<span data-ttu-id="324b1-104">In diesem Thema wird veranschaulicht, wie Benachrichtigungen von Änderungen, die vom Benutzer vorgenommen wurden, an das Steuerelement für die Datums-und Zeitauswahl (DTP) verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="324b1-104">This topic demonstrates how to process notification of changes, made by the user, to the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="324b1-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="324b1-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="324b1-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="324b1-106">Technologies</span></span>

-   [<span data-ttu-id="324b1-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="324b1-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="324b1-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="324b1-108">Prerequisites</span></span>

-   <span data-ttu-id="324b1-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="324b1-109">C/C++</span></span>
-   <span data-ttu-id="324b1-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="324b1-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="324b1-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="324b1-111">Instructions</span></span>


<span data-ttu-id="324b1-112">Ein DTP-Steuerelement sendet den [Dtn \_ datetimechange](dtn-datetimechange.md) -Benachrichtigungs Code, wenn eine Änderung auftritt.</span><span class="sxs-lookup"><span data-stu-id="324b1-112">A DTP control sends the [DTN\_DATETIMECHANGE](dtn-datetimechange.md) notification code whenever a change occurs.</span></span> <span data-ttu-id="324b1-113">Diese Benachrichtigung wird z. b. generiert, wenn der Benutzer eines der Felder im-Steuerelement ändert oder wenn das Steuerelement auf den [**DTS \_ shownone**](date-and-time-picker-control-styles.md) -Stil festgelegt ist, wenn der Benutzer den Zustand des Kontrollkästchens des Steuer Elements ändert.</span><span class="sxs-lookup"><span data-stu-id="324b1-113">For example, this notification will be generated when the user changes one of the fields in the control or, in the case where the control is set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style, when the user changes the state of the control's check box.</span></span>

<span data-ttu-id="324b1-114">Die Anwendung muss Code enthalten, um Dtn \_ datetimechange-Nachrichten zu verarbeiten, die vom DTP-Steuerelement gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="324b1-114">Your application must include code to process DTN\_DATETIMECHANGE messages that are sent by the DTP control.</span></span>

<span data-ttu-id="324b1-115">Das folgende C++-Codebeispiel ist eine Anwendungs definierte Funktion, die den Zustand eines DTP-Steuer Elements angibt, das auf den **DTS \_ shownone** -Stil festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="324b1-115">The following C++ code example is an application-defined function designed to indicate the state of a DTP control that is set to the **DTS\_SHOWNONE** style.</span></span>



```C++
void WINAPI DoDateTimeChange(LPNMDATETIMECHANGE lpChange)
{
    // If the user has unchecked the DTP's check box, change the
    // text in a static control to show the appropriate message.
    //
    // g_hwndDlg - a program-global address of a dialog box.

    if(lpChange->dwFlags == GDT_NONE)
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Disabled");
    else
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Active");
}
```



## <a name="related-topics"></a><span data-ttu-id="324b1-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="324b1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="324b1-117">Verwenden von Steuerelementen für Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="324b1-117">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="324b1-118">Steuerelement Verweis für Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="324b1-118">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="324b1-119">Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="324b1-119">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




