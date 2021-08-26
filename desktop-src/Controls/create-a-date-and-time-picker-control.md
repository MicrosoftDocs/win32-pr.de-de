---
title: Erstellen eines Steuerelements für die Datums- und Uhrzeitauswahl
description: In diesem Thema wird veranschaulicht, wie Ein DTP-Steuerelement (Date and Time Picker) dynamisch erstellt wird.
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa3f18e6033d3764e385280da383d74c351201694969266dcc383654a4372ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920890"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a>Erstellen eines Steuerelements für die Datums- und Uhrzeitauswahl

In diesem Thema wird veranschaulicht, wie Ein DTP-Steuerelement (Date and Time Picker) dynamisch erstellt wird. Im zugehörigen C++-Codebeispiel wird ein DTP-Steuerelement in einem moduslosen Dialogfeld erstellt. Er verwendet den [**DTS \_ SHOWNONE-Stil,**](date-and-time-picker-control-styles.md) um dem Benutzer zu ermöglichen, die Deaktivierung des Datums innerhalb des Steuerelements zu simulieren.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Registrieren Sie die Fensterklasse, indem Sie die [**InitCommonControlsEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) aufrufen und das BIT "DATE \_ \_ CLASSES" in der zugehörigen [**INITCOMMONCONTROLSEX-Struktur**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) angeben.


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a>Schritt 2:

Verwenden Sie zum Erstellen des DTP-Steuerelements die [**CreateWindowEx-Funktion.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Geben Sie [**DATETIMEPICK \_ CLASS**](common-control-window-classes.md) als Fensterklasse an, und übergeben Sie das Handle an das übergeordnete Dialogfeld.

Im folgenden C++-Codebeispiel wird die [**CreateDialog-Funktion**](/windows/desktop/api/winuser/nf-winuser-createdialoga) verwendet, um ein modusloses Dialogfeld zu erstellen. Anschließend wird **CreateWindowEx** zum Erstellen des DTP-Steuerelements aufrufen.


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

[Verwenden von Steuerelementen für die Datums- und Uhrzeitauswahl](using-date-and-time-picker.md)
</dt> <dt>

[Datums- und Uhrzeitauswahl-Steuerelementreferenz](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Datums- und Uhrzeitauswahl](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 