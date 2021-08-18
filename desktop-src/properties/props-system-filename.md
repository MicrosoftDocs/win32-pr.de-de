---
description: Der Dateiname, einschließlich der Erweiterung.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System.FileName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8a92febe0a4f2dfe8cc9d5741118fdb76bcb56c7bcd1ef5c3d881e8c0f9abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119096919"
---
# <a name="systemfilename"></a>System.FileName

Der Dateiname, einschließlich der Erweiterung. System.FileExtension wird von dieser Eigenschaft abgeleitet.

Es ist möglich, dass das Element in einem Dateisystem nicht vorhanden ist (d. h., es kann nicht mit CreateFile geöffnet werden). Wenn das Element jedoch als Datei dargestellt wird und sein Name der standardmäßigen Win32-Dateibenennungssyntax folgt, sollte die Datenquelle diese Eigenschaft aus geben. Wenn das Element keine Datei ist, sollte die Datenquelle diese Eigenschaft als VT \_ EMPTY aus geben.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

Das Element ist möglicherweise nicht in einem Dateisystem vorhanden (d. h., es kann nicht mit CreateFile geöffnet werden). Wenn das Element jedoch als Datei aus logischem Sinn dargestellt wird und sein Name der Win32-Standardsyntax für die Dateibenennung entspricht, sollte die Datenquelle diese Eigenschaft aus geben. Wenn ein Element keine Datei ist, ist der Wert für diese Eigenschaft VT \_ EMPTY. Weitere Informationen finden Sie unter System.ItemNameDisplay. Dies hat den gleichen Wert wie System.ParsingName für Elemente, die vom Dateiordner der Shell bereitgestellt werden.

In der folgenden Tabelle sind Beispiele für Pfad- und Dateinameneigenschaftswerte aufgeführt:



| Pfad                               | Eigenschaftswert |
|------------------------------------|----------------|
| c: \\ Persönliche \\ Dateienhello.txt \\     | hello.txt      |
| \\\\server \\ share \\ mydir \\news.doc | news.doc       |
| \\\\\\ \\ Serverfreigabe-numbers.xls     | numbers.xls    |
| c: \\ Stuff \\ MyFolder                | Myfolder       |
| \[E-Mail-Nachricht\]                  | VT \_ EMPTY      |
| \[song.wma auf einem portablen Gerät\]    | song.wma       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[Numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[Filtercontrol](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
