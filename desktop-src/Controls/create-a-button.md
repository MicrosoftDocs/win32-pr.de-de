---
title: Erstellen einer Schaltfläche
description: Um Schaltflächen dynamisch zu erstellen, verwenden Sie die Funktion "up Window" oder "kreatewindowex". In diesem Thema wird veranschaulicht, wie Sie mit der Funktion "up Window" eine standardmäßige pushschaltfläche erstellen.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039870"
---
# <a name="how-to-create-a-button"></a>Erstellen einer Schaltfläche

Um Schaltflächen dynamisch zu erstellen, verwenden Sie die Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ". In diesem Thema wird veranschaulicht, wie Sie mit der Funktion "up **Window** " eine standardmäßige pushschaltfläche erstellen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Verwenden Sie [**die Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowa) "Funktion", um ein Schaltflächen-Steuerelement zu erstellen.

Im folgenden C++-Beispiel ist der *m- \_ HWND* -Parameter das Handle für das übergeordnete Fenster. Der [**\_ DEFPUSHBUTTON**](button-styles.md) -Stil von "bin" gibt an, dass eine Standard Schaltfläche "Push" erstellt wird Beachten Sie, dass die Größen-und Positionswerte angegeben werden müssen, da bei Verwendung von **CW \_ usedefault** für eine Schaltfläche die Werte auf NULL festgelegt werden.


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
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

 

 