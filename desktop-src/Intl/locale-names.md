---
description: Ein Gebiets Schema Name basiert auf den sprachtagging-Konventionen von RFC 4646 (Windows Vista und höher) und wird durch locale \_ sname dargestellt.
ms.assetid: 221aae7b-3a7c-4995-ae78-50d97de436d8
title: Gebiets Schema Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9808db94615cba4416c12995b9c969eaaf5a3fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348131"
---
# <a name="locale-names"></a>Gebiets Schema Namen

Ein [](locales-and-languages.md) Gebiets Schema Name basiert auf den sprachtagging-Konventionen von RFC 4646 (Windows Vista und höher) und wird durch [locale \_ sname](locale-sname.md)dargestellt. Im Allgemeinen wird das Muster `<language>-<REGION>` verwendet. Hier ist Sprache ein ISO 639-Sprachcode in Kleinbuchstaben. Die Codes aus ISO 639-1 werden verwendet, wenn Sie verfügbar sind. Andernfalls werden Codes aus ISO 639-2/T verwendet. Region gibt einen Bezeichner in Großbuchstaben der ISO 3166-1-Land/Region an. Der Gebiets Schema Name für Englisch (USA) lautet z. b. "en-US", und der Gebiets Schema Name für Divehi (Malediven) ist "DV-MV".

> [!Note]  
> Der Konstante Gebiets Schema [ \_ Name maximale \_ \_ Länge](locale-name-constants.md) gibt die maximale Länge eines Gebiets Schema namens an. Sie enthält Platz für ein abschließendes NULL-Zeichen.

 

Wenn das Gebiets Schema ein neutrales Gebiets Schema (keine Region) ist, folgt der [ \_ sname](locale-sname.md) -Wert des Gebiets Schemas dem Muster `<language>` . Wenn es sich um ein neutrales Gebiets Schema handelt, für das das Skript maßgeblich ist, ist das Muster `<language>-<Script>` .

Wenn ein Gebiets Schema mit einem anderen Skript von einem anderen Gebiets Schema für die gleiche Sprache und Region unterschieden werden muss, \_ folgt der SNAME-Wert des Gebiets Schemas dem Muster `<language>-<Script>-<REGION>` , bei dem es sich bei dem Skript um einen [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html) -Skriptcode für den ersten Beispielsweise \_ ist der Wert für das Gebiets Schema sname für das spezifische Gebiets Schema Uzbek (Latin, Usbekistan) "UZ-Latn-UZ". Die Skript Komponente ist in Fällen nicht enthalten, in denen eine Sprache häufig nur in einem Skript geschrieben wird.

Sortier Reihenfolgen für Gebiets Schemas werden mithilfe von [Sortierreihenfolge-bezeichlern](sort-order-identifiers.md)festgelegt, z \_ . b. Um zwei oder mehr Sortier Reihenfolgen für dieselbe Sprache und Region zu unterscheiden, folgt der Gebiets Schema Name dem Muster `<language>-<REGION>\_<sort order>` . Wenn Sie sowohl das Skript als auch die Sortierreihenfolge unterscheiden müssen, folgt der Name dem Muster `<language>-<Script>-<REGION>\_<sort order>` . Die Standard Sortierreihenfolge wird nie explizit angegeben, sondern nur die Alternative Sortierreihenfolge. Beispielsweise ist Ungarisch (Ungarn) mit dem Sort \_ -Standard oder dem numerisch äquivalenten Sort \_ Hungarian \_ -Standard als "HU-HU" gekennzeichnet. Ungarisch (Ungarn) mit Sortierreihenfolge Sort \_ Hungarian \_ Technical wird als "HU-HU \_ technl" bezeichnet.

Bei einem [Ersatz](custom-locales.md)Gebiets Schema muss der Gebiets Schema Name mit dem Namen für das zu ersetzende Gebiets Schema identisch sein. Bei einem ergänzenden Gebiets Schema sollte der Gebiets Schema Name dem Muster von `<language>-<REGION>-x-<custom>` oder folgen `<language>-<Script>-<REGION>-x-<custom>` , wobei `<custom>` eine alphanumerische Zeichenfolge für das ergänzende Gebiets Schema ist. Beispielsweise könnte ein zusätzliches Gebiets Schema, das für ein Unternehmen mit dem Namen fabricam spezifisch ist, "en-US-x-fabricam" genannt werden.

Eine Anwendung kann die aktuellen Gebiets Schema Namen mithilfe der Funktionen [**getsystemdefaultlocalename**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) und [**getuserdefaultlocalename**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename) abrufen. Obwohl jeder Thread seinen eigenen Gebiets Schema Bezeichner mit [**getthreadlocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) abrufen und festlegen kann und ihn mit [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)festlegen kann, sind keine Analog Funktionen zum Abrufen und Festlegen des Gebiets Schemas mit dem Namen vorhanden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gebiets Schemas und Sprachen](locales-and-languages.md)
</dt> <dt>

[Benutzerdefinierte Gebiets Schemata](custom-locales.md)
</dt> <dt>

[Gebiets Schema Bezeichner](locale-identifiers.md)
</dt> <dt>

[Sortierreihenfolge-IDs](sort-order-identifiers.md)
</dt> </dl>

 

 



