---
description: Die Auslösegeschwindigkeit der Kamera, wenn das Foto entnommen wurde. Dies wird in Apex Units angegeben.
ms.assetid: 7f51b3b9-d701-4e7a-80bd-87c1a60e56f7
title: System. Photo. shutterspeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172ce97bf87e79dd86f83e68c91940748bbc283f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042175"
---
# <a name="systemphotoshutterspeed"></a>System. Photo. shutterspeed

Die Auslösegeschwindigkeit der Kamera, wenn das Foto entnommen wurde. Dies wird in Apex Units angegeben. Diese Eigenschaft wird aus [System. Photo. shutterspeednumerator](./props-system-photo-shutterspeednumerator.md) und [System. Photo. shutterspeednenner](./props-system-photo-shutterspeeddenominator.md)berechnet.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Die Konvertierung dieses Werts in die Auswertungszeit finden Sie in der Version der austauschbaren Abbild Datei (EXIF) 2,2 (Anhang C). Verwenden Sie [System. Photo. ExposureTime](./props-system-photo-exposuretime.md) in allen shellansichten anstelle von [System. Photo. shutterspeed]().

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Exchangeable Image File Format für digitale Kameras: EXIF Version 2,2](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

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

 

 
