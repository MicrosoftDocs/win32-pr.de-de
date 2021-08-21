---
description: Der benutzerfreundliche Typname des Elements.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System.ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f145aa2491f3352c4691be95c0e8ae16a75e8e0880732904e983fbf02c167dbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553750"
---
# <a name="systemitemtypetext"></a>System.ItemTypeText

Der benutzerfreundliche Typname des Elements. Dieser Wert ist nicht für die programmgesteuerte Analyse vorgesehen.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

Wenn [System.ItemType](./props-system-itemtype.md) VT EMPTY ist, ist der Wert \_ dieser Eigenschaft ebenfalls VT \_ EMPTY. Wenn es sich bei dem Element um eine Datei handelt, ist der Wert dieser Eigenschaft derselbe, als ob Sie den System.ItemType-Wert der Datei an [**PSFormatForDisplay übergeben hätten.**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay)

Diese Eigenschaft sollte nicht mit [System.Kind](./props-system-kind.md)verwechselt werden, bei dem es sich um einen benutzerfreundlichen Namen auf hoher Ebene handelt. Beispielsweise sind für eine .doc Dokumentdatei die verschiedenen Eigenschaften wie hier gezeigt:



| Eigenschaft                                               | Wert                   |
|--------------------------------------------------------|-------------------------|
| [System.Kind](./props-system-kind.md)                 | Dokument                |
| [System.ItemType](./props-system-itemtype.md)         | .doc                    |
| [System.ItemTypeText]() | Microsoft Word Dokument |



 

Beispielwerte:



| Pfad                                   | ItemTypeText            |
|----------------------------------------|-------------------------|
| c: \\ mydir \\ bar \\hello.txt              | Textdatei               |
| \\\\server \\ share \\ mydir \\goodnews.doc | Microsoft Word Dokument |
| \\\\\\ \\ Serverfreigabeordner              | Dateiordner             |
| c: \\ MyDir \\ MyFolder                    | Dateiordner             |
| /Postfachkonto/Posteingang/'Re: Hello!    | Outlook E-Mail-Nachricht  |



 

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

 

 
