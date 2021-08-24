---
description: Ein Locale Name basiert auf den Sprachtagingkonventionen von RFC 4646 (Windows Vista und höher) und wird durch LOCALE \_ SNAME dargestellt.
ms.assetid: 221aae7b-3a7c-4995-ae78-50d97de436d8
title: Locale Names
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed4c09900544e96c0f05166d1f4054972e9d8ff89fc108c185695a7506859bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147402"
---
# <a name="locale-names"></a>Locale Names

Ein [Locale-Name](locales-and-languages.md) basiert auf den Konventionen für Sprachtags von RFC 4646 (Windows Vista und höher) und wird durch [LOCALE \_ SNAME dargestellt.](locale-sname.md) Im Allgemeinen wird das `<language>-<REGION>` Muster verwendet. Hier ist die Sprache ein Iso 639-Sprachcode in Kleinbuchstaben. Die Codes aus ISO 639-1 werden verwendet, wenn sie verfügbar sind. Andernfalls werden Codes aus ISO 639-2/T verwendet. REGION gibt einen Iso 3166-1-Länder-/-Regionbezeichner in Großbuchstaben an. Der Name des Locale für Englisch (USA) ist z. B. "en-US", und der Name des Locale für Divehi (Wird) ist "dv-MV".

> [!Note]  
> Die Konstante [LOCALE \_ NAME MAX \_ \_ LENGTH](locale-name-constants.md) gibt die maximale Länge eines Locale-Namens an. Sie enthält Leerzeichen für ein beendendes NULL-Zeichen.

 

Wenn das Locale ein neutrales Locale (keine Region) ist, folgt der [LOCALE \_ SNAME-Wert](locale-sname.md) dem Muster `<language>` . Wenn es sich um ein neutrales Locale handelt, für das das Skript von Bedeutung ist, ist das Muster `<language>-<Script>` .

Wenn ein Locale mithilfe eines anderen Skripts von einem anderen Locale für dieselbe Sprache und Region unterschieden werden muss, folgt der LOCALE-SNAME-Wert dem Muster , wobei Script ein \_ `<language>-<Script>-<REGION>` ISO [15924-Skriptcode](https://www.unicode.org/iso15924/iso15924-codes.html) mit Anfangsbuchstaben ist. Beispielsweise ist der LOCALE SNAME-Wert für das spezifische \_ Locale Uzill (Lateinisch, Uz-Latn-UZ). Die Skriptkomponente ist nicht in Fällen enthalten, in denen eine Sprache häufig nur in einem Skript geschrieben wird.

Sortierreihenfolge für Locales wird mithilfe von [Sortierreihenfolgebezeichnern](sort-order-identifiers.md)festgelegt, z. B. SORT \_ DEFAULT. Um zwei oder mehr Sortierreihenfolge für dieselbe Sprache und Region zu unterscheiden, folgt der Name des Locale dem Muster `<language>-<REGION>\_<sort order>` . Wenn Sie sowohl das Skript als auch die Sortierreihenfolge unterscheiden müssen, folgt der Name dem Muster `<language>-<Script>-<REGION>\_<sort order>` . Die Standardsortierreihenfolge wird nie explizit angegeben, sondern nur die alternative Sortierreihenfolge. Beispielsweise wird "Hu-HU" für "Hu-HU" festgelegt, z.B. "Numerisch "Sort default" oder \_ \_ \_ "SORT NUMERISCH DEFAULT". \_ \_ "Hu-HU technl" ist "Hu-HU \_ technl" für "Hu-HU".

Für ein [Ersatz-Locale](custom-locales.md)muss der Name des Locale mit dem Namen für das zu ersetzende Locale identisch sein. Bei einem ergänzenden Locale sollte der Name des Locale dem Muster von oder entsprechen, wobei eine `<language>-<REGION>-x-<custom>` `<language>-<Script>-<REGION>-x-<custom>` alphanumerische Zeichenfolge ist, die spezifisch für das zusätzliche `<custom>` Locale ist. Ein zusätzliches, für ein Unternehmen spezifisches Locale namens Fabricam kann beispielsweise "en-US-x-fabricam" genannt werden.

Eine Anwendung kann die aktuellen Locale-Namen mithilfe der [**Funktionen GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) und [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename) abrufen. Während jeder Thread mit [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) seinen eigenen Locale-Bezeichner abrufen und festlegen und mit [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)festlegen kann, gibt es keine analogen Funktionen zum Abrufen und Festlegen des Locale nach Name.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lokal und Sprachen](locales-and-languages.md)
</dt> <dt>

[Benutzerdefinierte Locales](custom-locales.md)
</dt> <dt>

[Locale Identifiers](locale-identifiers.md)
</dt> <dt>

[Bezeichner der Sortierreihenfolge](sort-order-identifiers.md)
</dt> </dl>

 

 



