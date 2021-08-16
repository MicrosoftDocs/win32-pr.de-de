---
description: Der Begriff &\# 0034;Sprache&0034; gibt eine Auflistung von Eigenschaften an, die in gesprochener und \# geschriebener Kommunikation verwendet werden.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Lokal und Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462fc66a3296312de73a472309457e12954b6f30c80857594808350306bf4994
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147153"
---
# <a name="locales-and-languages"></a>Lokal und Sprachen

Der Begriff "Sprache" gibt eine Auflistung von Eigenschaften an, die in gesprochener und geschriebener Kommunikation verwendet werden. Jede Sprache verfügt über einen Sprachnamen und einen Sprachbezeichner, die die bestimmte Codepage (ANSI, DOS, Macintosh) angeben, die zum Darstellen des geografischen Standorts für die Sprache im Betriebssystem verwendet wird. [](code-pages.md) [](table-of-geographical-locations.md) Eine neutrale Sprache wird durch einen Namen wie "en" für Englisch angegeben. Eine geografisch spezifischere Sprache kann durch einen Namen angegeben werden, der sowohl Informationen zum Land/zur Region als auch zum Land enthält. Beispielsweise hat das Locale English (USA) den Sprachnamen "en-US".

Ein "Locale" ist eine Auflistung sprachbezogener Benutzerpräferenzinformationen, die als Liste von Werten dargestellt werden. Windows XP unterstützt mehr als 150 Windows Vista etwa 200. Jedes Locale wird durch eine Sprache und eine Sortierreihenfolge definiert und verfügt sowohl über einen Locale-Namen als auch über einen Locale Identifier. Ein Beispiel für einen Locale-Namen für Deutsch (Deutschland) ist "de-DE \_ phonebook".

Jedes Betriebssystem verfügt über mindestens ein installiertes Locale und verfügt häufig über viele Lokale, aus denen der Benutzer auswählen kann. Jedem Locale sind eine Vielzahl von Informationen zugeordnet, mit Anderen als dem Namen und Bezeichner. Locale information types are described in [Locale Information Constants](locale-information-constants.md).

Das Betriebssystem weist jedem Thread ein -Locale zu und weist zunächst das durch LOCALE SYSTEM DEFAULT definierte "Standard-System-Locale" [ \_ \_ zu.](locale-system-default.md) Dieses Locale wird festgelegt, wenn das Betriebssystem installiert ist oder wenn der Benutzer es mithilfe des Regionalen und Sprachoptionenbereichs des Systemsteuerung. Beim Ausführen eines Threads in einem Prozess, der dem Benutzer gehört, weist das Betriebssystem dem Thread das Standard-Benutzer-Locale zu. Dieses Locale wird durch [LOCALE \_ USER DEFAULT \_ definiert.](locale-user-default.md) Eine Anwendung kann beide Standardeinstellungen überschreiben, indem sie die [**SetThreadLocale-Funktion**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) verwendet, um das Locale für einen Thread explizit fest zu legen.

Die Implementierung einer Sprache erfordert ein entsprechendes -Locale. Das Betriebssystem implementiert eine neutrale Sprache, indem es die Daten für das Einer bestimmten Version der Sprache zugeordnete Gebiet auswählt, in der Regel das am weitesten verbreitete Gebiet.

Ab Windows Vista ist es möglich, dass eine bestimmte Sprache einem zusätzlichen Locale entspricht, bei dem es sich um einen Typ von benutzerdefiniertem Locale handelt. Da ergänzende Locales alle einen einzigen Locale-Bezeichner gemeinsam nutzen, sollten Ihre Anwendungen diese Locales und die entsprechenden Sprachen nach Namen und nicht nach Bezeichner verarbeiten.

Sprachkonzepte sind eng mit Dem-Locale-Konzepten verknüpft, aber die beiden Begriffe sind nicht austauschbar. Allgemein gilt: Funktionen, die [](multilingual-user-interface.md) sich auf die mehrsprachige Benutzeroberfläche, befassen sich mit Sprachen, während die NLS-Funktionen auf Dies gilt.

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Benutzerdefinierte Locales](custom-locales.md)
-   [Sprachen-IDs](language-identifiers.md)
-   [Sprachnamen](language-names.md)
-   [Locale Identifiers](locale-identifiers.md)
-   [Locale Names](locale-names.md)
-   [Pseudo-Locales](pseudo-locales.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Unterstützung der Landessprache](about-national-language-support.md)
</dt> <dt>

[Codepages](code-pages.md)
</dt> <dt>

[Locale Information Constants](locale-information-constants.md)
</dt> <dt>

[Multilingual User Interface](multilingual-user-interface.md)
</dt> <dt>

[Tabelle der geografischen Standorte](table-of-geographical-locations.md)
</dt> <dt>

[Benutzeroberfläche-Sprachverwaltung](user-interface-language-management.md)
</dt> <dt>

[**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



