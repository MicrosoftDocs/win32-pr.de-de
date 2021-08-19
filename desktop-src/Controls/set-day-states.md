---
title: Festlegen von Tageszuständen
description: In diesem Thema wird veranschaulicht, wie Tageszustandsinformationen festgelegt werden. Das Monatskalender-Steuerelement verwendet Tageszustandsinformationen, um zu bestimmen, wie bestimmte Tage innerhalb des Steuerelements gezogen werden.
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3ed2c99e6faf18f0e1d06ec06eaaf9a0d573faebe6f3697e43562603447571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078474"
---
# <a name="how-to-set-day-states"></a>Festlegen von Tageszuständen

In diesem Thema wird veranschaulicht, wie Tageszustandsinformationen festgelegt werden. Das Monatskalender-Steuerelement verwendet Tageszustandsinformationen, um zu bestimmen, wie bestimmte Tage innerhalb des Steuerelements gezogen werden.

Monatskalender-Steuerelemente, die den [**MCS \_ DAYSTATE-Stil**](month-calendar-control-styles.md) verwenden, unterstützen Tagzustände. Tageszustandsinformationen werden als 32-Bit-Datentyp [**monthdaystate**](monthdaystate.md)ausgedrückt. Jedes Bit in einem **MONTHDAYSTATE-Bitfeld** (0 bis 30) gibt den Zustand eines Tages in einem Monat an. Wenn ein Bit eingeschaltet ist, wird der entsprechende Tag fett dargestellt.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Eine Anwendung kann Tagzustandsinformationen explizit festlegen, indem sie die [**MCM \_ SETDAYSTATE-Nachricht**](mcm-setdaystate.md) sendet oder das entsprechende Makro [**MonthCal \_ SetDayState verwendet.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) Tageszustandsinformationen werden jedoch in der Regel als Reaktion auf den [MCN \_ GETDAYSTATE-Benachrichtigungscode](mcn-getdaystate.md) festgelegt, der gesendet wird, wenn das Steuerelement aktualisiert werden muss, da z. B. ein anderer Monat in die Ansicht gescrollt wurde.

Der folgende Beispielcode zeigt, wie der [MCN \_ GETDAYSTATE-Benachrichtigungscode](mcn-getdaystate.md) in einem [**WM NOTIFY-Meldungshandler \_**](wm-notify.md) verarbeitet wird. McN \_ GETDAYSTATE wird verarbeitet, indem angegeben wird, dass der erste und der 15. Tag jedes sichtbaren Monats hervorgehoben werden sollen. Der **cDayState-Member** der [**NMDAYSTATE-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) gibt die Anzahl der [**MONTHDAYSTATE-Werte**](monthdaystate.md) an, die im Array benötigt werden, wobei eine beliebige maximale Größe angegeben wird. Der Code durchläuft dann eine Schleife, um die entsprechenden Bits in jedem gültigen Element des Arrays mithilfe des von der Anwendung definierten **BOLDDAY-Makros** festzulegen.



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

[Monatskalender-Steuerelementreferenz](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Informationen zu Monatskalender-Steuerelementen](month-calendar-controls.md)
</dt> <dt>

[Verwenden von Monatskalender-Steuerelementen](using-month-calendar-controls.md)
</dt> </dl>

 

 




