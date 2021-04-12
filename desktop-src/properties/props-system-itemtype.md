---
description: Der kanonische Typ des Elements.
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System. ItemType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0159a12e1cc3c6d85e461461cad20334a641fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218076"
---
# <a name="systemitemtype"></a>System. ItemType

Der kanonische Typ des Elements.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Der Wert für System. ItemType soll Programm gesteuert analysiert werden und kann wie folgt lauten:

-   Eine Dateierweiterung, die auf einen ProgID-Wert (HKEY \_ Classes \_ root) verweist, \\ <ProgID> der den anzeigen Amen für den Typ enthält.
-   Ein ProgID-Wert (HKEY \_ Classes \_ rroot \\ <ProgID> ), der den anzeigen Amen für den Typ enthält.

Das friendlytykename-Element einer ProgID sollte eine lokalisierte Version des Anwendungs namens ( @winword.dll ,-42) sein, während der Standardwert des ProgID-Schlüssels ein nicht lokalisierter Name ist (Word.Doc-enument. 12).

Wenn kein kanonischer Typ vorhanden ist, ist der Wert VT \_ empty. Wenn es sich bei dem Element um eine Datei handelt ([System. filename](./props-system-filename.md) ist nicht "VT \_ empty"), ist der Wert identisch mit der Datei " [System. FileExtension](./props-system-fileextension.md)". Verwenden Sie [System. itemtypetext](./props-system-itemtypetext.md) , wenn Sie den Typ für Endbenutzer in einer Ansicht anzeigen möchten.

> [!Note]  
> Wenn es sich bei dem Element um eine Datei handelt, führt die Übergabe des [System. ItemType]() -Werts an [**psformatfordisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) zum gleichen Wert wie [System. itemtypetext](./props-system-itemtypetext.md).

 

Beispielwerte:



| Pfad                                   | ItemType         |
|----------------------------------------|------------------|
| c: \\ "MyDir"- \\ Leiste \\hello.txt              | .txt             |
| \\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc | .doc             |
| \\\\Server \\ Freigabe \\ Ordner              | Verzeichnis        |
| c: \\ mydir \\ meinOrdner                    | Verzeichnis        |
| \[desktop\]                            | Ordner           |
| /Mailbox Account/Inbox/"Re: Hello!"    | MAPI/IPM. Nachricht |



 

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
</dt> <dt>

[Programmgesteuerte Bezeichner](../shell/fa-progids.md)
</dt> </dl>

 

 
