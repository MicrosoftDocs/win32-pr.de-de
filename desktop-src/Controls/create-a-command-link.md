---
title: Erstellen eines Befehls Links
description: In diesem Thema wird eine Möglichkeit zum Erstellen eines Befehls Links beschrieben.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8024a7f060a7bae3779b9ec9ebec40bd81c74bb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474461"
---
# <a name="how-to-create-a-command-link"></a>Erstellen eines Befehls Links

In diesem Thema wird eine Möglichkeit zum Erstellen eines Befehls Links beschrieben.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-an-instance-of-the-command-link-button"></a>Schritt 1: Erstellen Sie eine Instanz der Befehls Link Schaltfläche.

Im folgenden C++-Codebeispiel gibt der "Format Bezeichner" ( [**\_ CommandLink**](button-styles.md) ) die Schaltfläche als Befehls Link Schaltfläche an.


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a>Schritt 2: Festlegen der Bezeichnung für den Befehls Link und den Erläuterungstext

Verwenden Sie die [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion, um die Bezeichnung für den Befehls Link und ergänzenden Text über die [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht und die [**BCM- \_ setnote**](bcm-setnote.md) -Nachricht festzulegen.


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Schaltflächen](about-buttons.md)
</dt> <dt>

[Button-Steuerelement Verweis](bumper-button-button-control-reference.md)
</dt> <dt>

[Verwenden von Schaltflächen](using-buttons.md)
</dt> <dt>

[Schaltfläche](buttons.md)
</dt> </dl>

 

 