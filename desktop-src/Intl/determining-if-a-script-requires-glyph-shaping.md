---
description: Im folgenden Beispiel wird scriptgetproperties aufgerufen, um herauszufinden, ob das Skript für jedes der aufeinander folgenden Elemente eine Symbol Strukturierung erfordert.
ms.assetid: 75c5946b-de38-48d9-a5e2-1e0b2dc9f3c7
title: Bestimmen, ob ein Skript eine Symbol Strukturierung erfordert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62eb20fb0335c5779352f15221653dad0c5320c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217808"
---
# <a name="determining-if-a-script-requires-glyph-shaping"></a>Bestimmen, ob ein Skript eine Symbol Strukturierung erfordert

Im folgenden Beispiel wird [**scriptgetproperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) aufgerufen, um herauszufinden, ob das Skript für jedes der aufeinander folgenden [Elemente](uniscribe-glossary.md) eine Symbol Strukturierung erfordert.


```C++
const SCRIPT_PROPERTIES **g_ppScriptProperties;
int g_iMaxScript;

WCHAR *pwcInChars = L"Unicode string to itemize";
int cInChars = wcslen(pwcInChars);
const int cMaxItems = 20;
SCRIPT_ITEM si[cMaxItems + 1];
SCRIPT_ITEM *pItems = si;
int cItems;

ScriptGetProperties(&g_ppScriptProperties,
                    &g_iMaxScript);

HRESULT hResult = ScriptItemize(pwcInChars,
                                cInChars,
                                cMaxItems,
                                NULL,
                                NULL,
                                pItems,
                                &cItems);
if (hResult == 0) {
    for (int i=0; i<cItems; i++) {
        if (g_ppScriptProperties[pItems[i].a.eScript]->fComplex) {

            // Item [i] is complex script text
            // requiring glyph shaping.

        } else {

            // The text may be rendered legibly without using Uniscribe. 
            // However, Uniscribe may still be used as a means of accessing 
            // font typographic features. 
        }
    }
} else {
    // Handle the error.
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von uniscri](using-uniscribe.md)
</dt> </dl>

 

 



