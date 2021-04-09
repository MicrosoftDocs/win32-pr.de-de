---
description: Dieses Thema enthält einige Anweisungen für die Handhabung von benutzerdefinierten Gebiets Schemas in Ihren Anwendungen.
ms.assetid: 2622e2b3-b952-4666-a440-85d73d11c5e0
title: Arbeiten mit benutzerdefinierten Gebiets Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0e59446496ae2985860c0fd6b1bd5bddde084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959222"
---
# <a name="working-with-custom-locales"></a>Arbeiten mit benutzerdefinierten Gebiets Schemas

Dieses Thema enthält einige Anweisungen für die Handhabung von [benutzerdefinierten](custom-locales.md) Gebiets Schemas in Ihren Anwendungen. Es empfiehlt sich, den gesamten Quellcode mit diesen Überlegungen vorzubereiten, da die Anwendung nicht steuert, ob benutzerdefinierte Gebiets Schemas auf dem Betriebssystem installiert werden.

## <a name="handle-locale_stime-constant-correctly"></a>Ordnungsgemäße Handhabung der Schema- \_ stime-Konstante

Wenn Sie über eine ältere Anwendung verfügen, die [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) zum Abrufen des veralteten Zeit Trennzeichens verwendet, das durch [locale \_ stime](locale-stime-constants.md)angegeben wird, kann die Anwendung das Zeitformat nicht analysieren. Beachten Sie, dass das Zeichen, das Stunden von Minuten trennt, sich von dem Zeichen unterscheidet, das Minuten von Sekunden trennt.

> [!Note]  
> Beachten Sie beim Programmieren für benutzerdefinierte Gebiets Schemas, dass Sie ungewöhnlich sind. Praktisch jedes Feld, das für NLS verfügbar ist, muss mit ungewöhnlichem Verhalten zurechtkommen. Beispielsweise ist das Zeitformat 12h34 ' 12 ' ' legitim und im allgemeinen verständlich. Dennoch treffen viele Anwendungen Annahmen über die Zeit Trennzeichen, die Puffer Längen oder Anzeigefelder unterbrechen können.

 

## <a name="distinguish-among-supplemental-locales"></a>Unterscheidung zwischen zusätzlichen Gebiets Schemata

Alle ergänzenden Gebiets Schemas verwenden die benutzerdefinierte Gebiets Schema- [ \_ \_ nicht angegebene](locale-custom-constants.md) Konstante für den Gebiets Schema [Bezeichner](locale-identifiers.md). Als Regel kann [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) nicht zwischen zusätzlichen Gebiets Schemas unterscheiden, sondern [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) , da dabei Gebiets Schema [Namen](locale-names.md) anstelle von Gebiets Schema Bezeichnerzeichen verwendet werden. Die Anwendung kann Informationen zu einem bestimmten ergänzenden Gebiets Schema nur abrufen, wenn dieses Gebiets Schema das aktuell ausgewählte Benutzer Gebiets Schema ist. Anschließend kann die Anwendung [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) aufrufen und den konstanten Gebiets Schema [- \_ Benutzer \_ Standard](locale-user-default.md) als Gebiets Schema Bezeichner übergeben.

## <a name="handle-replacement-locales"></a>Austausch Gebiets Schemas behandeln

Um die Zuverlässigkeit von Windows beizubehalten, denken Sie daran, dass ein von Ihrer Anwendung unterstütztes Ersetzungs Gebiets Schema den Gebiets Schema Bezeichner für das ersetzte Gebiets Schema nicht ändern kann Keines der beiden Ersetzungs Gebiets Schemas kann die Sortierungs Eigenschaften von Windows ändern.

Obwohl ein Ersatz Gebiets Schema den Standardkalender ändern kann, muss es den ursprünglichen Standardwert an einer beliebigen Stelle in der Liste der verfügbaren Kalender beibehalten. Beispielsweise wird für das thailändische Gebiets Schema (Thailand) der buddhistische Thai-Kalender als Standard verwendet. Ein Administrator kann ein Ersatz Gebiets Schema erstellen, in dem der gregorianische lokalisierte Kalender verwendet wird. Die Liste der verfügbaren Kalender enthält jedoch weiterhin einen Eintrag für den thailändischen Thai-Kalender.

Für Ersatz Gebiets Schemata sollte Ihre Anwendung normalerweise Gebiets Schema spezifische Informationen einsehen, anstatt eine "Verknüpfung" basierend auf den Kenntnissen eines bestimmten Gebiets Schemas zu versuchen. Wenn [**getthreadlocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) beispielsweise das aktuelle Gebiets Schema als Englisch (USA) abruft, kann es sich tatsächlich um ein Ersatz Gebiets Schema handeln, das in Kraft treten darf.

## <a name="customize-calendars"></a>Kalender anpassen

Ihre Anwendungen können Tag-und Monatsnamen für gregorianische Kalender, aber nicht für nicht gregorianische Kalender anpassen. Ebenso unterstützt nls die Erstellung benutzerdefinierter Kalender nicht. Weitere Informationen finden Sie unter [Datum und Kalender](date-and-calendar.md).

## <a name="handle-sorting-sequences"></a>Behandeln von Sortier Sequenzen

Ein zusätzliches Gebiets Schema kann eine beliebige von Microsoft definierte Sortierreihenfolge verwenden. Ein Ersatz Gebiets Schema muss dieselbe Sortierreihenfolge wie das Gebiets Schema verwenden, das es ersetzt. NLS unterstützt das Erstellen von benutzerdefinierten Sortier Sequenzen nicht. Weitere Informationen finden Sie unter [Handling Sortieren in Ihren Anwendungen](handling-sorting-in-your-applications.md).

## <a name="localize-custom-locale-information"></a>Lokalisieren von benutzerdefinierten Gebiets Schema Informationen

NLS stellt keinen Mechanismus zum Lokalisieren von benutzerdefinierten Gebiets Schema Informationen bereit. Daher ruft die [Konstante locale \_ SLanguage](locale-slanguage.md) oder das Gebiets Schema [ \_ slocalizedlanguagename](locale-slocalized-constants.md) , das als Gebiets Schema Bezeichner für ein benutzerdefiniertes Gebiets Schema verwendet wird, immer Werte ab, die dem Gebiets [ \_ Schema snativelangname](locale-snative-constants.md) oder [locale \_ snativelanguagename](locale-snative-constants.md)zugeordnet sind

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprache](using-national-language-support.md)
</dt> <dt>

[Benutzerdefinierte Gebiets Schemata](custom-locales.md)
</dt> <dt>

[Datum und Kalender](date-and-calendar.md)
</dt> <dt>

[Behandeln von Sortierungen in Ihren Anwendungen](handling-sorting-in-your-applications.md)
</dt> </dl>

 

 



