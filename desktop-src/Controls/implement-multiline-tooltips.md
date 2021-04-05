---
title: So implementieren Sie mehrzeilige Quick Infos
description: Mehrzeilige Quick Infos ermöglichen das Anzeigen von Text in mehr als einer Zeile.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d6f32d638b2d33ea6270aa5f8ce2c09f0f4174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708663"
---
# <a name="how-to-implement-multiline-tooltips"></a>So implementieren Sie mehrzeilige Quick Infos

Mehrzeilige Quick Infos ermöglichen das Anzeigen von Text in mehr als einer Zeile.

Sie werden von [Version 4,70](common-control-versions.md) und höher der allgemeinen Steuerelemente unterstützt. Die Anwendung erstellt eine mehrzeilige QuickInfo, indem eine [**TTM- \_ SetMaxTipWidth**](ttm-setmaxtipwidth.md) -Meldung gesendet wird, die die Breite des Anzeige Rechtecks angibt. Text, der diese Breite überschreitet, wird in die nächste Zeile umschlossen, anstatt den Anzeigebereich zu erweitern. Die Rechtecks Höhe wird nach Bedarf erweitert, um den zusätzlichen Zeilen Rechnung zu tragen. Das QuickInfo-Steuerelement umschließt die Linien automatisch, oder Sie können eine Kombination aus Wagen Rücklauf/Zeilenvorschub, \\ r \\ n, verwenden, um Zeilenumbrüche an bestimmten Positionen zu erzwingen

Die resultierende Anzeige wird in der folgenden Abbildung dargestellt.

![Screenshot eines Dialog Felds mit einer QuickInfo, die Text wie einen mehrzeiligen Absatz enthält](images/tt-multiline.png)

> [!Note]  
> Der Text Puffer, der vom **szText** -Member der [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur angegeben wird, kann nur 80 Zeichen umfassen. Wenn Sie eine längere Zeichenfolge verwenden müssen, verweisen Sie auf den **lpszText** -Member von **nmttdispinfo** auf einen Puffer, der den gewünschten Text enthält.

 

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="implement-multiline-tooltips"></a>Implementieren von mehrzeiligen Quick Infos

Das folgende Code Fragment ist ein Beispiel für einen einfachen [TTN \_ getdispinfo](ttn-getdispinfo.md) -Benachrichtigungs Handler. Dadurch wird eine mehrzeilige QuickInfo aktiviert, indem das Anzeige Rechteck auf 150 Pixel festgelegt wird. Ein manueller Zeilenumbruch wird nach dem ersten Wort eingefügt, um anzuzeigen, dass Zeilenumbrüche schwierig und weich sind.


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Quick Infos](using-tooltip-contro.md)
</dt> </dl>

 

 




