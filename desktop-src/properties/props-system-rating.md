---
description: Ein Bewertungssystem, das ganzzahlige Werte zwischen 1 und 99 verwendet. Dies ist das Bewertungssystem, das von der Windows Vista-Shell verwendet wird.
ms.assetid: a6288d29-1ef3-4da1-bd30-577336ab6817
title: System. Rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e411e313f0fa6042a8cbe3a076a7166928020af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351641"
---
# <a name="systemrating"></a>System. Rating

Ein Bewertungssystem, das ganzzahlige Werte zwischen 1 und 99 verwendet. Dies ist das Bewertungssystem, das von der Windows Vista-Shell verwendet wird.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = OneStar
            minValue = 1
            setValue = 1
            defineMaxValue = 12
            text = 1 Star
            defineToken = RATING_ONE_STAR
         enumRange
            name = TwoStars
            minValue = 13
            setValue = 25
            defineMaxValue = 37
            text = 2 Stars
            defineToken = RATING_TWO_STARS
         enumRange
            name = ThreeStars
            minValue = 38
            setValue = 50
            defineMaxValue = 62
            text = 3 Stars
            defineToken = RATING_THREE_STARS
         enumRange
            name = FourStars
            minValue = 63
            setValue = 75
            defineMaxValue = 87
            text = 4 Stars
            defineToken = RATING_FOUR_STARS
         enumRange
            name = FiveStars
            minValue = 88
            setValue = 99
            defineMaxValue = 99
            text = 5 Stars
            defineToken = RATING_FIVE_STARS
         enumRange
            name
            minValue = 100
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            defineMinName = RATING_UNRATED_MIN
            setValue = 0
            defineSetName = RATING_UNRATED_SET
            defineMaxValue = 0
            defineMaxName = RATING_UNRATED_MAX
            text = Unrated
         enumRange
            minValue = 1
            defineMinName = RATING_ONE_STAR_MIN
            setValue = 1
            defineSetName = RATING_ONE_STAR_SET
            defineMaxValue = 12
            defineMaxName = RATING_ONE_STAR_MAX
            text = 1 Star
         enumRange
            minValue = 13
            defineMinName = RATING_TWO_STARS_MIN
            setValue = 25
            defineSetName = RATING_TWO_STARS_SET
            defineMaxValue = 37
            defineMaxName = RATING_TWO_STARS_MAX
            text = 2 Stars
         enumRange
            minValue = 38
            defineMinName = RATING_THREE_STARS_MIN
            setValue = 50
            defineSetName = RATING_THREE_STARS_SET
            defineMaxValue = 62
            defineMaxName = RATING_THREE_STARS_MAX
            text = 3 Stars
         enumRange
            minValue = 63
            defineMinName = RATING_FOUR_STARS_MIN
            setValue = 75
            defineSetName = RATING_FOUR_STARS_SET
            defineMaxValue = 87
            defineMaxName = RATING_FOUR_STARS_MAX
            text = 4 Stars
         enumRange
            minValue = 88
            defineMinName = RATING_FIVE_STARS_MIN
            setValue = 99
            defineSetName = RATING_FIVE_STARS_SET
            defineMaxValue = 99
            defineMaxName = RATING_FIVE_STARS_MAX
            text = 5 Stars
         enumRange
            minValue = 100
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Informationen zur Kompatibilität mit Bewertungssystemen, die Werte zwischen 1 und 5 verwenden, finden Sie unter Eigenschaften [System. simplerating](./props-system-simplerating.md). Beachten Sie jedoch, dass System. simplerating in der Windows Vista-Shell nicht verwendet wird.

In der folgenden Tabelle wird beschrieben, was das in der Shell-Benutzeroberfläche verwendete sternbewertungssystem im Hinblick auf den [System. Rating]() -Wert bedeutet.



| System. Rating | Bewertung mit Sternen |
|---------------|-------------|
| 1-12          | Ein Stern      |
| 13-37         | Zwei Sterne     |
| 38-62         | Drei Sterne     |
| 63-87         | Vier Sterne     |
| 88-99         | Fünf Sterne     |



 

Wenn ein Benutzer ein Element durch Auswahl eines Stern Bewertungs Werts in der Benutzeroberfläche bewertet, werden die tatsächlichen [System. Rating]() -Werte wie in der folgenden Tabelle dargestellt zugewiesen:



| Bewertung mit Sternen | Über die Benutzeroberfläche zugewiesener Wert |
|-------------|---------------------------|
| Ein Stern      | 1                         |
| Zwei Sterne     | 25                        |
| Drei Sterne     | 50                        |
| Vier Sterne     | 75                        |
| Fünf Sterne     | 99                        |



 

Wenn die Datei einen [System. simplerating](./props-system-simplerating.md) -Wert anstelle eines [System. Rating]() -Werts aufweist, verwenden Sie die folgende Tabelle, um Werte für System. Rating zu konvertieren und anzugeben.



| System. simplerating | System. Rating |
|---------------------|---------------|
| 1                   | 1             |
| 2                   | 25            |
| 3                   | 50            |
| 4                   | 75            |
| 5                   | 99            |



 

Wenn die Datei sowohl [System. Rating]() als auch [System. simplerating](./props-system-simplerating.md) persistent ist, verwenden Sie immer den Wert System. Rating, wenn Sie direkt angefordert wird, ohne dass auf System. simplerating verwiesen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[propertydescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[SearchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[Labelinfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[TypeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[Display Info](./propdesc-schema-displayinfo.md)
</dt> <dt>

[StringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[BooleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[NumberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedlist](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[DrawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editcontrol](./propdesc-schema-editcontrol.md)
</dt> <dt>

[FilterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[querycontrol](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
