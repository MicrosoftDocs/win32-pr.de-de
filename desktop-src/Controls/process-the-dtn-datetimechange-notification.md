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
# <a name="how-to-process-the-dtn_datetimechange-notification"></a>Verarbeiten der Dtn \_ datetimechange-Benachrichtigung

In diesem Thema wird veranschaulicht, wie Benachrichtigungen von Änderungen, die vom Benutzer vorgenommen wurden, an das Steuerelement für die Datums-und Zeitauswahl (DTP) verarbeitet werden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Ein DTP-Steuerelement sendet den [Dtn \_ datetimechange](dtn-datetimechange.md) -Benachrichtigungs Code, wenn eine Änderung auftritt. Diese Benachrichtigung wird z. b. generiert, wenn der Benutzer eines der Felder im-Steuerelement ändert oder wenn das Steuerelement auf den [**DTS \_ shownone**](date-and-time-picker-control-styles.md) -Stil festgelegt ist, wenn der Benutzer den Zustand des Kontrollkästchens des Steuer Elements ändert.

Die Anwendung muss Code enthalten, um Dtn \_ datetimechange-Nachrichten zu verarbeiten, die vom DTP-Steuerelement gesendet werden.

Das folgende C++-Codebeispiel ist eine Anwendungs definierte Funktion, die den Zustand eines DTP-Steuer Elements angibt, das auf den **DTS \_ shownone** -Stil festgelegt ist.



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

[Verwenden von Steuerelementen für Datums-und Zeitauswahl](using-date-and-time-picker.md)
</dt> <dt>

[Steuerelement Verweis für Datums-und Zeitauswahl](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Datums-und Zeitauswahl](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




