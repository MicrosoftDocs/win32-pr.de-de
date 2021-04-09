---
title: Verarbeiten der DTN_WMKEYDOWN Benachrichtigung
description: In diesem Thema wird veranschaulicht, wie eine Dtn- \_ wmKeyDown-Benachrichtigung verarbeitet wird. Durch die Behandlung dieses Benachrichtigungs Codes kann der Besitzer des Steuer Elements bestimmte Antworten auf Tastatureingaben innerhalb der Rückruf Felder des Steuer Elements bereitstellen.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec97ffc5853743c357081b974d155ee0e0977d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103858562"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a>Verarbeiten der Dtn- \_ wmKeyDown-Benachrichtigung

In diesem Thema wird veranschaulicht, wie eine [Dtn- \_ wmKeyDown](dtn-wmkeydown.md) -Benachrichtigung verarbeitet wird. Durch die Behandlung dieses Benachrichtigungs Codes kann der Besitzer des Steuer Elements bestimmte Antworten auf Tastatureingaben innerhalb der Rückruf Felder des Steuer Elements bereitstellen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Die Steuerelemente für Datums-und Zeitauswahl (DTP) senden die [Dtn- \_ wmKeyDown](dtn-wmkeydown.md) -Nachricht, um zu melden, dass der Benutzereingaben in einem Rückruf Feld eingegeben hat. Wenn Sie dieselben Tastatur Antworten emulieren möchten, die für Standard-DTP-Felder unterstützt werden, oder benutzerdefinierte Antworten bereitstellen, muss Ihre Anwendung Code enthalten, um diese Benachrichtigung zu verarbeiten.

Das folgende C++-Codebeispiel ist eine Anwendungs definierte Funktion, die die [Dtn- \_ wmKeyDown](dtn-wmkeydown.md) -Benachrichtigung verarbeitet.

**Sicherheitswarnung:** Die falsche Verwendung von **lstrincmp** kann die Sicherheit Ihrer Anwendung beeinträchtigen. Bevor Sie z. b. **lstrcmp** im folgenden Codebeispiel aufrufen, sollten Sie sicherstellen, dass die beiden Zeichen folgen mit Null enden. Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
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

 

 




