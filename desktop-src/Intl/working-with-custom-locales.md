---
description: Dieses Thema enthält einige Anweisungen für die Behandlung benutzerdefinierter Locales in Ihren Anwendungen.
ms.assetid: 2622e2b3-b952-4666-a440-85d73d11c5e0
title: Arbeiten mit benutzerdefinierten Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a969681e685a7044f9c583c907515a51559866d28d997cf43fa639127eee27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680930"
---
# <a name="working-with-custom-locales"></a>Arbeiten mit benutzerdefinierten Locales

Dieses Thema enthält einige Anweisungen für die Behandlung [benutzerdefinierter Locales](custom-locales.md) in Ihren Anwendungen. Es ist am besten, den Quellcode unter Berücksichtigung dieser Überlegungen vorzubereiten, da Ihre Anwendung nicht kontrolliert, ob benutzerdefinierte Lokale auf dem Betriebssystem installiert sind.

## <a name="handle-locale_stime-constant-correctly"></a>Korrektes Behandeln der \_ LOCALE-STIME-Konstante

Wenn Sie über eine ältere Anwendung verfügen, die [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) verwendet, um das durch [LOCALE \_ STIME](locale-stime-constants.md)angegebene veraltete Zeittrennzeichen zu erhalten, kann die Anwendung das Zeitformat nicht analysieren. Beachten Sie, dass sich das Zeichen, das Stunden von Minuten trennt, von dem Zeichen abtrennt, das Minuten von Sekunden trennt.

> [!Note]  
> Beachten Sie bei der Programmierung für benutzerdefinierte Lokales, dass sie ungewöhnlich sind. Praktisch jedes für NLS verfügbare Feld muss mit ungewöhnlichem Verhalten umgehen. Beispielsweise ist das Zeitformat 12H34'12'' legitim und allgemein verständlich. Viele Anwendungen machen jedoch Annahmen über die Zeittrennzeichen, die Pufferlängen oder Anzeigefelder unterbricht.

 

## <a name="distinguish-among-supplemental-locales"></a>Unterscheiden zwischen ergänzenden Locales

Alle zusätzlichen Locales verwenden die [LOCALE \_ CUSTOM \_ UNSPECIFIED-Konstante](locale-custom-constants.md) für den [Locale Identifier](locale-identifiers.md). In der Regel kann [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) nicht zwischen ergänzenden Locales unterscheiden, [](locale-names.md) aber [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) kann, da es Anstelle von Locale-Bezeichnern Locale-Namen verwendet. Ihre Anwendung kann Informationen zu einem bestimmten zusätzlichen Locale nur abrufen, wenn es sich bei diesem Locale um das aktuell ausgewählte Benutzer-Locale handelt. Anschließend kann die Anwendung [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) aufrufen und die Konstante [LOCALE \_ USER \_ DEFAULT](locale-user-default.md) als Locale Identifier übergeben.

## <a name="handle-replacement-locales"></a>HandleErsetzungs-Locales

Denken Sie daran, dass ein Windows, das von Ihrer Anwendung unterstützt wird, den Locale Identifier des ersetzten Locale nicht ändern kann, um die Zuverlässigkeit des ersetzten Windows zu gewährleisten. Kein Ersatz-Locale kann die Sortiereigenschaften der Windows.

Obwohl ein Ersatz-Locale den Standardkalender ändern kann, muss der ursprüngliche Standardwert an einer bestimmten Stelle in der Liste der verfügbaren Kalender beibehalten werden. Das Thailändisch -Locale (Thai) verwendet beispielsweise den thailändisch-Kalender als Standard. Ein Administrator kann ein Ersatz-Locale erstellen, das den gregorianischen lokalisierten Kalender verwendet. Die Liste der verfügbaren Kalender enthält jedoch weiterhin einen Eintrag für den Thai-Kalender.

Für Ersetzungs-Locales sollte Ihre Anwendung in der Regel die für das Lokale spezifischen Informationen lesen, anstatt basierend auf dem Wissen über ein bestimmtes Locale eine "Verknüpfung" zu versuchen. Wenn [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) z. B. das aktuelle Locale als Englisch (USA) abruft, kann es tatsächlich ein Ersatz-Locale sein, das wirksam werden soll.

## <a name="customize-calendars"></a>Anpassen von Kalendern

Ihre Anwendungen können Tag- und Monatsnamen für gregorianische Kalender anpassen, jedoch nicht für nicht gregorianische Kalender. Ebenso unterstützt NLS die Erstellung benutzerdefinierter Kalender nicht. Weitere Informationen finden Sie unter [Datum und Kalender.](date-and-calendar.md)

## <a name="handle-sorting-sequences"></a>Verarbeiten von Sortiersequenzen

Ein zusätzliches Locale kann eine beliebige von Microsoft definierte Sortierreihenfolge verwenden. Ein Ersatz-Locale muss dieselbe Sortierreihenfolge wie das von ihm ersetzte Locale verwenden. NLS unterstützt die Erstellung benutzerdefinierter Sortiersequenzen nicht. Weitere Informationen finden Sie unter [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).

## <a name="localize-custom-locale-information"></a>Lokalisieren benutzerdefinierter Locale-Informationen

NLS bietet keinen Mechanismus zum Lokalisieren benutzerdefinierter Locale-Informationen. Daher ruft die Konstante [LOCALE \_ SLANGUAGE](locale-slanguage.md) oder [LOCALE \_ SLOCALIZEDLANGUAGENAME,](locale-slocalized-constants.md) die als Locale Identifier für ein benutzerdefiniertes Locale verwendet wird, immer Werte ab, die [LOCALE \_ SNATIVELANGNAME](locale-snative-constants.md) oder [LOCALE \_ SNATIVELANGUAGENAME zugeordnet](locale-snative-constants.md)sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung der Landessprache](using-national-language-support.md)
</dt> <dt>

[Benutzerdefinierte Locales](custom-locales.md)
</dt> <dt>

[Datum und Kalender](date-and-calendar.md)
</dt> <dt>

[Behandeln der Sortierung in Ihren Anwendungen](handling-sorting-in-your-applications.md)
</dt> </dl>

 

 



