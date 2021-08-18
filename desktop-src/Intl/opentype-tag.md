---
description: Definiert ein 4-Byte-Array, das vier 8-Bit-ASCII-Werte für Leerzeichen, A-Z oder a-z enthält, um OpenType-Skript-, Sprach- und Schriftartfeaturetags zu identifizieren.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (Usp10.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c784fa7f6243e7e5444dcbc64c690ce7184d6ace469759c19be9de87854732
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040780"
---
# <a name="opentype_tag"></a>\_OPENTYPE-TAG

Definiert ein 4-Byte-Array, das vier 8-Bit-ASCII-Werte für Leerzeichen, A-Z oder a-z enthält, um OpenType-Skript-, Sprach- und Schriftartfeaturetags zu identifizieren.


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a>Hinweise

In den folgenden Beispielen werden Darstellungen von OpenType-Featuretags definiert.

-   Das Featuretag für das Feature "ligature" ist "liga".
-   Die Sprachtags für "Deutsch", "Urdu" und "Deutsch" sind "ROM", "URD" bzw. "FAR". Beachten Sie, dass jedes dieser Tags mit einem Leerzeichen endet.
-   Die Skripttags für lateinische und arabische Skripts sind "latn" bzw. "arabisch".

Weitere Informationen zu OpenType-Featuretags und zur OpenType-Spezifikation finden Sie unter <https://www.microsoft.com/typography/otspec/featuretags.htm> .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Verteilbare Komponente<br/>          | Usp10.dll Version 1.600 oder höher unterWindows XPand höher<br/>                |
| Header<br/>                   | <dl> <dt>Usp10.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Uniscribe-Strukturen](uniscribe-structures.md)
</dt> <dt>

[**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




