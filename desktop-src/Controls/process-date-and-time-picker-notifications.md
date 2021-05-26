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
# <a name="how-to-process-date-and-time-picker-notifications"></a>Verarbeiten von Datums- und Uhrzeitauswahlbenachrichtigungen

In diesem Abschnitt wird veranschaulicht, wie Sie Datums- und Uhrzeitauswahlbenachrichtigungen verarbeiten.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche Programmierung

## <a name="instructions"></a>Instructions


Ein DTP-Steuerelement (Datums- und Uhrzeitauswahl) sendet Benachrichtigungsmeldungen an das übergeordnete Fenster, wenn Ereignisse, die normalerweise durch Eingabe des Benutzers ausgelöst werden, im Steuerelement auftreten. Ihre Anwendung muss Code enthalten, um den Typ der Benachrichtigungsnachricht zu bestimmen und entsprechend zu reagieren.

Wenn Sie Rückruffelder mit den DTP-Steuerelementen in Ihrer Anwendung verwenden möchten, müssen Sie darauf vorbereitet sein, DIE Benachrichtigungscodes [DTN \_ FORMATQUERY,](dtn-formatquery.md) [DTN \_ FORMAT](dtn-format.md)und [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) zu verarbeiten. Weitere Informationen zu Rückruffeldern finden Sie unter [Rückruffelder.](date-and-time-picker-controls.md)

Im folgenden C++-Codebeispiel wird die von einem DTP-Steuerelement gesendete Benachrichtigungsnachricht identifiziert und die entsprechende anwendungsdefinierte Funktion aufruft. In den folgenden Themen finden Sie Codebeispiele, die veranschaulichen, wie die in diesem Beispiel angezeigten Benachrichtigungen behandelt werden.

|   Themen                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [Verarbeiten der \_ DTN-DATETIMECHANGE-Benachrichtigung](process-the-dtn-datetimechange-notification.md) |
| [Verarbeiten der \_ DTN-FORMATQUERY-Benachrichtigung](process-the-dtn-formatquery-notification.md)       |
| [Verarbeiten der \_ DTN-FORMATbenachrichtigung](process-the-dtn-format-notfication.md)                  |
| [Verarbeiten der \_ DTN-WMKEYDOWN-Benachrichtigung](process-the-dtn-wmkeydown-notification.md)           |



 



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

[Datums- und Uhrzeitauswahlbenachrichtigungen](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[Datums- und Uhrzeitauswahl-Steuerelementreferenz](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Verwenden von Steuerelementen für die Datums- und Uhrzeitauswahl](using-date-and-time-picker.md)
</dt> <dt>

[Datums- und Uhrzeitauswahl](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




