---
description: Das Erwerbsdatum der Datei oder des Mediums.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System.DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a78ae9ccfe938551ab6c4a265972e48c3aad1c1791f02cfa933c583c6d4b0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599180"
---
# <a name="systemdateacquired"></a>System.DateAcquired

Das Erwerbsdatum der Datei oder des Mediums. Diese Eigenschaft bezieht sich auf einen bestimmten Benutzer oder eine Bestimmte Benutzergruppe. Diese Daten werden beispielsweise als Hauptsortierachse für den virtuellen Ordner **New Musik** verwendet, mit dem Benutzer die neuesten Ergänzungen ihrer Sammlung durchsuchen können.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

[DateAcquired]() wird als Wert im Hauptstream der Datei gespeichert, ist aber möglicherweise nicht immer vorhanden. In diesen Fällen kann das Kaufdatum basierend auf anderen bekannten Datumsangaben für den Inhalt geschätzt werden. Der Metadatenhandler sollte einen Satz von Regeln verwenden, um das zurückzugebende Datum zu bestimmen. Im folgenden Beispiel wird dies für Musikdateien veranschaulicht.

-   Für erworbene Musik sollte die Erstellungszeit der Datei verwendet werden, wenn kein Datum für den Erwerb vorhanden ist. Der Downloadanbieter sollte jedoch die [DateAcquired-Eigenschaft]() in der Datei festlegen.
-   Bei Musikdateien, die der Benutzer oder die Gruppe "entwendet" hat (Kopieren von Musik oder Video von einer CD oder DVD auf eine Festplatte), sollte das Erwerbsdatum das Datum sein, an dem die Aktion durchgeführt wurde. Beispielsweise das [WM/EncodingTime-Attribut.](../wmp/wm-encodingtime-attribute.md)
-   Für Musik, die von einem anderen Speicherort kopiert wird, sollte die Erstellungszeit der Datei als Erwerbsdatum verwendet werden.

Beispiele für [System.DateAcquired]() sind Das Datum und die Uhrzeit, zu der Bilder von einer Kamera erworben werden oder wenn Musik online gekauft wird. Dies ist nicht identisch mit [System.DateImported](./props-system-dateimported.md).

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

 

 
