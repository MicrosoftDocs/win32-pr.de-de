---
description: Verwenden von persistenten Gebiets Schema Daten
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: Verwenden von persistenten Gebiets Schema Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4fe4990da53e4db9f71b2feffbd9eb40aedee9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869076"
---
# <a name="using-persistent-locale-data"></a>Verwenden von persistenten Gebiets Schema Daten

Eine globalisierte Anwendung speichert oder überträgt häufig Daten, z. b. Datum und Uhrzeit. Beachten Sie bei der Entscheidung, wie Ihre Anwendung die Daten Persistenz verarbeiten soll,, dass die Daten nicht garantiert identisch mit dem Computer oder zwischen den Ausführungen der Anwendung sind. Dies gilt [für beide Gebiets](locales-and-languages.md) Schemas, die mit Windows und [benutzerdefinierten](custom-locales.md)Gebiets Schemata ausgeliefert werden.

Beim Entwerfen der Anwendung müssen eine Vielzahl von Gebiets Schema bezogenen Datenänderungen berücksichtigt werden, die auftreten können. Beispiel:

-   Währungssymbole können sich ändern, wenn Länder den Euro annehmen.
-   Regionale Einstellungen können sich ändern. Beispielsweise kann das Format d/m/y für ein bestimmtes Gebiets Schema in das Format m/d/y geändert werden.
-   Die Schreibweise von Tagnamen kann aufgrund von Rechtschreibreform geändert werden. Außerdem können sich die Groß-/Kleinschreibung für Monats-oder Tages Namen ändern

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a>Verwenden von Locale-Independent Formaten für den Speicher-und Datenaustausch

Eine Anwendung, die Daten beibehält, sollte Gebiets Schema unabhängige Formate für den Speicher-und Datenaustausch verwenden. Beispiele sind hart codierte oder Standardformate. Der invariante Gebiets [Schema \_ Name \_ ](locale-name-constants.md)für das Gebiets Schema und binäre Speicherformate.

Wenn persistente Sortier Daten erforderlich sind, muss die Anwendung die [**comparestringordinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) -Funktion verwenden. Beachten Sie, dass ein invarianter Format nicht für die [Sortierung](sorting.md)invariante bleibt, sondern nur für Gebiets Schema-und Kalenderdaten.

## <a name="use-the-user-default-locale-for-data-presentation"></a>Verwenden des Standard Gebiets Schemas für die Datenpräsentation

Um persistente Daten darzustellen, empfiehlt es sich, die Daten mit dem Standard Gebiets Schema des Benutzers neu zu formatieren. Die Verwendung dieses Gebiets Schemas ermöglicht Benutzer Überschreibungen. Weitere Informationen finden Sie unter [locale \_ User \_ default](locale-user-default.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprache](using-national-language-support.md)
</dt> <dt>

[Benutzerdefinierte Gebiets Schemata](custom-locales.md)
</dt> <dt>

[Sortierung](sorting.md)
</dt> </dl>

 

 



