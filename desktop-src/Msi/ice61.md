---
description: ICE61 überprüft die upgradetabelle einer Windows Installer Datenbank.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f5a685d5b0a4f2bd5ce8dac70a738cbe2e0b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357897"
---
# <a name="ice61"></a>ICE61

ICE61 prüft die upgradetabelle, um sicherzustellen, dass die folgenden Bedingungen zutreffen:

-   Alle Eigenschaften von "aktionproperty" sind in der Eigenschaften Tabelle nicht vorgeschrieben.
-   Alle Eigenschaften von "aktionproperty" sind öffentliche Eigenschaften.
-   Alle Eigenschaften von "aktionproperty" sind in der [**securecustomproperties**](securecustomproperties.md) -Eigenschaft enthalten.
-   Alle Eigenschaften von "aktionproperty" sind für jeden Datensatz in der upgradetabelle eindeutig.
-   Alle versionmax-Werte sind nicht kleiner als die entsprechenden versionmin-Werte.
-   Versionmin-und versionmax-Werte sind gültige Produktversionen. Das gültige Format der Produktversion finden Sie unter der [**ProductVersion**](productversion.md) -Eigenschaft.
-   Es wird nicht versucht, eine neuere oder gleiche Version des aktuellen Produkts zu entfernen.

Wenn eine Warnung oder ein Fehler, der von ICE61 gemeldet wird, nicht behoben wird, führt dies im Allgemeinen zu Problemen beim Upgrade Ihrer Anwendung Je nach dem genauen Fehler kann es daran liegen, Dateien von der älteren Version zu schließen, Dateien aus der älteren Version zu löschen, auch wenn Sie von der neuen Anwendung benötigt werden, oder das Upgrade abzuschließen.

## <a name="result"></a>Ergebnis

ICE61 gibt eine Warnung oder einen Fehler aus, wenn eine der oben genannten Bedingungen nicht erfüllt ist.

## <a name="example"></a>Beispiel

ICE61 meldet die folgenden Fehler und Warnungen für die gezeigten Beispiele.

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

In diesem Fall würde die erste Zeile versuchen, ein Produkt derselben Version zu entfernen. (Die versionmax-Spalte ist gleich der Produktversion in der Eigenschaften Tabelle).

Um diesen Fehler zu beheben, verwenden Sie eine Version in der versionmax-Spalte, die niedriger als die in der Eigenschaften Tabelle angegebene aktuelle Version ist. Entfernen Sie das Bit **msidbupgradeattributesversionmaxinclusive** aus der Spalte Attribute, wenn versionmax gleich der aktuellen Version ist. Wenn die Absicht lediglich ist, das Produkt zu erkennen und nicht zu entfernen, wird dieser Fehler auch durch Hinzufügen des **msidbupgraentattributesonlydetect** -Bits zur Spalte Attribute behoben.

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

Wenn die Eigenschaft nicht in der [**securecustomproperties**](securecustomproperties.md) -Eigenschaft aufgeführt ist, wird die-Eigenschaft nicht an die Serverseite der Installation übergeben, wenn die-Eigenschaft gefunden wird.

Um diesen Fehler zu beheben, fügen Sie [**securecustomproperties**](securecustomproperties.md)die Eigenschaft hinzu.

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

Upgradeeigenschaften müssen öffentliche Eigenschaften sein, damit das Ergebnis an die Serverseite der Installation übermittelt werden soll.

Um diesen Fehler zu beheben, verwenden Sie alle Großbuchstaben im Eigenschaftsnamen.

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

Eine Eigenschaft kann nur in einer Zeile der upgradetabelle verwendet werden.

Um diesen Fehler zu beheben, verwenden Sie eine andere Eigenschaft für die zweite Zeile.

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

Die Mindestversion muss kleiner als die maximale Version sein.

Um diesen Fehler zu beheben, überprüfen Sie die Versionsnummern für Typos. Wenn Sie richtig sind und Sie den Bereich zwischen den beiden Versionen verwenden möchten, können Sie Sie so ändern, dass versionmin kleiner als versionmax ist.

[Eigenschaften Tabelle](property-table.md)



| Eigenschaft                                                 | Wert                                  |
|----------------------------------------------------------|----------------------------------------|
| [**UpgradeCode auch**](upgradecode.md)                       | {61aa4c55-e17f-11d2-93bb-0060089a76db} |
| [**ProductVersion**](productversion.md)                 | 2.01.0000                              |
| [**Securecustomproperties**](securecustomproperties.md) | Oldappfound                            |



 

[Upgradetabelle](upgrade-table.md)



| UpgradeCode auch                            | Versionmin | Versionmax | Sprache | Attribute | Entfernen                | Aktions Eigenschaft  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| {61aa4c55-e17f-11d2-93bb-0060089a76db} |            | 2.01.0000  |          | 513        |                       | Oldappfound     |
| {61aa4c55-e17f-11d2-93bb-0060089a76db} | 2.01.0001  | 2.01.0000  |          |            |                       | Oldappfound     |
| {C6CB4596-D8E8-D5A4-635F-9FE456D682EB} | 1.00.0000  | 2.00.0000  | 1033     |            | \[Appfeatureenglish\] | Englische appfound |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



