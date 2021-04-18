---
description: Der Begriff &\# 0034; Sprache&\# 0034; gibt eine Sammlung von Eigenschaften an, die bei der gesprochenen und geschriebenen Kommunikation verwendet werden.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Gebiets Schemas und Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2c0d0fa41b9186b2135d9497d52de24577bbae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357412"
---
# <a name="locales-and-languages"></a>Gebiets Schemas und Sprachen

Der Begriff "Sprache" gibt eine Sammlung von Eigenschaften an, die bei der gesprochenen und geschriebenen Kommunikation verwendet werden. Jede Sprache verfügt über einen Sprachnamen und einen sprach Bezeichner, der die jeweilige [Codepage](code-pages.md) (ANSI, DOS, Macintosh) angibt, die zum Darstellen des [geografischen Standorts](table-of-geographical-locations.md) für die Sprache des Betriebssystems verwendet wird. Eine neutrale Sprache wird durch einen Namen wie "en" für Englisch angegeben. Eine geografisch spezifischere Sprache kann durch einen Namen angegeben werden, der sowohl Gebiets Schema-als auch Land-/Regionsinformationen enthält. Beispielsweise hat das Gebiets Schema Englisch (USA) den Sprachen Namen "en-US".

Ein "Gebiets Schema" ist eine Sammlung von sprachbezogenen Benutzer Einstellungs Informationen, die als Liste von Werten dargestellt werden. Windows XP unterstützt mehr als 150 Gebiets Schemas, und Windows Vista unterstützt etwa 200. Jedes Gebiets Schema wird durch eine Sprache und eine Sortierreihenfolge definiert und verfügt sowohl über einen Gebiets Schema Namen als auch über einen Gebiets Schema Bezeichner. Ein Beispiel für einen Gebiets Schema Namen für Deutsch (Deutschland) ist "de-de \_ Phonebook".

Jedes Betriebssystem verfügt über mindestens ein installiertes Gebiets Schema und verfügt häufig über viele Gebiets Schemas, aus denen der Benutzer auswählen kann. Jedes Gebiets Schema verfügt über eine Vielzahl von Informationen, die mit dem Namen und Bezeichner verknüpft sind. Gebiets Schema Informationstypen werden unter "Gebiets Schema [Informations Konstanten](locale-information-constants.md)" beschrieben.

Das Betriebssystem weist jedem Thread ein Gebiets Schema zu und weist anfänglich das "System Standard Gebiets Schema" zu, das durch das Gebiets Schema [ \_ System \_ default](locale-system-default.md)definiert ist. Dieses Gebiets Schema wird festgelegt, wenn das Betriebssystem installiert wird, oder wenn der Benutzer es mithilfe der Optionen Regions-und Sprachoptionen der Systemsteuerung auswählt. Beim Ausführen eines Threads in einem Prozess, der dem Benutzer angehört, weist das Betriebssystem dem Thread das Standard Gebiets Schema des Benutzers zu. Dieses Gebiets Schema wird von der [locale \_ User \_ default](locale-user-default.md)definiert. Eine Anwendung kann beide Standardeinstellungen überschreiben, indem Sie die [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) -Funktion verwendet, um das Gebiets Schema für einen Thread explizit festzulegen.

Die Implementierung einer Sprache erfordert ein entsprechendes Gebiets Schema. Das Betriebssystem implementiert eine neutrale Sprache durch Auswahl der Daten für das Gebiets Schema, das einer bestimmten Version der Sprache zugeordnet ist, in der Regel das am weitesten verbreitete Gebiets Schema.

Ab Windows Vista ist es möglich, dass eine bestimmte Sprache einem ergänzenden Gebiets Schema entspricht, bei dem es sich um eine Art benutzerdefiniertes Gebiets Schema handelt. Da ergänzende Gebiets Schemas alle einen einzelnen Gebiets Schema Bezeichner gemeinsam nutzen, sollten Ihre Anwendungen diese Gebiets Schemas und die entsprechenden Sprachen nach Namen anstelle von Bezeichner verarbeiten.

Sprach Konzepte sind eng mit Gebiets Schema Konzepten verknüpft, aber die beiden Begriffe sind nicht austauschbar. Im Allgemeinen sind Funktionen, die sich auf die [mehrsprachige Benutzeroberfläche](multilingual-user-interface.md) beziehen, mit Sprachen zu tun, während die NLS-Funktionen auf Gebiets Schemas reagieren.

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Benutzerdefinierte Gebiets Schemata](custom-locales.md)
-   [Sprachen-IDs](language-identifiers.md)
-   [Sprachnamen](language-names.md)
-   [Gebiets Schema Bezeichner](locale-identifiers.md)
-   [Gebiets Schema Namen](locale-names.md)
-   [Pseudo Gebiets Schemata](pseudo-locales.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Unterstützung der Landessprache](about-national-language-support.md)
</dt> <dt>

[Codepages](code-pages.md)
</dt> <dt>

[Gebiets Schema Informations Konstanten](locale-information-constants.md)
</dt> <dt>

[Multilingual User Interface](multilingual-user-interface.md)
</dt> <dt>

[Tabelle der geografischen Standorte](table-of-geographical-locations.md)
</dt> <dt>

[Sprach Verwaltung in der Benutzeroberfläche](user-interface-language-management.md)
</dt> <dt>

[**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



