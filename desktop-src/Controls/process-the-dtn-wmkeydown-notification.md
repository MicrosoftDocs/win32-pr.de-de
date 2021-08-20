---
title: Verarbeiten der DTN_WMKEYDOWN Benachrichtigung
description: In diesem Thema wird die Verarbeitung einer DTN \_ WMKEYDOWN-Benachrichtigung veranschaulicht. Durch die Behandlung dieses Benachrichtigungscodes kann der Besitzer des Steuerelements bestimmte Antworten auf Tastatureingaben innerhalb der Rückruffelder des Steuerelements bereitstellen.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbef0804afb388f9cadad60b04bf93ce4730ef255476f0c7f216edfd24846a19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540350"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a>Verarbeiten der \_ DTN-WMKEYDOWN-Benachrichtigung

In diesem Thema wird die Verarbeitung einer [DTN \_ WMKEYDOWN-Benachrichtigung](dtn-wmkeydown.md) veranschaulicht. Durch die Behandlung dieses Benachrichtigungscodes kann der Besitzer des Steuerelements bestimmte Antworten auf Tastatureingaben innerhalb der Rückruffelder des Steuerelements bereitstellen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


DTP-Steuerelemente (Datums- und Uhrzeitauswahl) senden die [DTN \_ WMKEYDOWN-Meldung,](dtn-wmkeydown.md) um zu melden, dass der Benutzer Eingaben in ein Rückruffeld eingegeben hat. Wenn Sie dieselben Tastaturantworten emulieren möchten, die für Standard-DTP-Felder unterstützt werden, oder benutzerdefinierte Antworten bereitstellen möchten, muss Ihre Anwendung Code enthalten, um diese Benachrichtigung zu verarbeiten.

Das folgende C++-Codebeispiel ist eine anwendungsdefinierte Funktion, die die [DTN \_ WMKEYDOWN-Benachrichtigung](dtn-wmkeydown.md) verarbeitet.

**Sicherheitswarnung:** Die **falsche Verwendung von lstrcmp** kann die Sicherheit Ihrer Anwendung gefährden. Vor dem Aufrufen von **lstrcmp** im folgenden Codebeispiel sollten Sie beispielsweise sicherstellen, dass die beiden Zeichenfolgen null-terminiert sind. Lesen Sie [sicherheitsaspekte: Microsoft Windows Controls,](sec-comctls.md) bevor Sie fortfahren.



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

[Verwenden von Steuerelementen für die Datums- und Uhrzeitauswahl](using-date-and-time-picker.md)
</dt> <dt>

[Datums- und Uhrzeitauswahl-Steuerelementreferenz](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Datums- und Uhrzeitauswahl](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




