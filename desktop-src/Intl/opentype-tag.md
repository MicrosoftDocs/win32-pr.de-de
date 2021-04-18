---
description: Definiert ein 4-Byte-Array, das 4 8-Bit-ASCII-Werte für Leerzeichen, a-z oder a-z enthält, um die Funktions Tags von OpenType-Skripts, Sprachen und Schriftart zu identifizieren.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf973c03f26bdb8f8b3799e1780fed5075d315cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368198"
---
# <a name="opentype_tag"></a>OpenType- \_ Tag

Definiert ein 4-Byte-Array, das 4 8-Bit-ASCII-Werte für Leerzeichen, a-z oder a-z enthält, um die Funktions Tags von OpenType-Skripts, Sprachen und Schriftart zu identifizieren.


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a>Bemerkungen

In den folgenden Beispielen werden Darstellungen von OpenType-Merkmals Tags definiert.

-   Das featuretag für die Ligaturen-Funktion ist "Liga".
-   Die Sprachen Tags für Rumänisch, Urdu und Persian sind "Rom", "URD" bzw. "All". Beachten Sie, dass jedes dieser Tags mit einem Leerzeichen endet.
-   Die Skript Tags für lateinische und arabische Skripts sind "Latn" bzw. "Arabisch".

Weitere Informationen zu OpenType-featuretags und der OpenType-Spezifikation finden Sie unter <https://www.microsoft.com/typography/otspec/featuretags.htm> .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Verteilbare Komponente<br/>          | Usp10.dll, Version 1,600 oder höher, onwindows Xpund höher<br/>                |
| Header<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unischreiber](uniscribe.md)
</dt> <dt>

[Uniscristrukturen](uniscribe-structures.md)
</dt> <dt>

[**Scriptgetfontalternateglyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[**Scriptgetfontfeaturetags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[**Scriptgetfontlanguagetags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[**Scriptgetfontscripttags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[**Scriptitemizeopentype**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[**Scriptplaceopentype**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[**Scriptpositionsingleglyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[**Scriptshapeopentype**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[**Scriptsubstitutesingleglyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




