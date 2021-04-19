---
description: Der Dateiname, einschließlich der Erweiterung.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System. filename
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f535eff4625178b3c32a04ea6d325505266a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367902"
---
# <a name="systemfilename"></a>System. filename

Der Dateiname, einschließlich der Erweiterung. System. File Extension wird von dieser Eigenschaft abgeleitet.

Es ist möglich, dass das Element in einem Dateisystem nicht vorhanden ist (d. h., es kann nicht mithilfe von "deatefile" geöffnet werden). Wenn das Element jedoch als Datei dargestellt wird und der Name der standardmäßigen Win32-Dateibenennungs Syntax folgt, sollte die Datenquelle diese Eigenschaft ausgeben. Wenn es sich bei dem Element nicht um eine Datei handelt, sollte die Datenquelle diese Eigenschaft als VT \_ empty ausgeben.

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

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Das Element ist möglicherweise nicht in einem Dateisystem vorhanden (d. h. es kann nicht mithilfe von "anatefile" geöffnet werden). wenn das Element jedoch als Datei aus dem logischen Sinne dargestellt wird und der Name der standardmäßigen Win32-Datei namens Syntax folgt, sollte die Datenquelle diese Eigenschaft ausgeben. Wenn es sich bei einem Element nicht um eine Datei handelt, ist der Wert für diese Eigenschaft VT \_ empty. Weitere Informationen finden Sie unter System. itemnamedisplay. Dies hat den gleichen Wert wie System. Parser Name für Elemente, die vom Datei Ordner der Shell bereitgestellt werden.

In der folgenden Tabelle sind Beispiele für Pfad-und Dateinamen Eigenschaftswerte aufgeführt:



| Pfad                               | Eigenschaftswert |
|------------------------------------|----------------|
| c: \\ \\ Eigene Dateien \\hello.txt     | hello.txt      |
| \\\\Server \\ Freigabe \\ "MyDir" \\news.doc | news.doc       |
| \\\\Server \\ Freigabe \\numbers.xls     | numbers.xls    |
| c: \\ Material \\ MyFolder                | MyFolder       |
| \[e-Mail senden\]                  | VT \_ leer      |
| \["Song. wma" auf einem tragbaren Gerät\]    | "Song. wma"       |



 

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

 

 
