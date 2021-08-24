---
description: ICE61 überprüft die Upgradetabelle einer Windows Installer-Datenbank.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c772a076decaa385d01047daa45871aeeaf7898d4cf3347606c4066d1f7f2b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580980"
---
# <a name="ice61"></a>ICE61

ICE61 überprüft die Upgradetabelle, um sicherzustellen, dass die folgenden Bedingungen erfüllt sind:

-   Alle ActionProperty-Eigenschaften sind in der Property-Tabelle nicht vorab erstellt.
-   Alle ActionProperty-Eigenschaften sind öffentliche Eigenschaften.
-   Alle ActionProperty-Eigenschaften sind in der [**SecureCustomProperties-Eigenschaft**](securecustomproperties.md) enthalten.
-   Alle ActionProperty-Eigenschaften sind für jeden Datensatz in der Upgradetabelle eindeutig.
-   Alle VersionMax-Werte sind nicht kleiner als die entsprechenden VersionMin-Werte.
-   Die Werte für VersionMin und VersionMax sind gültige Produktversionen. Das gültige Produktversionsformat finden Sie in der [**ProductVersion-Eigenschaft.**](productversion.md)
-   Es wird nicht versucht, eine neuere oder gleiche Version des aktuellen Produkts zu entfernen.

Wenn eine von ICE61 gemeldete Warnung oder ein Von ICE61 gemeldeter Fehler nicht behoben wird, führt dies in der Regel zu Problemen beim Upgrade Ihrer Anwendung. Je nach dem genauen Fehler kann dies alles sein, z. B. das Zurücklassen von Dateien aus der älteren Version, das Löschen von Dateien aus der älteren Version, obwohl sie von der neuen Anwendung benötigt werden, oder das vollständige Fehlschlagen des Upgrades.

## <a name="result"></a>Ergebnis

ICE61 gibt eine Warnung oder einen Fehler aus, wenn eine der oben genannten Bedingungen nicht zutrifft.

## <a name="example"></a>Beispiel

ICE61 meldet die folgenden Fehler und Warnungen für die gezeigten Beispiele.

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

In diesem Fall versucht die erste Zeile, ein Produkt der gleichen Version zu entfernen. (Die Spalte VersionMax entspricht der Produktversion in der Tabelle Property.)

Um diesen Fehler zu beheben, verwenden Sie eine Version in der Spalte VersionMax, die niedriger ist als die aktuelle Version, die in der Tabelle Property angegeben ist. Entfernen Sie das Bit **msidbUpgradeAttributesVersionMaxInclusive** aus der Spalte Attributes, wenn VersionMax gleich der aktuellen Version ist. Wenn die Absicht nur darin besteht, das Produkt zu erkennen und nicht zu entfernen, wird dieser Fehler auch durch Hinzufügen des **MsidbUpgradeAttributesOnlyDetect-Bits** zur Spalte Attributes behoben.

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

Sofern die Eigenschaft nicht in der [**SecureCustomProperties-Eigenschaft**](securecustomproperties.md) aufgeführt ist, wird die Eigenschaft nicht an die Serverseite der Installation übergeben, wenn die Eigenschaft gefunden wird.

Um diesen Fehler zu beheben, fügen Sie [**secureCustomProperties**](securecustomproperties.md)die -Eigenschaft hinzu.

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

Upgradeeigenschaften müssen öffentliche Eigenschaften sein, damit das Ergebnis an die Serverseite der Installation übergeben wird.

Um diesen Fehler zu beheben, verwenden Sie alle Großbuchstaben im Eigenschaftennamen.

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

Eine Eigenschaft kann nur in einer Zeile der Upgrade-Tabelle verwendet werden.

Verwenden Sie eine andere Eigenschaft für die zweite Zeile, um diesen Fehler zu beheben.

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

Die Mindestversion muss kleiner als die maximale Version sein.

Um diesen Fehler zu beheben, überprüfen Sie Ihre Versionsnummern auf Tippfehler. Wenn sie richtig sind und Sie den Bereich zwischen den beiden Versionen verwenden möchten, wechseln Sie sie so, dass VersionMin kleiner als VersionMax ist.

[Eigenschaftentabelle](property-table.md)



| Eigenschaft                                                 | Wert                                  |
|----------------------------------------------------------|----------------------------------------|
| [**Upgradecode**](upgradecode.md)                       | {61AA4C55-E17F-11D2-93BB-0060089A76DB} |
| [**ProductVersion**](productversion.md)                 | 2.01.0000                              |
| [**SecureCustomProperties**](securecustomproperties.md) | OLDAPPFOUND                            |



 

[Upgradetabelle](upgrade-table.md)



| Upgradecode                            | VersionMin | VersionMax | Sprache | Attribute | Entfernen                | ActionProperty  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} |            | 2.01.0000  |          | 513        |                       | OLDAPPFOUND     |
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} | 2.01.0001  | 2.01.0000  |          |            |                       | OLDAPPFOUND     |
| {C6CB4596-D8E8-D5A4-635F-9FE456D682EB} | 1.00.0000  | 2.00.0000  | 1033     |            | \[AppFeatureEnglish\] | EnglishAPPFOUND |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



