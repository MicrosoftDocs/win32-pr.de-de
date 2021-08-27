---
title: Implementieren von mehrstufigen QuickInfos
description: Mehrzeilen-QuickInfos ermöglichen das Anzeigen von Text in mehr als einer Zeile.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0d9f4172b256d2e6b72fb59ace4dc377fa3a0061e3ee0e6c0f234a74aad06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085625"
---
# <a name="how-to-implement-multiline-tooltips"></a>Implementieren von mehrstufigen QuickInfos

Mehrzeilen-QuickInfos ermöglichen das Anzeigen von Text in mehr als einer Zeile.

Sie werden von [Version 4.70](common-control-versions.md) und höher der allgemeinen Steuerelemente unterstützt. Ihre Anwendung erstellt eine mehrzweckige QuickInfo, indem sie eine [**TTM \_ SETMAXTIPWIDTH-Nachricht**](ttm-setmaxtipwidth.md) sendet und dabei die Breite des Anzeigerechtecks angibt. Text, der diese Breite überschreitet, wird mit der nächsten Zeile umschließen, anstatt den Anzeigebereich zu verbreitern. Die Rechteckhöhe wird nach Bedarf erhöht, um die zusätzlichen Linien aufzunehmen. Das QuickInfo-Steuerelement umbricht die Zeilen automatisch, oder Sie können eine Wagenrücklauf-/Zeilenfeedkombination (r n) verwenden, um Zeilenumbrüche an \\ \\ bestimmten Stellen zu erzwingen.

Die resultierende Anzeige wird in der folgenden Abbildung dargestellt.

![Screenshot eines Dialogfelds mit einer QuickInfo, die Text enthält, der wie ein mehrzeiler Absatz angeordnet ist](images/tt-multiline.png)

> [!Note]  
> Der vom **szText-Member** der [**NMTTDISPINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) angegebene Textpuffer kann nur 80 Zeichen aufnehmen. Wenn Sie eine längere Zeichenfolge verwenden müssen, verweisen Sie den **lpszText-Member** von **NMTTDISPINFO** auf einen Puffer, der den gewünschten Text enthält.

 

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="implement-multiline-tooltips"></a>Implementieren von mehrstufigen QuickInfos

Das folgende Codefragment ist ein Beispiel für einen einfachen [TTN \_ GETDISPINFO-Benachrichtigungshandler.](ttn-getdispinfo.md) Sie ermöglicht eine mehrstufige QuickInfo, indem das Anzeigerechteck auf 150 Pixel festgelegt wird. Nach dem ersten Wort wird ein manueller Zeilenumbruch eingefügt, um zu zeigen, dass Zeilenumbrüche schwierig und weich sein können.


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

[Verwenden von QuickInfo-Steuerelementen](using-tooltip-contro.md)
</dt> </dl>

 

 




