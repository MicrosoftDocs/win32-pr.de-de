---
title: Implementieren von Quick Infos für Status leisten Symbole
description: Eine nicht eindringliche Möglichkeit, eine erklärende Meldung für ein Status leisten Symbol anzuzeigen, ist die Implementierung einer QuickInfo. Die QuickInfo wird beim Klicken nicht mehr angezeigt, Sie können aber auch einen Timeout Wert angeben.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277fb8d15654ae51565c1a461a9a8414d3e9213c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474397"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a>Implementieren von Quick Infos für Status leisten Symbole

Eine nicht eindringliche Möglichkeit, eine erklärende Meldung für ein Status leisten Symbol anzuzeigen, ist die Implementierung einer QuickInfo. Die QuickInfo wird beim Klicken nicht mehr angezeigt, Sie können aber auch einen Timeout Wert angeben.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="implement-tooltips-for-status-bar-icons"></a>Tooltips für StatusBar-Symbole implementieren

Im folgenden Code Fragment wird veranschaulicht, wie einem Status leisten Symbol eine QuickInfo-Sprechblase hinzugefügt wird.


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a>Bemerkungen

Eine ausführliche Erläuterung der Statusleiste finden Sie in [der Taskleiste](/windows/desktop/shell/taskbar).

Zum Anzeigen einer QuickInfo-Sprechblase müssen Sie das NIF- \_ infoflag in der [**notifyiendata**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) -Struktur festlegen und die Elemente **szinfo** und **utimeout** verwenden, um den QuickInfo-Text und die Timeout Dauer anzugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Quick Infos](using-tooltip-contro.md)
</dt> </dl>

 

 