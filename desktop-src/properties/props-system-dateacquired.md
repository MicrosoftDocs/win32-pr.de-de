---
description: Das Erfassungs Datum der Datei oder des Mediums.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. dateerworbener
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a85f36df252202c319e90460807e16fefa3d559a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218087"
---
# <a name="systemdateacquired"></a>System. dateerworbener

Das Erfassungs Datum der Datei oder des Mediums. Diese Eigenschaft bezieht sich auf einen bestimmten Benutzer oder eine Gruppe von Benutzern. Diese Daten werden z. b. als Haupt Sortier Achse für den virtuellen Ordner **New Music** verwendet, der es Benutzern ermöglicht, die neuesten Ergänzungen zu Ihrer Sammlung zu durchsuchen.

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

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

[Dateerworbener]() wird als Wert im Hauptstream der Datei gespeichert, ist jedoch möglicherweise nicht immer vorhanden. In diesen Fällen kann das Erwerbsdatum auf Grundlage anderer bekannter Datumsangaben für den Inhalt angezeigt werden. Der Metadatenhandler sollte einen Satz von Regeln verwenden, um das Datum zu bestimmen, das zurückgegeben werden soll. Dies wird im folgenden Beispiel für Musikdateien veranschaulicht.

-   Bei erworbener Musik sollte die Erstellungszeit der Datei verwendet werden, wenn kein Erstellungsdatum vorhanden ist. Der Download Anbieter sollte jedoch die [dateerwordeeigenschaft]() in der Datei festlegen.
-   Bei Musikdateien, die der Benutzer oder die Gruppe "gerissen" (Kopieren von Musik oder Video von einer CD oder DVD auf eine Festplatte), sollte das Erfassungs Datum das Datum sein, an dem die Aktion stattfindet. Beispielsweise das [WM/encodingtime-](../wmp/wm-encodingtime-attribute.md) Attribut.
-   Bei Musik, die von einem anderen Speicherort kopiert wurde, sollte die Erstellungszeit der Datei als Erwerbsdatum verwendet werden.

Beispiele für [System. dateerworbene]() sind das Datum und die Uhrzeit, zu denen Bilder von einer Kamera bezogen werden oder wenn Musik online erworben wird. Dies ist nicht identisch mit [System. dateimportiert](./props-system-dateimported.md).

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

 

 
