---
description: Definiert einige oder alle Zeichenattribute, Glyphen, Vorwärtsbreiten, x- und y-Positionen, Zeichen-zu-Glyph-Zuordnungen usw. für eine Zeichenfolge.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (Usp10.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9481c641f182015d7a318c21c490f45fcc934e0df1baa52483707628eb4daa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390299"
---
# <a name="script_string_analysis"></a>\_ \_ SKRIPTZEICHENFOLGENANALYSE

Definiert einige oder alle Zeichenattribute, Glyphen, Vorwärtsbreiten, x- und y-Positionen, Zeichen-zu-Glyph-Zuordnungen usw. für eine Zeichenfolge.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Hinweise

Dies ist eine nicht transparente Struktur, die dynamisch zugeordnet und von [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)abgerufen wird. Sie ist auch für alle anderen **ScriptString-Funktionen \*** erforderlich.

Da die Analyse umfangreich sein kann, ist es wichtig, dass Ihre Anwendung [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) aufruft, sobald sie mit der Zeichenfolge fertig ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Verteilbare Komponente<br/>          | Internet Explorer 5 oder höher amWindows Me/98/95<br/>                         |
| Header<br/>                   | <dl> <dt>Usp10.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Uniscribe-Strukturen](uniscribe-structures.md)
</dt> <dt>

[**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[**ScriptStringFree**](script-string-analysis.md)
</dt> </dl>

 

 




