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
# <a name="how-to-set-day-states"></a>Festlegen von Tages Zuständen

In diesem Thema wird veranschaulicht, wie Sie Informationen zum Tageszustand festlegen. Das Monatskalender-Steuerelement verwendet Tages Zustandsinformationen, um zu bestimmen, wie bestimmte Tage innerhalb des Steuer Elements gezeichnet werden.

Monatskalender-Steuerelemente, die die [**MCS \_ daystate**](month-calendar-control-styles.md) -Support Tages Zustände verwenden. Die Tages Zustandsinformationen werden als 32-Bit-Datentyp [**MONTHDAYSTATE**](monthdaystate.md)ausgedrückt. Jedes Bit in einem **MONTHDAYSTATE** -Bitfeld (0 bis 30) gibt den Status eines Tags in einem Monat an. Wenn ein Bit ist, wird der entsprechende Tag fett formatiert angezeigt.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Eine Anwendung kann tagzustands Informationen explizit festlegen, indem Sie die [**MCM \_ SetDayState**](mcm-setdaystate.md) -Nachricht oder das entsprechende Makro, [**monthcal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate), sendet. Allerdings werden Tages Zustandsinformationen in der Regel als Reaktion auf den [MCN \_ getdaystate](mcn-getdaystate.md) -Benachrichtigungs Code festgelegt, der immer dann gesendet wird, wenn das Steuerelement aktualisiert werden muss, da z. b. ein anderer Monat in der Ansicht angezeigt wird.

Der folgende Beispielcode zeigt, wie der [MCN \_ getdaystate](mcn-getdaystate.md) -Benachrichtigungs Code in einem WM-Benachrichtigungs Nachrichten Handler verarbeitet wird. [**\_**](wm-notify.md) MCN \_ getdaystate wird verarbeitet, indem angegeben wird, dass der erste und der fünfzehnte Tag jedes sichtbaren Monats hervorgehoben werden sollen. Der **cdaystate** -Member der [**nmdaystate**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) -Struktur gibt die Anzahl der im Array benötigten [**MONTHDAYSTATE**](monthdaystate.md) -Werte an, die eine beliebige maximale Größe erhalten. Der Code wird dann durchlaufen, um die entsprechenden Bits in jedem gültigen Element des Arrays mit dem von der Anwendung definierten **boldday** -Makro festzulegen.



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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verweis für Monatskalender-Steuerelement](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Informationen zu Monatskalender-Steuerelementen](month-calendar-controls.md)
</dt> <dt>

[Verwenden von Monatskalender-Steuerelementen](using-month-calendar-controls.md)
</dt> </dl>

 

 




