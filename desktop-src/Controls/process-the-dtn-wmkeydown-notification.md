---
title: Verarbeiten der DTN_WMKEYDOWN Benachrichtigung
description: In diesem Thema wird veranschaulicht, wie eine Dtn- \_ wmKeyDown-Benachrichtigung verarbeitet wird. Durch die Behandlung dieses Benachrichtigungs Codes kann der Besitzer des Steuer Elements bestimmte Antworten auf Tastatureingaben innerhalb der Rückruf Felder des Steuer Elements bereitstellen.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec97ffc5853743c357081b974d155ee0e0977d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103858562"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a><span data-ttu-id="b3176-104">Verarbeiten der Dtn- \_ wmKeyDown-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="b3176-104">How to Process the DTN\_WMKEYDOWN Notification</span></span>

<span data-ttu-id="b3176-105">In diesem Thema wird veranschaulicht, wie eine [Dtn- \_ wmKeyDown](dtn-wmkeydown.md) -Benachrichtigung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b3176-105">This topic demonstrates how to process a [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span> <span data-ttu-id="b3176-106">Durch die Behandlung dieses Benachrichtigungs Codes kann der Besitzer des Steuer Elements bestimmte Antworten auf Tastatureingaben innerhalb der Rückruf Felder des Steuer Elements bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b3176-106">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b3176-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="b3176-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b3176-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="b3176-108">Technologies</span></span>

-   [<span data-ttu-id="b3176-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b3176-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b3176-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="b3176-110">Prerequisites</span></span>

-   <span data-ttu-id="b3176-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="b3176-111">C/C++</span></span>
-   <span data-ttu-id="b3176-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="b3176-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b3176-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="b3176-113">Instructions</span></span>


<span data-ttu-id="b3176-114">Die Steuerelemente für Datums-und Zeitauswahl (DTP) senden die [Dtn- \_ wmKeyDown](dtn-wmkeydown.md) -Nachricht, um zu melden, dass der Benutzereingaben in einem Rückruf Feld eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b3176-114">Date and time picker (DTP) controls send the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) message to report that the user has typed input in a callback field.</span></span> <span data-ttu-id="b3176-115">Wenn Sie dieselben Tastatur Antworten emulieren möchten, die für Standard-DTP-Felder unterstützt werden, oder benutzerdefinierte Antworten bereitstellen, muss Ihre Anwendung Code enthalten, um diese Benachrichtigung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="b3176-115">If you want to emulate the same keyboard responses that are supported for standard DTP fields or provide custom responses, your application must include code to handle this notification.</span></span>

<span data-ttu-id="b3176-116">Das folgende C++-Codebeispiel ist eine Anwendungs definierte Funktion, die die [Dtn- \_ wmKeyDown](dtn-wmkeydown.md) -Benachrichtigung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b3176-116">The following C++ code example is an application-defined function that processes the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span>

<span data-ttu-id="b3176-117">**Sicherheitswarnung:** Die falsche Verwendung von **lstrincmp** kann die Sicherheit Ihrer Anwendung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="b3176-117">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="b3176-118">Bevor Sie z. b. **lstrcmp** im folgenden Codebeispiel aufrufen, sollten Sie sicherstellen, dass die beiden Zeichen folgen mit Null enden.</span><span class="sxs-lookup"><span data-stu-id="b3176-118">For example, before calling **lstrcmp** in the following code example, you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="b3176-119">Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="b3176-119">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="b3176-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3176-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3176-121">Verwenden von Steuerelementen für Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="b3176-121">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="b3176-122">Steuerelement Verweis für Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="b3176-122">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b3176-123">Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="b3176-123">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




