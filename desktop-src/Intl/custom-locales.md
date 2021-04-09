---
description: Benutzerdefinierte Gebietsschemas
ms.assetid: 110efeab-c02f-4244-8950-a975cfc91e8a
title: Benutzerdefinierte Gebietsschemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50108750fb1209aa210b04d8be9adcd48e5fd308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960570"
---
# <a name="custom-locales"></a>Benutzerdefinierte Gebietsschemas

**Windows Vista und höher:** Benutzerdefinierte Gebiets Schemas unterstützen internationale Eigenschaften, die eine kulturell geeignetere Benutzer Leistung bieten als solche, die mit dem Betriebssystem von Microsoft geliefert werden. Durch die Verwendung von benutzerdefinierten Gebiets Schemas können Administratoren die von Microsoft bereitgestellten Gebiets Schemas erweitern oder die Daten in einem Gebiets Schema ersetzen, das mit Windows ausgeliefert wird, z. b. Währungssymbole oder Namen der Monate des Jahrs.

Die zwei Arten von benutzerdefinierten Gebiets Schemas sind ergänzende Gebiets Schemata und Ersatz Gebiets Schemas. Ergänzende Gebiets Schemata sind benutzerdefinierte Gebiets Schemas, mit denen Unternehmen, Universitäten, Behörden und andere dritte Gebiets Schema Daten erstellen können, die im Liefer Betriebssystem nicht verfügbar sind. Ersatz Gebiets Schemas sind benutzerdefinierte Gebiets Schemas, die mit dem Betriebssystem ausgeliefert werden, ohne die Gebiets Schema- [IDs oder Gebiets](locale-identifiers.md) Schema [Namen](locale-names.md)

Zum Erstellen von benutzerdefinierten Gebiets Schemas können Sie das von NLS bereitgestellte Hilfsprogramm "Locale Builder" verwenden Weitere Informationen finden Sie unter [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158). Anweisungen zum Verwenden von benutzerdefinierten Gebiets Schemas in Ihren Anwendungen finden Sie unter [Arbeiten mit benutzerdefinierten](working-with-custom-locales.md)Gebiets Schemas.

## <a name="comparison-of-custom-locale-types"></a>Vergleich zwischen benutzerdefinierten Gebiets Schema Typen

In der folgenden Tabelle werden die Unterschiede zwischen ergänzenden und Ersatz Gebiets Schemas beschrieben.



| Element                                                                                                                           | Zusätzliches Gebiets Schema                                                                                                                                                                                                                   | Ersatz Gebiets Schema                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kalender                                                                                                                      | Kann jeden der von Microsoft bereitgestellten Kalender einschließen. Mindestens einer der bereitgestellten Kalender muss der gregorianische lokalisierte Kalender sein.                                                                                              | Kann jeden der von Microsoft bereitgestellten Kalender einschließen. Mindestens einer der bereitgestellten Kalender muss der gregorianische lokalisierte Kalender sein, und die Auflistung muss den Standardkalender des ersetzten Gebiets Schemas enthalten. |
| Sortierung                                                                                                                        | Kann beliebige von Microsoft bereitgestellte Sortierungen verwenden.                                                                                                                                                                                          | Behält das Sortier Verhalten des Gebiets Schemas bei, das ersetzt wird.                                                                                                                                                            |
| Tag-und Monatsnamen                                                                                                            | Kann nur für den gregorianischen Standardkalender, nicht für nicht gregorianische Kalender, nicht für spezialisierte gregorianische Kalender (z. b. den gregorianischen Kalender für den Nahen Osten Französisch) angepasst werden.                                           | Identisch mit dem ergänzenden Gebiets Schema.                                                                                                                                                                                      |
| Sprachen Name ([ \_ Gebiets Schema ssprache oder Gebiets](locale-slanguage.md) Schema [ \_ slocalizedlanguagename](locale-slocalized-constants.md)) | Gibt das Gebiets [ \_ Schema snativelangname](locale-snative-constants.md) oder [locale \_ snativelanguagename](locale-snative-constants.md)zurück.                                                                                                       | Behält den Sprachnamen des Gebiets Schemas bei, das ersetzt wird.                                                                                                                                                                 |
| Gebiets Schema Bezeichner                                                                                                              | Auf Gebiets [Schema \_ Benutzer \_ ](locale-custom-constants.md) definiert festgelegt, es sei denn, das Gebiets Schema ist der aktuell ausgewählte Standard für Standards und Formate des Benutzers. in diesem Fall ist es auf [ \_ benutzerdefiniertes \_ ](locale-custom-constants.md)Gebiets Schema festgelegt. | Speichert den Gebiets Schema Bezeichner des Gebiets Schemas, das ersetzt wird.                                                                                                                                                             |
| Gebiets Schema Name                                                                                                                    | Liches sollte an das in Gebiets Schema [Namen](locale-names.md)erörterte Muster angepasst werden.                                                                                                                                                      | Behält den Gebiets Schema Namen des Gebiets Schemas bei, das ersetzt wird.                                                                                                                                                                   |



 

## <a name="supplemental-locale-examples"></a>Ergänzende Gebiets Schema Beispiele



| Gebiets Schema Name    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| de-ca-fabricam | Fabricam ist ein kanadischer PC-Hersteller mit Niederlassungen auf der ganzen Welt. Um ein konsistentes Verhalten der Benutzeroberfläche für alle Computer bereitzustellen, entwickelt das Unternehmen ein Gebiets Schema für die unternehmensweite Verwendung.                                                                                                                                                          |
| Fr-US          | Woodlawn Bank verwendet Windows XP Embedded für seine automatisierten Teller Computer (Geldautomaten), die die Bank über Nordamerika mit Benutzeroberflächen in Französisch, Englisch und Spanisch ausgeliefert. Zur Gewährleistung eines konsistenten Erlebnisses erstellt die Bank ein Gebiets Schema für Französisch in der USA, die USA Formate, aber französische Tages-und Monatsnamen aufweist. |



 

## <a name="replacement-locale-example"></a>Beispiel für Ersatz Gebiets Schema



| Gebiets Schema Name | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| de-DE       | Fabricam ist ein kanadischer PC-Hersteller mit Niederlassungen auf der ganzen Welt. Um ein konsistentes Verhalten der Benutzeroberfläche für alle Computer bereitzustellen, entwickelt das Unternehmen ein Gebiets Schema für die unternehmensweite Verwendung. Es verwendet ein 24-Stunden-Format, verhält sich aber andernfalls wie das unterstützte englische Gebiets Schema (USA). Da das benutzerdefinierte Gebiets Schema dem unterstützten Gebiets Schema ähnelt, beschließt fabricam, es als Ersatz Gebiets Schema anstelle eines ergänzenden Gebiets Schemas zu implementieren. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gebiets Schemas und Sprachen](locales-and-languages.md)
</dt> <dt>

[Arbeiten mit benutzerdefinierten Gebiets Schemas](working-with-custom-locales.md)
</dt> </dl>

 

 



