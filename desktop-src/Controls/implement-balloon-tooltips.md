---
title: Implementieren von Quick Infos zur Sprechblase
description: Quick Infos für die Sprechblase ähneln Standard-Quick Infos, werden aber in einem Zeichenstil \ 0034; Sprechblase \ 0034; angezeigt. mit einem stem, das auf das Tool zeigt.
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708669"
---
# <a name="how-to-implement-balloon-tooltips"></a>Implementieren von Quick Infos zur Sprechblase

Quick Infos für die Sprechblase ähneln Standard-Quick Infos, werden jedoch in einer "Sprechblase" im Zeichenstil angezeigt, wobei ein stem auf das Tool zeigt. Quick Infos für die Sprechblase können entweder einzeilige oder mehrzeilige Zeilen sein. Sie werden auf die gleiche Weise wie Standard-Quick Infos erstellt und behandelt.

Die Standardposition des Stamms und des Rechtecks wird in der folgenden Abbildung dargestellt. Wenn das Tool zu nah am oberen Rand des Bildschirms ist, wird die QuickInfo unterhalb des Tool Rechtecks angezeigt. Wenn das Tool zu nah am rechten Bildschirmrand ist, gelten ähnliche Prinzipien, aber die QuickInfo wird auf der linken Seite des Tool Rechtecks angezeigt.

![Screenshot eines Dialog Felds eine QuickInfo-Sprechblase mit einer Textzeile wird oberhalb und rechts neben dem Ziel angezeigt.](images/tt-balloon.png)

Sie können die Standard Positionierung ändern, indem Sie das Steuerelement " **ttf \_ centertip** " im **uFlags** -Member der QuickInfo-Struktur " [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) " festlegen. In diesem Fall verweist das stem normalerweise auf den Mittelpunkt des unteren Randes des Tool Rechtecks, und das Text Rechteck wird direkt unterhalb des Tools angezeigt. Der Stamm wird an das Text Rechteck in der Mitte des oberen Rands angefügt. Wenn das Tool zu nah am unteren Bildschirmrand ist, wird das Text Rechteck oberhalb des Tools zentriert, und der Stamm wird an die Mitte des unteren Rands angefügt.

Die folgende Abbildung zeigt eine QuickInfo, die sich auf das Tool konzentriert.

![Screenshot eines Dialog Felds eine QuickInfo-Sprechblase mit einer Textzeile wird unter dem Ziel zentriert angezeigt](images/tt-ballooncenter.png)

Wenn Sie den Speicherort der Stamm Punkte angeben möchten, legen Sie das " **ttf \_ Track** "-Flag im **uFlags** -Member der ToolTip- [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur fest. Anschließend geben Sie die Koordinate an, indem Sie eine [**TTM \_ trackposition**](ttm-trackposition.md) -Nachricht mit den x-und y-Koordinaten im *LPARAM* -Wert senden. Wenn **ttf \_ centertip** ebenfalls festgelegt ist, zeigt das Stamm Modul immer noch auf die Position, die von der **TTM \_ trackposition** -Nachricht angegeben wird.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="implement-balloon-tooltips"></a>Tooltipps für die Sprechblase implementieren

Im folgenden Beispielcode wird veranschaulicht, wie Sie eine zentrierte Sprechblasen-QuickInfo **mit dem Steuer \_** Element Stil der QuickInfo-Sprechblase implementieren


```C++
hwndToolTips = CreateWindow(TOOLTIPS_CLASS, NULL, 
                            WS_POPUP | TTS_NOPREFIX | TTS_BALLOON, 
                            0, 0, 0, 0, NULL, NULL, g_hinst, NULL);

if (hwndTooltip)
{
    TOOLINFO ti;

    ti.cbSize   = sizeof(ti);
    ti.uFlags   = TTF_TRANSPARENT | TTF_CENTERTIP;
    ti.hwnd     = hwnd;
    ti.uId      = 0;
    ti.hinst    = NULL;
    ti.lpszText = LPSTR_TEXTCALLBACK;

    GetClientRect(hwnd, &ti.rect);

    SendMessage(hwndToolTips, TTM_ADDTOOL, 0, (LPARAM) &ti );

}
            
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Quick Infos](using-tooltip-contro.md)
</dt> <dt>

[**QuickInfo-Stile**](tooltip-styles.md)
</dt> </dl>

 

 




