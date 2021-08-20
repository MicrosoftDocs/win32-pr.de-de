---
title: Verarbeiten der DTN_DATETIMECHANGE benachrichtigung
description: In diesem Thema wird veranschaulicht, wie Sie Benachrichtigungen über Vom Benutzer vorgenommene Änderungen am DTP-Steuerelement (Datums- und Uhrzeitauswahl) verarbeiten.
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9490059a202eff69a05b34a086e74d6df52758713fd5b66d899d1ab114a31040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829921"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a>Verarbeiten der \_ DTN-DATETIMECHANGE-Benachrichtigung

In diesem Thema wird veranschaulicht, wie Sie Benachrichtigungen über Vom Benutzer vorgenommene Änderungen am DTP-Steuerelement (Datums- und Uhrzeitauswahl) verarbeiten.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Ein DTP-Steuerelement sendet den [DTN DATETIMECHANGE-Benachrichtigungscode, \_ ](dtn-datetimechange.md) wenn eine Änderung auftritt. Diese Benachrichtigung wird z. B. generiert, wenn der Benutzer eines der Felder im Steuerelement ändert oder wenn das Steuerelement auf den [**DTS \_ SHOWNONE-Stil**](date-and-time-picker-control-styles.md) festgelegt ist, wenn der Benutzer den Zustand des Kontrollkästchens des Steuerelements ändert.

Ihre Anwendung muss Code zum Verarbeiten von DTN \_ DATETIMECHANGE-Nachrichten enthalten, die vom DTP-Steuerelement gesendet werden.

Das folgende C++-Codebeispiel ist eine anwendungsdefinierte Funktion, die den Zustand eines DTP-Steuerelements angibt, das auf den **DTS \_ SHOWNONE-Stil** festgelegt ist.



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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Steuerelementen für die Datums- und Uhrzeitauswahl](using-date-and-time-picker.md)
</dt> <dt>

[Datums- und Uhrzeitauswahl-Steuerelementreferenz](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Datums- und Uhrzeitauswahl](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




