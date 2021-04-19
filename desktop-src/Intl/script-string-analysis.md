---
description: Definiert einige oder alle Zeichen Attribute, Glyphen, vorab breiten, x-und y-Positionen, Zeichen-zu-Glyphen-Zuordnungen usw. für eine Zeichenfolge.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352274"
---
# <a name="script_string_analysis"></a>Skript für \_ Zeichen folgen \_ Analyse

Definiert einige oder alle Zeichen Attribute, Glyphen, vorab breiten, x-und y-Positionen, Zeichen-zu-Glyphen-Zuordnungen usw. für eine Zeichenfolge.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Bemerkungen

Dabei handelt es sich um eine nicht transparente Struktur, die von [**scriptstringanalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)dynamisch zugeordnet und abgerufen wird. Dies ist auch für alle anderen **scriptstring \** _-Funktionen erforderlich.

Da die Analyse sehr groß sein kann, ist es wichtig, dass die Anwendung [_ *scriptstringfree* *](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) aufruft, sobald Sie mit der Zeichenfolge fertig ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Verteilbare Komponente<br/>          | Internet Explorer 5 oder höher onwindows Me/98/95<br/>                         |
| Header<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unischreiber](uniscribe.md)
</dt> <dt>

[Uniscristrukturen](uniscribe-structures.md)
</dt> <dt>

[**Scriptstringanalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[**Scriptstringfree**](script-string-analysis.md)
</dt> </dl>

 

 




