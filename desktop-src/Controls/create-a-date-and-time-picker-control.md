---
title: Erstellen eines Steuer Elements für die Datums-und Zeitauswahl
description: In diesem Thema wird veranschaulicht, wie Sie ein Steuerelement für Datums-und Zeitauswahl (DTP) dynamisch erstellen.
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1253a2972b8d858a7440b3e472d5b3aa347b8175
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104209357"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a>Erstellen eines Steuer Elements für die Datums-und Zeitauswahl

In diesem Thema wird veranschaulicht, wie Sie ein Steuerelement für Datums-und Zeitauswahl (DTP) dynamisch erstellen. Das dazugehörige C++-Codebeispiel erstellt ein DTP-Steuerelement in einem nicht modalem Dialogfeld. Er verwendet den [**DTS- \_ shownone**](date-and-time-picker-control-styles.md) -Stil, um dem Benutzer zu ermöglichen, die Deaktivierung des Datums im Steuerelement zu simulieren.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Registrieren Sie die Fenster Klasse, indem Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufrufen \_ und \_ in der zugehörigen [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur das Bit "ICC Date Classes" angeben.


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a>Schritt 2:

Um das DTP-Steuerelement zu erstellen, verwenden Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ". Geben Sie die [**datetimepick- \_ Klasse**](common-control-window-classes.md) als Fenster Klasse an, und übergeben Sie das Handle an das übergeordnete Dialogfeld.

Im folgenden C++-Codebeispiel wird [**die Funktion "-Dialogfeld**](/windows/desktop/api/winuser/nf-winuser-createdialoga) " verwendet, um ein nicht modalem Dialogfeld zu erstellen. Anschließend wird " **kreatewindowex** " aufgerufen, um das DTP-Steuerelement zu erstellen.


```C++
  hwndDlg = CreateDialog  (g_hinst,
                           MAKEINTRESOURCE(IDD_DIALOG1),
                           hwndMain,
                           DlgProc);

  if(hwndDlg)
      hwndDP = CreateWindowEx(0,
                           DATETIMEPICK_CLASS,
                           TEXT("DateTime"),
                           WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                           20,50,220,20,
                           hwndDlg,
                           NULL,
                           g_hinst,
                           NULL);
```



## <a name="complete-example"></a>Vollständiges Beispiel


```C++
//  CreateDatePick creates a DTP control within a dialog box.
//  Returns the handle to the new DTP control if successful, or NULL 
//  otherwise.
// 
//    hwndMain - The handle to the main window.
//    g_hinst  - global handle to the program instance.

HWND WINAPI CreateDatePick(HWND hwndMain)
{
    HWND hwndDP = NULL;
    HWND hwndDlg = NULL;

    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(icex);
    icex.dwICC = ICC_DATE_CLASSES;

    InitCommonControlsEx(&icex);

    hwndDlg = CreateDialog  (g_hinst,
                             MAKEINTRESOURCE(IDD_DIALOG1),
                             hwndMain,
                             DlgProc);

    if(hwndDlg)
        hwndDP = CreateWindowEx(0,
                             DATETIMEPICK_CLASS,
                             TEXT("DateTime"),
                             WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                             20,50,220,20,
                             hwndDlg,
                             NULL,
                             g_hinst,
                             NULL);

    return (hwndDP);
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

 

 