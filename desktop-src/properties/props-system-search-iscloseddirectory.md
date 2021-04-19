---
description: Wird von einem Containerelement als true ausgegeben, um anzugeben, dass die untergeordneten Elemente nicht durch einen Indexer aufgezählt werden müssen, wenn das Containerelement seit der letzten durch Forstung der Indexüberprüfung nicht geändert wurde.
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: System. search. iscloseddirectory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366120"
---
# <a name="systemsearchiscloseddirectory"></a>System. search. iscloseddirectory

Wird von einem Containerelement als **true** ausgegeben, um anzugeben, dass die untergeordneten Elemente nicht durch einen Indexer aufgezählt werden müssen, wenn das Containerelement seit der letzten durch Forstung der Indexüberprüfung nicht geändert wurde. Dies trägt zur Optimierung der Leistung von Indexern bei. In diesen Container Fällen (Beispiele sind eine e-Mail mit Anlagen oder eine komprimierte Datei mit der Erweiterung ". zip") sind untergeordnete Elemente nicht mit ihrem übergeordneten Element verbunden. Wenn beispielsweise die [System. DateModified](./props-system-datemodified.md) -Eigenschaft eines enthaltenen Elements geändert wird, ändert sich der System. DateModified-Wert des Containers in Match. Außerdem werden auch alle untergeordneten Elemente gelöscht, wenn ein übergeordnetes Element gelöscht wird. Wenn sich der Container nicht geändert hat, weiß der Indexer daher, dass sich nichts darin geändert hat, und muss den Container nicht öffnen, um den Inhalt einzeln zu überprüfen.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

> [!IMPORTANT]
> Wenn ein Element **true** für diese Eigenschaft ausgibt, muss jedes seiner untergeordneten Elemente die [System. search. isfullyenthalteneigenschaft](./props-system-search-isfullycontained.md) als **true** ausgeben, um zu verhindern, dass diese Elemente aus dem Index gelöscht werden.

 

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

 

 
