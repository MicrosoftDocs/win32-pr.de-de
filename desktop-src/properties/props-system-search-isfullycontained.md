---
description: Wird von allen untergeordneten Elementen eines Containers als true ausgegeben (z. b. eine e-Mail oder eine komprimierte Datei mit der Erweiterung ". zip"), die System. search. iscloseddirectory als true ausgibt. Dadurch wird sichergestellt, dass die untergeordneten Elemente im Suchindex enthalten sind.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System. search. isfullyenthaltene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1245f29a2940146a4e5d8f0a392210173be75e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530050"
---
# <a name="systemsearchisfullycontained"></a>System. search. isfullyenthaltene

Wird von allen untergeordneten Elementen eines Containers als **true** ausgegeben (z. b. eine e-Mail oder eine komprimierte Datei mit der Erweiterung ". zip"), die [System. search. iscloseddirectory](./props-system-search-iscloseddirectory.md) als **true** ausgibt. Dadurch wird sichergestellt, dass die untergeordneten Elemente im Suchindex enthalten sind.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Mithilfe der [System. search. iscloseddirectory](./props-system-search-iscloseddirectory.md) -Eigenschaft kann die indexerleistung optimiert werden, da der Indexer die Enumeration der untergeordneten Elemente eines Containers überspringen kann. Diese untergeordneten Elemente sind jedoch vom Indexer als nicht besucht gekennzeichnet und werden aus dem Index gelöscht. Wenn Sie [System. search. isfullyenthaltene]() als **true** ausgeben, wird ein Element nicht aus dem Index gelöscht, obwohl es nicht besucht wurde.

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

 

 
