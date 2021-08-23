---
title: Implementieren von QuickInfos für Statusleistensymbole
description: Eine nicht inintrusive Möglichkeit, eine erläuternde Meldung für ein Statusleistensymbol anzuzeigen, besteht in der Implementierung einer QuickInfo. Die QuickInfo wird beim Klicken nicht mehr angezeigt, Sie können aber auch einen Time out-Wert angeben.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2bd100dc6edb2aac7b4c8c5df3781e76391ae2d9d0ad456533384ed8701f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958579"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a>Implementieren von QuickInfos für Statusleistensymbole

Eine nicht inintrusive Möglichkeit, eine erläuternde Meldung für ein Statusleistensymbol anzuzeigen, besteht in der Implementierung einer QuickInfo. Die QuickInfo wird beim Klicken nicht mehr angezeigt, Sie können aber auch einen Time out-Wert angeben.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="implement-tooltips-for-status-bar-icons"></a>Implementieren von QuickInfos für Statusleistensymbole

Das folgende Codefragment veranschaulicht, wie Sie einem Statusleistensymbol eine QuickInfo für eine Sprechblase hinzufügen.


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



## <a name="remarks"></a>Hinweise

Eine ausführliche Erläuterung der Statusleiste finden Sie unter [Die Taskleiste.](/windows/desktop/shell/taskbar)

Zum Anzeigen einer QuickInfo für die Sprechblasen müssen Sie das \_ NIF-INFO-Flag in der [**NOTIFYICONDATA-Struktur**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) festlegen und die **Elemente szInfo** und **uTimeout** verwenden, um den QuickInfo-Text und die Timeoutdauer anzugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von QuickInfo-Steuerelementen](using-tooltip-contro.md)
</dt> </dl>

 

 