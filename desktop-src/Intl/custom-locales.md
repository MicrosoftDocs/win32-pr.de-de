---
description: Benutzerdefinierte Gebietsschemas
ms.assetid: 110efeab-c02f-4244-8950-a975cfc91e8a
title: Benutzerdefinierte Gebietsschemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda75d0d097bf6860e1385bb2557d56c2b2d2a1df530404781817590e381b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754920"
---
# <a name="custom-locales"></a>Benutzerdefinierte Gebietsschemas

**Windows Vista und höher:** Benutzerdefinierte Gebietsschemas unterstützen internationale Eigenschaften, die eine kulturell geeignetere Benutzeroberfläche bieten als diejenigen, die mit den standard-Gebietsschemas ausgestattet sind, die von Microsoft mit dem Betriebssystem ausgeliefert werden. Mithilfe von benutzerdefinierten Gebietsschemas können Administratoren den von Microsoft bereitgestellten Gebietsschemasatz erweitern oder die Daten in einem Gebietsschema ersetzen, das mit Windows geliefert wird, z. B. Währungssymbole oder Namen der Monate des Jahres.

Die beiden Typen von benutzerdefinierten Gebietsschemas sind zusätzliche Gebietsschemas und Ersetzungsschemas. Zusätzliche Gebietsschemas sind benutzerdefinierte Gebietsschemas, die es Unternehmen, Universitäten, Behörden und anderen Dritten ermöglichen, Gebietsschemadaten zu erstellen, die im Versandbetriebssystem nicht verfügbar sind. Ersetzungsschemas sind benutzerdefinierte Gebietsschemas, die mit dem Betriebssystem versendet werden, ohne die [Gebietsschemabezeichner](locale-identifiers.md) oder [Gebietsschemanamen](locale-names.md)zu ändern.

Sie können das von NLS bereitgestellte Hilfsprogramm Locale Builder verwenden, um benutzerdefinierte Gebietsschemas zu erstellen. Weitere Informationen finden Sie unter [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158). Anweisungen zum Verwenden von benutzerdefinierten Gebietsschemas in Ihren Anwendungen finden Sie unter [Arbeiten mit benutzerdefinierten Gebietsschemas.](working-with-custom-locales.md)

## <a name="comparison-of-custom-locale-types"></a>Vergleich von benutzerdefinierten Gebietsschematypen

In der folgenden Tabelle werden die Unterschiede zwischen ergänzenden Gebietsschemas und Ersetzungsschemas beschrieben.



| Element                                                                                                                           | Zusätzliches Gebietsschema                                                                                                                                                                                                                   | Ersetzungsschema                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kalender                                                                                                                      | Kann einen der von Microsoft bereitgestellten Kalender enthalten. Mindestens einer der bereitgestellten Kalender muss der gregorianische lokalisierte Kalender sein.                                                                                              | Kann einen der von Microsoft bereitgestellten Kalender enthalten. Mindestens einer der bereitgestellten Kalender muss der gregorianische lokalisierte Kalender sein, und die Sammlung muss den Standardkalender des ersetzten Gebietsschemas enthalten. |
| Sortierung                                                                                                                        | Kann eine der von Microsoft bereitgestellten Sortierungen verwenden.                                                                                                                                                                                          | Behält das Sortierverhalten des Gebietsschemas bei, das ersetzt wird.                                                                                                                                                            |
| Tag- und Monatsnamen                                                                                                            | Kann nur für den gregorianischen Standardkalender angepasst werden, nicht für nicht gregorianische Kalender und nicht für spezialisierte gregorianische Kalender, z. B. den gregorianischen Kalender im Mittleren Osten.                                           | Identisch mit für zusätzliches Gebietsschema.                                                                                                                                                                                      |
| Sprachname ([LOCALE \_ SLANGUAGE](locale-slanguage.md) oder [LOCALE \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)) | Gibt [LOCALE \_ SNATIVELANGNAME](locale-snative-constants.md) oder [LOCALE \_ SNATIVELANGUAGENAME](locale-snative-constants.md)zurück.                                                                                                       | Behält den Sprachnamen des Gebietsschemas bei, das ersetzt wird.                                                                                                                                                                 |
| Gebietsschemabezeichner                                                                                                              | Legen Sie diese Einstellung auf [LOCALE \_ CUSTOM \_ UNSPECIFIED](locale-custom-constants.md) fest, es sei denn, das Gebietsschema ist das aktuell ausgewählte Gebietsschema Standards und Formate des Benutzers. In diesem Fall ist es auf [LOCALE \_ CUSTOM \_ DEFAULT](locale-custom-constants.md)festgelegt. | Behält den Gebietsschemabezeichner des Gebietsschemas bei, das ersetzt wird.                                                                                                                                                             |
| Gebietsschemaname                                                                                                                    | Willkürlich; sollte dem Muster entsprechen, das unter [Gebietsschemanamen](locale-names.md)erläutert wird.                                                                                                                                                      | Behält den Gebietsschemanamen des Gebietsschemas bei, das ersetzt wird.                                                                                                                                                                   |



 

## <a name="supplemental-locale-examples"></a>Beispiele für zusätzliche Gebietsschemas



| Gebietsschemaname    | Beschreibung                                                                                                                                                                                                                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-CA-fabricam | Fabricam ist ein pc-Hersteller in Kanada mit Niederlassungen weltweit. Um ein konsistentes Benutzeroberflächenverhalten für alle Computer zu gewährleisten, entwickelt das Unternehmen ein Gebietsschema für die unternehmensweite Verwendung.                                                                                                                                                          |
| fr-US          | Die Woodlawn Bank verwendet Windows XP Embedded für ihre automatisierten Geldautomaten (ATMs), die von der Bank über Nordamerika mit Benutzeroberflächen in Französisch, Englisch und Spanisch ausgeliefert werden. Um eine konsistente Benutzererfahrung zu gewährleisten, erstellt die Bank ein Gebietsschema für Französisch in der USA, das USA Formaten, aber namen für französische Tage und Monate hat. |



 

## <a name="replacement-locale-example"></a>Beispiel für ein Ersetzungsschema



| Gebietsschemaname | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-US       | Fabricam ist ein pc-Hersteller in Kanada mit Niederlassungen weltweit. Um ein konsistentes Benutzeroberflächenverhalten für alle Computer zu gewährleisten, entwickelt das Unternehmen ein Gebietsschema für die unternehmensweite Verwendung. Er verwendet eine 24-Stunden-Uhr, verhält sich aber andernfalls wie das unterstützte Gebietsschema für Englisch (USA). Da das benutzerdefinierte Gebietsschema dem unterstützten Gebietsschema so ähnlich ist, beschließt Fabricam, es als Ersatzschema anstelle eines zusätzlichen Gebietsschemas zu implementieren. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gebietsschemas und Sprachen](locales-and-languages.md)
</dt> <dt>

[Arbeiten mit benutzerdefinierten Gebietsschemas](working-with-custom-locales.md)
</dt> </dl>

 

 



