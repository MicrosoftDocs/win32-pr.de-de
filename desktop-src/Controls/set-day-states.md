---
title: Festlegen von Tages Zuständen
description: In diesem Thema wird veranschaulicht, wie Sie Informationen zum Tageszustand festlegen. Das Monatskalender-Steuerelement verwendet Tages Zustandsinformationen, um zu bestimmen, wie bestimmte Tage innerhalb des Steuer Elements gezeichnet werden.
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa1fc105c94a15e1a658218013dca00129c883c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949257"
---
# <a name="how-to-set-day-states"></a><span data-ttu-id="b5dd7-104">Festlegen von Tages Zuständen</span><span class="sxs-lookup"><span data-stu-id="b5dd7-104">How to Set Day States</span></span>

<span data-ttu-id="b5dd7-105">In diesem Thema wird veranschaulicht, wie Sie Informationen zum Tageszustand festlegen.</span><span class="sxs-lookup"><span data-stu-id="b5dd7-105">This topic demonstrates how to set day state information.</span></span> <span data-ttu-id="b5dd7-106">Das Monatskalender-Steuerelement verwendet Tages Zustandsinformationen, um zu bestimmen, wie bestimmte Tage innerhalb des Steuer Elements gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b5dd7-106">The month calendar control uses day state information to determine how it draws specific days within the control.</span></span>

<span data-ttu-id="b5dd7-107">Monatskalender-Steuerelemente, die die [**MCS \_ daystate**](month-calendar-control-styles.md) -Support Tages Zustände verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5dd7-107">Month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style support day states.</span></span> <span data-ttu-id="b5dd7-108">Die Tages Zustandsinformationen werden als 32-Bit-Datentyp [**MONTHDAYSTATE**](monthdaystate.md)ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="b5dd7-108">Day state information is expressed as a 32-bit data type, [**MONTHDAYSTATE**](monthdaystate.md).</span></span> <span data-ttu-id="b5dd7-109">Jedes Bit in einem **MONTHDAYSTATE** -Bitfeld (0 bis 30) gibt den Status eines Tags in einem Monat an.</span><span class="sxs-lookup"><span data-stu-id="b5dd7-109">Each bit in a **MONTHDAYSTATE** bitfield (0 through 30) specifies the state of a day in a month.</span></span> <span data-ttu-id="b5dd7-110">Wenn ein Bit ist, wird der entsprechende Tag fett formatiert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5dd7-110">If a bit is on, the corresponding day is displayed in bold.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b5dd7-111">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="b5dd7-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b5dd7-112">Technologien</span><span class="sxs-lookup"><span data-stu-id="b5dd7-112">Technologies</span></span>

-   [<span data-ttu-id="b5dd7-113">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b5dd7-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b5dd7-114">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="b5dd7-114">Prerequisites</span></span>

-   <span data-ttu-id="b5dd7-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="b5dd7-115">C/C++</span></span>
-   <span data-ttu-id="b5dd7-116">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="b5dd7-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b5dd7-117">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="b5dd7-117">Instructions</span></span>


<span data-ttu-id="b5dd7-118">Eine Anwendung kann tagzustands Informationen explizit festlegen, indem Sie die [**MCM \_ SetDayState**](mcm-setdaystate.md) -Nachricht oder das entsprechende Makro, [**monthcal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate), sendet.</span><span class="sxs-lookup"><span data-stu-id="b5dd7-118">An application can explicitly set day state information by sending the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message or by using the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="b5dd7-119">Allerdings werden Tages Zustandsinformationen in der Regel als Reaktion auf den [MCN \_ getdaystate](mcn-getdaystate.md) -Benachrichtigungs Code festgelegt, der immer dann gesendet wird, wenn das Steuerelement aktualisiert werden muss, da z. b. ein anderer Monat in der Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b5dd7-119">However, day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed because, for example, a different month has scrolled into view.</span></span>

<span data-ttu-id="b5dd7-120">Der folgende Beispielcode zeigt, wie der [MCN \_ getdaystate](mcn-getdaystate.md) -Benachrichtigungs Code in einem WM-Benachrichtigungs Nachrichten Handler verarbeitet wird. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="b5dd7-120">The following example code shows how to process the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code in a [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="b5dd7-121">MCN \_ getdaystate wird verarbeitet, indem angegeben wird, dass der erste und der fünfzehnte Tag jedes sichtbaren Monats hervorgehoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b5dd7-121">It processes MCN\_GETDAYSTATE by specifying that the first and fifteenth day of each visible month should be highlighted.</span></span> <span data-ttu-id="b5dd7-122">Der **cdaystate** -Member der [**nmdaystate**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) -Struktur gibt die Anzahl der im Array benötigten [**MONTHDAYSTATE**](monthdaystate.md) -Werte an, die eine beliebige maximale Größe erhalten.</span><span class="sxs-lookup"><span data-stu-id="b5dd7-122">The **cDayState** member of the [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure specifies the number of [**MONTHDAYSTATE**](monthdaystate.md) values that are needed in the array, which is given an arbitrary maximum size.</span></span> <span data-ttu-id="b5dd7-123">Der Code wird dann durchlaufen, um die entsprechenden Bits in jedem gültigen Element des Arrays mit dem von der Anwendung definierten **boldday** -Makro festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b5dd7-123">The code then loops to set the appropriate bits in each valid element of the array, using the application-defined **BOLDDAY** macro.</span></span>



```C++
    #define BOLDDAY(ds, iDay)  \
        if (iDay > 0 && iDay < 32)(ds) |= (0x00000001 << (iDay - 1))

    case WM_NOTIFY:
            if (((LPNMHDR)lParam)->code == MCN_GETDAYSTATE)
            {
                MONTHDAYSTATE rgMonths[12] = { 0 };
                int cMonths = ((NMDAYSTATE*)lParam)->cDayState;
                for (int i = 0; i < cMonths; i++)
                {
                    BOLDDAY(rgMonths[i], 1);
                    BOLDDAY(rgMonths[i], 15);
                }
                ((NMDAYSTATE*)lParam)->prgDayState = rgMonths;
                return TRUE;
            }
            break;
```



## <a name="related-topics"></a><span data-ttu-id="b5dd7-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5dd7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5dd7-125">Verweis für Monatskalender-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b5dd7-125">Month Calendar Control Reference</span></span>](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b5dd7-126">Informationen zu Monatskalender-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="b5dd7-126">About Month Calendar Controls</span></span>](month-calendar-controls.md)
</dt> <dt>

[<span data-ttu-id="b5dd7-127">Verwenden von Monatskalender-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="b5dd7-127">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 




