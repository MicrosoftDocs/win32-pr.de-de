---
description: Der Anzeigename im &\# 0034;&\# 0034;-Formular.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34e21c0ded147789cadccc99aaf9b2a1910398430419edacc498214c6489d77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598470"
---
# <a name="systemitemnamedisplay"></a>System.ItemNameDisplay

Der Anzeigename im "vollständigsten" Formular. Dies ist die eindeutige Darstellung des Elementnamens, der für Endbenutzer am besten geeignet ist.

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

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

Dieser Wert ist die Verkettung von [System.ItemNamePrefix](./props-system-itemnameprefix.md) und [System.ItemName](./props-system-itemname.md).

Wenn es sich bei dem Element um eine Datei handelt, enthält diese Eigenschaft den Anzeigenamen, wie im Datei-Explorer gezeigt. Es gibt akzeptable Fälle, [in denen System.FileName](./props-system-filename.md) angegeben wird, der Wert dieser Eigenschaft jedoch völlig unterschiedlich ist. E-Mail-Nachrichten sind ein gutes Beispiel. Wenn es sich bei dem Element um eine E-Mail-Nachricht handelt, ist der Elementname normalerweise der Betreff. In diesem Fall muss der Wert die Verkettung von [System.ItemNamePrefix](./props-system-itemnameprefix.md) und [System.ItemName sein.](./props-system-itemname.md) Da der Wert von System.ItemNamePrefix alle nachstellenden Leerzeichen ausschließt, muss die Verkettung beim Generieren von [System.ItemNameDisplay ein Leerzeichen enthalten.]() Beachten Sie, dass diese Eigenschaft nicht garantiert eindeutig ist, sondern dafür konzipiert ist, den wahrscheinlichsten Kandidaten zu bewerben, der eindeutig sein kann und auch für Endbenutzer sinnvoll ist.

Für Dokumente könnte beispielsweise [System.Title](./props-system-title.md) als [System.ItemNameDisplay]()verwendet werden, aber in der Praxis ist der Titel der Dokumente möglicherweise nicht nützlich oder eindeutig genug, um als einziges System.ItemNameDisplay zu funktionieren. Stattdessen ist die [Angabe von System.FileName](./props-system-filename.md) als Wert von System.ItemNameDisplay die bessere Wahl. In Windows E-Mail wird E-Mail im Dateisystem als EML-Dateien gespeichert. Die System.FileName-Werte für diese Dateien sind nicht benutzerfreundlicher, da sie GUIDs sind. In diesem Beispiel ist es [sinnvoller, System.Subject](./props-system-subject.md) als System.ItemNameDisplay zu fördern.

**Kompatibilitätshinweise:**

-   Shellordnerimplementierung auf Windows Vista: Verwenden Sie PKEY ItemNameDisplay für die Namensspalte, wenn der \_ Windows-Explorer [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SLKDN NORMAL) aufrufen soll, um den Wert des Namens zu \_ erhalten. Verwenden Sie einen anderen PKEY, z. B. PKEY ItemName, wenn Sie möchten, dass Windows Explorer entweder den Eigenschaftenspeicher des Ordners oder \_ [**IShellFolder2::GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) aufruft, um den Wert des Namens zu erhalten.
-   Shellordnerimplementierung auf Windows XP: Die erste Spalte muss die Namensspalte sein, und Windows Explorer ruft [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) auf, um den Wert des Namens zu erhalten. PKEY/SCID spielt keine Rolle.



| Elementtyp     | Beispiel                   |
|---------------|---------------------------|
| Datei          | hello.txt                 |
| `Message`       | Re: Wo befindet sich die Besprechung? |
| Geräteordner | song.wma                  |
| Ordner        | Dokumente                 |



 

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

 

 
