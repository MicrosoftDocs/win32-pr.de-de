---
description: Der Anzeige Name in &\# 0034; die meisten&\# 0034;-Formular.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753112"
---
# <a name="systemitemnamedisplay"></a>System.ItemNameDisplay

Der Anzeige Name im Formular "ganz fertig". Dabei handelt es sich um die eindeutige Darstellung des Element namens, der für Endbenutzer am besten geeignet ist.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Dieser Wert ist die verkettierung von [System. itemnameprefix](./props-system-itemnameprefix.md) und [System. ItemName](./props-system-itemname.md).

Wenn es sich bei dem Element um eine Datei handelt, enthält diese Eigenschaft den anzeigen Amen, wie im Datei-Explorer angezeigt. Es gibt akzeptable Fälle, in denen [System. filename](./props-system-filename.md) angegeben ist, der Wert dieser Eigenschaft jedoch vollständig anders ist. E-Mail-Nachrichten sind ein gutes Beispiel. Handelt es sich bei dem Element um eine e-Mail-Nachricht, ist der Elementname normalerweise der Betreff. In diesem Fall muss der Wert die Verkettung von [System. itemnameprefix](./props-system-itemnameprefix.md) und [System. ItemName](./props-system-itemname.md)sein. Da der Wert von System. itemnameprefix alle nachfolgenden Leerzeichen ausschließt, muss die Verkettung ein Leerzeichen enthalten, wenn [System. itemnamedisplay]()erzeugt wird. Beachten Sie, dass diese Eigenschaft nicht unbedingt eindeutig ist, sondern so konzipiert ist, dass Sie den wahrscheinlichsten Kandidaten herauf Stufen kann, der eindeutig sein kann und für Endbenutzer sinnvoll ist.

Für Dokumente könnte z [. b. System. Title](./props-system-title.md) als [System. itemnamedisplay]()verwendet werden. in der Praxis ist der Titel der Dokumente jedoch möglicherweise nicht nützlich oder eindeutig genug, um als alleinige System. itemnamedisplay-Funktion zu fungieren. Stattdessen ist die Angabe von " [System. filename](./props-system-filename.md) " als Wert von "System. itemnamedisplay" eine bessere Wahl. In Windows Mail wird e-Mail als EML-Dateien im Dateisystem gespeichert. Die System. filename-Werte für diese Dateien sind nicht Menschen freundlich, da Sie GUIDs sind. In diesem Beispiel ist die herauf Stufung von [System. Subject](./props-system-subject.md) als System. itemnamedisplay sinnvoller.

**Kompatibilitäts Hinweise:**

-   Shell-Ordner Implementierungen unter Windows Vista: Verwenden Sie "pkey \_ itemnamedisplay" für die Spalte "Name", wenn Sie möchten, dass Windows-Explorer [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(shgdn \_ Normal) aufruft, um den Wert des Namens abzurufen. Verwenden Sie einen anderen pkey (z. b. pkey \_ ItemName), wenn Sie möchten, dass Windows-Explorer entweder den Eigenschaften Speicher des Ordners oder [**IShellFolder2:: getdetailsex**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) aufruft, um den Wert des Namens abzurufen.
-   Shell-Ordner Implementierungen unter Windows XP: die erste Spalte muss die Namensspalte sein, und Windows Explorer ruft [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) auf, um den Wert des Namens zu erhalten. Pkey/scid ist unerheblich.



| Elementtyp     | Beispiel                   |
|---------------|---------------------------|
| File          | hello.txt                 |
| `Message`       | Neu: wo ist das Meeting? |
| Geräte Ordner | "Song. wma"                  |
| Ordner        | Dokumente                 |



 

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

 

 
