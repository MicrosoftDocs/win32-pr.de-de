---
description: Wird von allen untergeordneten Elementen eines Containers als TRUE ausgegeben (z. B. eine E-Mail oder eine komprimierte Datei mit einer .zip Namenserweiterung), die System.Search.IsClosedDirectory als TRUE ausgibt. Dadurch wird sichergestellt, dass die untergeordneten Elemente im Suchindex enthalten sind.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System.Search.IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce7f325be26abdb81dcb51da7018f6da786e6ec5f3a31111e4ae3823acf8c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117864989"
---
# <a name="systemsearchisfullycontained"></a>System.Search.IsFullyContained

Wird von allen untergeordneten Elementen eines Containers als **TRUE** ausgegeben (z. B. eine E-Mail oder eine komprimierte Datei mit einer .zip Namenserweiterung), die [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) als **TRUE** ausgibt. Dadurch wird sichergestellt, dass die untergeordneten Elemente im Suchindex enthalten sind.

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

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

Die [System.Search.IsClosedDirectory-Eigenschaft hilft,](./props-system-search-iscloseddirectory.md) die Indexerleistung zu optimieren, indem der Indexer die Enumeration der untergeordneten Elemente eines Containers überspringen kann. Diese untergeordneten Elemente werden jedoch vom Indexer als nicht besucht markiert und daher aus dem Index gelöscht. Wenn [System.Search.IsFullyContained]() als **TRUE** ausgegeben wird, wird ein Element nicht aus dem Index gelöscht, obwohl es nicht besucht wurde.

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

 

 
