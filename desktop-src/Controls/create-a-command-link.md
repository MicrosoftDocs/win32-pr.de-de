---
title: Erstellen eines Befehlslinks
description: In diesem Thema wird eine Möglichkeit zum Erstellen eines Befehlslinks beschrieben.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c61888921f06e017ec1ea625730c3cc52de5ab364db22fc01fd021ce5629c63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920900"
---
# <a name="how-to-create-a-command-link"></a>Erstellen eines Befehlslinks

In diesem Thema wird eine Möglichkeit zum Erstellen eines Befehlslinks beschrieben.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-an-instance-of-the-command-link-button"></a>Schritt 1: Erstellen Sie eine Instanz der Befehlslinkschaltfläche.

Im folgenden C++-Codebeispiel gibt die Formatkonstant [**BS \_ COMMANDLINK**](button-styles.md) die Schaltfläche als Befehlslinkschaltfläche an.


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



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a>Schritt 2: Festlegen der Befehlslinkbezeichnung und des Erklärungstexts

Verwenden Sie [**die SendMessage-Funktion,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) um die Befehlslinkbezeichnung und den ergänzenden Text über die [**WM \_ SETTEXT-Nachricht**](/windows/desktop/winmsg/wm-settext) bzw. die [**BCM \_ SETNOTE-Nachricht**](bcm-setnote.md) zu festlegen.


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Schaltflächen](about-buttons.md)
</dt> <dt>

[Referenz zum Schaltflächensteuerfeld](bumper-button-button-control-reference.md)
</dt> <dt>

[Verwenden von Schaltflächen](using-buttons.md)
</dt> <dt>

[Schaltfläche](buttons.md)
</dt> </dl>

 

 