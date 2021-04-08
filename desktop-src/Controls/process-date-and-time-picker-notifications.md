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
# <a name="how-to-process-date-and-time-picker-notifications"></a>Verarbeiten von Benachrichtigungen zu Datums-und Zeitauswahl

In diesem Abschnitt wird veranschaulicht, wie Benachrichtigungen für Datums-und Zeitauswahl verarbeitet werden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Ein DTP-Steuerelement (Datums-und Zeitauswahl) sendet Benachrichtigungs Meldungen an das übergeordnete Fenster, wenn Ereignisse, die normalerweise durch Eingabe des Benutzers ausgelöst werden, im-Steuerelement auftreten. Die Anwendung muss Code enthalten, um den Typ der Benachrichtigungs Meldung zu bestimmen und entsprechend zu reagieren.

Wenn Sie beabsichtigen, Rückruf Felder mit den DTP-Steuerelementen in der Anwendung zu verwenden, müssen Sie darauf vorbereitet sein, das [Dtn \_ formatQuery](dtn-formatquery.md)-, [Dtn- \_ Format](dtn-format.md)und [Dtn \_ wmKeyDown](dtn-wmkeydown.md) -Benachrichtigungs Codes zu verarbeiten. Weitere Informationen zu Rückruf Feldern finden Sie unter [Rückruf Felder](date-and-time-picker-controls.md).

Im folgenden C++-Codebeispiel wird die von einem DTP-Steuerelement gesendete Benachrichtigungs Meldung identifiziert, und die entsprechende Anwendungs definierte Funktion wird aufgerufen. In den folgenden Themen finden Sie Codebeispiele, die veranschaulichen, wie die in diesem Beispiel angezeigten Benachrichtigungen verarbeitet werden.

|                                                                                                        |
|--------------------------------------------------------------------------------------------------------|
| [Verarbeiten der Dtn \_ datetimechange-Benachrichtigung](process-the-dtn-datetimechange-notification.md) |
| [Verarbeiten der Dtn \_ formatQuery-Benachrichtigung](process-the-dtn-formatquery-notification.md)       |
| [Verarbeiten der Dtn- \_ Format Benachrichtigung](process-the-dtn-format-notfication.md)                  |
| [Verarbeiten der Dtn- \_ wmKeyDown-Benachrichtigung](process-the-dtn-wmkeydown-notification.md)           |



 



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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datums-und Zeitauswahl Benachrichtigungen](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[Steuerelement Verweis für Datums-und Zeitauswahl](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Verwenden von Steuerelementen für Datums-und Zeitauswahl](using-date-and-time-picker.md)
</dt> <dt>

[Datums-und Zeitauswahl](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




